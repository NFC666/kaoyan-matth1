# 📌 第四章 不定积分 考研核心通关笔记

---

## ① 本章核心知识框架 (Core Concept Map)

### 4.1 不定积分的概念与性质

#### 一、原函数与不定积分的概念

**定义（原函数）**：若在区间 $I$ 上 $F'(x) = f(x)$，则称 $F(x)$ 为 $f(x)$ 在 $I$ 上的一个原函数。

**原函数存在定理**：若 $f(x)$ 在区间 $I$ 上**连续**，则 $f(x)$ 在 $I$ 上必存在原函数。

- *极简例子：* $f(x) = 2x$，$F(x) = x^2$ 是一个原函数，$x^2 + 1$ 也是原函数

**注意**：
- 有第一类间断点的函数**没有**原函数（导数不可能有第一类间断点）
- 初等函数在其定义区间内必有原函数（因为初等函数在其定义区间内连续）

**定义（不定积分）**：$f(x)$ 在区间 $I$ 上的全体原函数称为 $f(x)$ 在 $I$ 上的不定积分，记作：

$$\int f(x)\,dx = F(x) + C$$

其中 $\int$ 为积分号，$f(x)$ 为被积函数，$x$ 为积分变量，$C$ 为**积分常数**。

- *极简例子：* $\int 2x\,dx = x^2 + C$（$C$ 不能丢！）

> ⚠️ **不定积分是一个函数族**，不是单个函数。丢 $C$ 是考研选填题最常见的扣分点。

#### 二、基本积分表（必背 13 式）

| # | 积分公式 | 对应的导数公式 |
|---|---------|--------------|
| 1 | $\displaystyle\int k\,dx = kx + C$ | $(kx)' = k$ |
| 2 | $\displaystyle\int x^\mu\,dx = \frac{x^{\mu+1}}{\mu+1} + C\;(\mu \neq -1)$ | $(x^{\mu+1})' = (\mu+1)x^\mu$ |
| 3 | $\displaystyle\int \frac{1}{x}\,dx = \ln|x| + C$ | $(\ln|x|)' = \frac{1}{x}$ |
| 4 | $\displaystyle\int e^x\,dx = e^x + C$ | $(e^x)' = e^x$ |
| 5 | $\displaystyle\int a^x\,dx = \frac{a^x}{\ln a} + C$ | $(a^x)' = a^x\ln a$ |
| 6 | $\displaystyle\int \sin x\,dx = -\cos x + C$ | $(-\cos x)' = \sin x$ |
| 7 | $\displaystyle\int \cos x\,dx = \sin x + C$ | $(\sin x)' = \cos x$ |
| 8 | $\displaystyle\int \sec^2 x\,dx = \tan x + C$ | $(\tan x)' = \sec^2 x$ |
| 9 | $\displaystyle\int \csc^2 x\,dx = -\cot x + C$ | $(-\cot x)' = \csc^2 x$ |
| 10 | $\displaystyle\int \sec x \tan x\,dx = \sec x + C$ | $(\sec x)' = \sec x \tan x$ |
| 11 | $\displaystyle\int \csc x \cot x\,dx = -\csc x + C$ | $(-\csc x)' = \csc x \cot x$ |
| 12 | $\displaystyle\int \frac{1}{1+x^2}\,dx = \arctan x + C$ | $(\arctan x)' = \frac{1}{1+x^2}$ |
| 13 | $\displaystyle\int \frac{1}{\sqrt{1-x^2}}\,dx = \arcsin x + C$ | $(\arcsin x)' = \frac{1}{\sqrt{1-x^2}}$ |

**扩展积分公式（高频）**：

