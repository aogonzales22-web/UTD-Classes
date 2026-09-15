## Modeling in the frequncy domain
- Start with a differential equation using first principles/laws
	- Electric Circuits (Ohm's Law, KCL, KVL, ...)
	- Mechanical Systems (Newtons Laws of motion)
	- $N^{th}$ order differential equations $\to\text{ Laplace Transform }\to\text{Transfer function}$ 
**diagram 1**

$G(s)$ describes the system in the frequency domain. $Y(s)=\mathcal{L}[y(t)]= \int^{\infty}_{0}y(t)e^{-st}dt$   $X(s)=L[s(t)]$
Let $g(t)$ be the response of the system to an impulse 
$$
\delta (t)= 
$$

$$
\int^{\infty}_{-\infty}\delta(t)dt=1
$$
Linearity $\alpha x_{1}+\beta x_{2}$  Time invariance $\delta(t)\to y(t)$, $\delta(t-\tau)\to g(t-\tau)$

$$
x(t)=\int^{\infty}_{0}x(\tau)\delta(t-\tau)d\tau
$$

$$
y(t)=\int^{\infty}_{0}x(\tau)g(t-\tau)d\tau=x(t)*g(t)
$$

$$
Y(s)=\mathcal{L}(y(t))=\int^{\infty}_{0}y(t)e^{-st}dt=\int^{\infty}_{0}x(\tau)e^{-s\tau}d\tau=G(s)X(s)
$$
$G(s)$ is the impulse response of the system in the frequency domain.
$Y(s)\to y(t)=\mathcal{L}^{-1}[Y(s)]$ Too hand!
Use partial fraction decomposition to get inverse Laplace transform of simpler functions.
$$
Y(s)=Y_{1}(s)+Y_{2}(s)+\dots Y_{n}(s)\to y(t)=y_{1}(t)+y_{2}(t)+\dots y_{n}(t)
$$
1. $x(t)=\delta(t)\to X(s)=\int^{\infty}_{0^-}\delta e^{-st}dt=-e^{-st}|_{t=0}=1$
2. $u(t)=\begin{cases}1 & t\geq 0 \\  0 & t< 0\end{cases}\to X(s)=\int^{\infty}_{0}u(t)e^{-st}dt=-\frac{1}{s}e^{-st}|^{\infty}_{0}=\frac{1}{s}$
3. $x(t)=e^{-at}\to X(s)=\frac{1}{s+a}$
4. $Y(s)=\mathcal{L}[y(t)]\to\mathcal{L}\left( \frac{dy}{dt} \right)=sY(s)$ if initial conditions are zero
5. $\mathcal{L}\left( \frac{d^2y}{dt} \right)=s^2Y(s)$ for zero initial conditions
### Example:
What is the unit step response of a system described by:
$$
y'(t)+y(t)=u(t)
$$
Taking Laplace Transform on both sides
$sY(s)+Y(s)=U(s)=\frac{1}{s}\to G(s)=\frac{Y(s)}{U(s)}=\frac{1}{s+1}$
$Y(s)=\frac{1}{s(s+1)}$
$Y(s)=\frac{A}{s}+\frac{B}{s+1}=\frac{1}{s(s+1)}; A=Y(s)s|_{s=0}=1; B=(s+1)Y(s)|_{s=1}=-1$
$Y(s)=\frac{1}{s}-\frac{1}{s+1}$
$y(t)+u(t)-e^{-t}u(t)=u(t)[1-e^{-t}]$
In general $Y(s)=\frac{N(s)}{D(s)}=\frac{N(s)}{(s-s_{1})(s-s_{2})(\dots)}=\frac{A}{(s-s_{1})}+\frac{B}{(s-s_{2})}+\dots$
Multiply both sides by $D(s):N(s)=\frac{D(s)A}{s-s_{1}}+\frac{D(s)B}{s-s_{2}}+\dots$
Equate the coefficient of all powers of s 

### Example
For $f(t)=te^{-st},$ Find $F(s)$

$$
x(t)=\frac{t\to\mathcal{L}\to_{1}}{s^2}X(s)\text{ and }\mathcal{L}[e^{-st}x(t)]=X(s+a)
$$

$$
x(t)=t\text{ and }a=+5\to F(s)=\frac{1}{(s+5)^2}
$$
### Example
For $F(s)=\frac{10}{s(s+2)(s+3)^2}=$, Find $f(t)$
1. Decompose $F(s)=\frac{A}{s}+\frac{B}{s+2}+\frac{C}{s+3}+\frac{D}{(s+3)^2}$
2. 