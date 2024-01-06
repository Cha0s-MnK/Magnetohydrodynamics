# 磁流体力学 (Magnetohydrodynamics)

Last edited by Cha0s_MnK on 2024-01-06 (UTC+08:00).

# Chapter 0: 引言 (Introduction)

## 0.1 序 (Preface)

## 0.1 缩写 (Abbreviations)

- HD: Hydrodynamics
- MHD: Magnetohydrodynamics
- FFF: Force-Free Field

## 0.2 数学准备 (Math Preparation)

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

# Chapter 1: 等离子体 (Plasma)

## 1.1 等离子体参量(Plasma Parameters)

宇宙中绝大部分的物质处于等离子体状态，等离子体是由处在非束缚态的带电粒子组成的多粒子体系，它和气体、液体、固体一起构成了自然界物质的四大基本形态。当物质达到气态以后，如果继续从外界得到能量，粒子又可以进一步分裂为电子和离子，这就是电离。

实际上，在绝对温度不等于零的任何气体中，总有若干粒子是电离的，但数量太少，不会使气体性质发生质的改变。但由于某种自然(如高温天体)或人为的原因，使带电粒子浓度超过一定数量(通常约需大于千分之一)以后，气体的行为在许多方面虽然仍与寻常流体相似，但这时中性粒子的作用退居次要地位，整个系统将受带电粒子的运动所支配，对外界电磁场敏感，且表现出一系列新的性质。像这样部分或完全电离的气体，它们由带电粒子和中性粒子组成，且表现出集体行为的一种准中性气体叫作等离子体。

所谓“集体行为”所包含的意义如下。考虑作用在一个分子上的力，由于分子是中性的，在分子上不存在净电磁力，而重力是可以忽略的。在这个分子与另一个分子碰撞前，它不受扰动地运动，这时碰撞支配了粒子的运动。在由带电粒子组成的等离子体中，情况就完全不同，当带电粒子运动时，它们能引起正负电荷的局部集中，从而产生电场。而电荷的运动也引起电流，以致产生磁场。这些场影响了远处其他带电粒子的运动，由于库仑力的长程性，带电粒子之间的相互作用力为长程力。例如在某一带电区域中，任意两个距离为r的带电粒子之间的相互作用力随着距离r增加按与距离r的平方成反比的规律减少，而区域内平均粒子数的增长率正比于$r^3$，所以对于区域内任一带电粒子来说，区域内的粒子数的增长率远大于其所受作用力的减少率。因此，任一给定粒子受到大量的、远处的连续相互作用力，这一影响要比受附近粒子较小的相互作用力的影响大得多。所以“集体行为”指的是不仅取决于局部条件而且还取决于远距离区域等离子体状态的运动。它是由库仑长程力所支配的等离子体的基本属性。

同时，宇宙中普遍存在影响空间中带电粒子运动的磁场。通常带电粒子受电磁力的作用远远超过引力的作用。

### 1.2.1 粒子密度(Particle Density)

在等离子体中，正负粒子所带的电荷在宏观上的分布总是呈现电中性的。所以等离子体满足电中性条件

$$
n_e = \sum_i n_i Z_i \tag{1.2.1}
$$

这里$n_e$是电子(数)密度，$n_i$是离子(数)密度，$Z_i$是离子电荷数。粒子密度$n=2n_e$是等离子体处于平衡态的两个独立参量之一。

### 1.2.2 温度(Temperature)

等离子体处于平衡态的另一个独立参量是等离子体温度$T$。运动粒子每一个自由度的平均能量等于$k_\mathrm{B} T / 2$，所以温度$T$与能量密度相关。在等离子体中，温度可用能量单位表示。用对应于$k_\mathrm{B} T$的能量来表示温度

$$
k_\mathrm{B} T_1 = 1 \mathrm{eV} \\
\Rightarrow T_1 = \frac{1 \mathrm{eV}}{k_\mathrm{B}} \approx \frac{1.602 \times 10^{-19}}{1.381 \times 10^{-23}} \mathrm{K} \approx 11604.5 \mathrm{K} \tag{1.2.2}
$$

