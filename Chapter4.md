# Chapter 4: 磁流体力学波 (Magnetohydrodynamics Wave)

波动是等离子体集体运动的基本形式。鉴于磁流体力学方程的适用性条件，要求导电流体中出现的波动是低频的(频率的高低相对于等离子体振荡频率或带电粒子的回旋频率而言)，故它们通常与离子的运动和振荡有关。考虑处于平衡态的磁流体体系，在受到微扰时，往往会在平衡态附近做本征运动。当磁流体系处在热力学平衡或准热力学平衡态时，这种本征运动的扰动振幅满足线性化的运动方程组，对扰动量进行傅里叶展开，可求解每一个傅里叶分量所满足的方程组，便可得到波动的色散关系。该色散关系所描述的波动被通称为磁流体力学波，它是等离子体波动中的一支低频波模。

## 4.1 均匀磁流体中的磁流体力学波

### 4.1.1 均匀理想磁流体力学波

一般可压缩流体中，小扰动以声波形式传播。由于等离子体的基本特性，在磁场存在的情况下，导电流体中小扰动的传播与一般流体具有显著的不同。除声波外，导电流体中还可能出现三种波动：阿尔文波、快磁声波和慢磁声波。第一种是横波，后两种为纵波和横波的混杂波(在特殊方向上取纵波形式)。波动的传播也不像声波那样是各向同性的，而是与磁场有关，呈现出各向异性的特征。

下面将从磁流体力学方程组出发，用微扰法推导均匀完全导电理想磁流体力学波动模式。对于宇宙等离子体，通常忽略其黏滞性，并认为电导率为无穷大，且将过程看作是绝热的。于是，均匀介质中完全导电理想磁流体力学基本方程组取如下形式

$$
\begin{align}
& \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \tag{4.1.1} \\
& \rho \left[ \frac{\partial \bm{v}}{\partial t} + (\bm{v} \cdot \nabla) \bm{v} \right] = - \nabla p + \frac{1}{\mu_0} (\nabla \times \bm{B}) \times \bm{B} \tag{4.1.2} \\
& \frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) \tag{4.1.3} \\
& \frac{\partial s}{\partial t} + (\bm{v} \cdot \nabla) s = 0 \tag{4.1.4} \\
& p = p (\rho, s) \tag{4.1.5} \\
& \nabla \cdot \bm{B} = 0 \tag{4.1.6}
\end{align}
$$

考虑对平衡态的小扰动，这时导电流体中各物理量可表示为

$$
\begin{align}
\bm{B} & = \bm{B}_0 + \bm{B}_1 \nonumber \\
\bm{v} & = \bm{v}_0 + \bm{v}_1 \nonumber \\
p & = p_0 + p_1 \nonumber \\
\rho & = \rho_0 + \rho_1 \nonumber \\
s & = s_0 + s_1 \nonumber
\end{align}
$$

$Q_0 (Q = \bm{B}, \bm{v}, p, \rho, s)$均为平衡时的量，而$Q_1$为扰动量。显然，根据小扰动的假定，取扰动量(比起平衡量)是一阶小量即$\displaystyle \frac{Q_1}{Q_0} = \varepsilon \ll 1$，并假定扰动前导电流体中各物理量的分布是均匀的，即$Q_0$均为常数，再引入变量

$$
\begin{align}
\bm{u}_0 = \frac{\bm{B}_0}{\sqrt{\mu_0 \rho_0}} \nonumber \\
\bm{u}_1 = \frac{\bm{B}_1}{\sqrt{\mu_0 \rho_0}} \nonumber
\end{align}
$$

将()式代入方程组式，可推得：

