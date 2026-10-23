# Z- parameters
$v_{1}=Z_{11}i_{1}+Z_{12}i_{2}$
$v_{2}=Z_{21}i_{1}+Z_{22}i_{2}$

$$
\begin{gathered}
\begin{bmatrix}
v_{1} \\
v_{2}
\end{bmatrix}
=\begin{bmatrix}
Z_{11} & Z_{12} \\
Z_{21} & Z_{22}
\end{bmatrix}
\begin{bmatrix}
i_{1} \\
i_{2}
\end{bmatrix}
\\
Z_{nm}=\frac{v_{n}}{i_{m}}|_{i_{h}=0 \text{ for }h\neq m}
\end{gathered}
$$
$i_{h}=0$ means open circuit at all other parts


Y-Parameters
$$
Y_{nm}=\frac{i_{n}}{v_{m}}|_{v_{h}=0\text{ for all other parts}}
$$
$v_{h}=0$ is short circuit

# Scattering (S) Parameters
S-Parameters are defined in a  $Z_{0}$ system. Typically, $Z_{0}=50\Omega$
![[Pasted image 20261014145253.png]]
the a's and b's are power waves or voltage waves depend on who you ask.
Professor calls them voltage waves

$S_{21}$ goes from port 1 to 2
$$
\begin{gathered}
a_{1}=\frac{V^{+}}{\sqrt{ Z_{0} }}\\
b_{1}=\frac{V^{-}}{\sqrt{ Z_{0} }} \\
b_{1}=S_{11}a_{1}+S_{12}a_{2} \\
b_{2}=S_{21}a_{1}+S_{22}a_{2} \\
\begin{bmatrix}
b_{1} \\
b_{2}
\end{bmatrix}
=
\begin{bmatrix}
S_{11} & S_{12} \\
S_{21} & S_{22}
\end{bmatrix}
\begin{bmatrix}
a_{1} \\
a_{2}
\end{bmatrix}
\\
S_{nm}=\frac{b_{n}}{a_{m}}|_{a_{h}=0\text{ for }h \neq m}
\end{gathered}
$$


$$
\begin{gathered}
S_{11}=\frac{b_{1}}{a_{1}}|_{a_{2}=0}=\text{ Input voltage Reflection Coefficient}=\Gamma_{IN} \\
S_{21}=\frac{b_{2}}{a_{1}}|_{a_{2}=0}=\text{ Forward Transmission Coefficient (Gain)} \\
S_{12}=\frac{b_{1}}{a_{2}}|_{a_{1}=0}=\text{ Reverse Transmission Coefficient (Isolation)} \\
S_{22}=\frac{b_{2}}{a_{2}}|_{a_{1}=0}=\text{ Ouput Voltage Reflection Coefficient}=\Gamma_{OUT}
\end{gathered}
$$

## Port 1

$$
\begin{gathered}
S_{11}=\Gamma_{IN}\\
SWR_{IN}=\frac{1+|S_{11|}}{1-|S_{11}|} \\
RL_{IN}=-10\log|S_{11}|^{2}(dB)
\end{gathered}
$$
## Transmission
$$
\text{Forward Gain}=|S_{21}|^{2}=\text{ (Linear Form)} \\
\text{Gain(Power)}=10\log|S_{21}|^{2}(dB) \\
\text{Reverse Gain}=|S_{12}|^{2}(dB) \\
\text{Isolation}=10\log|S_{12}|^{2}(dB)
$$
