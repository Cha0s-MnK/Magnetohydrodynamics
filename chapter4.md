# Chapter 4: 磁流体力学波 (Magnetohydrodynamics Wave)

波动是等离子体集体运动的基本形式。鉴于磁流体力学方程的适用性条件，要求导电流体中出现的波动是低频的(频率的高低相对于等离子体振荡频率或带电粒子的回旋频率而言)，故它们通常与离子的运动和振荡有关。考虑处于平衡态的磁流体体系，在受到微扰时，往往会在平衡态附近做本征运动。当磁流体系处在热力学平衡或准热力学平衡态时，这种本征运动的扰动振幅满足线性化的运动方程组，对扰动量进行傅里叶展开，可求解每一个傅里叶分量所满足的方程组，便可得到波动的色散关系。该色散关系所描述的波动被通称为磁流体力学波，它是等离子体波动中的一支低频波模。

## 4.1 均匀理想磁流体力学波

一般可压缩流体中，小扰动以声波形式传播。由于等离子体的基本特性，在磁场存在的情况下，导电流体中小扰动的传播与一般流体具有显著的不同。除声波外，导电流体中还可能出现三种波动：Alfvén波、快磁声波和慢磁声波。第一种是横波，后两种为纵波和横波的混杂波(在特殊方向上取纵波形式)。波动的传播也不像声波那样是各向同性的，而是与磁场有关，呈现出各向异性的特征。

下面将从磁流体力学方程组出发，用微扰法推导均匀完全导电理想磁流体力学波动模式。对于宇宙等离子体，通常忽略其黏滞性，并认为电导率为无穷大，且将过程看作是绝热的。于是，均匀介质中完全导电理想磁流体力学基本方程组取如下形式

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \\ \\
\displaystyle \rho \left[ \frac{\partial \bm{v}}{\partial t} + (\bm{v} \cdot \nabla) \bm{v} \right] = - \nabla p + \frac{1}{\mu_0} (\nabla \times \bm{B}) \times \bm{B} \\ \\
\displaystyle \frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) \\ \\
\displaystyle \frac{\partial S}{\partial t} + (\bm{v} \cdot \nabla) S = 0 \\
p = p (\rho, S) \\
\nabla \cdot \bm{B} = 0 \tag{4.1.1}
\end{cases}
$$

考虑对平衡态的小扰动，这时导电流体中各物理量可表示为

$$
\begin{align}
& \bm{B} = \bm{B}_0 + \bm{B}_1 \tag{4.1.2} \\
& \bm{v} = \bm{v}_0 + \bm{v}_1 \tag{4.1.3} \\
& p = p_0 + p_1 \tag{4.1.4} \\
& \rho = \rho_0 + \rho_1 \tag{4.1.4} \\
& s = s_0 + s_1 \tag{4.1.5}
\end{align}
$$

$Q_0 (Q = \bm{B}, \bm{v}, p, \rho, s)$均为平衡时的量，而$Q_1$均为扰动量。显然，根据小扰动的假定，取扰动量(比起平衡量)是一阶小量即$\displaystyle \frac{Q_1}{Q_0} \ll 1$，并假定扰动前导电流体中各物理量的分布是均匀的，即$Q_0$均为常数，再引入变量

$$
\begin{align}
\bm{u}_0 = \frac{\bm{B}_0}{\sqrt{\mu_0 \rho_0}} \tag{4.1.6} \\
\bm{u}_1 = \frac{\bm{B}_1}{\sqrt{\mu_0 \rho_0}} \tag{4.1.7}
\end{align}
$$

将式$(4.1.2)-(4.1.7)$式代入方程组$(4.1.1)$，可推得：

