# Topics for Exam 1
## Chapter 1 
Plane waves
$$
\begin{gathered}
E_{x}=E_{0}\cos(\omega t-\beta z)\left( \frac{V}{m} \right) \text{ Right Hand Rule} \\
\omega=\frac{2\pi}{f} \\
\beta=\frac{2\pi}{\lambda} \\
v_{p}=\frac{\omega}{\beta} \\
f=\frac{c}{\lambda}\implies \text{ free space}\\
\end{gathered}
$$

In dielectric
$$
\begin{gathered}
f=\frac{v_{p}}{\lambda_{diel}} \\
v_{p}=\frac{c}{\sqrt{ \epsilon_{r} }} \\
\lambda_{diel}=\frac{\lambda_{0}}{\sqrt{ \epsilon_{r} }} \\
\mu_{0}, \space \mu_{r}, \space \epsilon_{0},\space\epsilon_{r}
\end{gathered}
$$

Passive Components
$$
\begin{gathered}
\text{R, L, C, TX Comp.} \\
jX_{L}=-j\omega L \\
jX_{C}=\frac{1}{j\omega C}=-\frac{j}{\omega C}
\end{gathered}
$$

Skin Depth
$$
\begin{gathered}
\delta=\frac{1}{\sqrt{ \pi f\mu\text{conductiviy of metal} }} \\
\text{ROT \#1 Need 3 $\delta$ for low-loss Rf operation}
\end{gathered}
$$

Resonant Freq.
$$
\begin{gathered}
\text{Know series and parallel setup} \\
f_{v}=\frac{1}{ 2\pi \sqrt{ LC }}
\end{gathered}
$$

RFC
$$
\begin{gathered}
l=\text{length of coil}\\
r=\text{radius of coil}\\
N=\text{number of turns}\\
L_{\text{Air Coil}}=\frac{10\pi r^2\mu_{0}N^2}{9r+10l}
\end{gathered}
$$

Straight Wire
$$
\begin{gathered}
l=\text{length of wire} \\
a = \text{radius of wire} \\
L_{\text{ext}}=\frac{\mu_{0}l }{2\pi}\left[ \ln\left( \frac{2l}{a}-1 \right) \right]
\end{gathered}
$$

# Chapter 2
TX Lines
$$
\begin{gathered}
\text{ROT \#2 when the average size, $L_{A}$, of a discrete component is $\geq$ a tenth of the operating wavelength, transmission line theory should be applied} \\
L\geq \frac{\lambda}{10}
\end{gathered}
$$

TX Lines (lossless)
$$
\begin{gathered}
Z_{0}=\sqrt{ \frac{L}{C} } \\
v_{p}=\frac{1}{\sqrt{ LC }}
\end{gathered}
$$

Microstrips
$$
\begin{gathered}
\lambda_{{ms}}=\frac{\lambda_{0}}{\sqrt{ eff }} \\
v_{p}=\frac{c}{\sqrt{ eff }}
\end{gathered}
$$

Voltage Reflection Coeff
$$
\begin{gathered}
\Gamma=\frac{V^-}{V^+} \\
\Gamma_{L}=\frac{Z_{L}-Z_{0}}{Z_{L}+Z_{0}} \\
\text{SWR}=\frac{1+|\Gamma|}{1-|\Gamma|} \\
\text{RL}=-10\log|\Gamma|^2(dB)\\
\text{ML}=-10\log(1-|\Gamma|^2)(dB)
\end{gathered}
$$

Impedance
$$
\begin{gathered}
Z_{IN}(d)=Z_{0}\frac{Z_{L}+jZ_{0}\tan(\beta d)}{Z_{0}+jZ_{L}\tan(\beta d)}\\
\text{Case 1} \to S.C. \\
\text{Case 2} \to O.C. \\
\text{Case 3} \to d=\frac{\lambda}{4}\to Z_{T}=\sqrt{ Z_{IN}\cdot Z_{L} }
\end{gathered}
$$

Power
$$
\begin{gathered}
dB=\text{Gain or Loss}=10\log\left( \frac{P_{2}}{P_{1}} \right)=\text{Relative Power} \\
dBm = 10\log P(\text{in mW})=\text{Absolute Power} \\
\text{Conjugate Match to achieve max power transfer}
\end{gathered}
$$