| 公式 | 使用频率 |
|------|---------|
| $\displaystyle\int \tan x\,dx = -\ln|\cos x| + C$ | ⭐⭐⭐ |
| $\displaystyle\int \cot x\,dx = \ln|\sin x| + C$ | ⭐⭐⭐ |
| $\displaystyle\int \sec x\,dx = \ln|\sec x + \tan x| + C$ | ⭐⭐⭐ |
| $\displaystyle\int \csc x\,dx = \ln|\csc x - \cot x| + C$ | ⭐⭐ |
| $\displaystyle\int \frac{1}{a^2 + x^2}\,dx = \frac{1}{a}\arctan\frac{x}{a} + C$ | ⭐⭐⭐ |
| $\displaystyle\int \frac{1}{\sqrt{a^2 - x^2}}\,dx = \arcsin\frac{x}{a} + C$ | ⭐⭐⭐ |
| $\displaystyle\int \frac{1}{x^2 - a^2}\,dx = \frac{1}{2a}\ln\left|\frac{x-a}{x+a}\right| + C$ | ⭐⭐ |
| $\displaystyle\int \frac{1}{\sqrt{x^2 \pm a^2}}\,dx = \ln|x + \sqrt{x^2 \pm a^2}| + C$ | ⭐⭐ |
| $\displaystyle\int \sqrt{a^2 - x^2}\,dx = \frac{a^2}{2}\arcsin\frac{x}{a} + \frac{x}{2}\sqrt{a^2 - x^2} + C$ | ⭐⭐ |

#### 三、不定积分的性质

1. **线性性质**：$\displaystyle\int [f(x) \pm g(x)]\,dx = \int f(x)\,dx \pm \int g(x)\,dx$
2. **常数可提出**：$\displaystyle\int k f(x)\,dx = k\int f(x)\,dx \quad (k \neq 0)$
3. **微分与积分互为逆运算**：
   - $\displaystyle\frac{d}{dx}\int f(x)\,dx = f(x)$
   - $\displaystyle\int f'(x)\,dx = f(x) + C$

---

### 4.2 换元积分法

#### 一、第一类换元法（凑微分法）⭐⭐⭐

**定理**：若 $\int f(u)\,du = F(u) + C$，且 $u = \varphi(x)$ 可导，则：

$$\int f[\varphi(x)]\varphi'(x)\,dx = \int f(u)\,du \Big|_{u=\varphi(x)} = F[\varphi(x)] + C$$

**核心思想**：将被积表达式「凑」成 $\int g(\varphi(x))\,d\varphi(x)$ 的形式。

*极简例子：* $\int \cos 2x\,dx = \frac{1}{2}\int \cos(2x)\,d(2x) = \frac{1}{2}\sin 2x + C$

**常见凑微分形式**（考研高频）：

| 形式 | 凑微分 | 结果类型 |
|------|--------|---------|
| $\displaystyle\int f(ax+b)\,dx$ | $= \frac{1}{a}\int f(ax+b)\,d(ax+b)$ | 线性凑 |
| $\displaystyle\int f(x^n)x^{n-1}\,dx$ | $= \frac{1}{n}\int f(x^n)\,d(x^n)$ | 幂函数凑 |
| $\displaystyle\int f(e^x)e^x\,dx$ | $= \int f(e^x)\,d(e^x)$ | 指数凑 |
| $\displaystyle\int f(\ln x)\frac{1}{x}\,dx$ | $= \int f(\ln x)\,d(\ln x)$ | 对数凑 |
| $\displaystyle\int f(\sin x)\cos x\,dx$ | $= \int f(\sin x)\,d(\sin x)$ | 三角凑 |
| $\displaystyle\int f(\cos x)\sin x\,dx$ | $= -\int f(\cos x)\,d(\cos x)$ | 三角凑 |
| $\displaystyle\int f(\tan x)\sec^2 x\,dx$ | $= \int f(\tan x)\,d(\tan x)$ | 三角凑 |
| $\displaystyle\int f(\arcsin x)\frac{1}{\sqrt{1-x^2}}\,dx$ | $= \int f(\arcsin x)\,d(\arcsin x)$ | 反三角凑 |
| $\displaystyle\int f(\arctan x)\frac{1}{1+x^2}\,dx$ | $= \int f(\arctan x)\,d(\arctan x)$ | 反三角凑 |

> 口诀：**「前看函数，后看微分；谁复杂先凑谁」**

#### 二、第二类换元法（变量代换法）⭐⭐

**定理**：设 $x = \psi(t)$ 单调可导且 $\psi'(t) \neq 0$，则：

