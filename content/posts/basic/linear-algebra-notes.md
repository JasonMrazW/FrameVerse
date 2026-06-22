---
title: "线性代数学习笔记"
date: 2026-06-20T11:00:39+08:00
draft: false
tags: ["入门", "数学", "线性代数"]
categories: ["入门资源"]
---

这篇文章用来记录线性代数学习过程中的关键概念、直觉理解和图形学相关应用。

## 学习目标

- 建立向量、矩阵、线性变换的几何直觉
- 理解坐标系、基、投影、旋转与缩放
- 掌握图形学中常见的矩阵变换与空间转换
- 为后续学习渲染管线、着色器、光线追踪和几何算法打基础

## 学习记录

| 日期 | 内容 | 关键收获 |
|------|------|----------|
| 待补充 | 向量与线性组合 | 待补充 |
| 待补充 | 矩阵与线性变换 | 待补充 |
| 待补充 | 基与坐标系 | 待补充 |
| 待补充 | 点积、叉积与投影 | 待补充 |
| 待补充 | 特征值与特征向量 | 待补充 |

## 核心概念

### 向量

向量不仅可以看作一组数字，也可以理解为带有方向和长度的量。在图形学中，向量常用于表示位置、方向、法线、速度和颜色等信息。

`unit vector 单位向量`：长度为1的向量，常用于表示方向。$\hat{i}, \hat{j}, \hat{k}$ 分别表示 x轴、y轴和 z轴的方向。

`linear combination 线性组合`：将多个向量按比例相加，得到一个新的向量. 
$$\vec{v} = i * \vec{a} + j * \vec{b}$$

`span 线性组合的范围`：由多个向量按比例相加得到的所有向量的集合。

通常使用point 表示向量，不用考虑箭头

`linear dependence 线性依赖`：多个向量之间存在线性关系，不能独立表示。

`linear independence 线性独立`：多个向量之间不存在线性关系，可以独立表示。

The basic of a vector space is a set of linear independent vectors that span the full space.

`basis 基`：线性独立的向量集合，可以表示空间中的所有向量。

`coordinate system 坐标系`：将空间中的向量表示为基向量的线性组合。

### 矩阵

矩阵可以理解为对空间的一种变换。常见变换包括缩放、旋转、平移、投影，以及不同坐标空间之间的转换。

### 线性变换

线性变换会保持网格线平行且等距，原点保持不动。理解线性变换的几何意义，有助于理解模型矩阵、视图矩阵和投影矩阵。

## 图形学关联

| 线性代数概念 | 图形学应用 |
|--------------|------------|
| 向量 | 位置、方向、法线、光照计算 |
| 点积 | 夹角、投影、漫反射光照 |
| 叉积 | 法线计算、坐标系构造 |
| 矩阵 | 模型变换、视图变换、投影变换 |
| 逆矩阵 | 坐标空间反向转换 |
| 特征值/特征向量 | PCA、形变分析、几何处理 |

## 待深入问题

- 为什么矩阵乘法可以表示连续的空间变换？
- 为什么法线变换需要使用逆转置矩阵？
- 齐次坐标为什么能把平移统一到矩阵乘法里？
- 投影矩阵如何把三维空间映射到裁剪空间？

## 参考资源

- [3Blue1Brown：线性代数的本质](https://www.bilibili.com/video/BV1ys411472E)
- [MIT 18.06 Linear Algebra](https://ocw.mit.edu/courses/18-06-linear-algebra-spring-2010/)
- [Immersive Math: Interactive Linear Algebra](https://immersivemath.com/ila/)
- 《3D Math Primer for Graphics and Game Development》
- 《Mathematics for 3D Game Programming and Computer Graphics》

持续更新中。
