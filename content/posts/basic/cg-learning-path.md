---
title: "计算机图形学学习路线"
date: 2026-06-20T09:52:49+08:00
draft: false
tags: ["入门", "学习路线"]
categories: ["入门资源"]
---

梳理计算机图形学的核心学习方向与技能树，供入门参考。

## 数学基础

图形学的根基是数学，建议优先掌握：

- **线性代数**：向量、矩阵、变换、特征值分解。推荐 *3Blue1Brown 线性代数本质（视频）*
- **微积分**：导数、梯度、积分，用于光照模型和物理模拟
- **几何**：解析几何、三角学、四元数（旋转表示）
- **概率统计**：蒙特卡洛积分、重要性采样（光线追踪核心）

## 编程基础

- **C/C++**：图形学主流语言，绝大多数引擎和工具链用 C++ 编写
- **Python**：快速原型、数据处理、Blender 脚本
- **OpenGL / Vulkan / DirectX**：至少掌握一个图形 API
- **Shader 语言**：GLSL（入门友好）→ HLSL → WGSL

## 核心方向

### 实时渲染（Real-time Rendering）

| 知识点 | 说明 |
|--------|------|
| 渲染管线 | 顶点 → 光栅化 → 片元，理解 GPU 工作原理 |
| PBR | 基于物理的渲染，金属度/粗糙度工作流 |
| 光照模型 | Blinn-Phong、Cook-Torrance、环境光遮蔽 |
| 阴影 | Shadow Map、CSM、PCF/PCSS 软阴影 |
| 后处理 | Bloom、HDR、色调映射、SSAO |

**推荐书单**：*Real-Time Rendering 4th*

### 光线追踪（Ray Tracing）

- 路径追踪、Whitted 风格光线追踪
- 加速结构：BVH、KD-Tree
- 降噪算法：SVGF、ReSTIR
- RTX 硬件光追管线

### 游戏引擎图形

- 场景管理与剔除：Frustum Culling、Occlusion Culling
- LOD 系统：网格简化、着色器 LOD
- GPU 驱动渲染：Bindless、Mesh Shader
- 了解 UE5 Nanite/Lumen 或 Unity HDRP 架构

### 着色器开发

- 材质系统：Standard PBR、Clear Coat、Subsurface
- 特效：体积光、粒子、屏幕空间反射
- 计算着色器：GPGPU 基础

### 图形算法

- 网格处理：细分、简化、平滑
- 动画：骨骼动画、蒙皮、IK
- 模拟：流体、布料、刚体
- 几何：贝塞尔曲线、B 样条、NURBS

## 学习路径建议

```
数学基础（线性代数 + 微积分）
    ↓
C++ 基础 + OpenGL 入门（learnopengl.com）
    ↓
实时渲染入门（Real-Time Rendering 精读）
    ↓
选一个方向深入：
├── 实时渲染 → 引擎开发
├── 光线追踪 → 离线渲染 / 电影
├── 着色器 → TA（技术美术）
└── 图形算法 → 学术研究
```

## 推荐资源

| 类型 | 资源 |
|------|------|
| 网站 | [LearnOpenGL](https://learnopengl.com/)、[Scratchapixel](https://www.scratchapixel.com/) |
| 书籍 | *Real-Time Rendering*、*PBRT*、*Fundamentals of Computer Graphics* |
| 视频 | GDC Vault、SIGGRAPH 论文演讲、闫令琪 Games101 课程 |
| 社区 | Reddit r/GraphicsProgramming、知乎图形学话题 |
| 工具 | RenderDoc、NVIDIA Nsight、ShaderToy |

持续更新中，欢迎补充。