$$\int f(x)\,dx \;\xrightarrow{x = \psi(t)}\; \int f[\psi(t)]\psi'(t)\,dt = \Phi(t) + C \;\xrightarrow{t = \psi^{-1}(x)}\; \Phi[\psi^{-1}(x)] + C$$

**常见代换类型**：

| 被积函数含 | 代换 | 目的 |
|-----------|------|------|
| $\sqrt{a^2 - x^2}$ | $x = a\sin t$（或 $a\cos t$） | 去根号 |
| $\sqrt{a^2 + x^2}$ | $x = a\tan t$ | 去根号 |
| $\sqrt{x^2 - a^2}$ | $x = a\sec t$ | 去根号 |
| $\sqrt[n]{ax+b}$ | $\sqrt[n]{ax+b} = t$ | 去根式 |
| $\sqrt[n]{\frac{ax+b}{cx+d}}$ | 令整个根式为 $t$ | 有理化 |

**三角代换回代方法**：画直角三角形，用边长关系表示三角函数。

*极简例子：* $\int \frac{dx}{\sqrt{a^2 - x^2}}$，令 $x = a\sin t$，$dx = a\cos t\,dt$：

$$\int \frac{a\cos t\,dt}{a\cos t} = \int dt = t + C = \arcsin\frac{x}{a} + C$$

**两类换元法的区别**：
- **第一类（凑微分）**：$\int g(\varphi(x))\varphi'(x)dx \to \int g(u)du$，即 $u = \varphi(x)$
- **第二类（变量代换）**：$\int f(x)dx \to \int f(\psi(t))\psi'(t)dt$，即 $x = \psi(t)$

> 口诀：**「第一类 $u = \varphi(x)$（函数变变量），第二类 $x = \psi(t)$（变量变函数）」**

---

### 4.3 分部积分法 ⭐⭐⭐

**公式**：

$$\int u\,dv = uv - \int v\,du$$

对应导数形式：$(uv)' = u'v + uv'$ 两边积分即得。

*极简例子：* $\int x e^x\,dx$，取 $u = x,\; dv = e^x dx$：
- $du = dx,\; v = e^x$
- $\int x e^x\,dx = x e^x - \int e^x\,dx = x e^x - e^x + C = e^x(x-1) + C$

**选取 $u$ 的优先级口诀——「LIATE 规则」**（反-对-幂-指-三）：

| 优先级 | 函数类型 | 应选为 $u$ | 原因 |
|--------|---------|-----------|------|
| 1（最高） | 对数函数 $\ln x$ | ✅ $u$ | 求导后简化（变 $\frac{1}{x}$） |
| 2 | 反三角函数 $\arcsin x, \arctan x$ | ✅ $u$ | 求导后化为有理式 |
| 3 | 幂函数 $x^n$ | 看情况 | 与指/三配对时选 $u$ |
| 4 | 三角函数 $\sin x, \cos x$ | $dv$ | 积分后仍是三角函数 |
| 5（最低） | 指数函数 $e^x$ | $dv$ | 积分后仍是指数函数 |

**中文口诀：反、对、幂、指、三，排前面的做 $u$。**

**三种经典模式**：

| 模式 | 被积函数 | $u$ 选择 | 技巧 |
|------|---------|---------|------|
| 模式 1 | $x^n e^{kx}$ 或 $x^n \sin ax$ | $u = x^n$ | $n$ 次分部积分降幂 |
| 模式 2 | $x^n \ln x$ 或 $x^n \arcsin x$ | $u = \ln x$ / $\arcsin x$ | 一步到位消去对数/反三角 |
| 模式 3 | $e^{ax}\sin bx$ 或 $e^{ax}\cos bx$ | $u$ 取谁都可以 | 两次分部积分后"回归"，解方程 |

*模式 3 极简例子：* $\int e^x \sin x\,dx$

$$\begin{aligned}
I &= \int e^x \sin x\,dx = e^x \sin x - \int e^x \cos x\,dx \\
  &= e^x \sin x - \left[e^x \cos x - \int e^x (-\sin x)\,dx\right] \\
  &= e^x \sin x - e^x \cos x - I
\end{aligned}$$

$$\Rightarrow 2I = e^x(\sin x - \cos x) \;\Rightarrow\; I = \frac{e^x}{2}(\sin x - \cos x) + C$$

