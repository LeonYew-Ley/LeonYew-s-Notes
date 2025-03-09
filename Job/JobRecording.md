# 

# 小黑板

新城国际，天府软件园，根据项目不同。

五个工作日，考核最后一天考核，和主程序沟通延期或提前，工位，学习资源。

UNity引擎，完成demo

小游戏，选择案例

Lua语言基础

薪资：没有正式工资，100/天津贴，培训通过，12号发工资，实习3000，毕业4000，五险一金（成都最低标准），调薪，一年一调，初一初二初三。966（半小时弹性），八小时，午休一小时，工作双休，培训期8点结束。

拼UI界面，初级界面，开发规范，做活动，做中大型功能。

800多人

### 自我介绍

面试官您好，我叫黎恩瑜，是一名来自西南石油大学的25应届本科生，很荣幸有机会面试 【公司】的 【职位】。我的专业是数字媒体技术，主修的是游戏程序设计和虚拟现实技术这两门游戏方向的课程，除此之外，数媒也属于计算机类的专业，也学习了数据结构、计算机组成原理、操作系统、（计算机网络）等课程。

在校期间，在校区团委任职了5学期的学生工作，担任过主任和部长的角色，可以说是一直在团队中学习，很熟悉团队的交流合作上的一些问题。

开发上，作为项目队长带领同学一起做过一个VR项目和一个基于Java和Swing框架的双人马里奥，其中VR项目获得了CMIT 元宇宙组的国家一等奖，自己独立开发了一个3D平台闯关游戏，还跟着Unity官方的2D教程，通过Ruby’s Adventure，掌握了一些2D开发的基本操作。

此外，建立了自己的Bilibili频道，发布了近20个视频，通过分享计算机操作和Minecraft服务器联机和维护的教程，获得了93万播放，1k关注。

~~目前在找实习的同时也在补充学习热更新和（寻路算法）的内容。~~

这就是我的一个简单介绍，希望您对我有一个初步的了解。

### 项目

VR

Bomb VR，这是一款基于 Steam VR 开发套件的游戏，玩家可以在VR乐园中体验各种公共的游乐设施和5个分别由团队成员独立开发的小游戏。

作为项目队长，我负责了项目框架的搭建，开发规范的制定，Git仓库的建立，以及一个3D迷宫的小游戏，在其中使用了Unity的基本操作，比如C#脚本，物理系统以及一些数学计算。

其中，开发部分，还设计了场景加载特效和墙来了的墙体加载部分。场景加载部分是新建了一个圆柱体，去掉了Collider，就不会发生碰撞，但是保留了trigger....

墙来了的墙体加载部分使用的是对象缓冲池，因为最开始用的是gameobj 的 initialize和destroy，会导致游戏非常卡顿，然后后面用就是ObjectPool，创建了ObjectPool类，因为要随机出现墙体，所以用的是List，从对象池随机抽取，再让其返回对象池。

3D迷宫这个小游戏，玩法是玩家通过双手手柄模拟现实中操作控制小球滚动到终点，可以切换关卡，重置游戏，触发菜单。旋转部分采用的是向量计算，将上下、前后、左右三个向量输入为矩阵，再将矩阵转为四元数（提一下什么是四元数），最后实现跟手的旋转。

U3D

这个项目是独立开发的一个3D平台闯关的游戏，玩家操控主角小骷髅进行跳跃冲刺等动作，收集金币到达终点通关。当时从敲定到完成加上记录开发流程的课程报告，只花了36小时，还取得了第一名的成绩，效率上算是还不错。然后这个项目涉及到了Unity基本操作，有玩家交互、玩家动画、UI响应、物理系统、BGM和SFX音效的添加。

2D

这个项目是我在接触Unity 2D时，根据Unity官方教程所完成的，目的是为了认识一下2D与3D的区别，掌握一下2D的物理系统和动画。开发起来和3D差不多，无非是组件上面添加了2D字样，比较大的区别就是地图的创建，使用到了TileMap，然后玩家角色的素材锚点，要设置在底部居中之类的。