### 1.2.3 Debye长度(Debye Length)

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

### 1.2.4 振荡频率(Oscillation Frequency)

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

### 1.2.5 电导率(Conductivity)

电导率是表征物质在外界电磁场存在时所呈现出来的物质导电性能的物理量，这个物理量表征了电磁场和等离子体的耦合。

当在电离气体中加一电场时，所有带电粒子都被加速，正负带电粒子反向运动。带电粒子和中性粒子间，以及正、负带电粒子间发生碰撞，将使平均速度很快达到定值。假设除了中性质点外，只考虑电子和一次电离原子，且假定电场不太强(宇宙中大多数情况如此)。如果在一秒钟内电子与离子或中性粒子的碰撞次数等于l，此处t。为自由运动时间。$\sigma$称为电导率。

以上结果均在无磁场时成立，当等离子体中存在磁场时，情况将复杂得多，此时电导率$\sigma$不再是各项同性，而是以张量形式出现

$$
\bm{j} = \overset{\rightarrow \rightarrow}{\sigma} \bm{E} \tag{1.2.}
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

# Chapter2: 磁流体力学方程 (MHD Equations)

## 2.1 磁流体力学 (MHD)

对于大部分宇宙等离子体，必须考虑带电粒子间的相互作用，严格地讲应该用动理论来处理。但是由于动理论的复杂性和数学上的困难性，如果我们所考虑的等离子体的特征尺度$l$远大于等离子体的平均自由程$\bar{l}$，等离子体参量变化的特征时间$\tau$远大于等离子体内带电粒子的平均碰撞时间$\bar{\tau}$，则此时可以把等离子体看作由无数流体“质点”或“流体元”连续组成，流体质点的尺度$\mathrm{d} l$必须满足

$$
l \gg \mathrm{d} l \gg \bar{l} \tag{2.1.1}
$$

上式表明流体质点尺度$\mathrm{d} l$是一个宏观上小而微观上大的尺度。此条件相当于要求等离子体中“碰撞占优势”。显然，另一个条件是

$$
\tau \gg \bar{\tau} \tag{2.1.2}
$$

事实上，由带电粒子组成的流体元更有利于成团条件，这是由于带电粒子间的作用力是长程库仑力，故带电粒子间的相互作用要比中性粒子间强得多，所以带电粒子间的碰撞频率远大于中性粒子之间的碰撞频率，从而有更短的平均自由程。此外，对于处于强磁场中的等离子体，即使其中粒子间的碰撞很小，甚至可认为是“无碰撞等离子体”的情况，也可以应用导电流体描述。因为在强磁场中，带电粒子被束缚在磁力线上，其横越磁力线的运动受到限制，即磁场此时起着碰撞所起的作用。这时要求磁化流体元的特征尺度远大于带电粒子的回旋半径，于是就可用流体描述了。因此等离子体，尤其是磁化等离子体，往往可以比中性粒子系在更低的密度和更高的温度下仍能用流体方法描述。把等离子体当作**导电流体**来研究，是一种相当有效且应用范围广泛的方法，这种理论称作**电磁流体力学**。

电磁流体力学是由流体力学和电动力学交叉形成的一门学科，流体力学方程和Maxwell方程组组成了它的基本方程组。电磁流体力学的特殊性和复杂性来源于流场和电磁场的耦合。导电流体在磁场中的运动将引起感应电场，从而产生电流。这个电流一方面与磁场相互作用，产生附加的电磁力，导致流体运动的改变；另一方面，它又将激发新的磁场，叠加在原来磁场上，改变原来磁场的位形。考虑到在大部分问题中，导电流体的速度是非相对论性的，这时在流场和电磁场耦合显著的情况下，磁场的作用将远大于电场，因此可以忽略电场的作用，所以通常也把电磁流体力学称为**磁流体力学**。

## 2.2 流体力学方程 (HD Equations)

