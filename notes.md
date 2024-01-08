# 磁流体力学 (Magnetohydrodynamics)

Last edited by Cha0s_MnK on 2024-01-08 (UTC+08:00).

# Chapter 0: 引言 (Introduction)

## 0.1 序 (Preface)

## 0.2 缩写 (Abbreviations)

- HD: Hydrodynamics
- FFF: Force-Free Field
- MHD: Magnetohydrodynamics

## 0.3 数学准备 (Math Preparation)

设$f, g$为**标量**(scalar)；$\bm{A}, \bm{B}, \bm{C}, \bm{D}$为**向量**(vector)，则有如下恒等式：

1. $\bm{A} \cdot (\bm{B} \times \bm{C}) = (\bm{A} \times \bm{B}) \cdot \bm{C} = \bm{B} \cdot (\bm{C} \times \bm{A}) = (\bm{B} \times \bm{C}) \cdot \bm{A} = \bm{C} \cdot (\bm{A} \times \bm{B}) = (\bm{C} \times \bm{A}) \cdot \bm{B}$

2. $\bm{A} \times (\bm{B} \times \bm{C}) = (\bm{C} \times \bm{B}) \times \bm{A} = (\bm{A} \cdot \bm{C})\bm{B} - (\bm{A} \cdot \bm{B})\bm{C}$

3. $\bm{A} \times (\bm{B} \times \bm{C}) + \bm{B} \times (\bm{C} \times \bm{A}) + \bm{C} \times (\bm{A} \times \bm{B}) = 0$

4. $(\bm{A} \times \bm{B}) \cdot (\bm{C} \times \bm{D}) = (\bm{A} \cdot \bm{C})(\bm{B} \cdot \bm{D}) - (\bm{A} \cdot \bm{D})(\bm{B} \cdot \bm{C})$

5. $(\bm{A} \times \bm{B}) \times (\bm{C} \times \bm{D}) = ((\bm{A} \times \bm{B}) \cdot \bm{D})\bm{C} - ((\bm{A} \times \bm{B}) \cdot \bm{C})\bm{D}$

6. $\nabla(fg) = f \nabla g + g \nabla f$

7. $\nabla \cdot (f\bm{A}) = f \nabla \cdot \bm{A} + \bm{A} \cdot \nabla f$

8. $\nabla \times (f\bm{A}) = f \nabla \times \bm{A} + \nabla f \times \bm{A}$

9. $\nabla \cdot (\bm{A} \times \bm{B}) = \bm{B} \cdot (\nabla \times \bm{A}) - \bm{A} \cdot (\nabla \times \bm{B})$

10. $\nabla \times (\bm{A} \times \bm{B}) = (\nabla \cdot \bm{B}) \bm{A} - (\nabla \cdot \bm{A}) \bm{B} + (\bm{B} \cdot \nabla) \bm{A} - (\bm{A} \cdot \nabla) \bm{B}$

11. $\bm{A} \times (\nabla \times \bm{B}) = \nabla(\bm{B} \cdot \bm{A}) - (\bm{A} \cdot \nabla) \bm{B}$

12. $\nabla(\bm{A} \cdot \bm{B}) = \bm{A} \times (\nabla \times \bm{B}) + \bm{B} \times (\nabla \times \bm{A}) + (\bm{A} \cdot \nabla) \bm{B} + (\bm{B} \cdot \nabla) \bm{A}$

13. $\nabla^2 f = \nabla \cdot (\nabla f)$

14. $\nabla^2 \bm{A} = \nabla(\nabla \cdot \bm{A}) - \nabla \times (\nabla \times \bm{A})$

15. $\nabla \times (\nabla f) = 0$

16. $\nabla \cdot (\nabla \times \bm{A}) = 0$

设$\overset{\rightarrow \rightarrow}{T}$为**张量**(tensor)；$\overset{\rightarrow \rightarrow}{I}$为单位张量，则有如下恒等式：