$$
\begin{cases}
\displaystyle \frac{\partial \rho_1}{\partial t} + (\bm{v}_0 \cdot \nabla) \rho_1 = - \rho_0 (\nabla \cdot \bm{v}_1) \\ \\
\displaystyle \frac{\partial \bm{v}_1}{\partial t} + (\bm{v}_0 \cdot \nabla) \bm{v}_1 = - \frac{1}{\rho_0} \nabla(p_1 + \rho_0 \bm{u}_0 \cdot \bm{u}_1) + (\bm{u}_0 \cdot \nabla) \bm{u}_1 \\ \\
\displaystyle \frac{\partial \bm{u}_1}{\partial t} + (\bm{v}_0 \cdot \nabla) \bm{u}_1 = (\bm{u}_0 \cdot \nabla) \bm{v}_1 - \bm{u}_0 (\nabla \cdot \bm{v}_1) \\ \\
\displaystyle \frac{\partial S_1}{\partial t} + (\bm{v}_0 \cdot \nabla) S_1 = 0 \\ \\
\displaystyle p_1 = \left( \frac{\partial p_0}{\partial \rho_0} \right)_{S_0} \rho_1 + \left( \frac{\partial p_0}{\partial S_0} \right)_{\rho_0} S_1 = c_\mathrm{s}^2 \rho_1 + b S_1 \\ \\
\nabla \cdot \bm{u}_1 = 0 \tag{4.1.8}
\end{cases}
$$

对于线性化的小扰动方程组$(4.1.8)$，任何复杂的解均可根据Fourier展开分解为各种单色平面波的叠加。而单色平面波的角频率$\omega$和波矢$\bm{k}$之间的关系(即色散关系)将包含扰动传播的基本特性。

选择下列坐标系进行讨论，平衡磁场$\bm{B}_0$位于$Ozx$平面，平面谐波沿$x$轴传播，传播方向与磁场的夹角为$\theta$，如下图所示

![4.1](Figures/4.1.jpg)

于是

$$
\begin{align}
& u_\mathrm{0x} = u_0 \cos \theta \tag{4.1.9} \\
& u_\mathrm{0y} = 0 \tag{4.1.10} \\
& u_\mathrm{0z} = u_0 \sin \theta \tag{4.1.11}
\end{align}
$$

将所有的扰动量都表示为单色平面波，即

$$
Q_1 (x, t) = \bar{Q}_1 e^{i (\omega t - k x)} \tag{4.1.12}
$$

其中$\bar{Q}_1$在各扰动量中都取为常数。将式$(4.1.9)-(4.1.12)$代入方程组$(4.1.8)$，可推得

$$
\begin{cases}
(\omega - k v_\mathrm{0x}) \rho_1 - \rho_0 k v_{1x} = 0 \nonumber \\
\displaystyle (\omega - k v_\mathrm{0x}) v_{1x} - \frac{k}{\rho_0} p_1 - k u_\mathrm{1 z} u_0 \sin \theta = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) v_\mathrm{1y} + k u_\mathrm{1 y} u_0 \cos \theta = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) v_\mathrm{1z} + k u_\mathrm{1 z} u_0 \cos \theta = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) u_\mathrm{1x} = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) u_\mathrm{1y} + k v_\mathrm{1 y} u_0 \cos \theta = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) u_\mathrm{1z} + k v_\mathrm{1 z} u_0 \cos \theta - k v_\mathrm{1 x} u_0 \sin \theta = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) s_1 = 0 \\
p_1 - c_\mathrm{s}^2 \rho_1 - b s_1 = 0 \tag{4.1.13}
\end{cases}
$$

未知量共9个，分别是$u_\mathrm{1x}$、$u_\mathrm{1y}$、$u_\mathrm{1z}$、$v_\mathrm{1x}$、$v_\mathrm{1y}$、$v_\mathrm{1z}$、$p_1$、$\rho_1$和$S_1$。方程组$(4.1.13)$是它们的线性齐次方程组。零解显然不是我们要求的，而线性齐次方程组具有非零解的条件，是其系数行列式为0。可推得

$$
\omega_0^2 \left[ \omega_0^2 - (ku_0 \cos \theta)^2 \right] \left[ \omega_0^4 - k^2 (c_\mathrm{s}^2 + u_0^2) \omega_0^2 +  k^2 c_\mathrm{s}^2 (k u_0 \cos \theta)^2 \right] = 0 \tag{4.1.14}
$$

