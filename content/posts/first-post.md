---
title: "FrameVerse 帧之寰宇"
date: 2026-06-20T08:00:00+08:00
draft: false
tags: ["入门"]
categories: ["随笔"]
---

探索计算机图形学的无限可能。

## 关注领域

- **实时渲染**：PBR、延迟渲染、前向+渲染管线
- **着色器开发**：GLSL / HLSL / WGSL，视觉效果与后处理
- **光线追踪**：路径追踪、蒙特卡洛方法、降噪
- **游戏引擎图形**：场景管理、剔除、LOD、GPU 驱动渲染
- **图形算法理论**：几何处理、网格优化、动画与模拟

## 代码示例：GLSL 简易菲涅尔效果

```glsl
vec3 fresnel_schlick(float cosTheta, vec3 F0) {
    return F0 + (1.0 - F0) * pow(clamp(1.0 - cosTheta, 0.0, 1.0), 5.0);
}
```

后续会持续分享渲染管线、Shader 技巧、图形算法等实践笔记，敬请期待。