对于大多数宏观呈电中性的等离子体来说，其热力学性质与中性气体相似，因此在热力学层面上的描述，可直接借鉴中性气体的热力学结果。

### 2.2.1 连续性方程 / 质量守恒方程 (Continuity Equation / Mass Conservation Equation)

$$
\frac{\mathrm{d} \rho}{\mathrm{d} t} + \rho \nabla \cdot \bm{v} = 0 \tag{2.2.1}
$$

或

$$
\frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \tag{2.2.2}
$$

其中

$$
\frac{\mathrm{d}}{\mathrm{d} t} = \frac{\partial}{\partial t} + \bm{v} \cdot \nabla \tag{2.2.3}
$$

$\displaystyle \frac{\mathrm{d}}{\mathrm{d} t}$为随体导数，$\displaystyle \frac{\partial}{\partial t}$为局部导数/就地导数，$\bm{v} \cdot \nabla$为位变导数或对流导数。

### 2.2.2 运动方程 / 动量守恒方程 (Motion Equation / Momentum Conservation Equation)

$$
\rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = \nabla \cdot \overset{\rightarrow \rightarrow}{p} + \rho_\mathrm{f} \bm{E} + \bm{j} \times \bm{B} + \rho \bm{f} \tag{2.2.4}
$$

其中$\overset{\rightarrow \rightarrow}{p}$为压强张量，由本构方程决定；$\bm{f}$为单位体积的外力。若不考虑黏性，则$(2.2.4)$式化为

$$
\rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = - \nabla p + \rho_\mathrm{f} \bm{E} + \bm{j} \times \bm{B} + \rho \bm{f}
$$

若流体不可压，且具有黏性$\eta$($\eta$为常数)，则$(2.2.4)$式化为

$$
\rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = - \nabla p + 2 \eta \nabla^2 \bm{v} + \rho_\mathrm{f} \bm{E} + \bm{j} \times \bm{B} + \rho \bm{f}
$$

### 2.2.3 能量方程 (Energy Equation)

$$
\rho \frac{\mathrm{d}}{\mathrm{d} t} (\varepsilon + \frac{1}{2} v^2) = - \nabla \cdot (\overset{\rightarrow \rightarrow}{P} \cdot \bm{v}) + \bm{E} \cdot \bm{j} + \rho \bm{f} \cdot \bm{v} - \nabla \cdot \bm{q} + H
$$

## 2.3 电动力学方程 (Electrodynamics Equations)

### 2.3.1 Maxwell方程组 (Maxwell Equation Set)

在宇宙等离子体物理中，一般使用真空中的Maxwell方程组。在国际单位制下，并忽略位移电流时

$$
\begin{cases}
\displaystyle \nabla \times \bm{E} = -\frac{\partial \bm{B}}{\partial t} \\
\nabla \times \bm{B} = \mu_0 \bm{j}_\mathrm{f} \\
\displaystyle \nabla \cdot \bm{E} = \frac{\rho_\mathrm{f}}{\varepsilon_0} \\
\nabla \cdot \bm{B} = 0 \tag{2.3.1}
\end{cases}
$$

其中$\rho_\mathrm{f}$表示自由电荷密度，$\bm{j}_\mathrm{f}$表示自由电流密度。

### 2.3.2 广义欧姆定律 (General Ohm Law)

要由Maxwell方程组单值地确定电磁场，必须给定电流密度$\bm{j} (\bm{r}, t)$，或者把电流密度与方程组里所包含的其他量联系起来，将电流密度$\bm{j}$、电磁场强度及确定导电介质性质与运动的参数联系起来的关系通常称为广义Ohm定律。大多数情况下，可将等离子体当作单一的导电流体来考虑，此时欧姆定律为

$$
\bm{j} = \sigma \bm{E}^* = \sigma (\bm{E} + \bm{v} \times \bm{B})
$$