其中：

$$
\omega_0 = \omega - k v_\mathrm{0x}
$$

上式就是均匀理想磁流体中波动传播的色散关系，确定了其中可能产生的几种性质完全不同的波动模式，下面分别进行讨论。

### 4.1.1 熵波 (Entropy Wave)

色散关系$(4.1.14)$式的一个解为

$$
\omega_0 = 0
$$

上式意味着波速为0，表示扰动并不在磁流体中传播。将它代入方程组$(4.1.13)$中，可得

$$
\begin{cases}
u_\mathrm{1x} = u_\mathrm{1y} = u_\mathrm{1z} = v_\mathrm{1x} = v_\mathrm{1y} = v_\mathrm{1z} = p_1 = 0 \\
\displaystyle \rho_1 = - \frac{b}{c_\mathrm{s}^2} S_1 \neq 0
\end{cases}
$$

上述解意味着均匀磁流体中，磁场扰动、速度扰动和压强扰动都不存在，只有密度和熵的扰动。习惯上将此情况称作熵波，但它实质上不是波，扰动只局限在局部区域内而并不传播。

### 4.1.2 Alfvén波 (Alfvén Wave)

色散关系$(4.1.14)$式的另一个解为：

$$
\omega_0 = \pm k u_0 \cos \theta
$$

由上式可得扰动传播的相速度为：

$$
v_\mathrm{p} = \frac{\omega_0}{k} = \pm u_0 \cos \theta = \pm \frac{B_0}{\sqrt{\mu_0 \rho_0}} \cos \theta \tag{4.1.15}
$$

当传播方向$\bm{k}$与磁场平行，即$\cos \theta = 1$时，代入方程组$(4.1.13)$可得：

$$
\begin{cases}
u_\mathrm{1x} = v_\mathrm{1x} = p_1 = \rho_1 = S_1 = 0 \\
u_\mathrm{1y} = \pm v_\mathrm{1y} \\
u_\mathrm{1z} = \pm v_\mathrm{1z} \tag{4.1.16}
\end{cases}
$$

上述解表明磁场在$x$方向，扰动在垂直于磁场的方向，波的传播方向为$x$方向，所以这种波动模式是横波。它的传播速度

$$
v_\mathrm{A} = \frac{\omega_0}{k} = \pm u_0 = \pm \frac{B_0}{\sqrt{\mu_0 \rho_0}} \tag{4.1.17}
$$

其中$B_0$越大意味着磁场张力的“恢复力”越大，使波动传播越快；而$\rho_0$越大表示运动物质的惯性越大，它无疑将滞迟波动的传播。这种波动是存在磁场时导电流体中所特有的一种波动，被命名为Alfvén波。由$(4.1.16)$式可知，这种波动模式中压强、密度和熵均无扰动，即在这种模式的波动中可压流体与不可压流体的作用完全相同，扰动的传播都是由磁张力所引起的。$(4.1.17)$式所示的波的相速度$v_\mathrm{A}$称为(剪切)Alfvén波速，通常把Alfvén波速看成是磁流体中的一个特征速度。

当传播方向$\bm{k}$与磁场有一夹角$\theta$时，代入方程组$(4.1.13)$可得：

$$
\begin{cases}
u_\mathrm{1x} = u_\mathrm{1z} = v_\mathrm{1x} = v_\mathrm{1z} = p_1 = \rho_1 = S_1 = 0 \\
u_\mathrm{1y} = \pm v_\mathrm{1y}
\end{cases}
$$

由上式所确定的波动，其基本模式与$(4.1.16)$式的阿尔文波相同，通常将它命名为斜Alfvén波。$(4.1.15)$式显示，斜阿尔文波的传播是各向异性的，波速与磁场和波矢$\bm{k}$的夹角有关。沿磁场方向传播时波速最大，这就是通常的Alfvén波；随着与磁场方向偏离的增大而波速越来越小；在与磁场垂直的方向上没有斜Alfvén波传播。

