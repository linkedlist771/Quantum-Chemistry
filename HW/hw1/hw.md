​                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     

# 量子化学作业-**1**

**作者**：丁力-202328015926048  

# 第一章

## 1.1 考虑一量子数为 $n$ 在长 $l$ 的一维箱中运动的粒子
- (a) 求在箱的左端 $1 / 4$ 区找到粒子的几率

> 从课本中，可以知道， 该量子数为n在长l的箱中的例子的波函数为：
> $$
> \psi_n(x)= \begin{cases}\left(\frac{2}{l}\right)^{1 / 2} \sin \frac{n \pi}{l} x, & 0<x<l \\ 0, & x \leqslant 0, x \geqslant l\end{cases}z
> $$
> 由波函数的定义，为了求得在箱子左端1/4的概率，直接进行积分便可以得到：
> $$
> \begin{align}
> P &= \int_{0}^{\frac{l}{4}} \mid \psi_{n}(x)\mid^2 dx\\
> &=  \int_{0}^{\frac{l}{4}} \mid \left(\frac{2}{l}\right)^{1 / 2} \sin \frac{n \pi}{l} x\mid^2 dx\\
> &=\int_0^{\frac{l}{4}} \frac{2}{l}(\sin (\frac{n \pi}{l} x))^2dx\\
> &= \frac{1}{4}-\frac{\sin(\frac{n\pi}{2})}{2n\pi}
> \end{align}
> $$
>

- (b) $n$ 为何值时此几率最大

> 为了求得几率最大对应的$n$,也就是求$\psi^2$的对应的最大的n，其实我们只用求$\psi$对应的最大的n即可，我们不妨画出$n=1,2....,n$对应的图，如下所示:
>
> ![image-20230923190346519](../../../../../AppData/Roaming/Typora/typora-user-images/image-20230923190346519.png)
>
> 很容易判断`n=3`时，其对应的概率最大，现在，对其进行证明，
>
> #### 情况 1：$ n $ 为偶数
> 当 $ n $ 为偶数时，有 $ \sin\left(\frac{n\pi}{2}\right) = 0 $，所以：
>
> $$
> f(n) = \frac{1}{4}
> $$
>
> #### 情况 2：$ n $ 为奇数
> 1. 子情况 1：$ n $ 是 4 的倍数加 1（即 $ n = 4k + 1 $，其中 $ k $ 是非负整数）
>    
>    这时，$ \sin\left(\frac{n\pi}{2}\right) = 1 $，所以：
>    
> $$
> f(n) = \frac{1}{4} - \frac{1}{2n\pi}
> $$
>
> 2. 子情况 2：$ n $ 是 4 的倍数加 3（即 $ n = 4k + 3 $，其中 $ k $ 是非负整数）
>
>    这时，$ \sin\left(\frac{n\pi}{2}\right) = -1 $，所以：
>    
> $$
> f(n) = \frac{1}{4} + \frac{1}{2n\pi}
> $$
>
> ### 找出最大值
> 通过比较各个情况，我们可以看到在 $ n $ 为奇数且是 4 的倍数加 3 时（即 $ n = 4k + 3 $），函数 $ f(n) $ 会取得相对较大的值：
>
> $$
> f(n) = \frac{1}{4} + \frac{1}{2n\pi}
> $$
>
> 因为 $ \frac{1}{2n\pi} $ 是一个随 $ n $ 增加而减小的项，所以 $ f(n) $ 在 $ n $ 最小（即 $ n=3 $）时取得最大值。
>

## 1.2 对于在长 $l$ 的一维箱中的粒子
可将坐标原点放在箱的中点。求如此选择原点时的波函数和能级。