### 为什么要实习

我希望通过这次实习，首先是了解到商业游戏的研发流程，如何从需求分析到最终上线的完整开发流程，还有项目合作之间的一些细节（补充VR开发的细节）

其次，想学习一下我比较欠缺的技能，比如Lua脚本、UGUI的系统性学习（因为目前我只使用过按键绑定，缩放、一些调整Inspector面板的基本操作），如果时间充裕或许还想学习一下优化。

### 反问

- [ ] 技术面
  
  - [ ] 如果我没有满足面试要求的话，站在您的角度，您觉得我还有哪些地方是需要继续提升的，我所做的项目上还缺少了哪些技术吗？
  - [ ] 基础可以，Xlua，热更新，联机，
  - [ ] “您认为我在这次面试中表现较好的部分和需要改进的部分是什么？”
  - [ ] 团队当前主要开发的项目类型是什么？比如手游、主机游戏还是行业应用？
  - [ ] 我进来以后的工作内容是什么呢？
  - [ ] 我们这边使用的脚本和框架一般是什么呢？
  - [ ] （对JD进一步询问）

- [ ] HR面
  
  - [ ] 五险一金
  
  - [ ] 实习期间的主要工作内容
  
  - [ ] 团队当前主要开发的项目类型是什么？比如手游、主机游戏还是行业应用？
  
  - [ ] 是否提供技术培训/mentorship
  
  - [ ] 实习后的转正机会
  
  - [ ] 实习期间的薪资和转正薪资
  
  - [ ] 团队的工作节奏是怎样的？是否需要频繁加班应对版本压力？
  
  - [ ] “后续流程大概需要多久？如果有下一轮面试，我需要重点准备哪些方面？”

# 继续复习

- [ ] xlua脚本

- [ ] Lua与热更新
  
  - [ ] Lua是什么
  
  - [ ] 热更新 Hybrid + yooassets

- [ ] 对象池、缓冲池的使用与原理

- [ ] Unity常用的脚本

- [ ] Unity算法
  
  - [ ] 四叉树，RVO2，AABB包围盒，kd树，A*等等

- [ ] Shader的编写

- [ ] 关卡管理

- [ ] C# 知识（概念、应用场景）
  
  - 接口与抽象类
  
  - 协程与多线程、进程

- [ ] 存档功能

- [ ] 牛客八股文，面经

- [ ] UGUI基础知识

# 面试要点

<mark>把握大厂校招截止时间和定义</mark>

内推

<mark>明确岗位，精准投递</mark>

不要再去准备作品集（积累的结果），应该准备临场的回答、

作品集：魔改网上教程，进度条游戏demo

itch.io可以放游戏demo，Profolio

笔试/技术面，技术面，主管面（压力面），总监+HR面

面试前2h准备

    demo链接，毕业设计链接，了解简历和岗位要求，把想说的想表达的写在iPad/屏幕后小黑板上

环节：自我介绍——问答——反问

    自我介绍：引导面试官提问预先准备的答案

<mark>hr面，提自己学习能力强，学东西快</mark>

# 天上友嘉（笔试）

## 网上试题

### 1.打乱一个数组。

```csharp
using System;

class Program
{
    static void Main()
    {
        int[] array = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
        Shuffle(array);

        Console.WriteLine("打乱后的数组:");
        foreach (int value in array)
        {
            Console.Write(value + " ");
        }
    }

    static void Shuffle(int[] array)
    {
        Random random = new Random();
        int n = array.Length;

        for (int i = n - 1; i > 0; i--)
        {
            // 生成一个随机索引 j (0 <= j <= i)
            int j = random.Next(0, i + 1);

            // 交换 array[i] 和 array[j]
            int temp = array[i];
            array[i] = array[j];
            array[j] = temp;
        }
    }
}
```

