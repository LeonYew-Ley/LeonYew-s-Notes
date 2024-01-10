> 标题：[Unity 3D] 1天开发闯关游戏_Day1_详细设计与实现
> 链接：[Yew's Blog](leonyew.fun)
> 工具：Written with [StackEdit中文版](https://stackedit.cn/).
> 日期：2024年1月10日

<!-- 图库：https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main -->

# 为什么没有Day2？
Day2心烦意乱，情绪比较抑郁，诸事不顺，搞了一天的 5G 随身 Wi-Fi 还搞坏了，损失 295 人民币。
希望今天能做得差不多吧。

# 详细设计与实现
# 喜闻乐见的新建文件夹
## 创建Git仓库
1. 创建文件夹 `IceBallProject`
2. 右键 + Shift：`Git Bash Here`
3. 输入命令：`Git Init`
4. 写一个简单的 `README.md`
5. 添加文件并Push到远端：
    ```
    git add .
    git commit -m "Init IceBallProject"
    git remote add origin https://github.com/<username>/<repository>.git
    git push -u origin master
    ```
6. 创建完成，查看GitHub是否同步：https://github.com/LeonYew-SWPU/IceBallUnity
7. 为了项目的二进制文件能够被比较出差异，同时打开 Unity Plastic SCM 版本管理工具，在项目二进制文件出错时进行同步比较。
## 创建Unity项目
打开 Unity Hub -- New Project -- 创建3D项目模板，创建好后如下：
<img alt="picture 0" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-132056.jpg" width="600" />  

给项目资源文件分类：分为Animation、Audio、Materials、Models、Prefebs、Scenes、Scripts
<img alt="picture 0" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-200727.jpg" width="600" />  

# 玩家功能部分

## 设置角色行走功能
利用网络上的素材，简单搭建场景并添加 Animator Controller 用来测试 Collider 和角色行走的功能
<img alt="picture 1" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-215210.jpg" width="600" />  

切换到侧视图，给小骷髅设置 Capsule Collider，给草方块添加 Mesh Collider
<img alt="picture 2" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-215404.jpg" width="600" />  

新建脚本：PlayerMovement.cs
在课堂上脚本的基础上，优化一下代码结构：利用 Character Controller 来控制玩家，可以用 SimpleMove 来代替 Translate 和一堆参数，还可以省去 RigidBody ，并且可以像 AI Navigation 中的 Agent 一样让角色能够走一定程度的障碍。

搭建如下障碍，并给角色添加 Character Controller。
<img alt="picture 9" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240111-025331.jpg" width="600" />  


优化后的代码如下：
```CS
public class PlayerMovement : MonoBehaviour
{
    public float moveSpeed;
    public float rotationSpeed;
    private CharacterController chracterController;

    private void Start()
    {
        chracterController = GetComponent<CharacterController>();
    }
    private void FixedUpdate()
    {
        float horizontalInput = Input.GetAxis("Horizontal");
        float verticalInput = Input.GetAxis("Vertical");

        Vector3 movementDirection = new Vector3(horizontalInput, 0, verticalInput);
        float magnitude = movementDirection.magnitude;
        movementDirection.Normalize();
        chracterController.SimpleMove(movementDirection * magnitude * moveSpeed);

        if (movementDirection != Vector3.zero)
        {
            Quaternion toRotation = Quaternion.LookRotation(movementDirection);

            transform.rotation = Quaternion.RotateTowards(transform.rotation, toRotation, rotationSpeed * Time.deltaTime);
        }
    }
}
```

只使用 Character Controller 效果如下：
<img alt="picture 10" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240111-030434.gif" width="600" />  


## 修复 Normalize 导致手柄无法线性控速
在获取输入的代码中，我们采用了以下代码来修复斜向速度超过1的问题：
```CS
movementDirection.Normalize();
```
但是这样也导致了小数值被格式化为 1，所以，在对数值格式化之前，应该先将 magnitude 存储起来，以确保游戏能在手柄上使用。

修改代码如下：
```CS
float magnitude = movementDirection.magnitude;
movementDirection.Normalize();
transform.Translate(movementDirection * magnitude * moveSpeed * Time.deltaTime, Space.World);
```

修改效果对比：
|修改前|修改后|
|-|-|
|<img alt="picture 8" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240111-024400.gif" width="600" />  |<img alt="picture 7" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240111-024339.gif" width="600" />  |

## 使用 CinemaMachine 添加跟随摄像机
在菜单栏 -- Window -- Package Manager，右上角搜索 Cinemachine，再点击 Install 安装。
在 Hierarchy 面板右键 -- Cinemachine -- Virtual Camera
<img alt="picture 11" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240111-031306.jpg" width="600" />  

这时，Main Camera 会出现一个 Cinemachine 的 logo，代表 Main Camera 被 Cinemachine 控制。在右侧的 Inspector 面板配置 Cinemachine：
<img alt="picture 12" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240111-031949.jpg" width="600" />  

效果如下：
<img alt="picture 13" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240111-032058.gif" width="600" />  


## 添加跳跃功能
分析跳跃逻辑如下：
<img alt="picture 4" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-232140.jpg" width="600" />  

因为跳跃的动画幅度较大，直接跳跃有可能会让动画跟不上（别问，问就是调一天也没调好），所以我们将跳跃拆成3个阶段：跳起、滞留、落地。
去 Adobe 的动作库网站： mixamo，将我们的小骷髅建模上传上去，分别找到这三个动作，然后下载。
<img alt="picture 5" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240111-013153.jpg" width="600" />  

将三个动作导入到Unity中，并对刚才的三个动作进行设置根动画，其中：Falling Idle 需要勾选 Loop Time，确保滞空的时候动作时间够长。
<img alt="picture 6" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240111-013328.jpg" width="600" />  




## 搭建第一关场景