> 此时，求解波函数的过程基本和坐标原点在边缘处相同，只是此时的波函数变为：
> $$
> V(x) =\begin{cases}
> \infty, x<-\frac{l}{2}\or x>\frac{l}{2}\\
> 0,-\frac{l}{2}\leq x\leq \frac{l}{2}
> 
> \end{cases}
> $$
> 此时，波函数的形式依然不变，只是边界条件发生了改变，也就是：
> $$
> \begin{align}
> &\psi(x)\mid_{x=\pm \frac{l}{2}} = 0 \\
> &A\sin(k\frac{l}{2})+B\cos(k\frac{l}{2})=0\and A\sin(-k\frac{l}{2})+B\cos(-k\frac{l}{2})=0\\
> &
> \end{align}
> $$
> 也就是得到：
> $$
> \begin{cases}
> A=0\\
> B\neq0\\
> \cos(\frac{kl}{2})=0
> \end{cases}或
> \begin{cases}
> A\neq0\\
> B=0\\
> \sin(\frac{kl}{2})=0
> \end{cases}
> $$
> 分别解得：
> $$
> \begin{cases}
> A=0\\
> B\neq0\\
> k=\frac{(2n+1)\pi}{l}
> \end{cases}或
> \begin{cases}
> A\neq0\\
> B=0\\
> k=\frac{2n\pi}{l}
> \end{cases}
> ,其中n\in N
> $$
> 得到的波函数为：
> $$
> \psi = A\sin(\frac{2n\pi x}{l}) 或B\cos(\frac{(2n+1)\pi x}{l})
> $$
> 不难看出，这两个解是相同的，所以我们只取正弦的表达形式即可, 又由波函数的归一化性质，我们可以得到：
> $$
> \int_{-\frac{l}{2}}^{\frac{l}{2}}|\psi|^2dx  = \int_{-\frac{l}{2}}^{\frac{l}{2}}| A\sin(\frac{2n\pi x}{l})|^2dx  = 1\rightarrow A= \sqrt{\frac{2}{l}}
> $$
> 所以我们求得此时的波函数为:
> $$
> \psi(x) = \begin{cases}
> \infty, x<-\frac{l}{2}\or x>\frac{l}{2}\\
> \sqrt{\frac{2}{l}}\sin(\frac{2n\pi x}{l}),-\frac{l}{2}\leq x\leq \frac{l}{2}
> \end{cases}
> $$
> 然后我们来求解能级：
> $$
> \frac{2mE}{\hbar^2} = k^2 = \frac{4n^2\pi^2}{l^2} \rightarrow E = \frac{2n^2\pi^2\hbar^2}{ml^2}
> $$
> 

## 1.3 三维谐振子的势能函数
$V=\frac{1}{2} k_x x^2+\frac{1}{2} k_y y^2+\frac{1}{2} k_z z^2$, 这些 $k$ 是三个力常数。解薛定谔方程求能量本征值。

> 将该势能场带入薛定谔方程，可以得到:
> $$
> -\frac{\hbar^2}{2m}\nabla ^2\psi +(\frac{1}{2} k_x x^2+\frac{1}{2} k_y y^2+\frac{1}{2} k_z z^2)\psi = E\psi
> $$
> 这是因为势能函数$V$是三个独立变量 $x,y,z$ 的函数，并且它们之间是可加的, 所以，我们可以将波函数分离变量为:
> $$
> \psi(x,y,z) = X(x)Y(y)Z(z)
> $$
> 那么，上述薛定谔方程可以变为：
> $$
> (-\frac{\hbar^2}{2m}\frac{\partial^2 \psi}{\partial x^2}+\frac{1}{2} k_x x^2\psi)+ 
> (-\frac{\hbar^2}{2m}\frac{\partial^2 \psi}{\partial y^2}+\frac{1}{2} k_y y^2\psi)+ 
> (-\frac{\hbar^2}{2m}\frac{\partial^2 \psi}{\partial z^2}+\frac{1}{2} k_z z^2\psi)
> = E\psi
> $$
> 然后我们这里也可以将能量分解为三个：
> $$
> E=E_x+E_y+E_z
> $$
> 那么上式可以分解为：
> $$
> \begin{cases}
> (-\frac{\hbar^2}{2m}\frac{\partial^2 \psi}{\partial x^2}+\frac{1}{2} k_x x^2\psi) = E_x\psi \\
> (-\frac{\hbar^2}{2m}\frac{\partial^2 \psi}{\partial y^2}+\frac{1}{2} k_y y^2\psi) = E_y\psi \\
> (-\frac{\hbar^2}{2m}\frac{\partial^2 \psi}{\partial z^2}+\frac{1}{2} k_z z^2\psi)  = E_z\psi\\
> \end{cases}
> $$
> 可以看出，这三个分别是三个维度的一维谐振子的薛定谔方程，所以根据一维谐振子的能量结果，我们可以得到：
> $$
> \begin{cases}
> E_x= (n_x+\frac{1}{2})\hbar \sqrt{\frac{k_x}{m}} \\
>  E_y=( n_y+\frac{1}{2} )\hbar \sqrt{\frac{k_y}{m}} \\
>  E_z=( n_z+\frac{1}{2})\hbar \sqrt{\frac{k_Z}{m}}  \\
> \end{cases}
> $$
> 所以，现在可以求得体系的本征值为:
>
> 
> $$
> E = (n_x + \frac{1}{2})\hbar\sqrt{\frac{k_x}{m}} + (n_y + \frac{1}{2})\hbar\sqrt{\frac{k_y}{m}} + (n_z + \frac{1}{2})\hbar\sqrt{\frac{k_z}{m}}
> $$
> 这里，$n_x, n_y, n_z $ 是各个方向上的量子数，可以是任何非负整数（包括零）。