$$
\begin{align}
& \frac{\partial \rho_1}{\partial t} + (\bm{v}_0 \cdot \nabla) \rho_1 = - \rho_0 (\nabla \cdot \bm{v}_1) \nonumber \\
& \frac{\partial \bm{v}_1}{\partial t} + (\bm{v}_0 \cdot \nabla) \bm{v}_1 = - \frac{1}{\rho_0} \nabla(p_1 + \rho_0 \bm{u}_0 \cdot \bm{u}_1) + (\bm{u}_0 \cdot \nabla) \bm{u}_1 \nonumber \\
& \frac{\partial \bm{u}_1}{\partial t} + (\bm{v}_0 \cdot \nabla) \bm{u}_1 = (\bm{u}_0 \cdot \nabla) \bm{v}_1 - \bm{u}_0 (\nabla \cdot \bm{v}_1) \nonumber \\
& \frac{\partial s_1}{\partial t} + (\bm{v}_0 \cdot \nabla) s_1 = 0 \nonumber \\
& p_1 = \left( \frac{\partial p_0}{\partial \rho_0} \right)_{s_0} \rho_1 + \left( \frac{\partial p_0}{\partial s_0} \right)_{\rho_0} s_1 = c_\mathrm{s}^2 \rho_1 + b s_1 \nonumber \\
& \nabla \cdot \bm{u}_1 = 0 \nonumber
\end{align}
$$

对于线性化的小扰动方程组(4.1-1)～(4.1-6)式，任何复杂的解均可根据Fourier展开分解为各种单色平面波的叠加。而单色平面波的角频率$\omega$和波矢$\bm{k}$之间的关系(即色散关系)将包含扰动传播的基本特性。

选择下列坐标系进行讨论，平衡磁场$\bm{B}_0$位于$Ozx$平面，平面谐波沿$x$轴传播，传播方向与磁场的夹角为$\theta$，如下图所示：

![]()

于是：

$$
\begin{align}
& u_{0x} = u_0 \cos \theta \tag{4.1.} \\
& u_{0y} = 0 \tag{4.1.} \\
& u_{0z} = u_0 \sin \theta \tag{4.1.}
\end{align}
$$
将所有的扰动量都表示为单色平面波，即

$$
Q_1 (x, t) = \bar{Q}_1 e^{i (\omega t - k x)} \tag{4.1.} \\
$$

其中$\bar{Q}_1$在各扰动量中都取为常数。有：

$$
\begin{align}
& \frac{\partial Q_1}{\partial t} = i \omega Q_1 \tag{4.1.} \\
& (\bm{v}_0 \cdot \nabla) Q_1 = v_{0 x} (- i k) Q_1 \tag{4.1.} \\
& (\bm{u}_0 \cdot \nabla) Q_1 = u_{0 x} (- i k) Q_1 \tag{4.1.} \\
& \nabla \cdot \bm{v}_1 = - i k v_{1x} \tag{4.1.} \\
& \nabla \cdot \bm{u}_1 = - i k u_{1x} \tag{4.1.}
\end{align}
$$

将式代入式，可推得：

$$
\begin{align}
& (\omega - k v_\mathrm{0x}) \rho_1 - \rho_0 k v_{1x} = 0 \nonumber \\
& (\omega - k v_\mathrm{0x}) v_{1x} - \frac{k}{\rho_0} p_1 - k u_\mathrm{1 z} u_0 \sin \theta = 0 \nonumber \\
& (\omega - k v_\mathrm{0x}) v_\mathrm{1y} + k u_\mathrm{1 y} u_0 \cos \theta = 0 \nonumber \\
& (\omega - k v_\mathrm{0x}) v_\mathrm{1z} + k u_\mathrm{1 z} u_0 \cos \theta = 0 \nonumber \\
& (\omega - k v_\mathrm{0x}) u_\mathrm{1x} = 0 \nonumber \\
& (\omega - k v_\mathrm{0x}) u_\mathrm{1y} + k v_\mathrm{1 y} u_0 \cos \theta = 0 \nonumber \\
& (\omega - k v_\mathrm{0x}) u_\mathrm{1z} + k v_\mathrm{1 z} u_0 \cos \theta - k v_\mathrm{1 x} u_0 \sin \theta = 0 \nonumber \\
& (\omega - k v_\mathrm{0x}) s_1 = 0 \nonumber \\
& p_1 - c_\mathrm{s}^2 \rho_1 - b s_1 = 0 \nonumber \\
& k u_\mathrm{1x} = 0 \nonumber
\end{align} \\
\begin{cases}
(\omega - k v_\mathrm{0x}) \rho_1 - \rho_0 k v_{1x} = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) v_{1x} - \frac{k}{\rho_0} p_1 - k u_\mathrm{1 z} u_0 \sin \theta = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) v_\mathrm{1y} + k u_\mathrm{1 y} u_0 \cos \theta = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) v_\mathrm{1z} + k u_\mathrm{1 z} u_0 \cos \theta = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) u_\mathrm{1x} = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) u_\mathrm{1y} + k v_\mathrm{1 y} u_0 \cos \theta = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) u_\mathrm{1z} + k v_\mathrm{1 z} u_0 \cos \theta - k v_\mathrm{1 x} u_0 \sin \theta = 0 \nonumber \\
(\omega - k v_\mathrm{0x}) s_1 = 0 \\
p_1 - c_\mathrm{s}^2 \rho_1 - b s_1 = 0 \tag{4.1.}
\end{cases}
$$

