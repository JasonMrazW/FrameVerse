---
title: "KaTeX 数学公式速查表"
date: 2026-06-21T09:07:39+08:00
draft: false
tags: ["入门", "数学", "KaTeX", "LaTeX"]
categories: ["入门资源"]
---

这篇文章记录博客中常用的 KaTeX 数学公式写法，方便写线性代数、图形学和渲染相关笔记时复制使用。

## 基础规则

| 场景 | 写法 | 说明 |
|------|------|------|
| 行内公式 | `$\vec{v}$` | 嵌入在正文中的短公式 |
| 独立公式块 | `$$ ... $$` | 单独成行展示的公式 |
| 下标 | `$v_x$` | 向量分量、序号 |
| 上标 | `$x^2$` | 幂、转置、逆矩阵 |
| 多字符上下标 | `$v_{normal}$` | 多字符需要用 `{}` 包起来 |

行内公式示例：向量可以写成 $\vec{v}$ 或 $\mathbf{v}$。

独立公式块示例：

$$
\mathbf{a} \cdot \mathbf{b} = \|\mathbf{a}\| \|\mathbf{b}\| \cos\theta
$$

## 向量

| 含义 | 写法 | 效果 |
|------|------|------|
| 箭头向量 | `$\vec{v}$` | $\vec{v}$ |
| 粗体向量 | `$\mathbf{v}$` | $\mathbf{v}$ |
| 单位向量 | `$\hat{\mathbf{v}}$` | $\hat{\mathbf{v}}$ |
| 向量分量 | `$\mathbf{v} = (x, y, z)$` | $\mathbf{v} = (x, y, z)$ |
| 向量长度 | `$\|\mathbf{v}\|$` | $\|\mathbf{v}\|$ |
| 归一化 | `$\hat{\mathbf{v}} = \frac{\mathbf{v}}{\|\mathbf{v}\|}$` | $\hat{\mathbf{v}} = \frac{\mathbf{v}}{\|\mathbf{v}\|}$ |

## 点积与叉积

| 含义 | 写法 | 效果 |
|------|------|------|
| 点积 | `$\mathbf{a} \cdot \mathbf{b}$` | $\mathbf{a} \cdot \mathbf{b}$ |
| 叉积 | `$\mathbf{a} \times \mathbf{b}$` | $\mathbf{a} \times \mathbf{b}$ |
| 夹角余弦 | `$\cos\theta = \frac{\mathbf{a}\cdot\mathbf{b}}{\|\mathbf{a}\|\|\mathbf{b}\|}$` | $\cos\theta = \frac{\mathbf{a}\cdot\mathbf{b}}{\|\mathbf{a}\|\|\mathbf{b}\|}$ |
| 投影 | `$\operatorname{proj}_{\mathbf{b}}\mathbf{a}$` | $\operatorname{proj}_{\mathbf{b}}\mathbf{a}$ |

常用推导：

$$
\operatorname{proj}_{\mathbf{b}}\mathbf{a}
= \frac{\mathbf{a}\cdot\mathbf{b}}{\|\mathbf{b}\|^2}\mathbf{b}
$$

## 矩阵

矩阵通常用独立公式块书写：

```markdown
$$
A =
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
```

渲染效果：

$$
A =
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

| 含义 | 写法 | 效果 |
|------|------|------|
| 转置 | `$A^T$` | $A^T$ |
| 逆矩阵 | `$A^{-1}$` | $A^{-1}$ |
| 逆转置 | `$(M^{-1})^T$` | $(M^{-1})^T$ |
| 矩阵乘向量 | `$M\mathbf{v}$` | $M\mathbf{v}$ |
| 齐次坐标 | `$\mathbf{p} = (x, y, z, 1)^T$` | $\mathbf{p} = (x, y, z, 1)^T$ |

## 变换矩阵

平移矩阵：

$$
T =
\begin{bmatrix}
1 & 0 & 0 & t_x \\
0 & 1 & 0 & t_y \\
0 & 0 & 1 & t_z \\
0 & 0 & 0 & 1
\end{bmatrix}
$$

缩放矩阵：

$$
S =
\begin{bmatrix}
s_x & 0 & 0 & 0 \\
0 & s_y & 0 & 0 \\
0 & 0 & s_z & 0 \\
0 & 0 & 0 & 1
\end{bmatrix}
$$

## 常用符号

| 含义 | 写法 | 效果 |
|------|------|------|
| 希腊字母 theta | `$\theta$` | $\theta$ |
| 希腊字母 alpha | `$\alpha$` | $\alpha$ |
| 希腊字母 beta | `$\beta$` | $\beta$ |
| 约等于 | `$\approx$` | $\approx$ |
| 不等于 | `$\neq$` | $\neq$ |
| 小于等于 | `$\leq$` | $\leq$ |
| 大于等于 | `$\geq$` | $\geq$ |
| 无穷 | `$\infty$` | $\infty$ |
| 求和 | `$\sum_{i=1}^{n} x_i$` | $\sum_{i=1}^{n} x_i$ |
| 积分 | `$\int_a^b f(x)\,dx$` | $\int_a^b f(x)\,dx$ |

## 分段与对齐

分段函数：

```markdown
$$
f(x) =
\begin{cases}
x, & x \geq 0 \\
-x, & x < 0
\end{cases}
$$
```

渲染效果：

$$
f(x) =
\begin{cases}
x, & x \geq 0 \\
-x, & x < 0
\end{cases}
$$

多行对齐：

```markdown
$$
\begin{aligned}
\mathbf{v} &= a\mathbf{i} + b\mathbf{j} + c\mathbf{k} \\
\|\mathbf{v}\| &= \sqrt{a^2 + b^2 + c^2}
\end{aligned}
$$
```

渲染效果：

$$
\begin{aligned}
\mathbf{v} &= a\mathbf{i} + b\mathbf{j} + c\mathbf{k} \\
\|\mathbf{v}\| &= \sqrt{a^2 + b^2 + c^2}
\end{aligned}
$$

## 图形学常用公式

Lambert 漫反射：

$$
L_d = k_d I \max(0, \mathbf{n}\cdot\mathbf{l})
$$

反射向量：

$$
\mathbf{r} = \mathbf{i} - 2(\mathbf{i}\cdot\mathbf{n})\mathbf{n}
$$

线性插值：

$$
\operatorname{lerp}(a, b, t) = (1-t)a + tb
$$

## 避坑说明

- 不要把公式放在反引号里，比如 `` `$\vec{v}$` ``，这样会被当作代码。
- 多字符下标或上标要用 `{}`，比如 `$v_{normal}$`，不要写 `$v_normal$`。
- 公式块建议上下各空一行，避免 Markdown 解析异常。
- 表格里可以写行内公式，但复杂矩阵建议放在表格外。
- KaTeX 不是完整 LaTeX，遇到不支持的命令可以查 [KaTeX 支持列表](https://katex.org/docs/supported)。

持续更新中。