## 1.4 一个一维体系有
$V(x)=\infty, \quad x<0$  
$V(x)=\frac{1}{2} k x^2, x \geqslant 0$  
求 $H$ 的本征值和本征函数。

>不难看出，这个势能场为半空间谐振子。
>
>其对应的薛定谔方程为:
>$$
>-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} + V\psi = E\psi
>$$
>$x<0$时，此时$V=\infty$：
>$$
>\psi =0
>$$
>$x\geq 0$时，$V = \frac{kx^2}{2}$：
>$$
>-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} +  \frac{kx^2}{2}\psi = E\psi
>$$
>也就是：
>$$
>\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} +  (E-\frac{kx^2}{2})\psi = 0
>$$
>此时为一般的一维谐振子的情况，我们可以得到此时的波函数：
>$$
>\psi(x) =\left(\frac{m \omega}{\pi \hbar}\right)^{1 / 4} \frac{1}{\sqrt{2^n n !}} H_n(\xi) e^{-\xi^2 / 2}
>$$
>
>其中，$H_n(\xi)$ 为 `Hermite多项式` ：
>$$
>\begin{align*}
>H_0(\xi) &= 1 \\
>H_1(\xi) &= 2\xi \\
>H_2(\xi) &= 4\xi^2 - 2 \\
>H_3(\xi) &= 8\xi^3 - 12\xi \\
>H_{n+1}(x) &= 2x H_n(x) - 2n H_{n-1}(x)\\
>\end{align*}
>$$
>其中，$\xi \equiv \sqrt{\frac{m \omega}{\hbar}} x$ ，但是这里为半空间谐振子，所以其对应的波函数为：
>$$
>\psi(x) = \begin{cases}
>\left(\frac{m \omega}{\pi \hbar}\right)^{1 / 4} \frac{1}{\sqrt{2^n n !}} H_n(\xi) e^{-\xi^2 / 2}, x>0\\
>0, x\leq 0
>\end{cases}
>$$
>由题意可知，此时:
>$$
>\psi(0) = 0
>$$
>对于 `Hermite多项式`，n为奇数的时候， 其为奇函数， n为偶数的时候，其为偶函数，但是$\psi(0)=0$,所以，此时 `Hermite多项式`只能取奇数项，也就是说
>
>此时的波函数为：
>$$
>\psi(x) = \begin{cases}
>\left(\frac{m \omega}{\pi \hbar}\right)^{1 / 4} \frac{1}{\sqrt{2^{2n-1} ({2n-1}) !}} H_{2n-1}(\xi) e^{-\xi^2 / 2}, x>0\\
>0, x\leq 0
>\end{cases}
>$$
>其对应的本征值为：
>$$
>E= (\frac{1}{2}+(2n-1))\hbar\sqrt{\frac{k}{m}} =  ( 2n-\frac{1}{2})\hbar\sqrt{\frac{k}{m}}, n \in N^*
>$$
>