**分部积分的关键判断**：
1. 被积函数是两个不同类型函数的乘积 $\to$ 分部积分
2. 被积函数含有 $\ln x$ 或反三角函数（单独出现也视为与 $1$ 的乘积）$\to$ 分部积分
3. 分部积分一次后积分项比原来简单 $\to$ 方向正确

---

### 4.4 有理函数的积分

#### 一、有理函数的积分

**定义**：有理函数 $R(x) = \frac{P_n(x)}{Q_m(x)}$，其中 $P_n$ 和 $Q_m$ 分别为 $n$ 次和 $m$ 次多项式。

**方法——部分分式分解（Partial Fraction Decomposition）**：

**Step 1**：若 $n \ge m$（假分式），先做多项式除法化为「多项式 + 真分式」。

*极简例子：* $\frac{x^2}{x+1} = x - 1 + \frac{1}{x+1}$

**Step 2**：将分母 $Q_m(x)$ 分解为一次因式和不可约二次因式的乘积。

**Step 3**：按以下规则拆分为部分分式之和：

| 分母因子 | 部分分式形式 |
|---------|-------------|
| $(x-a)$ | $\displaystyle\frac{A}{x-a}$ |
| $(x-a)^k$ | $\displaystyle\frac{A_1}{x-a} + \frac{A_2}{(x-a)^2} + \cdots + \frac{A_k}{(x-a)^k}$ |
| $x^2+px+q$（不可约） | $\displaystyle\frac{Ax+B}{x^2+px+q}$ |
| $(x^2+px+q)^k$ | $\displaystyle\frac{A_1x+B_1}{x^2+px+q} + \cdots + \frac{A_kx+B_k}{(x^2+px+q)^k}$ |

**Step 4**：通过待定系数法确定各常数（通分 + 比较同次幂系数）。

**Step 5**：逐项积分。两类基本积分结果：

- $\displaystyle\int \frac{1}{x-a}\,dx = \ln|x-a| + C$
- $\displaystyle\int \frac{1}{(x-a)^k}\,dx = -\frac{1}{(k-1)(x-a)^{k-1}} + C \quad (k \ge 2)$
- 对 $\frac{Ax+B}{x^2+px+q}$：分子凑成分母的导数 $+$ 常数，拆为 $\arctan$ 型 + $\ln$ 型

*极简例子：* $\int \frac{dx}{x^2 - 1} = \frac{1}{2}\int\left(\frac{1}{x-1} - \frac{1}{x+1}\right)dx = \frac{1}{2}\ln\left|\frac{x-1}{x+1}\right| + C$

#### 二、可化为有理函数的积分举例

**① 三角有理式 $\int R(\sin x, \cos x)\,dx$**

**万能代换**（通用但计算量大）：令 $t = \tan\frac{x}{2}$

$$\sin x = \frac{2t}{1+t^2},\quad \cos x = \frac{1-t^2}{1+t^2},\quad dx = \frac{2}{1+t^2}dt$$

**更优先的特殊情况**：

| 条件 | 代换 | 更简便 |
|------|------|--------|
| $R(-\sin x, \cos x) = -R(\sin x, \cos x)$（关于 $\sin x$ 为奇函数） | $t = \cos x$ | ✅ |
| $R(\sin x, -\cos x) = -R(\sin x, \cos x)$（关于 $\cos x$ 为奇函数） | $t = \sin x$ | ✅ |
| $R(-\sin x, -\cos x) = R(\sin x, \cos x)$（偶函数） | $t = \tan x$ | ✅ |

> 一般优先用特殊代换，实在不行再用万能代换。

**② 简单无理函数的积分**

| 被积函数含 | 代换 |
|-----------|------|
| $\sqrt[n]{ax+b}$ | $t = \sqrt[n]{ax+b}$ |
| $\sqrt[n]{\frac{ax+b}{cx+d}}$ | $t = \sqrt[n]{\frac{ax+b}{cx+d}}$ |
| $\sqrt{ax+b}$ 和 $\sqrt{ax+b}$ 的不同根次 | $t = \sqrt[\text{lcm}]{ax+b}$（取最小公倍数次根） |