### 4.1.3 磁声波 (Magnetosonic Wave)

色散关系$(4.1.14)$式的还有一组解为：

$$
\omega_0^4 - k^2 (c_\mathrm{s}^2 + u_0^2) \omega_0^2 +  k^2 c_\mathrm{s}^2 (k u_0 \cos \theta)^2 = 0
$$

解上式可得扰动传播的速度为

$$
c_\mathrm{M\pm}^2 = \frac{\omega^2}{k^2} = \frac{1}{2} \left[ c_\mathrm{s}^2 + u_0^2 \pm \sqrt{(c_\mathrm{s}^2 + u_0^2)^2 - 4 c_\mathrm{s}^2 u_0^2 \cos^2 \theta} \right] \tag{4.1.18}
$$

上式给出了两种波动模式，其中取正号的称为**快磁声波**(fast magnetosonic wave)，而取负号的称为**慢磁声波**(slow magnetosonic wave)。显然快慢磁声波的相速度是各向异性的，波速与磁场和波矢$\bm{k}$的夹角有关。下面就扰动传播方向与磁场方向之间的几种不同夹角分别进行讨论。

#### 4.1.3.1

当$\theta = 0$，即扰动随磁场传播时，$(4.1.18)$式变为

$$
c_\mathrm{M\pm}^2 = \frac{\omega_0^2}{k^2} = \frac{1}{2} \left( c_\mathrm{s}^2 + u_0^2 \pm |c_\mathrm{s}^2 - u_0^2| \right)
$$

即

$$
\begin{cases}
c_\mathrm{M+} = \max(c_\mathrm{s}, u_0) \\
c_\mathrm{M-} = \min(c_\mathrm{s}, u_0) \tag{4.1.19}
\end{cases}
$$

将上式代入方程组中，当$c_\mathrm{M} = c_\mathrm{s}$时可得

$$
\begin{cases}
u_\mathrm{1x} = u_\mathrm{1y} = u_\mathrm{1z} = v_\mathrm{1y} = v_\mathrm{1z} = S_1 = 0 \\ \\
\displaystyle v_\mathrm{1x} = \frac{\rho_1}{\rho_0} c_\mathrm{s} \\ \\
p_1 = c_\mathrm{s}^2 \rho_1
\end{cases}
$$

上式所描述的是由磁流体密度的疏密扰动引起并由热压力驱动而形成的纵波，即其传播方向和流体元扰动的方向一致，其图像与声波十分相像，因电子和离子的分离很小，可以认为电子和离子基本上粘合在一起运动，而离子所受的恢复力除热压强外，显然还有由于电荷分离而引起的静电力(尽管电子和离子分离小，但其因分离而引起的静电力却与热压强相当)，这不同于仅受热压强作用的声波，它叫作离子声波。声波的传播仅仅由于中性质点间的碰撞，而离子声波中驱动波所需的位能，除来源于离子之间的热运动外，还来源于静电能，它由电子振荡与离子振荡的振幅差所产生。在无碰撞等离子体中，离子声波的传播则全靠静电力。

将$(4.1.19)$式代入方程组$(4.1.13)$中，当$c_\mathrm{M} = u_0$时可得

$$
\begin{cases}
u_\mathrm{1x} = v_\mathrm{1x} = p_1 = \rho_1 = S_1 = 0 \\
u_\mathrm{1y} = - v_\mathrm{1y} \neq 0 \\
u_\mathrm{1z} = - v_\mathrm{1z}\neq 0 \tag{4.1.20}
\end{cases}
$$

上式与$(4.1.16)$式一样，这正是Alfvén波模式，其相速度为

$$
v_\mathrm{p} = \frac{\omega_0}{k} = c_\mathrm{M} = u_0 = \frac{B_0}{\sqrt{\mu_0 \rho_0}}
$$

所以沿着磁场方向有两支波，一支是离子声波，它是纵波；另一支是Alfvén波，它是横波，它的速度扰动和磁场扰动的方向均与磁场垂直。