式中。电导率， *为等效电场。然而，对于那些远未达到热力学平衡的完全电离等离子体，必须分别考虑各种成分气体的运动及它们之间的耦合。下面讨论完全电离等离子体情况下，即它由电子气和离子气两种成分组成，由二流体模型来导出完全电离等离子体中联系电流密度和其他量之间关系的表达式。

等离子体二流体描述的方程组的严格推导必须借助于动理论。但也可以从流体力学
和电动力学的考虑直接写出。以下考虑最简单的模型，即认为电子气体和离子气体各自
独立地运动着，因而对每种成分可分别写出它们的流体运动方程，不同成分之间由于碰撞
而产生的相互作用，则可以归结为某个平均的体积力，它的大小等于电子和离子在碰撞时
动量变化率的平均值。此外，认为电子气体和离子气体都是理想气体，因而它们的内部应
力只有压力。这时，可直接写出电子气和离子气的运动方程：

## 2.4

### 2.4.1 磁感应方程 (Magnetic Induction Equation)

导电流体中磁场变化所遵循的方程称为磁感应方程：

$$
\frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) - \nabla \times [\eta_\mathrm{m}(\nabla \times \bm{B})] \tag{2.4.1}
$$

其中$\displaystyle \eta_\mathrm{m}=\frac{1}{\sigma \mu_0}$是**磁扩散系数**(magnetic diffusion coefficient)。当电导率$\sigma$在空间上为均匀的常量时，上式可化为：

$$
\frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) + \eta_\mathrm{m} \nabla^2 \bm{B} \tag{2.4.2}
$$

### 2.4.2 磁雷诺数 (Magnetic Reynolds Number)

求解磁感应方程是十分困难的，通常采用所谓量级分析法来处理微分方程式。应用量级分析法时，用有关物理量的特征数值代替微分方程式中相应的各项。例如用量级分析法来估算(2.4.2)式中右端两项的大小时，可用所研究问题的特征长度$l$的倒数$\displaystyle \frac{1}{l}$代替对空间的一阶导数，用$\displaystyle \frac{1}{l^2}$代替对空间的二阶导数，于是有

$$
\begin{align}
    \nabla \times (\bm{v} \times \bm{B}) &\approx \frac{vB}{l} \tag{2.4.3} \\
    \nabla^2 \bm{B} &\approx \frac{B}{l^2} \tag{2.4.4}
\end{align}
$$

其中$v, B$分别为导电流体的运动速度和磁感应强度的特征值，而如下定义磁雷诺数$R_\mathrm{m}$：

$$
\frac{\nabla \times (\bm{v} \times \bm{B})}{\eta_\mathrm{m} \nabla^2 \bm{B}} \approx \frac{vl}{\eta_\mathrm{m}} = R_\mathrm{m} \tag{2.4.5}
$$

显然，磁雷诺数$R_\mathrm{m}$的大小直接表征了导电流体中磁场变化的主要决定因素。当$R_\mathrm{m} \gg 1$时，磁感应方程式中右端第一项流动项起重要作用，磁场的变化主要由导电流体运动所决定；而当$R_\mathrm{m} \ll 1$时，磁感应方程式中右端第二项即扩散项起主要作用，磁场的变化主要通过扩散而衰减和趋于均匀化。

通常宇宙等离子体都具有大的特征尺度，因此大磁雷诺数是磁流体力学问题的基本特征之一，宇宙等离子体的运动常常是天体磁场变化的主要原因。

### 2.4.3 磁扩散效应 (Magnetic Diffusion Effect)

当流体静止($\bm{v} = 0$)时，磁感应方程$(2.4.2)$式变为

$$
\frac{\partial \bm{B}}{\partial t} = \eta_\mathrm{m} \nabla^2 \bm{B} \tag{2.4.6}
$$
上式是一个扩散方程，它表示在不运动的导电流体中，磁场随时间的变化是由磁场分布的不均匀所引起的。磁场将从强的区域向弱的区域扩散，扩散的结果使导电流体中的磁场分布趋向于均匀化，而总的磁场能量趋向于减小。由$(2.4.6)$式可知，磁场扩散的速率不但与磁场的不均匀性$\nabla^2 \bm{B}$有关，还取决于导电流体本身的性质。磁扩散系数$\eta_\mathrm{m}$越大，磁场的扩散就越快。