独立的方程有9个，未知量为9个，方程组(4.1-8)是它们的线性齐次代数方程组。零解显然不是我们要求的，而线性齐次代数方程组具有非零解的条件，是方程组(4.1-8)的系数行列式为零，将(4.1-9)式代入并将行列式展开，便可得到均匀理想磁流体中波动传播的色散方程式：

$$
\omega_0^2 \left[ \omega_0^2 - (ku_0 \cos \theta)^2 \right] \left[ \omega_0^4 - k^2 (c_\mathrm{s}^2 + u_0^2) \omega_0^2 +  k^2 c_\mathrm{s}^2 (k u_0 \cos \theta)^2 \right] = 0 \tag{4.1.}
$$

其中：

$$
\omega_0 = \omega - k v_\mathrm{0x} \tag{4.1.}
$$

上式给出了均匀可压缩理想磁流体中波动的基本性质，确定了其中可能产生的几种性质完全不同的波动模式，下面分别进行讨论。

### 4.1.1 熵波 (Entropy Wave)

色散关系$(4.1.)$式的一个解为

$$
\omega_0 = 0 \tag{4.1.}
$$

上式意味着波速为0，表示扰动并不在磁流体中传播。将它代入方程组中，可得：

$$
\begin{cases}
u_\mathrm{1x} = u_\mathrm{1y} = u_\mathrm{1z} = v_\mathrm{1x} = v_\mathrm{1y} = v_\mathrm{1z} = p_1 = 0 \\
\displaystyle \rho_1 = - \frac{b}{c_\mathrm{s}^2} S_1 \neq 0 \tag{4.1.}
\end{cases}
$$

上述解意味着均匀磁流体中，磁场扰动、速度扰动和压强扰动都不存在，只有密度和熵的扰动。它们之间的关系由$(4.1.)$式确定。习惯上将此情况称作熵波，但它实质上不是波，扰动只局限在局部区域内而并不传播。

### 4.1.2 Alfvén波 (Alfvén Wave)

色散关系$(4.1.)$式的另一个解为：

$$
\omega_0 = \pm k u_0 \cos \theta \tag{4.1.}
$$

由上式可得扰动传播的相速度为：

$$
v_\mathrm{p} = \frac{\omega_0}{k} = \pm u_0 \cos \theta = \pm \frac{B_0}{\sqrt{\mu_0 \rho_0}} \cos \theta \tag{4.1.}
$$

当传播方向$\bm{k}$与磁场平行，即$\cos \theta = 1$时，代入方程组$(4.1.)$可得：

$$
\begin{cases}
u_\mathrm{1x} = v_\mathrm{1x} = p_1 = \rho_1 = S_1 = 0 \\
u_\mathrm{1y} = \pm v_\mathrm{1y} \\
u_\mathrm{1z} = \pm v_\mathrm{1z} \tag{4.1.}
\end{cases}
$$

上述解表明磁场在$x$方向，扰动在垂直于磁场的方向，波的传播方向为$x$方向，所以这种波动模式是横波。它的传播速度

$$
v_\mathrm{A} = \frac{\omega_0}{k} = \pm u_0 = \pm \frac{B_0}{\sqrt{\mu_0 \rho_0}} \tag{4.1.}
$$

其中$B_0$越大意味着磁场张力的“恢复力”越大，使波动传播越快；而$\rho_0$越大表示运动物质的惯性越大，它无疑将滞迟波动的传播。这种波动是存在磁场时导电流体中所特有的一种波动，被命名为Alfvén波。由(4.1-15)式可知，这种波动模式中压强、密度和嫡均无扰动，即在这种模式的波动中可压流体与不可压流体的作用完全相同，扰动的传播都是由磁张力所引起的。(4.1-16)式所示的波的相速度$v_\mathrm{A}$称为(剪切)Alfvén波速，通常把Alfvén波速看成是磁流体中的一个特征速度。

