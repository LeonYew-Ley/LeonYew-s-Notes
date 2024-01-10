> 标题：[Unity 3D] 4天开发冰球游戏_Day3_详细设计与实现
> 链接：[Yew's Blog](leonyew.fun)
> 工具：Written with [StackEdit中文版](https://stackedit.cn/).
> 日期：2024年1月8日
> 图库：https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main

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

# 搭建场景Demo
在 Maya 2024 中搭建一个冰球桌，用来给场景限制大小。
<img alt="picture 1" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-134332.jpg" width="600" />  

导出为 `.fbx` 格式
<img alt="picture 2" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-134444.jpg" width="600" />  

导入到 Unity 3D 场景中
<img alt="picture 3" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-145803.jpg" width="600" />  

创建两个小球，简单赋予材质，准备编写物理弹射脚本
<img alt="picture 4" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-150655.jpg" width="600" />  

给场景和冰球添加 `Mesh Collider` 和 `Rigid Body` 这样可以完成最基本的碰撞逻辑
<img alt="picture 7" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-173526.jpg" width="600" />  


# 实现鼠标拖拽冰球功能
通过Console面板的输出，我们可以知道鼠标的位移规律：`窗口左下角为原点，向右为 x 轴正方向，向上为 y 轴正方向`
<img alt="picture 5" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-154514.jpg" width="600" />  
Transform 和 mousePosition 的对应关系如下：
 Transform | mousePosition | 方向 |
|-|-|-|
|z|x|水平|
|x|y|竖直|
|y|z|垂直|

拖拽逻辑如下：
<img alt="picture 6" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-161944.jpg" width="600" />  

根据拖拽逻辑，可以编写如下代码：
太难了，不做了！好不容易实现了效果，结果2D和3D的坐标转换，因为透视关系的原因，小球不跟手，一旦离开中心区域就与鼠标间隔一定距离。
打把 英雄联盟！
等等，英雄的移动不就是通过鼠标交互的吗，所以还是决定使用学到的射线检测方法，返回鼠标点击的坐标，然后再让冰球移动过去吧。

所以，新的拖拽逻辑如下：
<img alt="picture 8" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-192752.jpg" width="600" />  
