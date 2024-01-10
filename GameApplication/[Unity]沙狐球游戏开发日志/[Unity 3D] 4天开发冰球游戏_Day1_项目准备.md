> 标题：[Unity 3D] 4天开发冰球游戏_Day1_项目准备
> 链接：[Yew's Blog](leonyew.fun)
> 工具：Written with [StackEdit中文版](https://stackedit.cn/).
> 日期：2024年1月8日
<!--  图库：https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main -->

# 4天？
这么快？不是我的能力强大到4天完成，是因为我只剩4天就要交这个大作业了 :D
# 灵感来源
做这个游戏的初衷是老家县城的电玩城里面有个冰球游戏自己很喜欢玩，而且也在近年的优秀游戏《双人成行(It Takes Two)》中玩到，游戏机制简单有趣，很适合作为合家欢游戏，正好这学期学习了做Unity游戏，所以准备把沙狐球作为这次的**期末作业**。
# 资料收集
## 作业要求
老师在文档里特意要我们标注**个人原创设计**和**按课程学习**的作品，但哪里会有作品完全原创、凭空出现呢，再完美的作品也离不开其他事务的启发和他人的帮助，所以自作主张，讲老师笔下的“个人原创”重新定义为：`自己基于对游戏的理解和结合课堂的知识独立制作的游戏，而不是跟着成品教程制作的游戏`
## 需要提交以下
- [ ] 实验报告（就直接截取我自己写的开发日志算了）
- [ ] 程序打包+发布运行（build一下就行，再分配一个game域名，用NPM反向代理一下，争取网页能运行我的小游戏）
- [ ] PPT（一个下午搞完）
- [ ] 录屏(PPT+游戏运行)（和PPT一个下午搞完！）
## 寻找参考
鉴于沙狐球是一个非常经典的游戏，肯定有很多大佬制作过了，所以我先上b站搜了一些例子来看看他们的UI设计和玩法设计借鉴一下：
|来源|截图|
|--|--|
|[原神中的冰球游戏](https://www.bilibili.com/video/BV1uV411j7GS/)|![输入图片说明](https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024-01-08/HF9f5saDS88630YP.png)|
|[Air Hockey上的冰球游戏](https://www.bilibili.com/video/BV1184y1V7Uj/)|![输入图片说明](https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024-01-08/P0oKz2Ls0MMBhYKi.png)|
|[Unity 顶视图冰球](https://www.bilibili.com/video/BV1ut4y1q7ta/)|![输入图片说明](https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024-01-08/y2QEEAUKWJKHYQO5.png)|
|[复刻4399沙狐球](https://www.bilibili.com/video/BV1ij411v7xz/)|![输入图片说明](https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024-01-08/z8EjW5CVZEIB1ZOA.png)|

## 额外知识
此外，我还了解到了一些有助于我后续开发的知识：

- [Unity中的可视化编程UVS](https://www.bilibili.com/video/BV15g4y177wd/)
- [Unity中的NetWorkManager来实现联机功能](https://www.bilibili.com/video/BV1As411L7P8/)
- [Unity的Git管理上传大型文件](https://blog.csdn.net/m0_56494923/article/details/130998078)
- [Button-TMP](https://www.bilibili.com/video/BV16o4y1w7U5/)
- [2D冰球开发教程](https://www.youtube.com/watch?v=ZlAMVEVHkuI&list=PLB6lc7nQ1n4hLTDIPJiUD6OlBSNvtp7YP&index=1)

ok，今天的进度就这么点，因为一直在配置博客。。。

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTcwMjkxMDg3OCw2ODE3NTIxOTIsOTEzMj
c4OTM1LC05MDg2MDk2MjBdfQ==
-->

# 项目概述
## 项目类型
Unity3D游戏项目
## 开发工具
- VisualStudio 2022
- Unity 2022.3.9f1C1
- Blender 3.6.4
- Git 2.39.1.windows
- Git LFS
## 设计方案简介
所设计的冰球游戏《沙狐球Ⅰ：冰雄传奇（Ice Hero Legends）》，是一款能够多人对战、局域网联机的冰球游戏，提供积分制和射门式两种玩法，并且两种玩法都支持多人对战和多张地图。

因项目周期有限，本次期末项目暂且实现积分制，后续可以关注 [Github Repo:Ice Ball Unity](https://github.com/LeonYew-SWPU/IceBallUnity) 查看项目的后续更新计划。
# 设计题目实现
## 需求分析
### 沙狐球Ⅰ：冰雄传奇 需求分析
#### 1. 引言
##### 1.1 背景
沙狐球Ⅰ：冰雄传奇（Ice Hero Legends）是一款寒冷时代为背景的多人对战冰球游戏，旨在为玩家提供欢乐、休闲、体育的游戏体验。游戏设定在白垩纪时代，动物们在灭绝前与朋友们玩起了沙狐球和冰球游戏。

##### 1.2 目的
该需求分析旨在明确沙狐球Ⅰ的功能、特性和性能要求，以确保游戏能够满足玩家的期望，并在多平台上稳定运行。

#### 2. 用户需求

##### 2.1 游戏类型
- 提供街机风格的游戏体验，支持单人和多人模式。

##### 2.2 游戏玩法
- 支持线上玩家对战，以及同屏/分屏玩家对战。
- 提供简单易上手的操控方式，通过鼠标或手柄进行移动和发射。

##### 2.3 游戏背景
- 游戏故事设定在白垩纪时代，动物们为了保持体温并乐观面对灾难，玩起了冰球游戏。

##### 2.4 道具系统
- 实现多种道具，如冰墙、冰刃、冰锥等，以增加游戏的竞技性。

##### 2.5 球场多样性
- 提供不同类型的冰球场地，包括传统的冰球场、极地冰原等，每个场地具有独特的地形和障碍物。
- 
##### 2.6 团队合作
- 支持多人对战，允许玩家组建团队进行2v2或3v3的冰球比赛，强调团队合作。

##### 2.7 图形和音效
- 采用Unity 3D游戏引擎，实现逼真的冰雪场地。
- 针对冰球碰撞、场景碰撞、场景氛围等方面的音效，创造紧张刺激的氛围。

#### 3. 系统需求

##### 3.1 平台支持
- 采用WebGL技术，部署到Web服务器上。
- 兼容主流游戏平台，包括PC和移动设备。

##### 3.2 性能要求
- 在各平台上保持流畅的游戏性能，确保用户体验。
- 支持竖屏设备的不同分辨率和设备规格。

#### 4. 开发和测试需求

##### 4.1 开发工具
- 使用Unity 3D作为游戏开发引擎。
- 配备Visual Studio集成开发环境（IDE）和 Git版本控制系统用于项目管理和回滚。

##### 4.2 测试
- 在不同设备和浏览器上进行兼容性测试。

## 概要设计
这里使用 GoodNotes 5 简单画一下这个项目的大概运行/设计流程：
<img alt="picture 8" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240110-113636.jpg" width="600" />

> 标题：[Unity 3D] 4天开发冰球游戏_Day1_项目准备
> 链接：[Yew's Blog](leonyew.fun)
> 工具：Written with [StackEdit中文版](https://stackedit.cn/).
> 日期：2024年1月8日