利用量级分析法可估算导电流体中磁场扩散的特征时间$\tau_\mathrm{d}$，对扩散方程$(2.4.6)$式应用量级分析法可得

$$
\begin{align}
    \frac{B}{\tau_\mathrm{d}} &\approx \eta_\mathrm{m} \frac{B}{l^2} \tag{2.4.7} \\
    \Rightarrow \tau_\mathrm{d} &\approx \frac{l^2}{\eta_\mathrm{m}} = \mu_0 \sigma l^2 \tag{2.4.8}
\end{align}
$$

$(2.4.8)$式表明，导电流体的电导率越大，磁场衰减越慢。当$\sigma \rightarrow + \infty$时，$\tau_\mathrm{d} \rightarrow + \infty$，磁场将不扩散，显然此时即为磁场冻结的情况。$(2.4.8)$式还表明，对于有限电导率的导电流体，其特征尺度越大，磁场的扩散速率便越小。所以，宇宙等离子体的巨大尺度使它们内部磁场的衰减具有很大的时标。

磁力线与其说是扩散出去了还不如说是被湮灭了，湮灭的本质是磁能通过欧姆耗散变为热能了。磁扩散近似时导电流体中的总磁能为

$$
W_\mathrm{B} = \frac{1}{2 \mu_0} \int B^2 \mathrm{d} V \tag{2.4.9}
$$

磁能的变化率为

$$
\frac{\partial W_\mathrm{B}}{\partial t} = - \int \frac{j^2}{\sigma} \mathrm{d} V \tag{2.4.10}
$$

$(2.4.10)$式表明，静止导电流体中磁场的扩散效应使总磁能减少，其本质是由电阻引起的焦耳耗散使磁能转变为导电流体的热能。因此可以认为导电流体中磁场的扩散与电磁能量的焦耳耗散是同一个物理过程，只是从不同的角度去描述它而已。由于在这个过程中，有序的磁能被转化为导电流体的无序热能，所以过程是不可逆的。

### 2.4.4 磁冻结效应 (Magnetic Freezing Effect)

当$\displaystyle R_\mathrm{m} = \frac{vl}{\eta_\mathrm{m}} = \mu_0 \sigma v l \gg 1$时，导电流体成为完全导电的理想流体，$(2.4.2)$式将近似为

$$
\frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) \tag{2.4.11}
$$

上式表明，这时磁场的变化将完全由流体的运动所决定。上式也意味着在完全导电的理想流体中，磁场的变化就如同磁力线黏附于导电流体质点上，随它一起运动。因此可形象地用磁力线“冻结”在流体上这样的概念来描述流体运动对磁场的影响，这就是所谓的磁冻结效应，而上式也被称为磁冻结方程。

利用磁冻结方程$(2.4.11)$式可以证明如下三个定理。

1. **磁通量守恒定理 / 柯林定理** (magnetic flux conservation law / Cowling theorem)：在完全导电的理想流体中，通过和流体一起运动的任意曲面的磁通量守恒。
2. **瓦伦定理** (Walen theorem)：在完全导电的理想流体中，起初位于某根磁力线上的流体质点，以后将一直位于这根磁力线上；在运动过程中流体元伸长或缩短式，磁场强度$\bm{B}$也随之成比例地增大或减小(当然前提是流体是不可压的)。
3. 在理想磁流体力学条件下，对有限维的磁场结构，当且仅当在封闭曲面上，磁场和流场满足$\bm{B} \cdot \bm{n} = \bm{v} \cdot \bm{n} = 0$，则磁螺度是一个守恒量。

## 2.5 磁应力 (Magnetic Stress)

