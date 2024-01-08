# Chapter2: 磁流体力学方程 (MHD Equations)

对于大部分宇宙等离子体，必须考虑带电粒子间的相互作用，严格地讲应该用动理论来处理。但是由于动理论的复杂性和数学上的困难性，如果我们所考虑的等离子体的特征尺度$l$远大于等离子体的平均自由程$\bar{l}$，等离子体参量变化的特征时间$\tau$远大于等离子体内带电粒子的平均碰撞时间$\bar{\tau}$，则此时可以把等离子体看作由无数流体“质点”或“流体元”连续组成，流体质点的尺度$\mathrm{d} l$必须满足

$$
l \gg \mathrm{d} l \gg \bar{l}
$$

上式表明流体质点尺度$\mathrm{d} l$是一个宏观上小而微观上大的尺度。此条件相当于要求等离子体中“碰撞占优势”。显然，另一个条件是

$$
\tau \gg \bar{\tau}
$$

事实上，由带电粒子组成的流体元更有利于成团条件，这是由于带电粒子间的作用力是长程库仑力，故带电粒子间的相互作用要比中性粒子间强得多，所以带电粒子间的碰撞频率远大于中性粒子之间的碰撞频率，从而有更短的平均自由程。此外，对于处于强磁场中的等离子体，即使其中粒子间的碰撞很小，甚至可认为是“无碰撞等离子体”的情况，也可以应用导电流体描述。因为在强磁场中，带电粒子被束缚在磁力线上，其横越磁力线的运动受到限制，即磁场此时起着碰撞所起的作用。这时要求磁化流体元的特征尺度远大于带电粒子的回旋半径，于是就可用流体描述了。因此等离子体，尤其是磁化等离子体，往往可以比中性粒子系在更低的密度和更高的温度下仍能用流体方法描述。把等离子体当作**导电流体**来研究，是一种相当有效且应用范围广泛的方法，这种理论称作**电磁流体力学**。

电磁流体力学是由流体力学和电动力学交叉形成的一门学科，流体力学方程和Maxwell方程组组成了它的基本方程组。电磁流体力学的特殊性和复杂性来源于流场和电磁场的耦合。导电流体在磁场中的运动将引起感应电场，从而产生电流。这个电流一方面与磁场相互作用，产生附加的电磁力，导致流体运动的改变；另一方面，它又将激发新的磁场，叠加在原来磁场上，改变原来磁场的位形。考虑到在大部分问题中，导电流体的速度是非相对论性的，这时在流场和电磁场耦合显著的情况下，磁场的作用将远大于电场，因此可以忽略电场的作用，所以通常也把电磁流体力学称为**磁流体力学**。

## 2.1 流体力学方程 (HD Equations)

对于大多数宏观呈电中性的等离子体来说，其热力学性质与中性气体相似，因此在热力学层面上的描述，可直接借鉴中性气体的热力学结果。

### 2.1.1 连续性方程 / 质量守恒方程 (Continuity Equation / Mass Conservation Equation)

$$
\frac{\mathrm{d} \rho}{\mathrm{d} t} + \rho \nabla \cdot \bm{v} = 0 \tag{2.2.1}
$$

或

$$
\frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \tag{2.2.2}
$$

其中

$$
\frac{\mathrm{d}}{\mathrm{d} t} = \frac{\partial}{\partial t} + \bm{v} \cdot \nabla
$$

$\displaystyle \frac{\mathrm{d}}{\mathrm{d} t}$为随体导数，$\displaystyle \frac{\partial}{\partial t}$为局部导数/就地导数，$\bm{v} \cdot \nabla$为位变导数或对流导数。

### 2.1.2 运动方程 / 动量守恒方程 (Motion Equation / Momentum Conservation Equation)

$$
\rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = \nabla \cdot \overset{\rightarrow \rightarrow}{p} + \rho_\mathrm{f} \bm{E} + \bm{j} \times \bm{B} + \rho \bm{f}
$$

其中$\overset{\rightarrow \rightarrow}{p}$为压强张量，由本构方程决定；其中$\rho_\mathrm{f}$为自由电荷密度；$\bm{f}$为单位体积的外力。对宇宙等离子体而言，通常可忽略电场力项$\rho_f \bm{E}$，即

