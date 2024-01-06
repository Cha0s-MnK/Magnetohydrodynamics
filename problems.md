# Problems

## 1.1

求下列条件下带电粒子的回旋半径和回旋频率：
(1) $0.5 \ \mathrm{G}$磁场中，能量为 $10 \ \mathrm{keV}$的质子；
(2) 磁场强度为$5 \times 10^{-5} \ \mathrm{G}$，速度为 $300 \ \mathrm{km} \cdot \mathrm{s}^{-1}$ 太阳风中的电子。

## 1.2

在下列条件下，求Debye长度$\lambda_\mathrm{D}$，等离子体振荡频率$\omega_\mathrm{p}$以及线频率$f_\mathrm{p}$：
(1) 地磁层，$n_\mathrm{e} \approx n_\mathrm{i} = 10^4 \ \mathrm{cm}^{-3}$，$T_\mathrm{e} \approx T_\mathrm{i} = 10^3 \ \mathrm{K}$；
(2) 日冕，$n_\mathrm{e} \approx n_\mathrm{i} = 10^8 \ \mathrm{cm}^{-3}$，$T_\mathrm{e} \approx T_\mathrm{i} = 10^6 \ \mathrm{K}$。

## 2.1

试推导考虑磁力的动量方程的守恒形式，其中$\overset{\rightarrow \rightarrow}{\bm{P}}$为应力张量:

$$
\frac{\partial(\rho \bm{v})}{\partial t} = -\nabla \cdot (\rho \bm{v} \bm{v} - \overset{\rightarrow \rightarrow}{\bm{P}} - \frac{\bm{B} \bm{B}}{\mu_0} + \frac{B^2}{2\mu_0} \bm{I})
$$

## 2.2

证明当热流$\bm{q} = 0$，无焦耳耗散，且$\overset{\rightarrow \rightarrow}{\bm{P}} = −p \overset{\rightarrow \rightarrow}{\bm{I}}$时，能量方程

$$
\rho \frac{\mathrm{d}}{\mathrm{d} t} \left( u + \frac{v^2}{2} \right) = \nabla \cdot (\overset{\rightarrow \rightarrow}{\bm{P}} \cdot \bm{v}) + \bm{E} \cdot \bm{j} - \nabla \cdot \bm{q}
$$

变为绝热方程

$$
\frac{\mathrm{d}}{\mathrm{d} t} \left( \frac{p}{\rho^\gamma} \right) = 0
$$

## 2.3

根据一维磁扩散方程

$$
\frac{\partial B}{\partial t} = \eta_\mathrm{m} \frac{\partial^2 B}{\partial x^2}
$$

的形式解，推导当初始条件为 $\eta_m$ 情况下，

$$
B(x,0) =
\begin{cases}
    B_0, & x > 0 \\
    0, & x = 0 \\
    -B_0, & x < 0
\end{cases}
$$

时，上述一维磁扩散方程的解为

$$
B(x, t) = \frac{2 B_0}{\sqrt{\pi}} \int_0^{\frac{x}{2 \sqrt{\eta_\mathrm{m} t}}} e^{-\alpha^2} \mathrm{d} \alpha
$$

## 3.1

试判别下列磁场是否是无作用力场？如果是，则是何种无作用力场?
(1)

$$
\begin{align}
B_\rho & = \frac{l}{k} B_0 J_1 (k \rho) \exp(-lz) \nonumber \\
B_\varphi & = \sqrt{1 - \frac{l^2}{k^2}} B_0 J_1 (k \rho) \exp(-lz) \nonumber \\
B_z & = B_0 J_0 (k \rho) \exp(-lz) \nonumber
\end{align}
$$

其中$k, l$为常数。
(2)

$$
\begin{align}
& B_\rho = 0 \nonumber \\
& B_\varphi = \frac{b \rho B_0}{1 + b^2 \rho^2} \nonumber \\
& B_z = \frac{B_0}{1 + b^2 \rho^2} \nonumber
\end{align}
$$

其中$B_0, b$为常数。

## 3.2

(1) 证明对于无作用力场，有下式成立：

$$
(\nabla^2 + \alpha^2) \bm{B} = \bm{B} \times \nabla \alpha
$$

(2) 判断如果上式成立，所对应的磁场是否一定为无作用力场？

## 3.3

对于一磁静力平衡位型，请证明
(1) $\nabla \cdot (\bm{B} \times \nabla p) = 0$；
(2) $(\bm{j} \cdot \nabla) \bm{B} = (\bm{B} \cdot \nabla) \bm{j}$。

## 4.1

设日冕由纯氢($\mathrm{H}$)大气组成，其温度为$1 \ \mathrm{MK}$，电子数密度为$3 \times 10^8 \ \mathrm{cm^{-3}}$，磁场为$5 \ \mathrm{G}$。请计算在上述特征参量下日冕中的声速、Alfvén速度以及等离子体$\beta$值(取$\gamma = 5/3$)。

## 4.2

在上述均匀日冕大气中激发一小扰动，请说明在平行磁场、垂直磁场及与磁场成$45^\circ$三个方向上各自能接收到什么波，并计算波动传播的速度。

## 4.3

对于MHD激波，可定义Alfvén马赫数$M_\mathrm{A1} = v_1 / v_\mathrm{A1}$，其中$v_1$和$v_\mathrm{A1}$分别为激波上游流速和Alfvén速度。请分别在垂直激波和平行激波位型下用激波压缩比(X)、上游等离子体$\beta$值($\beta_1$)等无量纲量表出$M_\mathrm{A1}$。

## 5.1

重力场下扰动速度方程写成

$$
\rho_0 \frac{\partial \bm{v}_1}{\partial t} = - \nabla p_1 + \frac{1}{\mu_0} \left[ (\nabla \times \bm{B}_1) \times \bm{B}_0 + (\nabla \times \bm{B}_0) \times \bm{B}_1 \right] + \rho_1 \bm{g}
$$

设系统平衡位型为

$$
\begin{cases}
\bm{B}_0 = \left( B_0 (z), 0, 0 \right) \\
p_0 = p_0 (z) \\
\rho_0 = \rho_0 (z)
\end{cases}
$$

(1) 证明当扰动取

$$
Q_1 (x, y, z, t) = \bar{Q}_1 (z) e^{i(ky − \omega t)}
$$

的形式时, 扰动速度方程各分量为

$$
\begin{cases}
\displaystyle -i \omega \rho_0 v_\mathrm{1x} = \frac{B_\mathrm{1z}}{\mu_0} \frac{\mathrm{d} B_0 (z)}{\mathrm{d} z} \\
\displaystyle -i\omega \rho_0 v_\mathrm{1y} = -i k \left(p_1 + \frac{B_0 B_\mathrm{1x}}{\mu_0} \right) \\
\displaystyle -i\omega \rho_0 v_\mathrm{1z} = -\frac{\mathrm{d}}{\mathrm{d} z} \left(p_1 + \frac{B_0 B_\mathrm{1x}}{\mu_0} \right) - \rho_1 g
\end{cases}
$$

(2) 证明当波数$k \rightarrow + \infty$时，$z$方向扰动速度方程可简化为

$$
i \omega \rho_0 v_\mathrm{1z} = \rho_1 g
$$