当传播方向$\bm{k}$与磁场有一夹角$\theta$时，代入方程组$(4.1.)$可得：

$$
\begin{cases}
u_\mathrm{1x} = u_\mathrm{1z} = v_\mathrm{1x} = v_\mathrm{1z} = p_1 = \rho_1 = S_1 = 0 \\
u_\mathrm{1y} = \pm v_\mathrm{1y} \tag{4.1.}
\end{cases}
$$

由上式所确定的波动，其基本模式与(4.1-15)式的阿尔文波相同，通常将它命名为斜Alfvén波。(4.1-13)式显示，斜阿尔文波的传播是各向异性的，波速与磁场和波矢$\bm{k}$的夹角有关。沿磁场方向传播时波速最大，这就是通常的Alfvén波；随着与磁场方向偏离的增大而波速越来越小；在与磁场垂直的方向上没有斜Alfvén波传播。

### 4.1.3 磁声波 (Magnetosonic Wave)

色散关系$(4.1.)$式的还有一组解为：

$$
\omega_0^4 - k^2 (c_\mathrm{s}^2 + u_0^2) \omega_0^2 +  k^2 c_\mathrm{s}^2 (k u_0 \cos \theta)^2 = 0 \tag{4.1.}
$$

解上式可得扰动传播的速度为

$$
c_\mathrm{M\pm}^2 = \frac{\omega^2}{k^2} = \frac{1}{2} \left[ c_\mathrm{s}^2 + u_0^2 \pm \sqrt{(c_\mathrm{s}^2 + u_0^2)^2 - 4 c_\mathrm{s}^2 u_0^2 \cos^2 \theta} \right] \tag{4.1.}
$$

上式给出了两种波动模式，其中取正号的称为**快磁声波**(fast magnetosonic wave)，而取负号的称为**慢磁声波**(slow magnetosonic wave)。显然快慢磁声波的相速度是各向异性的，波速与磁场和波矢$\bm{k}$的夹角有关。下面就扰动传播方向与磁场方向之间的几种不同夹角分别进行讨论。

#### 4.1.3.1

当$\theta = 0$，即扰动随磁场传播时，$(4.1.)$式变为

$$
c_\mathrm{M\pm}^2 = \frac{\omega_0^2}{k^2} = \frac{1}{2} \left( c_\mathrm{s}^2 + u_0^2 \pm |c_\mathrm{s}^2 - u_0^2| \right) \tag{4.1.}
$$

即

$$
\begin{cases}
c_\mathrm{M+} = \max(c_\mathrm{s}, u_0) \\
c_\mathrm{M-} = \min(c_\mathrm{s}, u_0) \tag{4.1.}
\end{cases}
$$

将上式代入方程组中，当$c_\mathrm{M} = c_\mathrm{s}$时可得

$$
\begin{cases}
u_\mathrm{1x} = u_\mathrm{1y} = u_\mathrm{1z} = v_\mathrm{1y} = v_\mathrm{1z} = S_1 = 0 \\
\displaystyle v_\mathrm{1x} = \frac{\rho_1}{\rho_0} c_\mathrm{s} \\
p_1 = c_\mathrm{s}^2 \rho_1 \tag{4.1.}
\end{cases}
$$

上式所描述的是由磁流体密度的疏密扰动引起并由热压力驱动而形成的纵波，即其传播方向和流体元扰动的方向一致，其图像与声波十分相像，因电子和离子的分离很小，可以认为电子和离子基本上粘合在一起运动，而离子所受的恢复力除热压强外，显然还有由于电荷分离而引起的静电力(尽管电子和离子分离小，但其因分离而引起的静电力却与热压强相当)，这不同于仅受热压强作用的声波，它叫作离子声波。声波的传播仅仅由于中性质点间的碰撞，而离子声波中驱动波所需的位能，除来源于离子之间的热运动外，还来源于静电能，它由电子振荡与离子振荡的振幅差所产生。在无碰撞等离子体中，离子声波的传播则全靠静电力。

## 4.2 阻尼Alfvén波 (Damped Alfvén Wave)

## 4.3 简单波 (Simple Wave)
