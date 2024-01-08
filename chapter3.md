# Chapter 3: 磁流体静力学 (Magnetohydrostatistics)

## 3.1 磁流体静平衡方程组及其性质

考虑仅有磁场力和压力时的静平衡态，由方程组$(2.5.1)$知此时磁流体应满足

$$
\begin{align}
& \nabla p = \bm{j} \times \bm{B} \tag{3.1.1} \\
& \bm{j} = \frac{1}{\mu_0} \nabla \times \bm{B} \tag{3.1.2} \\
& \nabla \cdot \bm{B} = 0 \tag{3.1.3}
\end{align}
$$

由向量公式可推得

$$
\begin{align}
\nabla p & = \frac{1}{\mu_0} (\bm{B} \cdot \nabla) \bm{B} - \nabla (\frac{B^2}{2 \mu_0}) \nonumber \\
& = \frac{1}{\mu_0} [(\bm{B} \cdot \nabla) \bm{B} - B \nabla B] \tag{3.1.4} \\
\nabla & \times (\bm{B} \cdot \nabla) \bm{B} = 0 \tag{3.1.5}
\end{align}
$$

因此可由$(3.1.3)$和$(3.1.5)$式解得磁场的静平衡位形；注意，解不一定是唯一的，它们给出了各种可能的位形。然后再将它(们)代入$(3.1.2)$和$(3.1.4)$式中，分别得到磁流体静平衡态时的电流分布和压强分布。由$(3.1.1)$式可得

$$
\begin{align}
\bm{B} \cdot \nabla p = 0 \nonumber \\
\bm{j} \cdot \nabla p = 0 \nonumber
\end{align}
$$

上式表明$\bm{B}, \bm{j}$均位于磁流体的等压面上。如果等压面是封闭的，则磁力线及电流线缠绕在该曲面上，绝不可能由磁力线和电流线穿越等压面的情况发生。通常电流线可以以任意角度与磁力线相交。在等压面上，除了$p$为常数，磁通量$\Phi$和电流$\bm{j}$也是常数。

## 3.2 无作用力场 (Force-Free Field)

当等离子体$\beta$值很小时，磁力处于主导地位，没有其它力可以与之平衡。为使系统平衡，必须要求磁力为0。这种磁场被称作无作用力场。

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

### 3.2.1 无电流场 / 势场 (Current-Free Field / Potential Field)

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

### 3.2.2 线性无作用力场 (Linear Force-Free Field)

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

## 3.3 箍缩效应 (Pinch Effect)

箍缩效应是等离子体所特有的一种效应。

### 3.3.1 线箍缩 / z箍缩 (Linear Pinch / Z-Pinch)

在无限长等离子体圆柱中通以轴向电流。由于问题具有轴对称性，选用柱坐标系。取对称轴为$z$轴，$\bm{j} = j_z (\rho) \bm{k}$的轴向电流将激发绕等离子体的环向磁场$\bm{B} = B_\varphi (\rho) \hat{\varphi}$，如下图所示

![3.3.1](Figures/3.3.1.jpg)

此时磁流体静平衡方程组化为

$$
\begin{cases}
\displaystyle \frac{\mathrm{d} p}{\mathrm{d} \rho} = - j_z B_\varphi \\
\displaystyle j_z = \frac{1}{\mu_0} \frac{1}{\rho} \frac{\mathrm{d}}{\mathrm{d} \rho} (\rho B_\varphi)
\end{cases}
$$

已知径向电流分布$j_z (\rho)$并注意到边界条件$p (a) = 0$后就可求得

$$
\begin{cases}
\displaystyle B_\varphi (\rho) = \frac{\mu_0}{\rho} \int_0^\rho j_z (\rho) \rho \mathrm{d} \rho \\ \\
\displaystyle p (\rho) = \int_\rho^a j_z (\rho) B_\varphi (\rho) \mathrm{d} \rho = \mu_0 \int_\rho^a \mathrm{d} \rho \frac{j_z (\rho)}{\rho} \left[ \int_0^\rho j_z (\rho) \rho \mathrm{d} \rho \right] \tag{3.3.1}
\end{cases}
$$

若柱内电流密度为常数，即

$$
j_z (\rho) = \begin{cases}
j_0 & \rho < a \\
0 & \rho \geqslant a
\end{cases}
$$

将上式代入$(3.3.1)$式得

$$
\begin{cases}

\end{cases}
$$

$j_z$、$B_\varphi$和$p$的径向分布如下图所示

## 3.5