*极简例子：* $\int \frac{\sqrt{x}}{1+\sqrt{x}}\,dx$，令 $t = \sqrt{x}$，$x = t^2$，$dx = 2t\,dt$：
原式 $= \int \frac{t}{1+t} \cdot 2t\,dt = 2\int\left(t-1+\frac{1}{t+1}\right)dt$（有理化后积分）

---

### 4.5 积分表的使用

考研中积分表不直接考，但以下**必须记住的递推公式**来自积分表：

**$\sin^n x$ 和 $\cos^n x$ 的递推公式**：

$$\int \sin^n x\,dx = -\frac{1}{n}\sin^{n-1}x\cos x + \frac{n-1}{n}\int \sin^{n-2}x\,dx$$

$$\int \cos^n x\,dx = \frac{1}{n}\cos^{n-1}x\sin x + \frac{n-1}{n}\int \cos^{n-2}x\,dx$$

*极简例子（$n=2$）：* $\int \sin^2 x\,dx = -\frac{1}{2}\sin x\cos x + \frac{1}{2}\int dx = \frac{x}{2} - \frac{\sin 2x}{4} + C$

---

## ② 必考题型分类索引

| # | 题型 | 核心判据 | 详细笔记 |
|---|------|---------|---------|
| 1 | 原函数与不定积分的概念 | 原函数存在性、间断点类型、$f$ 与 $F$ 关系判定 | [[题型1_原函数与不定积分概念]] |
| 2 | 第一类换元法（凑微分） | 被积函数含 $\varphi'(x)f(\varphi(x))$ 结构 | [[题型2_第一类换元法]] |
| 3 | 第二类换元法（变量代换） | 含根式 $\sqrt{a^2 \pm x^2}$、$\sqrt{x^2 \pm a^2}$ 或 $\sqrt[n]{ax+b}$ | [[题型3_第二类换元法]] |
| 4 | 分部积分法 | 两类函数乘积、含 $\ln x$/反三角、$e^{ax}\sin bx$ 型 | [[题型4_分部积分法]] |
| 5 | 有理函数的积分 | 真分式、假分式、分母可因式分解 | [[题型5_有理函数的积分]] |
| 6 | 可化为有理函数的积分 | 三角有理式、无理根式 | [[题型6_可化为有理函数的积分]] |

---

## ③ 高频考点与多维变换

### Top 5 高频考点

| 排名 | 考点 | 近15年考频 | 典型分值 |
|------|------|-----------|---------|
| 1 | 分部积分法 | 几乎每年 | 5-10分 |
| 2 | 第一类换元法（凑微分） | 每年必然 | 4-5分 |
| 3 | 有理函数积分 | 10次 | 5-10分 |
| 4 | 第二类换元法（三角代换） | 8次 | 4-5分 |
| 5 | 原函数/不定积分概念题 | 6次 | 3-5分（选填） |

### 【示例：一题多角度】

**核心概念**：$\displaystyle\int \frac{dx}{x^2\sqrt{1+x^2}}$

**角度一：三角代换（经典解法）**
令 $x = \tan t$，$dx = \sec^2 t\,dt$，$\sqrt{1+x^2} = \sec t$

$$\begin{aligned}
\int \frac{dx}{x^2\sqrt{1+x^2}}
&= \int \frac{\sec^2 t\,dt}{\tan^2 t \cdot \sec t}
= \int \frac{\cos t}{\sin^2 t}\,dt \\
&= \int \csc t \cot t\,dt = -\csc t + C
= -\frac{\sqrt{1+x^2}}{x} + C
\end{aligned}$$

**角度二：倒代换（更巧妙）**
令 $x = \frac{1}{t}$，$dx = -\frac{1}{t^2}dt$

$$\int \frac{dx}{x^2\sqrt{1+x^2}} = \int \frac{-1/t^2\,dt}{(1/t^2)\sqrt{1+1/t^2}} = -\int \frac{dt}{\sqrt{t^2+1}} = -\ln|t + \sqrt{t^2+1}| + C$$

再代回 $t = \frac{1}{x}$ 即得。虽然形式不同但等价。