$$
\rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = \nabla \cdot \overset{\rightarrow \rightarrow}{p} + \bm{j} \times \bm{B} + \rho \bm{f} \tag{2.2.3}
$$

对宇宙等离子体而言，一般不考虑黏性(下文如无特别说明，均考虑无黏性磁流体)，即满足

$$
\overset{\rightarrow \rightarrow}{p} = - p \overset{\rightarrow \rightarrow}{I}
$$

则$(2.2.3)$式化为

$$
\rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = - \nabla p + \bm{j} \times \bm{B} + \rho \bm{f} \tag{2.2.4}
$$

有时也会考虑不可压缩但有黏性$\eta$($\eta$为常数)的磁流体，则$(2.2.3)$式化为

$$
\rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = - \nabla p + 2 \eta \nabla^2 \bm{v} + \bm{j} \times \bm{B} + \rho \bm{f} \tag{2.2.5}
$$

### 2.1.3 能量方程 (Energy Equation)

对宇宙等离子体而言，通常满足所谓**绝热条件**，即不考虑热传导、热辐射及其它可能的热源。此时能量方程为

$$
\begin{align}
\rho \frac{\mathrm{d}}{\mathrm{d} t} (u + \frac{v^2}{2}) & = - \nabla \cdot (p \bm{v}) + (\bm{j} \times \bm{B}) \cdot \bm{v} + \frac{j^2}{\sigma} + \rho \bm{f} \cdot \bm{v} \nonumber \\
& = - \nabla \cdot (p \bm{v}) + \bm{E} \cdot \bm{j} + \rho \bm{f} \cdot \bm{v} \tag{2.2.6}
\end{align}
$$

其中$u$为单位质量的内能；$\displaystyle \frac{j^2}{\sigma}$为Ohm耗散。与$(2.2.4)$式相应的**机械能方程**(mechanical energy equation)为

$$
\rho \frac{\mathrm{d}}{\mathrm{d} t} (\frac{v^2}{2})= - \nabla p \cdot \bm{v} + (\bm{j} \times \bm{B}) \cdot \bm{v} + \rho \bm{f} \cdot \bm{v} \nonumber
$$

联立上式与$(2.2.6)$式，可得

$$
\rho \frac{\mathrm{d} u}{\mathrm{d} t} = - p \nabla \cdot \bm{v} + \frac{j^2}{\sigma}
$$

对宇宙等离子体而言，通常可视为理想气体，即满足

$$
\begin{align}
& p = \frac{\rho R T}{\mu} = n k_\mathrm{B} T \tag{2.2.7} \\
& u = \frac{p}{(\gamma - 1) \rho} \tag{2.2.8}
\end{align}
$$

可推得

$$
\rho T \frac{\mathrm{d} S}{\mathrm{d} t} = \frac{\rho^\gamma}{\gamma - 1} \frac{\mathrm{d}}{\mathrm{d} t} \left( \frac{p}{\rho^\gamma} \right) = \frac{j^2}{\sigma} \tag{2.2.9}
$$

其中$S$是单位质量的熵。

## 2.2 电动力学方程 (Electrodynamics Equations)

### 2.2.1 Maxwell方程组 (Maxwell Equation Set)

对宇宙等离子体而言，通常使用真空中的Maxwell方程组，且忽略**位移电流**(displacement current)。在国际单位制下

$$
\begin{cases}
\displaystyle \nabla \times \bm{E} = -\frac{\partial \bm{B}}{\partial t} \\ \\
\nabla \times \bm{B} = \mu_0 \bm{j}_\mathrm{f} \\ \\
\displaystyle \nabla \cdot \bm{E} = \frac{\rho_\mathrm{f}}{\varepsilon_0} \\ \\
\nabla \cdot \bm{B} = 0 \tag{2.3.1}
\end{cases}
$$

其中$\bm{j}_\mathrm{f}$表示自由电流密度。

### 2.2.2 广义欧姆定律 (General Ohm Law)

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

## 2.3 磁感应方程 (Magnetic Induction Equation)

本节讨论运动的磁流体对磁场的作用，暂不考虑磁场力对磁流体运动的影响。磁流体中磁场变化所遵循的方程称为磁感应方程

$$
\frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) - \nabla \times [\eta_\mathrm{m}(\nabla \times \bm{B})] \tag{2.4.1}
$$

