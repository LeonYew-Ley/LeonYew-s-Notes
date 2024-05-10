# 利用 TrailRender 在 Unity 中制作笔刷功能
要制作笔刷，我们会用到Trail Renderer 或 Line Renderer。不过，Line Renderer的原理是在多个顶点之间形成直线，所有不太适用于连续的笔刷效果，因此，我们采用 Trail Renderer，用于在移动的游戏对象后面随着时间推移渲染出来的一条多边形轨迹，常用于制作物体的运动尾迹。
## 创建 Stroke 预制体
由于我们要实现多个笔刷功能，一个笔划应该保存为一个实例，所以我们要为笔划创建 Prefeb，并添加 Trail Renderer 在它上面。

Hierarchy 面板 > 右键 > Create Empty Object > 命名为 Stroke

Inspector 面板 > Add Component > Trail Renderer

创建 Prefeb：将 Stroke 拖入 Project 面板 Prefeb 文件夹，完成预制体创建。

## 创建脚本
由于脚本需要绑定到游戏对象上面才能运行，所以我们创建一个名为 Script 的空物体，把脚本绑定在它身上。

注：如果把脚本绑定在 Stroke 身上，由于脚本中需要实例化 Stroke，所以会导致实例化的 Stroke 数量呈指数级增长（2,4,8,16,32...）

在 Project 面板创建脚本，命名为 BrushController，脚本内容如下：
```cs
using System;
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using Valve.VR;

public class Stroke_PC : MonoBehaviour
{
    public TrailRenderer trailRenderer; // 获取 TrailRenderer 组件
    private GameObject currentTrail; // 当前轨迹
    private List<GameObject> trailList = new List<GameObject>(); // 保存实例化轨迹的列表
    private Vector3 mousePos; // 鼠标位置
    private Boolean isPainting; // 是否正在绘制

    void Update()
    {
        // 检测鼠标左键按下

        if (Input.GetMouseButtonDown(0))
        {
            PaintingStart(); // 开始绘制轨迹
        }
        // 检测鼠标左键长按
        if (Input.GetMouseButton(0) && isPainting)
        {
            PaintingContinue(); // 继续绘制轨迹
        }

        // 检测鼠标左键释放
        if (Input.GetMouseButtonUp(0))
        {
            PaintingStop(); // 停止绘制
        }
    }
    private void PaintingStart()
    {
        Debug.Log("PaintingStart");
        isPainting = true;
        currentTrail = Instantiate(trailRenderer.gameObject, GetMousePosition(), Quaternion.identity); // 实例化轨迹
    }
    private void PaintingContinue()
    {
        Debug.Log("PaintingContinue");
        currentTrail.gameObject.transform.position = GetMousePosition();
    }

    private void PaintingStop()
    {
        Debug.Log("PaintingStop");
        isPainting = false;
        trailList.Add(currentTrail); // 将当前轨迹添加到列表
        currentTrail = null; // 清楚轨迹，为下一次绘制做准备
    }

    private Vector3 GetMousePosition()
    {
        mousePos = Input.mousePosition;
        mousePos.z = 5f;
        return Camera.main.ScreenToWorldPoint(mousePos);
    }
}
```

## 设置脚本、测试功能
将 Stroke 预制体从 Hierarchy 面板拖到脚本的 trailRenderer 中，运行游戏。
<img alt="picture 0" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240510-153553.gif" width="600" />  