**启示**：含 $\frac{1}{x^2}$ 因子时常可用倒代换 $x = \frac{1}{t}$ 简化。

### 【示例：一题多角度 · 分部积分策略】

> **题目**：$\displaystyle\int x\arctan x\,dx$

**角度一：LIATE 规则（反三角在前，选 $u$）**
$u = \arctan x$，$dv = x\,dx$

$du = \frac{1}{1+x^2}dx$，$v = \frac{x^2}{2}$

$$\int x\arctan x\,dx = \frac{x^2}{2}\arctan x - \frac{1}{2}\int \frac{x^2}{1+x^2}\,dx$$

化简：$\frac{x^2}{1+x^2} = 1 - \frac{1}{1+x^2}$

$$= \frac{x^2}{2}\arctan x - \frac{1}{2}\left(x - \arctan x\right) + C = \frac{x^2+1}{2}\arctan x - \frac{x}{2} + C$$

**角度二：先凑微分再分部**
$\int x\arctan x\,dx = \frac{1}{2}\int \arctan x\,d(x^2+1)$（凑微分小技巧）

结果与角度一完全一致，但多了一个 $\frac{1}{2}\arctan x$ 的路径选择。

**启示**：同一道题两种 $u$ 选择思路都能做，LIATE 规则选 $u = \arctan x$ 最自然。

---

## ④ 方法论与解题通法 (Methodology)

### 方法一：积分方法选择决策树 ⭐⭐⭐

```
遇到不定积分？
  ├── 是否为基本积分表中的形式？ → 直接套公式
  ├── 是否可通过恒等变形化为基本形式？ → 拆项 / 三角恒等变形
  ├── 是否含 φ'(x)f(φ(x)) 结构？ → 第一类换元法（凑微分）
  ├── 是否含 √(a²±x²) 或 √(x²±a²)？ → 第二类换元法（三角代换）
  ├── 是否为两类函数乘积？
  │     ├── 含 ln x 或反三角？ → u = ln x / 反三角，分部积分
  │     ├── 含 xⁿeᵏˣ / xⁿsin x？ → u = xⁿ，分部积分降幂
  │     ├── 含 eᵃˣsin bx？ → 分部积分两次 + 解方程
  │     └── 含 xⁿ(ln x)ᵐ？ → u = (ln x)ᵐ，多次分部
  ├── 是否为有理函数？ → 部分分式分解
  ├── 是否为三角有理式？ → 特殊代换 > 万能代换
  └── 是否为无理函数？ → 去根号代换
```

### 方法二：凑微分的「五看法」

| 看 | 内容 | 技巧 |
|----|------|------|
| 看分母 | 分母的导数是否在分子中出现？ | 是 $\to$ 凑 $\int \frac{du}{u}$ |
| 看根号 | 根号内式子求导是否在外部？ | 是 $\to$ 凑 $\int \frac{du}{\sqrt{u}}$ |
| 看指数 | 是否有 $f(e^x)e^x$ 结构？ | 是 $\to$ 凑 $\int f(e^x)de^x$ |
| 看复合 | 复合函数内外层导数关系？ | 外导/内导 是否匹配 |
| 看常数 | 差常数倍能否补上？ | 是 $\to$ 乘 $\frac{1}{k}$ 补 |

### 方法三：「分部积分的选 $u$ 三步法」

1. **看有没有 $\ln x$ 或反三角** → 有则直接选 $u = \ln x$ / 反三角
2. **看有没有 $x^n$ 与 $e^x$ 或 $\sin/\cos$ 乘积** → 有则选 $u = x^n$
3. **看是否 $e^{ax}\sin bx$ / $e^{ax}\cos bx$** → 任意选，两次分部后解方程

### 方法四：有理函数积分的待定系数速算法

**技巧 1 — 赋值法**：部分分式等式中代入分母的根，直接得到对应系数。
- *极简例子：* $\frac{1}{(x-1)(x+2)} = \frac{A}{x-1} + \frac{B}{x+2}$，代入 $x=1$ 得 $A = \frac{1}{3}$，代入 $x = -2$ 得 $B = -\frac{1}{3}$