#### 4.1.3.2

当$\displaystyle \theta = \frac{\pi}{2}$时，即波动传播方向与磁场垂直，这时$\cos \theta = 0$，由$(4.1.18)$式可得

$$
\begin{cases}
c_\mathrm{M+} = \sqrt{c_\mathrm{s}^2 + u_0^2} \\
c_\mathrm{M-} = 0 \tag{4.1.21}
\end{cases}
$$

将上式代入方程组$(4.1.13)$中，可得

$$
\begin{cases}
u_\mathrm{1x} = u_\mathrm{1y} = v_\mathrm{1y} = v_\mathrm{1z} = S_1 = 0 \\ \\
\displaystyle u_\mathrm{1z} = \frac{\rho_1}{\rho_0} u_0 \\ \\
\displaystyle v_\mathrm{1x} = \frac{\rho_1}{\rho_0} \sqrt{c_\mathrm{s}^2 + u_0^2} \\ \\
p_1 = c_\mathrm{s}^2 \rho_1 \tag{4.1.22}
\end{cases}
$$

由$(4.1.21)$和$(4.1.22)$式所描述的波动模式称作磁声波。显然，磁声波$(\displaystyle \theta = \frac{\pi}{2})$的波速$c_\mathrm{M+} = \sqrt{c_\mathrm{s}^2 + u_0^2}$是磁流体中低频扰动传播的最大可能速度。其物理原因在于，由热压力产生的导电流体的“弹性”与磁压力引起的磁场的准“弹性”，在$\bm{k} \perp \bm{B}_0$的情况下产生了“最佳”的叠加，从而导致扰动的传播具有最快速度。$(4.1.21)$式右端两项，正是这两种“弹性”在数量上的叠加的表征。$(4.1.22)$式给出的波动图像表明，对于磁声波，速度扰动在波的传播方向，而磁场的扰动则在与传播方向垂直的方向上。因此，它不是单一的纵波或模波，而是一种纵波和横波的混杂波。所以在与磁场垂直方向上传播着一支叫作磁声波的混杂波，或者亦可说传播着一支磁声波和另一支并不传播的熵波。

#### 4.1.3.3

当$\displaystyle 0 < \theta < \frac{\pi}{2}$，这是一般情况，传播方向既不在磁场方向也不在与磁场垂直的方向。这时，波动模式可分为快磁声波和慢磁声波两类。由$(4.1.18)$式可知

$$
\begin{cases}
\max(c_\mathrm{s}, v_\mathrm{A}) \leqslant c_\mathrm{M+} \leqslant \sqrt{c_\mathrm{s}^2 + v_\mathrm{A}^2} \\
0 \leqslant c_\mathrm{M-} \leqslant \min(c_\mathrm{s}, v_\mathrm{A})
\end{cases}
$$

将上式代入方程组$(4.1.13)$中，可得

$$
\begin{cases}
u_\mathrm{1x} = u_\mathrm{1y} = v_\mathrm{1y} = S_1 = 0 \\ \\
\displaystyle u_\mathrm{1z} = \frac{\rho_1}{\rho_0} \frac{c_\mathrm{M \pm}^2 - c_\mathrm{s}^2}{u_0 \sin \theta} \\ \\
\displaystyle v_\mathrm{1x} = \frac{\rho_1}{\rho_0} c_\mathrm{M \pm} \\ \\
\displaystyle v_\mathrm{1z} = - \frac{\rho_1}{\rho_0} \frac{c_\mathrm{M \pm}^2 - c_\mathrm{s}^2}{c_\mathrm{M \pm} \tan \theta} \\ \\
p_1 = c_\mathrm{s}^2 \rho_1
\end{cases}
$$

上式表明，对于磁声波，熵是守恒的。在扰动传播的方向上，只有速度扰动，而在垂直于传播方向上，则速度和磁场扰动均存在，这意味着快慢磁声波都是混杂波。