### 2.判断一个数是否是 2 的阶次方。

### 3.数组排序（快排）

```csharp
class QuickSort{
    public static void Main(string[] args){
        int[] A={49,38,65,97,76,13,27,49};
        PrintArray(A,A.Length);
        MyQuickSort(A,0,A.Length-1);

        Console.ReadKey();
    }
    static void PrintArray(int[] A, int length){
        for (int i = 0; i < length; i++)
        {
            Console.Write($"{A[i]} ");
        }
        Console.Write("\n");
    }

    public static void MyQuickSort(int[] A, int low, int high){
        if(low < high){
            int pivotpos = Partition(A,low,high);
            PrintArray(A,A.Length);
            MyQuickSort(A,low,pivotpos-1);
            MyQuickSort(A,pivotpos+1,high);
        }
    }
    public static int Partition(int[] A,int low, int high){
        int pivot = A[low];
        while(low < high){
            while(low<high && A[high]>=pivot)
                --high;
            A[low] = A[high];
            while(low < high && A[low]<=pivot)
                ++low;
            A[high]=A[low];
        }
        A[low] = pivot;
        return low;
    }
}
        return low;
        }
    }
```

### 4.给两个数求之前的斐波那契数列。

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        int start = 10;
        int end = 100;

        List<int> fibonacciNumbers = GetFibonacciNumbersBetween(start, end);

        Console.WriteLine($"斐波那契数列在 {start} 和 {end} 之间的数是:");
        foreach (int number in fibonacciNumbers)
        {
            Console.WriteLine(number);
        }
    }

    static List<int> GetFibonacciNumbersBetween(int start, int end)
    {
        List<int> fibonacciNumbers = new List<int>();

        int a = 0;
        int b = 1;

        while (a <= end)
        {
            if (a >= start)
            {
                fibonacciNumbers.Add(a);
            }

            int temp = a;
            a = b;
            b = temp + b;
        }

        return fibonacciNumbers;
    }
}
```

### 5.用面向对象编程交换两个篮子里的苹果和鸡蛋

# 武汉众娱（技术一面+hr面，offer已拒）

**技术面**

自我介绍

项目介绍

<mark>想通过实习学习到什么</mark>

C#学了多久

<mark>3D粒子系统</mark>

<mark>对Lua有了解吗</mark>

讲述一下你在Unity中掌握的一些技能

如何在unity中画一条线

    DrawLine函数

<mark>在运行中如何调整3D模型。在UI中如何查看旋转一个3D模型（灵图互动测试题）</mark>

<mark>如何修改编辑器中的功能</mark>

建议去做一点完整一点的项目，向自己喜欢的类型上完善

**hr面（聊嗨了，放松警惕了）**

- 自我介绍

- 项目介绍
  
  - VR

- 最喜欢的游戏
  
  - Minecraft，小学开始玩，也是由此接触编程，编了一些模组（说<mark>比较简单</mark>，就是在HUD上面展示To-Do List）

- 摄影
  
  - 器材：变焦定焦，摄影设备
  
  - 拍婚礼：早上5点起来，赚了3k，<mark>太累了，干了两单就没干了，不想伤身体</mark>

- 毕设？毕设进度？
  
  - 描述了一下，操控小猫，类似捣蛋鹅的
  
  - 还没开始

- 那怎么有空实习？
  
  - 游戏程序期末的时候我也只花了36小时，效率还是比较高（<mark>没说得了第一</mark>）

- 简历上专业技能和兴趣爱好为什么没有Unity
  
  - 做简历没经验，昨天有位学长才纠正了我，以为要最大程度的丰富信息，所以基本没有重复的地方，简历还是应该展示有关于Unity的兴趣爱好和技能。

- 成都人为什么要来武汉，成都游戏公司也挺多的吧？
  
  - 才毕业，不想接下来几十年一直留在成都，想去武汉杭州其他的新一线城市发展，而且面试了两家，成都公司技术比较落后，脚本语言还在用JS, Boo，有一家还在自研引擎，感觉不是很适合。

- 有亲戚在武汉吗？
  
  - 表哥在武汉工作

- 来过武汉吗？
  
  - 没有（<mark>应该提前了解一下武汉的</mark>）

反问：

- 实习薪资？转正薪资？
  
  - 3，8-12。T1-T8，应届实习基本可以定在T2。

- 有专门的技术培训吗？
  
  - 有Mentor，发任务做Demo，能力过关进组

- 工作内容？
  
  - 出海休闲小游戏
  
  - H5，卡牌，弹珠

# 成都·火娃娃游戏

## hr一面

- 上班时间能否接受（12:30—22:30）
  
  - 22点可以接受，偶尔1点可以，经常1点不行

- 自我介绍+项目介绍

- 期望薪资
  
  - 实习4，转正8-12（直接下一个话题了）

- 加班的态度
  
  - 可以接受加班，但经常1点不行

- 是否熬夜
  
  - 1点睡算熬夜吗？（23点以后都算熬夜）

- 此前面试过哪种公司，目前拿了几个offer了
  
  - 成都天上友嘉+武汉，拿了一个武汉那边的offer

- 有没有了解过我们做的游戏，看过PV没有
  
  - 没有。（<mark>应该提前了解的</mark>）
  
  - 【《烽火与炊烟》第二支实机PV！自由开放绝美中国风】 https://www.bilibili.com/video/BV1b2CbYjEhf/?share_source=copy_web&vd_source=e96b797ceb2cdca0a51cc68fda96dce4

反问

- 有无晚餐补贴
  
  - 无，初创公司，财务紧张，晚上有打车补贴

- 薪资通常如何
  
  - 实习3，转正6

# 好未来

## 网络面经

**一面HR 群面**

一个三角形有三个顶点，给定一个点，如何判断该点在这个三角形的内部还是外部？请给出你的思路和算法

请实现一个简单的排序算法（如冒泡排序、快速排序等），并解释其原理和时间复杂度

你了解哪些常见的设计模式？在 Unity 开发中，哪些设计模式比较常用？请举例说明

1. **单例模式**：确保一个类只有一个实例，并提供全局访问点。
2. **观察者模式**：定义对象间的一对多依赖关系，当一个对象状态改变时，其依赖者会自动收到通知。
3. **工厂模式**：定义一个创建对象的接口，由子类决定实例化哪个类。
4. **策略模式**：定义一系列算法，使它们可以互相替换，且算法的变化独立于客户端。
5. **状态模式**：允许对象在其内部状态改变时改变其行为。

1.2  
C#GC GC优化

数据结构，堆，队列，二叉树，数组，链表的一些基本操作  
冒泡，归并排序  
A*算法  

    G cost + H cost = Sum Cost，计算代价寻路

TCP和UDP的区别  

    TCP是面向连接、可靠的、有序的传输协议，而UDP是无连接、不可靠的、无序的传输协议。
状态同步和帧同步，状态同步一次性处理这么多数据不会死机吗  
    同步玩家的状态，仅同步玩家的操作，逻辑判断到服务器上再处理

Image和rawimage有什么区别  
    `Image` 是 Unity 中 UI 系统的组件，用于显示精灵或纹理；`RawImage` 则直接显示纹理，适合非 UI 场景。
锚点  
锚点是 Unity UI 中用于定义 UI 元素相对于父容器或屏幕的定位基准点。

忘了什么时候投的 hr打电话约面  
自我介绍  
线程进程协程区别 
线程是操作系统调度的基本单位，进程是独立运行的程序实例，协程是用户态轻量级线程，由程序控制切换。  

协程的底层 ✅  

什么时候会用到协程和多线程 ✅❌ 
说了资源加载的时候 面试官指出协程还是在unity主线程运行的 如果资源加载时间过长依然会卡顿 并补上了在进行网络连接的时候单独开一个线程  

dfs bfs区别 ✅  
状态同步和帧同步✅  

canvas 三种渲染方式✅  
Canvas 的三种渲染方式是 `Screen Space - Overlay`（覆盖屏幕）、`Screen Space - Camera`（基于相机）和 `World Space`（世界空间）。

animator的layer什么作用 什么时候用？✅  
Animator 的 Layer 用于管理不同动画层的混合和权重，适用于需要同时播放多个独立动画（如上半身和下半身动作）的情况。

怎么做多分辨率下的ui适配✅  
使用 Unity 的锚点（Anchors）和 Canvas Scaler 组件，结合自适应布局和相对定位，实现多分辨率下的 UI 适配。

已经有了这个gameobject 如何判断这个ui界面是否显示✅❌  
可以通过检查 `gameObject.activeInHierarchy` 和 `gameObject.GetComponent<CanvasGroup>()?.alpha` 来判断 UI 界面是否显示。

https （说不会然后不问了）❌  

有一块半圆形的滑道 一个人物带着滑板去滑雪 怎么实现让这个滑板时刻贴紧滑道❌  

**二面 8/1 26min**

实习负责的内容  

用到了哪些Unity的组件  

UGUI 优化方面，注意点  

骨骼动画 有了解过吗 X  

Animator的原理？  

用Animator的话要怎么去管理配置，方便策划美术？ X  

Lua的协程  

怎么管理协程的唤醒和挂起 X  

运动模拟有做过吗，一个抛物线的运动 X  

几何的算法有了解吗  

2D的 点和三角形的关系怎么做  

2D 的叉乘的含义是什么  

复杂一点的，2D 的俩个 OBB 检测重叠怎么做 X  

C# 的异步 async await 有了解吗，有应用过吗  

假如await异步等待加载一个网络AB包，出错了怎么处理 X  

怎么去管理异步资源的加载释放的  

TCP/IP协议族和OSI七层模型的关系 X  

网络部分有写过吗，介绍TCP，UDP  

有了解TCP 底层 滑动窗口，拥塞控制算法  

## 技术一面

- 自我介绍

- 接触Unity大概多少时间了，什么途径接触到的
  
  - 大三上，游戏程序设计

- 问项目：VR项目
  
  - VR项目中，团队协作的问题
    
    - 如实回答
  
  - <mark>VR主程序和项目框架的搭建</mark>，指的是？（忘了，答得不好）
  
  - 异步场景加载指的是？

- UGUI
  
  - 怎么保证UI自适应？
    
    - 锚点+缩放

- 问项目：3D闯关游戏
  
  - 如何实现的控制玩家移动
    
    - 监听玩家移动，InputManager，
    
    - Character Controller / Rigidbody
      
      - CC没重力，怎么实现走到悬崖边上掉下去
        
        - 代码中给Controller一个力
  
  - 跳跃如何实现的？
    
    - 给一个向上初速度，给一个加速度减下来，落地的时候与地面Layer碰撞
    
    - （HR说应该使用CC自带的<mark>isGrounded</mark>，太久没复习项目了，忘记了）
  
  - 人物移动各种动画状态，要让动画过渡，如何实现？
    
    - Animator中设置
  
  - Cinemachine插件，如何使用的？
    
    - 第三人称视角，绕过障碍物，摄像机轨迹
    
    - 如何自己实现上述效果？
      
      - 最开始回答的是trigger检测障碍物，后面回答的用raycast射线检测

- 有使用AI为自己降本增效吗？
  
  - 只说了都使用过，水论文
  
  - 有利用AI写代码吗？
    
    - copilot也有用
  
  - （<mark>应该编一个文生图的</mark>）

- Mono状态机的生命周期
  
  - 大概都答出来了，onawake，onstart，update，fixedupdate，destroy
  
  - 哪些功能会写到对应的生命周期函数？
    
    - 答得不好，移动可以写在fixedupdate
    
    - 为什么不卸载update？
      
      - 防止高帧数让玩家移动过快
    
    - <mark>update可以指定</mark>，你知道吗？

- 平时都是使用C#吗？
  
  - 找实习的时候已经了解了lua的广泛使用

- C#中值类型和引用类型的区别？
  
  - struct和class，栈、堆
  
  - <mark>Vector3</mark>属于哪种类型？应该用struct还是类？
    
    - 应该用类吧。（错了，是struct）

- <mark>ArrayList和List使用上的区别</mark>
  
  - 只知道装箱的区别

- 寻路系统怎样实现？
  
  - A star算法，计算代价
  
  - Unity中的封装有用过吗？
    
    - 有的，John Lemon里面的敌人

- 两个箱子<mark>碰撞的必要条件</mark>？
  
  - 至少一方要有rigidbody
  
  - 两个箱子必须要有collider吧？
    
    - 解释了一下，算是补救了
  
  - <mark>collider上面 isTrigger有什么用</mark>？
    
    - 需要在接触面上进行事件检测的时候勾上。（不知道对不对）

- <mark>平时有用过协程吗</mark>？
  
  - 没有，只见过别人用线程。

- 对于倒计时的设计，你可以怎么实现？
  
  - Sleep函数吗
    
    - 可是会让所有事件卡起来
    
    - 或许可以开一个线程。
    
    - 不用线程怎么做？
      
      - <mark>用过deltatime吗？可以在update里使用deltatime累加到一秒</mark>。

- 接触过Unity光源吗？
  
  - 接触过，举了几例。

- <mark>有一个开门的动画，如何让它开到一半停住呢</mark>？
  
  - 不知道

- 怎么处理资源资源加载？
  
  - AssetsBundle
  
  - 有了解<mark>ab包</mark>吗？
  
  - 有了解<mark>assetsBundle和resource</mark>吗？

- UI的三种渲染模式是做什么场景下展示出来？
  
  - Overlay，worldspace，camera
  
  - <mark>overlay不太清楚</mark>

- 如果需要<mark>存档，应该怎么实现</mark>？
  
  - 不清楚，但是我觉得可以存到json文件中，loadscene的时候可以读取json文件
  
  - 存到哪儿？
    
    - 可以存到根目录
    
    - 如何获取？
      
      - 忘了，但是应该是有一个函数的。

- 有接触过<mark>对象池</mark>吗？
  
  - VR项目墙来了，我们处理了这个问题，介绍了项目中怎样做的对象池。

反问

- 好未来提供技术培训吗？
  
  - 有mentor指定学习计划，安排任务

- Unity看重哪一方面呢？
  
  - 兴趣、学习能力
  
  - Lua开发

- 好未来教育公司，开发的一般是什么应用呢？
  
  - 英语天天练

- 我有什么地方可以改进的？
  
  - Unity基础还可以，大部分东西都使用过
  
  - 腾讯xlua插件
  
  - 游戏改造成联机版，学习网络方面，热更新
  
  - 主流热更新Lua+AB包

# Unity面试基本问题

自动寻路
动态加载资源与方式
引擎中有哪些坐标空间
相机中的Clipping Plane、Near、Far数值有什么意义
四元数的作用
OnEnbale、Awake、Start运行时的先后顺序
相机的移动在Update函数中好吗?物理更新一般是在Update中吗?
简述Prefab作用
简述垃圾回收机制与如何避免
场景中Static对象有什么作用
Unity实现移动有哪些方法
协程是如何实现的
【ScriptableObject如何存储在硬盘中
【BFS查找Hierarchy中游戏对象,查找中途停止搜索后如何获取到停止搜索的这个目录

用过哪些Unity插件
看过哪些Unity向的作品、网站、博主