本节将研究磁场对导电流体的作用，这是流场和磁场耦合的另一方面。磁场对导电流体的作用力又被称为**安培力**(Ampere force)或**洛伦兹力**(Lorentz force)。在不考虑位移电流情况下，单位体积导电流体所受到的磁场力$\bm{f}$为

$$
\bm{f} = \bm{j} \times \bm{B} = \frac{1}{\mu_0} (\nabla \times \bm{B}) \times \bm{B} \tag{2.5.1}
$$

上式可由向量公式化为

$$
\bm{f} = \nabla \cdot \frac{\bm{B} \bm{B}}{\mu_0} - \nabla \left( \frac{B^2}{2 \mu_0} \right) = \nabla \cdot (\frac{\bm{B} \bm{B}}{\mu_0} - \frac{B^2}{2 \mu_0} \overset{\rightarrow \rightarrow}{I})
$$

其中

$$
\overset{\rightarrow \rightarrow}{P_\mathrm{B}} = \frac{1}{\mu_0} (\bm{B} \bm{B} - \frac{B^2}{2} \overset{\rightarrow \rightarrow}{I})
$$

为磁应力张量。于是作用在外法向为$\bm{n}$的单位面积上的磁场应力为

$$
\bm{p}_\mathrm{B} (\bm{n}) = \overset{\rightarrow \rightarrow}{P_\mathrm{B}} \bm{n} = \frac{1}{\mu_0} \left[ (\bm{B} \cdot \bm{n}) \bm{B} - \frac{B^2}{2} \bm{n} \right]
$$

可推得

$$
\int_V \bm{f} \mathrm{d} V = \int_S \bm{p}_\mathrm{B} (\bm{n}) \mathrm{d} S
$$

其中$S$为包围体积$V$的封闭曲面。上式表明，作用在体积$V$的导电流体上的磁场力，在作用效果上可被看作作用在包围体积$V$的封闭曲面$S$上的压力，由$()$式给出。

## 2.6 磁流体力学基本方程组 (MHD Basic Equation Set)

磁流体力学方程组必须同时满足流体力学方程组和电磁场方程及考虑流场与磁场的耦合。但不难看出该联立方程组还是不封闭的。为了使磁流体力学方程组完备，还必须联立描述热力学状态参数之间关系的状态方程。如前所说，通常我们把宇宙等离子体当作理想气体，这时有如下关系式

$$
\begin{align}
p = \frac{\rho R T}{\mu} = n k_\mathrm{B} T \\
\varepsilon = \frac{p}{(\gamma - 1) \rho}
\end{align}
$$

### 2.6.1 理想磁流体力学方程组

通常在大部分情况下可将宇宙等离子体当作无黏性导电流体，此时可得到仅考虑电阻的磁流体力学方程组

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \\ \\
\displaystyle \rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = -\nabla p + \bm{j} \times \bm{B} + \rho \bm{f} \\ \\
\displaystyle \frac{\rho^\gamma}{\gamma - 1} \frac{\mathrm{d}}{\mathrm{d} t} \left( \frac{p}{\rho^\gamma} \right) = -\nabla \cdot \bm{q} - L_\mathrm{r} + \frac{j^2}{\sigma} \\ \\
\displaystyle \frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) - \nabla \times \left[ \eta_\mathrm{m} (\nabla \times \bm{B}) \right] \\ \\
\nabla \times \bm{B} = \mu_0 \bm{j} \\ \\
\bm{j} = \sigma (\bm{E} + \bm{v} \times \bm{B}) \\ \\
\displaystyle p = \frac{\rho R T}{\mu} \\ \\
\nabla \cdot \bm{B} = 0
\end{cases}
$$

### 2.6.2 完全导电理想磁流体力学方程组