其中$\displaystyle \eta_\mathrm{m}=\frac{1}{\sigma \mu_0}$称为**磁扩散系数**(magnetic diffusion coefficient)。当电导率$\sigma$在空间上均匀时，上式可化为

$$
\frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) + \eta_\mathrm{m} \nabla^2 \bm{B} \tag{2.4.2}
$$

### 2.3.1 磁Reynolds数 (Magnetic Reynolds Number)

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

## 2.5 磁压强 (Magnetic Stress)

本节讨论磁场对磁流体的作用，这是流场和磁场耦合的另一方面。磁场对磁流体的作用力又被称为**安培力**(Ampere force)或**洛伦兹力**(Lorentz force)。单位体积磁流体所受到的磁场力$\bm{f}$为

$$
\bm{f} = \bm{j} \times \bm{B} = \frac{1}{\mu_0} (\nabla \times \bm{B}) \times \bm{B} \tag{2.5.1}
$$

上式可由向量公式化为

$$
\bm{f} = \nabla \cdot \frac{\bm{B} \bm{B}}{\mu_0} - \nabla \left( \frac{B^2}{2 \mu_0} \right) = \nabla \cdot \overset{\rightarrow \rightarrow}{p_\mathrm{B}}
$$

其中

$$
\overset{\rightarrow \rightarrow}{p_\mathrm{B}} = \frac{1}{\mu_0} (\bm{B} \bm{B} - \frac{B^2}{2} \overset{\rightarrow \rightarrow}{I})
$$

为磁压强张量。于是作用在外法向为$\bm{n}$的单位面积上的磁场压强为

$$
\bm{p}_\mathrm{B} = \overset{\rightarrow \rightarrow}{p_\mathrm{B}} \bm{n} = \frac{1}{\mu_0} \left[ (\bm{B} \cdot \bm{n}) \bm{B} - \frac{B^2}{2} \bm{n} \right] \tag{2.5.2}
$$

可推得

$$
\int_V \bm{f} \mathrm{d} V = \int_S \bm{p}_\mathrm{B} \mathrm{d} S
$$

其中$S$为包围体积$V$的封闭曲面。上式表明，作用在体积$V$的磁流体上的磁场力，在作用效果上可被看作作用在包围体积$V$的封闭曲面$S$上的磁场压力，由$(2.5.2)$式给出。

## 2.5 磁流体力学基本方程组 (MHD Basic Equation Set)

### 2.5.1 理想磁流体力学方程组

对宇宙等离子体而言，通常忽略电场力，满足绝热条件，视为理想气体，使用真空中的Maxwell方程组，并忽略位移电流。一般不考虑黏性时，由$(2.1.2)()$式

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \\ \\
\displaystyle \rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = -\nabla p + \bm{j} \times \bm{B} + \rho \bm{f} \\ \\
\displaystyle \frac{\rho^\gamma}{\gamma - 1} \frac{\mathrm{d}}{\mathrm{d} t} \left( \frac{p}{\rho^\gamma} \right) = \frac{j^2}{\sigma} \\ \\
\displaystyle \frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) - \nabla \times \left[ \eta_\mathrm{m} (\nabla \times \bm{B}) \right] \\ \\
\nabla \times \bm{B} = \mu_0 \bm{j} \\ \\
\bm{j} = \sigma (\bm{E} + \bm{v} \times \bm{B}) \\ \\
\nabla \cdot \bm{B} = 0 \tag{2.5.1}
\end{cases}
$$

### 2.2.2 完全导电理想磁流体力学方程组

对完全导电的磁流体而言

$$
\begin{align}
& \sigma \rightarrow + \infty \nonumber \\
& \eta_\mathrm{m} = \frac{1}{\mu_0 \sigma} \rightarrow 0 \nonumber
\end{align}
$$

方程组$(2.5.1)$化为

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \\ \\
\displaystyle \rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = -\nabla p + \bm{j} \times \bm{B} + \rho \bm{f} \\ \\
\displaystyle \frac{\mathrm{d}}{\mathrm{d} t} \left( \frac{p}{\rho^\gamma} \right) = 0 \\ \\
\displaystyle \frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) \\ \\
\nabla \times \bm{B} = \mu_0 \bm{j} \\ \\
\nabla \cdot \bm{B} = 0 \tag{2.5.2}
\end{cases}
$$

### 2.5.3 磁流体力学特征参数 (MHD Characteristic Parameters)

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