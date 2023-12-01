# Unity实例01：走迷宫找到出口
> 日期：2023年11月21日  
 班级：数字媒体技术1302班  
 课程：游戏应用程序开发  
 环境：Unity 2022.3.9f1c1  

# 开发准备 Dev Preparation
## 核心功能 TO-DO Func
1. 创建主角
2. 游戏角色添加动画
3. 游戏环境设置
4. 游戏人物控制
5. 镜头跟踪
6. 通关触发
7. 静态、动态敌人
8. 视觉渲染
9. 音效控制
10. 项目的发布
11. ...

## 资源准备 Res Preparation
1. 去 [Unity Assets Store](https://assetstore.unity.com/) 下载官方资源：[3D Beginner](https://assetstore.unity.com/packages/essentials/tutorial-projects/unity-learn-3d-beginner-tutorial-resources-urp-143848)
2. 检查资源兼容性，URP通用渲染管线和SRP可编程渲染管线


# 开发过程 Dev Progress

## 项目创建 Initialize Project
1. 查看版本是否支持某些3D模板
2. 选择普通`3D(URP)`模板，创建项目`INS01_3DTutorial`
3. 下载Package之后，开始开发程序

## 场景搭建 Scene Setup
1. 在Store界面点击`添加到我的资源`，选择`在Unity中打开`
2. 然后在`Package Manager`选择`Download`，等待下载完成
3. 选择`Import --> Next`，等待资源导入
4. 在`UnityTechnologies\Prefebs`将官方下载的Package中的Prefeb预制体场景`Level`拖出来
5. 给场景的 Position Reset一下。
6. 给Scene更名为`MainScene`，方便后续开发

## 添加角色 Import Character
1. 在该路径下：`Models\Characters`
2. 将 `JohnLemon` 的 `Prefeb` 拖到场景 (MainScene) 中并 `Reset Position`

## 角色动画 Animator
1. 形成动画的方式：修改Transform的属性
2. 使用Unity的动画资源
   1. 在Animation\Animation下找到John@Walk和John@Idle
3. 创建动画
   1. Window --> Animation 打开Animation窗口
   2. 新建一个动画，查看Inspector面板，可以看到Animator
   3. 在Animator窗口，可以看到John连接到了TestAnimation
   4. 删除TestAnimation，将Unity中的John@Idle导入进来并让John连接到Idle动画
   5. 点击运行游戏，可以查看到效果。
4. Animation 和 Animator 的区别

| Animation | Animator |
| ---- | ---- |
| 动画设置，控制一个动画播放的各类方法和数据 | 动画控制器：动画切换、叠加以及控制骨骼等复杂的效果 |


## 角色设置 Character Coding
### 行走动画处理
1. 创建Animator来控制
   1. Entry：进入
   2. Exit：退出
   3. 创建动作转换
      1. 创建Bool Parameter：isWalking
      2. Entry --(default)--> Idle <===> Walk
      3. 设置conditions
      4. 取消勾选 `Has Exit Time`
2. 绑定了角色的 Animator 勾选 `Apply Root Motion`
3. 运行游戏，改变 isWalking 的值，查看效果
### 添加刚体 Rigid Body
为了让角色与环境产生正确的动作交互，需要给角色添加上 `Rigidbody`
1. Animator 会与 Rigidbody 更新冲突，导致角色上升
Fix: 将 Animator 的 `Update Mode` 更改为 `Animate Physics`

### 按键行走实现 Walking Code
参考效果：GTA V 中游戏角色转向行走

核心技术：
- 确定角色朝向
- 更改角色朝向
- 摄像机视角跟随转动
- 响应鼠标拖拽和键盘响应的视角转动

## 光源
光源主要有以下几类：
- 点光源
- 方向光（太阳光）
- 聚光灯
- 面光源

### 调整光线
这里我们使用方向光来模拟月光，并在Lightning面板中进行调整。

### 全局照明（GI）
- 通过预先计算好的光照贴图提供间接光照信息（烘培）

## 自动寻路
1. 若Unity版本在2022以下，首先在Package Manager中安装：AI Navigation的包
2. 打开寻路面板：Window -- AI -- AI Navigation
3. 