对于完全导电的理想流体$\sigma \rightarrow + \infty$，$\eta_\mathrm{m} \rightarrow 0$，方程组$(2.6.3)$化为

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \\ \\
\displaystyle \rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = -\nabla p + \bm{j} \times \bm{B} + \rho \bm{f} \\ \\
\displaystyle \frac{\rho^\gamma}{\gamma - 1} \frac{\mathrm{d}}{\mathrm{d} t} \left( \frac{p}{\rho^\gamma} \right) = -\nabla \cdot \bm{q} - L_\mathrm{r} \\ \\
\displaystyle \frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) \\ \\
\nabla \times \bm{B} = \mu_0 \bm{j} \\ \\
\displaystyle p = \frac{\rho R T}{\mu} \\ \\
\nabla \cdot \bm{B} = 0
\end{cases}
$$

若又不考虑辐射损失和其他加热的绝热情况下，上述方程组可化为

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \\ \\
\displaystyle \rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = -\nabla p + \bm{j} \times \bm{B} \\ \\
\displaystyle \frac{\mathrm{d}}{\mathrm{d} t} \left( \frac{p}{\rho^\gamma} \right) = 0 \\ \\
\displaystyle \frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) \\ \\
\nabla \times \bm{B} = \mu_0 \bm{j} \\ \\
\nabla \cdot \bm{B} = 0
\end{cases}
$$

### 2.6.3 磁流体力学的特征参数

Alfvén速度

$$
v_\mathrm{A} = \frac{B_0}{\sqrt{\mu_0 \rho_0}}
$$

磁Mach数/Alfvén Mach数

$$
M \! a_\mathrm{A} = \frac{v_0}{v_\mathrm{A}} = \frac{v_0 \sqrt{\mu_0 \rho_0}}{B_0}
$$

其中$v_0$为等离子体速度的特征值。Mach数

$$
M \! a = \frac{v_0}{c_\mathrm{s}} = v_0 \sqrt{\frac{\rho_0}{\gamma p_0}}
$$

其中$\rho_0$为等离子体密度的特征值，$p_0$为等离子体压强的特征值。等离子体$\beta$值

$$
\beta = \frac{2 \mu_0 p_0}{B_0^2}
$$

其中$B_0$为等离子体磁场的特征值。

# Chapter 3: 磁流体静力学 (Magnetohydrostatistics)

## 3.1 磁流体平衡时的性质

考虑只有电磁力和压力之间的平衡，此时磁流体静平衡应满足的方程组为

$$
\begin{align}
    & \nabla p = \bm{j} \times \bm{B} \tag{3.1.1} \\
    & \bm{j} = \frac{1}{\mu_0} \nabla \times \bm{B} \tag{3.1.2} \\
    & \nabla \cdot \bm{B} = 0 \tag{3.1.3}
\end{align}
$$

根据向量公式可得：

$$
\begin{align}
    \nabla p & = \frac{1}{\mu_0} (\bm{B} \cdot \nabla) \bm{B} - \nabla (\frac{B^2}{2 \mu_0}) \nonumber \\
    & = \frac{1}{\mu_0} [(\bm{B} \cdot \nabla) \bm{B} - B \nabla B] \tag{3.1.4} \\
    \nabla & \times (\bm{B} \cdot \nabla) \bm{B} = 0 \tag{3.1.5}
\end{align}
$$

因此可由$(3.1.3)$和$(3.1.5)$式解得磁场的静平衡位形。然后再将它代入$(3.1.2)$和$(3.1.4)$式中，分别得到导电流体平衡态下的电流分布和压强分布。注意，满足$(3.1.3)$和$(3.1.5)$式的解不是唯一的，它们给出了导电流体静平衡时磁场的各种可能位形。

由$(3.1.1)$式可得：

$$
\begin{align}
    \bm{B} \cdot \nabla p = 0 \tag{3.1.6} \\
    \bm{j} \cdot \nabla p = 0 \tag{3.1.7}
\end{align}
$$

上式表明$\bm{B}, \bm{j}$均位于等离子体的等压面上。如果等压面是封闭的，则磁力线及电流线缠绕在该曲面上，绝不可能由磁力线和电流线穿越等压面的情况发生。通常电流线可以以任意角度与磁力线相交。

在等压面上，除了$p$为常数，磁通量$\Phi$和电流$\bm{j}$也是常数。

