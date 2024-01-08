# Chapter 6: 理想磁流体力学不稳定性

一个磁流体体系在达到平衡态后仍可以有偏离平衡值的扰动存在。对处在热平衡态附近的磁流体体系来说，这种扰动一般是局部的、无规的、随机的，其扰动振幅在热涨落的水平，此种扰动的传播即为Chapter 4所讨论的磁流体波。当磁流体处于力学平衡状态但处于非热力学平衡态时，其内部存在着一定数量的自由能。在一定的物理条件下，它能以快速变化的形式发展成为在大范围、长时间、能量超过热噪声水平的大幅度集体运动，这种集体运动就称为不稳定的模式。由于它常用磁流体力学方程进行处理，故相应的现象通常称为磁流体力学不稳定性。

不稳定性过程的特点是任何偏离力学平衡的小扰动都将导致系统更进一步偏离平衡
状态，最后使平衡态被彻底破坏。每种不稳定的扰动在其演化过程中都会依次经历三个
阶段：线性阶段、非线性阶段及饱和阶段。本章只讨论磁流体的线性不稳定性。用数学语
言来讲，若用$x$表示偏离，上述过程便意味着$x$随时间的变化可以用线性微分方程表述

$$
\frac{\mathrm{d}^2 x}{\mathrm{d} t^2} = \kappa \tag{6.1.1}
$$

如果$\kappa$是正实数，解上式可得

$$
x = x_0 e^{\pm \sqrt{\kappa} t}
$$

这表明偏离可以以指数形式增长。这样的平衡态是不稳定的。如果$\kappa$是负实数，那么$(6.1.1)$式的解是

$$
x = x_0 \cos (\sqrt{- \kappa} t + \varphi)
$$

其中$\omega = \sqrt{- \kappa}$。系统在平衡态附近小幅振荡而不会继续偏离平衡态。这样的平衡是稳定平衡。研究给予平衡位形以某种形式的扰动后，作用于磁流体上力的变化。微扰破坏平衡条件，产生净作用力，如果这个力的方向和微扰方向相反，则微扰产生的力是回复力(即指向平衡位置)，系统对微扰是稳定的；反之，如果力和微扰同向，则会进一步促进扰动，因而系统线性不稳定。这种分析方法只能应用于一些相对简单或特殊的平衡位形。

考虑重力时，理想磁流体力学基本方程组为

$$
\begin{cases}
\displaystyle \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \bm{v}) = 0 \\ \\
\displaystyle \rho \frac{\mathrm{d} \bm{v}}{\mathrm{d} t} = -\nabla p + \bm{j} \times \bm{B} - \rho \nabla \varPhi_\mathrm{g} \\ \\
\displaystyle \frac{\mathrm{d}}{\mathrm{d} t} \left( \frac{p}{\rho^\gamma} \right) = 0 \\ \\
\displaystyle \frac{\partial \bm{B}}{\partial t} = \nabla \times (\bm{v} \times \bm{B}) \\ \\
\nabla \times \bm{B} = \mu_0 \bm{j} \\ \\
\nabla \cdot \bm{B} = 0
\end{cases}
$$

其中重力加速度$\bm{g} = - \nabla \varPhi_\mathrm{g}$。

## 6.3 Rayleigh-Taylor不稳定性

重力场中轻流体支撑重流体的平衡位形是不稳定的，人们将这类不稳定性称作Rayleigh-Taylor不稳定性。宇宙等离子体中，考虑引力(重力)的作用具有普遍性，在许多情况下它具有重要意义。当宇宙等离子体的密度梯度方向与重力方向相反时，或者在重力场中密度较小的二种磁流体支托另一种密度大的磁流体时，这类平衡经常是不稳定的。由于磁场的存在，电磁力与重力同时对磁流体作用，使稳定性问题更复杂。

### 6.3.1 流体力学中的Rayleigh-Taylor不稳定性

流体力学中的Rayleigh-Taylor不稳定性研究的是重力场中两种密度不同的流体边界面的稳定性问题。

如下图所示，重力场中存在两种密度不同而处于平衡状态的流体：一种流体(下标为1)位于$Oxy$平面之上，另一种流体(下标为2)位于$Oxy$平面之下。重力沿$z$轴向下。下面研究边界面上出现的任何小扰动将如何发展和传播，以及它如何影响边界面两边的流体。

![6.1](Figures/6.1.jpg)

假设流体是理想的，那么理想流体的基本方程组为($i = 1, 2$)