1. $\nabla \cdot (\bm{A} \bm{B}) = (\nabla \cdot \bm{A}) \bm{B} + (\bm{A} \cdot \nabla) \bm{B}$

2. $\nabla \cdot (f \overset{\rightarrow \rightarrow}{T}) = \nabla f \cdot \overset{\rightarrow \rightarrow}{T} + f \nabla \cdot \overset{\rightarrow \rightarrow}{T}$

设$\bm{r} = x\bm{i} + y\bm{j} + z\bm{k}$是直角坐标系中从原点指向$(x, y, z)$处的位置向量，则有如下恒等式：

1. $\nabla \cdot \bm{r} = 3$

2. $\nabla \times \bm{r} = 0$

3. $\displaystyle \nabla r = \frac{\bm{r}}{r}$

4. $\displaystyle \nabla(\frac{1}{r}) = -\frac{\bm{r}}{r^3}$

5. $\displaystyle \nabla \cdot (\frac{\bm{r}}{r^3}) = 4\pi\delta(\bm{r})$

6. $\nabla \bm{r} = \overset{\rightarrow \rightarrow}{I}$

在直角坐标系$(x, y, z)$中，有：

1. $\displaystyle \nabla f = \frac{\partial f}{\partial x} \bm{i} + \frac{\partial f}{\partial y} \bm{j} + \frac{\partial f}{\partial z} \bm{k}$

2. $\displaystyle \nabla \cdot \bm{A} = \frac{\partial A_x}{\partial x} \bm{i} + \frac{\partial A_y}{\partial y} \bm{j} + \frac{\partial A_z}{\partial z} \bm{k}$

3. $\displaystyle \nabla \times \bm{A} = \left( \frac{\partial A_z}{\partial y} - \frac{\partial A_y}{\partial z} \right) \bm{i} + \left( \frac{\partial A_x}{\partial z} - \frac{\partial A_z}{\partial x} \right) \bm{j} + \left( \frac{\partial A_y}{\partial x} - \frac{\partial A_x}{\partial y} \right) \bm{k}$

4. $\displaystyle \nabla^2 f = \frac{\partial^2 f}{\partial x^2} \bm{i} + \frac{\partial^2 f}{\partial y^2} \bm{j} + \frac{\partial^2 f}{\partial z^2} \bm{k}$

在柱坐标系$(\rho, \varphi, z)$中，有：

1. $\displaystyle \nabla f = \frac{\partial f}{\partial \rho} \hat{\rho} + \frac{1}{\rho} \frac{\partial f}{\partial \varphi} \hat{\varphi} + \frac{\partial f}{\partial z} \hat{z}$

2. $\displaystyle \nabla \cdot \bm{A} = \frac{1}{\rho} \frac{\partial}{\partial \rho} (\rho A_\rho) + \frac{1}{\rho} \frac{\partial A_{\varphi}}{\partial \varphi} + \frac{\partial A_z}{\partial z}$

3. $\displaystyle \nabla \times \bm{A} = \left( \frac{1}{\rho} \frac{\partial A_z}{\partial \varphi} - \frac{\partial A_{\varphi}}{\partial z} \right) \hat{\rho} + \left( \frac{\partial A_\rho}{\partial z} - \frac{\partial A_z}{\partial \rho} \right) \hat{\varphi} + \frac{1}{\rho} \left( \frac{\partial}{\partial \rho} (\rho A_\varphi) - \frac{\partial A_\rho}{\partial \varphi} \right) \hat{z}$

4. $\displaystyle \nabla^2 f = \frac{\partial^2 f}{\partial \rho^2} + \frac{1}{\rho} \frac{\partial f}{\partial \rho} + \frac{1}{\rho^2} \frac{\partial^2 f}{\partial \varphi^2} + \frac{\partial^2 f}{\partial z^2}$

在球坐标系$(r, \theta, \varphi)$中，有：