## 3.2 无作用力场 (Force-Free Field, FFF)

当等离子体$\beta$很小时，磁力处于主导地位，没有其它力可以与之平衡。为使系统平衡，必须要求磁力为0。这种磁场被称作无作用力场。

### 3.3.1 无作用力场基本方程

$$
\begin{align}
    & \nabla \times \bm{B} = \alpha \bm{B} \tag{3.3.1} \\
    & \nabla \cdot \bm{B} = 0 \tag{3.3.2} \\
    & \bm{j} = \frac{1}{\mu_0} \nabla \times \bm{B} = \frac{\alpha}{\mu_0} \bm{B} \tag{3.3.3}
\end{align}
$$

其中标量函数$\alpha = \alpha (\bm{r}, t)$被称为**无力因子**(force-free factor)。可推得：

$$
\bm{B} \cdot \nabla \alpha = 0 \tag{3.3.4}
$$

上式表明$\alpha$在磁场方向(同时也是电流方向)梯度为0，或者说沿磁力线(同时也是电流线)$\alpha$为常数。

### 3.3.2 无电流场 / 势场 (Current-Free Field / Potential Field)

无电流场中电流处处为零，即

$$
\nabla \times \bm{B} = 0 \tag{3.3.5}
$$

且

$$
\alpha = 0 \tag{3.3.6}
$$

$(3.3.5)$式表明无电流场可以表示为一标量函数的梯度，即

$$
\bm{B} = \nabla \Psi \tag{3.3.7}
$$

这里的标量函数$\Psi$称为磁势。因此，无电流场也被称为势场。可推得磁势应满足Laplace方程

$$
\nabla^2 \Psi = 0 \tag{3.3.8}
$$

求解方程$(3.3.8)$，由给定边界条件，可得$\Psi$的空间分布。再由$(3.3.7)$式我们就可以得到具体的势场位形。

通常采用分离变量方法求解拉普拉斯方程(3.3-9)。在直角坐标系(x，y，z)下，x-y平面上方空间中随、增加而衰减的势场周期解具有
平=aexp(ik,x+iky-kz) (3.3-10)
的形式。其中k、k，、k为正实数且满足k+k=k。如果在四个侧面上(x=0，y=0，x=a，y=b)磁场法向分量为零，则上述通解的具体形式为
=Zam sin
n=0 m0 co 2nt.x
a sin2m元y
b enmz (3.3-11)
其中ki=(2nn/a)2+(2mx/b)。
在柱坐标系(r，0，z)下，方程(3.3-9)的通解可以写成
平=[caJa(kr)+d,Y.(kr)]enBke (3.3-12)
其中J，和Y。分别为第一类和第二类贝塞尔函数。或者当问题与x无关时，

对于一封闭区域，给定边界面上法向磁场，由此唯一确定的势场所具有的磁能对应该区域中最低磁能状态，这就是**势场能量最低原理**。

### 3.3.3 线性无作用力场 (Linear Force-Free Field)

对于线性无作用力场，$\alpha$为常数。可推得其方程：

$$
\nabla^2 \bm{B} + \alpha^2 \bm{B} = 0
$$

我们先求解下列标量Helmholtz方程

$$
\nabla^2 \psi + \alpha^2 \psi = 0
$$

取$\bm{n}$为一确定的单位向量，则满足$(3.3.10)$式的解为

$$
\bm{B} = \nabla \times (\psi \bm{n}) + \frac{1}{\alpha} \nabla \times \nabla \times (\psi \bm{n})
$$

再给定适当的边界条件，就可以求解线性无作用力场的具体位形。

在一个封闭的冻结型磁场系统中，磁螺度

$$
H = \int_V \bm{A} \cdot \bm{B} \mathrm{d} V
$$

不随时间改变。对于给定的磁螺度，该系统极小磁能状态对应一个线性无力场。

在有限电导率情况下，扩散型线性无作用力场衰变后仍为无作用力场。

### 3.4 箍缩效应 (Pinch Effect)

### 3.5