上面的讨论充分显示了磁流体中波动模式的多样性。其根本原因在于扰动传播在磁流体中传播可以依靠两种应力：热压力和磁应力。这两种作用力有时互相独立，如离子声波、(剪切)Alfvén波(包括斜Alfvén波)；有时又互相耦合，如快、慢磁声波。磁应力的作用可分为磁张力和磁压力，其中与磁场张力相关的磁力线的“刚性”将造成扰动以(剪切)Alfvén波(包括斜Alfvén波)的模式传播，这显然是一种横波。由于它的传播仅仅是由于磁力线的振动(磁力线形状的变化)引起的，因此不改变磁力线的密度，在均匀理想导电流体中，与磁力线冻结的流体密度也不变。所以(剪切)Alfvén波(包括Alfvén波)在传播中不产生流体的密度扰动，这就是在不可压缩磁流体和可压缩磁流体中都能传播(剪切)Alfvén波(包括斜Alfvén波)的物理原因。流体的热压力与磁压力几乎总是相互耦合着的，磁力线的密度变化(即磁场强度的变化)必然与流体密度的变化同时出现。无疑，这种变化只能出现在可压缩流体中，所以只有在可压磁流体中才能有离子声波和快慢磁声波等波动模式。热压力和磁压力的耦合可以使导电流体的“弹性”加强，也可使“弹性”减弱。当流体被压缩时($\rho_1 > 0$)，该压缩区的扰动场$\bm{B}_1$增强原有的磁场，则产生的恢复力将大于只考虑热压力时的恢复力，于是原有的离子声波将被加速，形成快磁声波。反之，如果压缩区的扰动场$\bm{B}_1$减弱原有的磁场，则耦合的恢复力便小于单一的热压力，离子声波将被减速，便形成慢磁声波。当$\displaystyle \theta = \frac{\pi}{2}$时，热压力与磁压力的耦合最直观，此时磁冻结使得热压力的增强与磁压力的增强完全同步，于是产生了传播速度最快的磁声波模式。下图给出了两种典型的磁流体力学波动——(剪切)Alfvén波和磁声波传播的十分形象的示意图。

## 4.2 阻尼Alfvén波 (Damped Alfvén Wave)

若Alfvén波在有限电导率和具有黏滞性的磁流体中传播，则有限电导率导致的焦耳耗散和流体黏滞性引起的热耗散，将造成Alfvén波的衰减，这时Alfvén波成为阻尼Alfvén波。考虑具有有限电导率和黏滞性的不可压缩磁流体，它满足下述方程组

$$
\begin{cases}
\nabla \cdot \bm{v} = 0 \\ \\
\displaystyle \rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = -\nabla p + \frac{1}{\mu_0} (\nabla \times \bm{B}) \times \bm{B} + \eta \nabla^2 \bm{v} \\ \\
\displaystyle \frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) + \eta_\mathrm{m} \nabla^2 \bm{B} \\ \\
\nabla \cdot \bm{B} = 0 \tag{4.2.1}
\end{cases}
$$

设平衡时的磁场为均匀场$\bm{B}_0$，$z$轴选在$\bm{B}_0$方向；扰动前流体处在静止状态，即$\bm{v}_0 = 0$；平衡时的压强为$p_0$。考虑对平衡态的小扰动，则

$$
\begin{cases}
\bm{B} = \bm{B}_0 + \bm{B}_1 \\
\bm{v} = \bm{v}_1 \\
p = p_0 + p_1
\end{cases}
$$

将上式代入方程组$(4.2.1)$，并仅讨论扰动沿$z$轴传播，于是扰动在x-y平面中是均匀的，可推得

$$
\begin{cases}
\nabla \cdot \bm{v}_1 = 0 \\ \\
\displaystyle \rho_0 \frac{\partial \bm{v}_1}{\partial t} = \frac{B_0}{\mu_0} \frac{\partial \bm{B}_1}{\partial z} - \nabla \left( p_1 + \frac{B_0 B_\mathrm{1z}}{\mu_0} \right) + \rho_0 \nu \nabla^2 \bm{v}_1 \\ \\
\displaystyle \frac{\partial \bm{B}_1}{\partial t} = B_0 \frac{\partial \bm{v}_1}{\partial z} + \eta_\mathrm{m} \nabla^2 \bm{B}_1 \\ \\
\nabla \cdot \bm{B}_1 = 0
\end{cases}
$$