$$
\begin{cases}
\displaystyle \rho_i \frac{\mathrm{d} \bm{v}_i}{\mathrm{d} t} = - \nabla p_i + \rho_i \bm{g} \\
\displaystyle \frac{\partial \rho_i}{\partial t} + \nabla \cdot (\rho_i \bm{v}_i) = 0 \\
\rho_i \bm{g} = - \nabla (\rho_i g z) \tag{6.3.1}
\end{cases}
$$

在小扰动假设下，即当$v_i \ll c_\mathrm{s}$时，可把流体看作是不可压缩的，即

$$
\nabla \cdot \bm{v}_i = 0 \tag{6.3.2}
$$

仅考虑无旋运动，这表明存在速度势函数，即

$$
\begin{align}
\nabla \times \bm{v}_i = 0 \nonumber \\
\Rightarrow \bm{v}_i = \nabla \varphi_i \tag{6.3.3}
\end{align}
$$

假设流体在$y$方向是均匀的，将$(6.3.2)(6.3.3)$式代入方程组$(6.3.1)$可推得

$$
\begin{align}
\displaystyle & \rho_i \frac{\partial \varphi_i}{\partial t} + p_i+ \rho_i g z = 0 \tag{6.3.4} \\
\displaystyle & \frac{\partial^2 \varphi_i}{\partial x^2} + \frac{\partial^2 \varphi_i}{\partial z^2} = 0 \tag{6.3.5}
\end{align}
$$

显然在两种流体的边界面($z = 0$)上应满足

$$
p_1 |_{z = 0} = p_2 |_{z = 0}
$$

由$(6.3.4)$式可推得

$$
\rho_1 \left. \left( \frac{\partial^2 \varphi_1}{\partial t^2} + g \frac{\partial \varphi_1}{\partial z} \right) \right|_{z = 0} = \rho_2 \left. \left( \frac{\partial^2 \varphi_2}{\partial t^2} + g \frac{\partial \varphi_2}{\partial z} \right) \right|_{z = 0} \tag{6.3.6}
$$

且满足

$$
\begin{align}
v_\mathrm{1 z} & = v_\mathrm{2 z} \nonumber \\
\Rightarrow \left. \frac{\partial \varphi_1}{\partial z} \right|_{z = 0} & = \left. \frac{\partial \varphi_2}{\partial z} \right|_{z = 0} \tag{6.3.7}
\end{align}
$$

考虑小扰动为沿$x$方向传播的单色平面波，即

$$
\varphi_i (x, z, t) = A_i (z) e^{i (\omega t - k x)}
$$

将上式代入$(6.3.5)$式，并考虑到边界条件

$$
A_1 (+ \infty) = A_2 (- \infty) = 0
$$

可推得

$$
\begin{cases}
\varphi_1 = C_1 e^{- k z + i (\omega t - k x)} \\
\varphi_2 = C_2 e^{k z + i (\omega t - k x)} \tag{6.3.8}
\end{cases}
$$

将上述解代入衔接条件$(6.3.6)(6.3.7)$式，可得色散关系

$$
\omega^2 = \frac{\rho_2 - \rho_1}{\rho_2 + \rho_1} g k
$$

上式表明，当$\rho_2 > \rho_1$，即密度小的流体位于密度大的流体之上，则$\omega$为实数，解的振幅与时间无关，小扰动不会破坏边界的稳定性。而当$\rho_2 < \rho_1$时，即密度大的流体位于密度小的流体之上时，$\omega$便为虚数，解的振幅将随时间无限增大，直至平衡受到破坏，上下流体互换位置为止。这便是典型的流体力学Rayleigh-Taylor不稳定性。显然，驱动不稳定性发展的能量来自重力势能。这是因为当扰动引起边界上面密度大的流体向下位移时，其势能的减少并不能由边界之下同样体积的小密度流体向上位移来抵偿，部分势能将转化为扰动能，驱使扰动发展，直到整个系统的位能减少到极小状态为止。这就对应于两种流体互换位置，轻流体位于重流体之上的情况。鉴于不稳定性造成的后果是互换位置，所以也把这种不稳定性叫作**互换不稳定性**。上式还表明，当发生不稳定性时，增长率与两种流体密度差的平方根成正比。增长率还与扰动波长的平方根成反比，波长越短，扰动增长越快。

### 6.3.2 磁流体力学中的Rayleigh-Taylor不稳定性

考虑了磁场，同时也考虑了密度的不均匀性，即磁流体是分层的。
考虑如下图所示的简化位形。等离子体中存在着密度梯度$\nabla \rho_0 (z)$，平衡态磁场B。在z- 平面中，其大小和方
向仅随>变化，即