1. $\displaystyle \nabla f = \frac{\partial f}{\partial r} \hat{r} + \frac{1}{r} \frac{\partial f}{\partial \theta} \hat{\theta} + \frac{1}{r \sin \theta} \frac{\partial f}{\partial \varphi} \hat{\varphi}$

2. $\displaystyle \nabla \cdot \bm{A} = \frac{1}{r^2} \frac{\partial}{\partial r} (r^2 A_r) + \frac{1}{r \sin \theta} \frac{\partial}{\partial \theta} (\sin \theta A_\theta) + \frac{1}{r \sin \theta} \frac{\partial A_{\varphi}}{\partial \varphi}$

3. $\displaystyle \nabla \times \bm{A} = \frac{1}{r \sin \theta} \left( \frac{\partial}{\partial \theta} (\sin \theta A_{\varphi}) - \frac{\partial A_\theta}{\partial \varphi} \right) \hat{r} + \frac{1}{r} \left( \frac{1}{\sin \theta} \frac{\partial A_r}{\partial \varphi} - \frac{\partial}{\partial r}(r A_{\varphi}) \right) \hat{\theta} + \frac{1}{r} \left( \frac{\partial}{\partial r} (r A_\theta) - \frac{\partial A_r}{\partial \theta} \right) \hat{\varphi}$

4. $\displaystyle \nabla^2 f = \frac{1}{r^2} \frac{\partial}{\partial r} \left(r^2 \frac{\partial f}{\partial r}\right) + \frac{1}{r^2 \sin \theta} \frac{\partial}{\partial \theta} \left(\sin \theta \frac{\partial f}{\partial \theta}\right) + \frac{1}{r^2 \sin^2 \theta} \frac{\partial^2 f}{\partial \varphi^2}$

## 0.4 Gauss单位制 (Gauss Units)

# Chapter 1: 等离子体 (Plasma)

宇宙中绝大部分的物质处于等离子体状态。等离子体是由处在非束缚态的带电粒子组成的多粒子体系，它和气体、液体、固体一起构成了自然界物质的四大基本形态。当物质达到气态以后，如果继续从外界得到能量，粒子又可以进一步分裂为电子和离子，这就是电离。

实际上，在绝对温度不等于零的任何气体中，总有若干粒子是电离的，但数量太少，不会使气体性质发生质的改变。但由于某种自然(如高温天体)或人为的原因，使带电粒子浓度超过一定数量(通常约需大于千分之一)以后，气体的行为在许多方面虽然仍与寻常流体相似，但这时中性粒子的作用退居次要地位，整个系统将受带电粒子的运动所支配，对外界电磁场敏感，且表现出一系列新的性质。像这样部分或完全电离的气体，它们由带电粒子和中性粒子组成，且表现出集体行为的一种准中性气体叫作等离子体。

所谓“集体行为”所包含的意义如下。考虑作用在一个分子上的力，由于分子是中性的，在分子上不存在净电磁力，而重力是可以忽略的。在这个分子与另一个分子碰撞前，它不受扰动地运动，这时碰撞支配了粒子的运动。在由带电粒子组成的等离子体中，情况就完全不同，当带电粒子运动时，它们能引起正负电荷的局部集中，从而产生电场。而电荷的运动也引起电流，以致产生磁场。这些场影响了远处其他带电粒子的运动，由于库仑力的长程性，带电粒子之间的相互作用力为长程力。例如在某一带电区域中，任意两个距离为r的带电粒子之间的相互作用力随着距离r增加按与距离r的平方成反比的规律减少，而区域内平均粒子数的增长率正比于$r^3$，所以对于区域内任一带电粒子来说，区域内的粒子数的增长率远大于其所受作用力的减少率。因此，任一给定粒子受到大量的、远处的连续相互作用力，这一影响要比受附近粒子较小的相互作用力的影响大得多。所以“集体行为”指的是不仅取决于局部条件而且还取决于远距离区域等离子体状态的运动。它是由库仑长程力所支配的等离子体的基本属性。

等离子体的产生条件：