其中$\displaystyle \nu = \frac{\eta}{\rho_0}$为运动粘滞系数。考虑到Alfvén波是横波，则$B_\mathrm{1z} = v_\mathrm{1z} = 0$，$\bm{v}_{1\perp} = v_\mathrm{1x} \bm{i} + v_\mathrm{1y} \bm{j}$为垂直于$\bm{B}_0$的小扰动。设无穷远处$p_1 = 0$，$B_\mathrm{1z} = 0$，可推得

$$
\frac{\partial^2 \bm{v}_{1 \perp}}{\partial t^2} - v_\mathrm{A}^2 \frac{\partial^2 \bm{v}_{1 \perp}}{\partial z^2} = (\eta_\mathrm{m} + \nu) \frac{\partial^3 \bm{v}_{1 \perp}}{\partial t \partial z^2} \tag{4.2.2}
$$

显然，当$\eta_\mathrm{m} = \nu = 0$时，上式便简化为理想磁流体中的Alfvén波的传播方程。上式右端即阻尼项。考虑上式的单色平面波解

$$
\bm{v}_{1 \perp} = \bar{\bm{v}}_{1 \perp} e^{i (\omega t - k z)}
$$

将它代入$(4.1.2)$式中，便得到阻尼Alfvén波的色散关系

$$
\omega^2 - v_\mathrm{A}^2 k^2 = i (\eta_\mathrm{m} + \nu) \omega k^2
$$

一般令波数$k$为实数，角频率$\omega$为复数，由上式可解得

$$
\tilde{\omega} = \frac{1}{2} \sqrt{4 v_\mathrm{A}^2 k^2 - (\eta_\mathrm{m} + \nu)^2 k^4} \pm \frac{1}{2} (\eta_\mathrm{m} + \nu) k^2 i \tag{4.2.3}
$$

有限电导率和有限黏滞性导致Alfvén波的衰减，其衰减的特征时间为

$$
\tau = \frac{2 \pi}{\Im(\tilde{\omega})} = \frac{4 \pi}{(\eta_\mathrm{m} + \nu) k^2}
$$

$(4.2.3)$式还表明，为了使阻尼Alfvén波有波动解，必须满足

$$
\begin{align}
\Re(\tilde{\omega}) & > 0 \nonumber \\
\Rightarrow v_\mathrm{A} & > \frac{1}{2} (\eta_\mathrm{m} + \nu) k
\end{align}
$$

## 4.3 简单波 (Simple Wave)

若初始扰动具有不是很小的有限振幅，则我们不能利用4.1节中的小扰动方法将方
程组线性化，而必须求解非线性方程组。下面我们讨论流体和磁流体的一维非定常流
动——（磁）简单波，由此了解有限振幅的传播规律和特性，及转变为激波的可能性和转化
条件。

在处理小扰动时，对方程组做线性化处理，得到方程的解是$(x + v t)$的函数(单色平面波)，它相当于形状不变但具有以速度$v$移动的波轮廓的“行波”(波轮廓是指各有关物理量——密度、速度等在沿波传播方向上的分布情况)。前面讨论的声波、磁声波、磁流波都属于这种情况。既然速度、密度和压强在这种行波中都只是同一组合$(x + v t)$的函数，所以它们相互之间都可用不显含坐标与时间的关系式来表达，例如$p = p (\rho)$，$v = v (\rho)$等。

如果扰动不是小振幅，而是有限波幅的情形，那么上述这些简单关系就不再成立。但是仍有可能采用小振幅线性方程解式$f (x + v t)$的推广来求出表示运动方程的准确解，这个解通常被称为简单波或Riemann波。

假定任意振幅波中密度和速度仍可相互以函数形式表达，由此我们来理解流体的一维非定常运动。

