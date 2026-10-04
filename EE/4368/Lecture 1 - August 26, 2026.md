 ## Chapter 1 - EMAG Review

**$\beta=\text{beta}=\frac{{2\pi}}{\lambda}=\text{Phase Propagation Constant}$**      
$\omega=\text{omega}=2\pi f\left( \frac{\text{Radians}}{\sec} \right)=\text{Radian Frequency}$
$\bar{P}=\text{Poynting Vector}$
$\alpha=\text{alpha}=\text{Attenuation Constant}$
$\text{Complex Propagation Constant}=\gamma =\alpha+j\beta$
$\text{Impendance}=\text{Force that impedes flow}$
$\text{Intrinsic Impedance}=\text{relate the Electric and Magnetic Field Components in Free Space}$
$Z_{f}=\text{in free space}$
$\mu=\text{Permeability}$
$\mu_{0}=\text{Permeability in Free Space}=1.256\times 10^{-6}\left( \frac{H}{m} \right)$
$\mu_{r}=\text{Relative Permeability(For this class)}=1.0$
$\epsilon=\text{Permittivity}$
$\epsilon_{0}=\text{Permittivity in Free Space}=8.854\times 10^{-12}\left( \frac{F}{m} \right)$
$\epsilon_{r}=\text{Relative Permittivity}$


Plane waves in free space
$$E_{x}=E_{0_{x}}\cos(\omega t-\beta z)\left( \frac{V}{m} \right)$$

$$
H_{y}=H_{0_{y}}\cos(\omega t-\beta z)\left( \frac{A}{m} \right)
$$
TEM: Transverse Electromagnetic (Right Hand Rule)
$$E_{x}\perp H_{y}\perp\text{Direction of Propagation}$$$$\bar{E} \times \bar{H} = \bar{P}$$
Intrinsic Impedance
$$
Z_{0}=Z_{f}=\frac{E_{x}}{H_{y}}=\sqrt{ \frac{\mu}{\epsilon} }=\sqrt{ \frac{\mu_{0}}{\epsilon_{0}} }
$$

$$
Z_{\text{diel}}=\sqrt{ \frac{{\mu_{0}\mu_{r}}}{\epsilon_{0}\epsilon_{r}} }
$$
In Free Space
$$
Z_{0}=Z_{f}=\sqrt{ \frac{\mu_{0}}{\epsilon_{0}} }=377\Omega
$$
In Dielectrics
$$
Z_{\text{diel}}=\sqrt{ \frac{{\mu_{0}\mu_{r}}}{\epsilon_{0}\epsilon_{r}} }=\frac{377}{\sqrt{ \epsilon_{r} }}\Omega
$$
	Duroid Substrate($\epsilon_r$) = 2.2
	FR-4 Substrate($\epsilon_r$) = 4.6
	Silicon Substrate($\epsilon_r$) = 11.7
	GaAs Substrate($\epsilon_r$) = 12.7

Phase Velocity, $v_{p}$

$$
v_{p}=\frac {\omega}{\beta}=\frac{1}{\sqrt{ \mu \epsilon }}
$$

$$
\text{In Free Space}=v_{p}=\frac{1}{\sqrt{ \mu_{0}\epsilon_{0} }}=c=3\times 10^8 \frac{m}{s}
$$

$$
\text{In Free Space, }f=\frac{c}{\lambda}
$$



## Future Concepts to touch on
**Passive Components**
- Do not require DC Bias
- R, L, C, TX lines (Transmission lines)
- Inductors: $jX_{L}=j\omega L=\text{Reactance}$
- Capacitors: $jX_{C}=\frac{1}{j\omega C}=-\frac{j}{\omega C}=\text{Reactance}$