**技巧 2 — 极限法**：两边乘以 $(x-a)^k$ 后取极限 $x \to a$。

**技巧 3 — 导数法**：用于重因式情况，对等式求导后代入。

---

## ⑤ 易错点红黑榜 (The Pitfall List)

### ❌ 错误 1：忘记加积分常数 $C$

- **错误表现**：$\int 2x\,dx = x^2$（漏 $C$）
- **正确理解**：不定积分是**函数族**，$C$ 代表整个平行曲线族。选填题中无 $C$ 直接扣分。

### ❌ 错误 2：混淆两类换元法

- **错误表现**：第二类换元法不做回代，答案里还留着 $t$
- **正确理解**：
  - **第一类**（凑微分）$\to$ 变量不变，不需要回代
  - **第二类**（变量代换）$\to$ 变量变了，**必须回代**到 $x$ 才能作为最终答案

### ❌ 错误 3：求导验证不匹配却没发现

**【对比示例】**：
```
❌ ∫ sin x cos x dx = (sin²x)/2 + C 和 = -(cos²x)/2 + C 互相矛盾？
✅ 两者只差常数 1/2，都属于同一函数族。求导验证：两边求导都等于 sin x cos x ✓
```

### ❌ 错误 4：分部积分 $u$ 和 $dv$ 选反

**【对比示例】**：
```
❌ ∫ x eˣ dx，选 u = eˣ, dv = x dx → v = x²/2, 积分变为 ∫ (x²/2)eˣ dx（更复杂！）
✅ ∫ x eˣ dx，选 u = x, dv = eˣ dx → v = eˣ, 积分变为 ∫ eˣ dx（一次解决）
```

### ❌ 错误 5：部分分式分母分解不完全

- **错误表现**：$x^3-1$ 只拆成 $(x-1)(x^2+x+1)$ 但不知道 $x^2+x+1$ 是否可约
- **正确理解**：$x^2+x+1$ 判别式 $\Delta = 1 - 4 = -3 < 0$，在实数域不可约 → 对应部分分式为 $\frac{Ax+B}{x^2+x+1}$

### ❌ 错误 6：三角有理式盲目用万能代换

- **错误表现**：$\int \frac{\sin x}{1+\cos^2 x}dx$ 也用 $t = \tan\frac{x}{2}$
- **正确理解**：$\sin x\,dx = -d(\cos x)$，令 $u = \cos x$：$\int \frac{-du}{1+u^2} = -\arctan u = -\arctan(\cos x) + C$，一步到位。

### ❌ 错误 7：忽略了 $dx$ 的转换

**【对比示例】**：
```
❌ ∫ sin(2x)dx = -cos(2x)/2？不对，漏了 dx 中的系数
✅ x = 2x? 不，令 u = 2x, du = 2dx → dx = du/2
   ∫ sin(2x)dx = (1/2)∫ sin u du = -cos u / 2 = -cos(2x)/2 ✓
```

### ❌ 错误 8：原函数存在性判断错误

**【对比示例】**：
```
❌ f(x) = 1/x 在 [-1,1] 上有原函数（它有第二类间断点 !x=0）
✅ f(x) = 1/x 在 [-1,0) ∪ (0,1] 各区间上分别有原函数 ln|x|+C，但在含 0 的区间上不连续，不满足原函数存在定理
```

---

## ⑥ 考研导向复习策略 (Exam Strategy)

### 优先级与建议题量

| 子专题 | 优先级 | 建议刷题量 | 说明 |
|--------|--------|-----------|------|
| 分部积分法 | **高** | 30道 | 必须熟练到本能反应 |
| 第一类换元法（凑微分） | **高** | 30道 | 形式最多变，需要大量积累 |
| 有理函数积分 | **高** | 25道 | 步骤固定但计算量大 |
| 第二类换元法 | **中** | 18道 | 三角代换三种模式练熟 |
| 三角有理式积分 | **中** | 15道 | 特殊代换优先 |
| 无理函数积分 | **低** | 10道 | 理解思路即可 |
| 原函数概念/性质 | **中** | 12道 | 选填重点，易错 |

### 跨章节连接