绝热条件下理想流体的基本方程组为

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \\ \\
\displaystyle \frac{\partial \bm{v}}{\partial t} + (\bm{v} \cdot \nabla) \bm{v} = -\frac{1}{\rho} \nabla p
\end{cases}
$$

在讨论一维流动时，化为

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \frac{\partial (\rho v)}{\partial x} = 0 \\ \\
\displaystyle \frac{\partial v}{\partial t} + v\frac{\partial v}{\partial x} + \frac{1}{\rho} \frac{\partial p}{\partial x} = 0
\end{cases}
$$

假设$p$、$\rho$和$v$之间互为单值函数，可推得

$$
\begin{align}
& v = \pm \int \frac{c_\mathrm{s}}{\rho} \mathrm{d} \rho \tag{4.3.1} \\
& x = (v \pm c_\mathrm{s}) + f (v) \nonumber \\
& c_\mathrm{s} = \sqrt{\frac{\mathrm{d} p}{\mathrm{d} \rho}} \nonumber
\end{align}
$$

其中$f$为任意函数。借助状态方程可积分$(4.3.1)$式。

再考虑绝热条件下完全导电的理想磁流体，其基本方程组为

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \nabla \cdot (\bm{\rho v}) = 0 \\ \\
\displaystyle \frac{\partial \bm{v}}{\partial t} + (\bm{v} \cdot \nabla) \bm{v} = -\frac{1}{\rho} \nabla p + \frac{1}{\mu_0 \rho} (\nabla \times \bm{B}) \times \bm{B} \\ \\
\displaystyle \frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B})
\end{cases}
$$

在讨论一维流动时，化为

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \frac{\partial (\rho v)}{\partial x} = 0 \\ \\
\displaystyle \frac{\partial v}{\partial t} + v \frac{\partial v}{\partial x} = -\frac{1}{\rho} \frac{\partial p}{\partial x} + \frac{1}{\mu_0 \rho} \left( B_y \frac{\partial B_y}{\partial x} + B_z \frac{\partial B_z}{\partial x} \right) \\ \\
\displaystyle B_x \frac{\partial B_y}{\partial x} = 0 \\ \\
\displaystyle B_x \frac{\partial B_z}{\partial x} = 0 \\ \\
\displaystyle \frac{\partial B_x}{\partial t} = 0 \\ \\
\displaystyle \frac{\partial B_y}{\partial t} = -\frac{\partial (v B_y)}{\partial x} \\ \\
\displaystyle \frac{\partial B_z}{\partial t} = -\frac{\partial (v B_z)}{\partial x} \tag{4.3.2}
\end{cases}
$$

由上述方程组可得

$$
\begin{align}
& \frac{\partial B_x}{\partial t} = 0 \nonumber \\
& \Rightarrow B_x = B_x (x) \nonumber
\end{align}
$$

于是分两种情况。若$B_x \neq 0$，由方程组$(4.3.2)$可得

$$
\begin{align}
& \frac{\partial B_y}{\partial x} = \frac{\partial B_z}{\partial x} = 0 \nonumber \\
& \Rightarrow \frac{\partial v}{\partial t} + v \frac{\partial v}{\partial x} = -\frac{1}{\rho} \frac{\partial p}{\partial x} \nonumber
\end{align}
$$

此时方程组与流体情形完全相同，相当于流动不受磁场影响。

若$B_x = 0$，即流动方向与磁场方向垂直。此时方程组$(4.3.2)$化为

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + v \frac{\partial \rho}{\partial x} = -\rho \frac{\partial v}{\partial x} \\ \\
\displaystyle \frac{\partial B}{\partial t} + v \frac{\partial B}{\partial x} = - B \frac{\partial v}{\partial x} \\ \\
\displaystyle \frac{\partial v}{\partial t} + v \frac{\partial v}{\partial x} = -\frac{1}{\rho} \frac{\partial}{\partial x} \left( p + \frac{B^2}{2\mu_0} \right)
\end{cases}
$$