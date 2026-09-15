# Conversion b/w transfer function & State Representations (Sections 3.5, 3.6)

Transfer function to state space (state equations)
$$
F(s)\to |G(s)| \to Y(s) \to \begin{cases}
\vec{x} = {A}\vec{x} +Bf & \text{(State Equation)} \\
y=Cx+df & (\text{Output Equation} )
\end{cases}
$$

$$
\frac{G(s)1}{s^n+a_{n-1}s^{n-1}+\dots a_{1}s+a_{0}}=\frac{Y(s)}{F(s)}\to F(s)=Y(s)[s^n+a_{n-1}s^{n-1}+\dots a_{1}s+a_{0}]
$$

$$
f(t)=y^n+ya_{n-1}y^{n-1}+\dots a_{1}y^1+a_{0}y
$$
In phase variable form, (its the matrix one) also called controllable canonical form, CCF, and it is important in discussing the pole-placement approahc an observable systems design
$$
x_{1}=y_{1}, x_{2}=x_{1}'=y'_{1}, x_{3}=x'_{2}=x_{1}''=y''
$$

$$
x_{n}=x'_{n-1}=y^{n-1}
$$

$$
x'_{n-1}=0x_{1}+\dots +x_{n} 
$$

$$
x'_{n}=y^n=f(t)-a_{n-1}y^{n-1}- \dots -a_{1}y^{1}-a_{0}y
$$

$$
A=\begin{bmatrix}
0 & 1 & 0 & - & - & - & - & 0 \\
0 & 0 & 1 & 0 & - & - & - & 0 \\
\dots \\
-a_{0} & -a_{1} & - & - & - & - & - & a_{n-1}
\end{bmatrix}
$$
## Example
$$
G(s)=\frac{b_{2}s^2+b_{1}s+b_{0}}{s^3+a_{2}s^2+a_{1}s+a_{0}}
$$

$$
N(s)=b_{2}s^2+b_{1}s+b_{0}
$$

$$
G_{D}(s)=s^5+a_{2}s^2+a_{1}s+a_{0}
$$