```
                    ┌──────────────────────────────────────┐
                    │   本章 (Ch04) 不定积分                  │
                    │   · 原函数与不定积分概念                  │
                    │   · 换元积分法（第一类 + 第二类）           │
                    │   · 分部积分法                          │
                    │   · 有理函数积分 / 三角有理式 / 无理式     │
                    └────────────────┬─────────────────────┘
                                     │
     ┌───────────────┬───────────────┼───────────────┬───────────────┐
     ↓               ↓               ↓               ↓               ↓
 Ch02 求导公式     Ch03 中值定理    Ch05 定积分      Ch07 微分方程    Ch09 重积分
 积分是求导的      原函数存在性     牛顿-莱布尼茨     一阶线性方程     累次积分换序
 逆向操作         依赖中值定理     公式直接依赖      的积分因子法     依赖换元
                                   不定积分          需要不定积分
```

#### 🔥 跨章节综合题命题模式

**模式 1：不定积分 + 定积分（Ch04 → Ch05 ⭐⭐⭐）**
> 不定积分是定积分计算的基础。Newton-Leibniz 公式：$\int_a^b f(x)dx = F(b)-F(a)$，$F$ 是 $f$ 的任意一个原函数。不定积分不过关，定积分直接卡死。

**模式 2：不定积分 + 微分方程（Ch04 → Ch07 ⭐⭐⭐）**
> 解一阶线性微分方程 $y' + P(x)y = Q(x)$ 时，积分因子 $\mu = e^{\int P(x)dx}$ 需要做不定积分。换元法和分部法在微分方程中反复用到。

**模式 3：不定积分 + 多元函数（Ch04 → Ch08 ⭐⭐）**
> 求偏导数时，对一个变量求导另一个变量视为常数 → 反过来，对一个变量积分时另一个变量也视为常数。

**模式 4：不定积分 → 定积分应用（Ch04 → Ch06 ⭐⭐）**
> 面积、体积、弧长的定积分表达式建立后，计算定积分时需要不定积分的所有技巧。

### 【终极母题推荐】

> **题目**（综合：换元 + 分部 + 有理函数）：
> $\displaystyle\int \frac{xe^x}{(1+x)^2}\,dx$

**解析**（多方法对比）：

**方法一：分部积分（最巧妙）**

注意到 $\frac{x}{(1+x)^2} = \frac{1}{1+x} - \frac{1}{(1+x)^2}$

$$\begin{aligned}
\int \frac{xe^x}{(1+x)^2}\,dx
&= \int e^x\left(\frac{1}{1+x} - \frac{1}{(1+x)^2}\right)dx \\
&= \int e^x \cdot \frac{1}{1+x}\,dx - \int e^x \cdot \frac{1}{(1+x)^2}\,dx
\end{aligned}$$

对第二项分部积分：$u = e^x, dv = \frac{dx}{(1+x)^2}$ → $du = e^x dx, v = -\frac{1}{1+x}$

第二项 $= -\frac{e^x}{1+x} + \int \frac{e^x}{1+x}\,dx$

第一项 $+$ 第二项 $= \int \frac{e^x}{1+x}\,dx + \frac{e^x}{1+x} - \int \frac{e^x}{1+x}\,dx = \frac{e^x}{1+x} + C$

**方法二：换元（$t = 1+x$）**

令 $t = 1+x$，$x = t-1$，$dx = dt$

$$\int \frac{(t-1)e^{t-1}}{t^2}\,dt = e^{-1}\int e^t\left(\frac{1}{t} - \frac{1}{t^2}\right)dt = e^{-1} \cdot \frac{e^t}{t} + C = \frac{e^x}{1+x} + C$$

**启示**：这道题浓缩了：
1. 部分分式拆项的思维（$\frac{x}{(1+x)^2}$ 的拆分）
2. 分部积分法 $u$ 与 $dv$ 的组合选择
3. 变量代换简化结构的眼光
4. 两种方法殊途同归的验证

**这道题做完且理解透彻 → 本章不定积分核心技巧"通关"。**

---

> **下一步**：完成后可进入 Ch05 定积分。本章的不定积分技巧（换元、分部、有理函数积分）是定积分计算的直接基础——**不定积分算不出来，定积分等于零**。