- 高温；
- 辐射。

宇宙中普遍存在影响空间中带电粒子运动的磁场，通常带电粒子受电磁力的作用远远超过引力的作用。

设在参考系1中电场和磁场是$\bm{E}_1$和$\bm{B}_1$

## 1.1 等离子体参量 (Plasma Parameters)

### 1.2.1 粒子密度 (Particle Density)

在等离子体中，正负粒子所带的电荷在宏观上的分布总是呈现电中性的。所以等离子体满足电中性条件

$$
n_e = \sum_i n_i Z_i \tag{1.2.1}
$$

这里$n_e$是电子(数)密度，$n_i$是离子(数)密度，$Z_i$是离子电荷数。粒子密度$n=2n_e$是等离子体处于平衡态的两个独立参量之一。

### 1.2.2 温度 (Temperature)

等离子体处于平衡态的另一个独立参量是温度$T$。运动粒子每一个自由度的平均能量等于$k_\mathrm{B} T / 2$，所以温度$T$与能量密度相关。在等离子体中，温度可用能量单位表示。用对应于$k_\mathrm{B} T$的能量来表示温度

$$
k_\mathrm{B} T_1 = 1 \mathrm{eV} \\
\Rightarrow T_1 = \frac{1 \mathrm{eV}}{k_\mathrm{B}} \approx \frac{1.602 \times 10^{-19}}{1.381 \times 10^{-23}} \mathrm{K} \approx 11604.5 \mathrm{K} \tag{1.2.2}
$$

### 1.2.3 Debye长度 (Debye Length)

等离子体在宏观上总是呈现出电中性的。但由于带电粒子本身的热运动，在一个适当小的区域里，电子和离子的分布有可能是不均匀的。下面我们来讨论由于带电粒子本身热运动的能量，可能产生局部偏离电中性区域的大小，即德拜长度。

考虑一个带正电荷$q$的离子位于坐标原点，引入Debye长度

$$
\lambda_D = \sqrt{\frac{\epsilon_0 k_\mathrm{B} T}{n e^2}} \tag{1.2.3}
$$

离子周围的电势分布$\varphi(r)$是

$$
\varphi(r) = \frac{q}{4 \pi \epsilon_0 r} e^{-\frac{r}{\lambda_D}} < \frac{q}{4 \pi \epsilon_0 r} \tag{1.2.4}
$$

称为Debye势。它等于Coulomb势乘上衰减因子$e^{-\frac{r}{\lambda_D}}$，因此随距离$r$的增加而下降得比Coulomb势快得多。

这个结果说明，在等离子体中，一个带电粒子的静电作用被其周围过剩的异号电荷所屏蔽，基本上不超过以Debye长度为半径的球的范围。这个“球”内
过剩的异号电荷与中心电荷基本抵消，使中心电荷的作用不能到达球外。所以Debye长度的物理意义有两方面：一方面，它是静电作用的屏蔽半径；另一方面，它又是热运动导致电荷分离的空间尺度。在Debye长度量级的范围内，正负电荷密度可以出现差别。由(1.2.3)式可知，Debye长度反映了热运动(它使气体趋向非电中性)和粒子密度(它借助于静电力使气体趋向电中性)之间的某种协调作用。

由于Debye长度代表了电离气体中维持电中性的最小尺度，因此，我们不难理解“准中性”的意义，即如果我们所研究的电离气体的尺度比Debye长度大得多，则在处理问题时，我们完全可以把电离气体当作电中性来处理。反之，若研究的电离气体的尺度与Debye长度同数量级，则电中性就不存在，问题的处理就复杂得多。所以，等离子体的严格定义应该包含：当电离气体的尺度远大于它的Debye半径时，这种电离气体才能称作等离子体。

### 1.2.4 振荡频率 (Oscillation Frequency)

上面已经指出，等离子体维持宏观电中性的趋势非常强烈，而热运动通常总是存在的，它使等离子体具有偏离电中性的趋势。如果等离子体内部小范围内(在Debye长度内)一旦出现某种电荷过剩，将会发生等离子体振荡。其中电子振荡(角)频率