$$
F(s)=Y_{1}sG_{d}(s)\to f(t)=y'''_{1}+a_{2}y''_{1}+a_{1}y'_{1}+a_{0}y
$$

$$
\begin{cases}
x_{1}'=x_{2} \\
x_{2}'=x_{3} \\
x_{3}'=f(t)-a_{2}x_{3}-a_{1}x_{2}-a_{0}x_{1}
\end{cases}
$$

$$
A=\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
-a_{0} & -a_{1} & -a_{2}
\end{bmatrix}
$$

$$
B=\begin{bmatrix}
0 \\
0 \\
1
\end{bmatrix}
$$

$$
Y(s)=N(s) dotY(s)\to y(t)=b_{2}y''_{1}+b_{1}y'_{1}+b_{2}y_{1}=b_{2}x_{3}+b_{1}x_{2}+b_{0}x_{1}
$$

$$
y(t)=C\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix}
+Df
$$

$$
C=\begin{bmatrix}
b_{0} & b_{1} & b_{0}
\end{bmatrix}
$$

$$
D=0
$$
Apply to $G(s)=\frac{2s+1}{s^2+7s+9}$

$$
A=\begin{bmatrix}
0 & 1 \\
-9 & -7
\end{bmatrix}
, B=\begin{bmatrix}
0 \\
1
\end{bmatrix}, C=\begin{bmatrix}
1 & 2
\end{bmatrix},D=0
$$
State Space to transfer function
$$
\begin{cases}
\bar{x'}=A\bar{x}+Bf \\
y=C\bar{x}+Df
\end{cases}\to G(s)=\frac{Y(s)}{F(s)}
$$
Assuming zero initial conditions, take Laplace transform of the state equations
$$
\begin{cases}
sX(s)=AX(s)+BF(s) \\
Y(s)=CX(s)+DF(s)
\end{cases}\to (sI-A)X(s)=BF(s)
$$
$I$ comes from the identity
$$
X(s)=(sI-A)^{-1}BF(s)
$$

$$
Y(s)=C(sI-A^{-1})BF(s)+DF(s)
$$

$$
G(s)=\frac{Y(s)}{F(s)}=C(sI-A)^{-1}B+D
$$

$$
[sI-A]^{-1}=\frac{Adj(sI-A)}{\det(sI-A)}
$$
Remember that rule
$$
Q\to Q^{-1}=\frac{Adj(Q)}{\det(0)}, Adj(Q)=[C_{ij}]^T,C_{ij}=(-1)^{i+j}M_{ij}, M_{ij}=\det(Q'),Q'=\text{Mtarix Q w/ i row and jth column removed}
$$

Continuing on
$$
G(s)=C\frac{Adj(sI-A)B}{\det(sI-A)}+D
$$

$$
G_{D}(s)=\frac{N(s)}{G(s)}=\det(sI-A):\text{Roots of $G_{d}(s) $ are the e-values of A= Poles of G(s)}
$$
Roots of N(s) are the zeros of G(s)
## Example
Given A, B, C of a system w/ output y and input f, find $G(s)=\frac{Y(s)}{F(s)}$

$$
A=\begin{bmatrix}
0 & 1 \\
-8 & -3
\end{bmatrix},B=\begin{bmatrix}
2 \\
3
\end{bmatrix},C=\begin{bmatrix}
4 & 6
\end{bmatrix}
$$

$$
G(s)=\frac{CAdj(sI-A)B}{\det(sI-A)}
$$

$$
[sI-A]=\begin{bmatrix}
s & -1 \\
8 & s=3
\end{bmatrix}
$$

$$
\det(sI-A)=s(s+3)+8=s^2+3s+8
$$


$$
Adj(sI-A)=\begin{bmatrix}
s+3 & -8 \\
1 & s
\end{bmatrix}^T=\begin{bmatrix}
s+3 & 1 \\
-8 & s
\end{bmatrix}
$$

$$
N(s)=\begin{bmatrix}
4 & 6
\end{bmatrix}\begin{bmatrix}
s+3 & 1 \\
-8 & s
\end{bmatrix}\begin{bmatrix}
2 \\
3
\end{bmatrix}=\begin{bmatrix}
4 & 6
\end{bmatrix}\begin{bmatrix}
2(s+3)+3 \\
2(-8)+3s
\end{bmatrix}=4(2s+9)+6(-16+3s)=26s-60
$$

$$
G(s)=\frac{26s-60}{s^2+3s+8}
$$
## Example
Convert the state and output equations shown below to a transfer function
$$
\dot{x}=\begin{bmatrix}
-4 & -1.5 \\
4 & 0
\end{bmatrix}x+\begin{bmatrix}
2 \\
0
\end{bmatrix}u(t)
$$

$$
y=\begin{bmatrix}
1.5 & 0.625 
\end{bmatrix}x
$$
### Answer
#### Notes
Main formula for this process
$$
G(s)=\frac{Y(s)}{F(s)}=C(sI-A)^{-1}B+D
$$


In dynamic systems and control theory, **$\dot{x}$** (pronounced **"x-dot"**) represents the **time derivative of the state vector $x(t)$**:

$$\dot{x} = \frac{dx(t)}{dt}$$

It defines the **rate of change** of the system's internal states over time.

**Key Concepts**

- **State Vector ($x$):** Represents the minimum set of variables (e.g., position, velocity, voltage, current) needed to completely describe the state of a system at any time $t$.
    
- **State Derivative ($\dot{x}$):** Expresses how those state variables evolve in response to the current state and external inputs $u(t)$.
    
- **Standard Linear State-Space Form:**
    
    $$\dot{x}(t) = Ax(t) + Bu(t)$$
    
    - **$A$ (State Matrix):** Describes the internal dynamics of the system.
        
    - **$B$ (Input Matrix):** Determines how external inputs $u(t)$ directly affect the rate of change of the states.



#### Solving
$$
A=\begin{bmatrix}
-4 & -1.5 \\
4 & 0
\end{bmatrix}, B=\begin{bmatrix}
2 \\
0
\end{bmatrix}, C=\begin{bmatrix}
1.5 & 0.625
\end{bmatrix}, D=0
$$

$$
G(s)=\frac{Y(s)}{F(s)}=C(sI-A)^{-1}B+D
$$

$$
\begin{bmatrix}
sI-A
\end{bmatrix}=\begin{bmatrix}
s+4 & 1.5 \\
-4 & s
\end{bmatrix}\to (sI-A)^{-1}=\frac{1}{s(s+4)+6}=\frac{1.5()}{}
$$