$$
\omega_\mathrm{e} = \sqrt{\frac{n_\mathrm{e} e^2}{m_\mathrm{e} \epsilon_0}} \approx 56.4 \sqrt{n_\mathrm{e}} \tag{1.2.5}
$$

在导出时，热运动和碰撞可以忽略不计。同理，离子振荡(角)频率为(注意到$m_i \gg m_e$)

$$
\omega_\mathrm{i} = \sqrt{\frac{n_\mathrm{i} e^2}{m_\mathrm{i} \epsilon_0}} \ll \omega_\mathrm{e} \tag{1.2.6}
$$

因此在一般情况下，常将电子振荡(角)频率看作等离子体固有的振荡(角)频率。

$$
\omega_\mathrm{p} = \sqrt{\omega_\mathrm{e}^2 + \omega_\mathrm{i}^2} \approx \omega_\mathrm{e} \tag{1.2.7}
$$

等离子体振荡频率是描述电荷分离的时间尺度。亦即反映了等离子体在电中性破坏后恢复电中性的快慢程度。由于等离子体振荡的存在，使振荡频率小于$\omega_\mathrm{p}$的任何外加场不能透入等离子体中。这是因为更快的等离子体振荡中和了外加场，因而等离子体对频率$\omega < \omega_\mathrm{p}$的电磁辐射是不透明的。所以等离子体振荡频率是电磁波在等离子体中传播的截止频率。

### 1.2.5 电导率 (Conductivity)

电导率是表征物质在外界电磁场存在时所呈现出来的物质导电性能的物理量，这个物理量表征了电磁场和等离子体的耦合。

当在电离气体中加一电场时，所有带电粒子都被加速，正负带电粒子反向运动。带电粒子和中性粒子间，以及正、负带电粒子间发生碰撞，将使平均速度很快达到定值。假设除了中性质点外，只考虑电子和一次电离原子，且假定电场不太强(宇宙中大多数情况如此)。如果在一秒钟内电子与离子或中性粒子的碰撞次数等于l，此处t。为自由运动时间。$\sigma$称为电导率。

以上结果均在无磁场时成立，当等离子体中存在磁场时，情况将复杂得多，此时电导率$\sigma$不再是各项同性，而是以张量形式出现

$$
\bm{j} = \overset{\rightarrow \rightarrow}{\sigma} \bm{E} \tag{1.2.8}
$$

## 1.3 单粒子模型 (Single Particle Model)

等离子体的基本行不仅取决于等离子体与外场的相互作用，也与等离子体质点之间的相互作用有关，本质上是一种集体效应，必须用统计物理学方法来处理。由于数学上的困难，通常在条件许可情况下，往往用近似理论来讨论等离子体问题。本节简述用等离子体单粒子模型所给出的结果。

用等离子体的单粒子模型处理问题时，实际上作了四个假定：

1. 忽略了粒子间的相互作用；
2. 不计带电粒子运动所产生的电磁场，且假定$\bm{E}$、$\bm{B}$为已知外场；
3. 仅考虑非相对论情形；
4. 忽略带电粒子由于辐射而产生的辐射阻尼。

单粒子模型适用于描述稀薄等离子体(对于稀薄等离子体可近似忽略粒子间的相互作用)，同时单粒子模型给予我们一种直观的概念，它是我们研究和了解等离子体集体效应的基础。在满足以上四个假定的前提下，复杂的运动方程组简化为一个方程

$$
m \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = q \bm{E} (\bm{r}, t) + q \bm{v} \times \bm{B} (\bm{r}, t) + \bm{F} (\bm{r}, t)
$$

其中$\bm{F}$为除电磁场力以外的外力。下面将对$\bm{E}$、$\bm{B}$和$\bm{F}$的各种可能情况，分别讨论单个带电粒子的运动规律。