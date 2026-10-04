**Attentiveness** Attentiveness is the quality of paying close, careful focus or showing thoughtful consideration toward others. 

## Chapter 1 Continuation
### Skin Effect
Resistance at DC = $R_{DC}$
$l=\text{length}$
$a=\text{radius}$
$\sigma=\text{conductivity}$
$R_{DC}=\frac{l}{\pi a^2\sigma_{cond}}=\text{Resistance at DC}$
$\mu=\mu_{0}\mu_{r}$
$\delta=\frac{1}{\sqrt{ f\mu \pi \sigma_{cond} }}=\text{Skin Depth}$
Skin Depth, describes the spatial deop-off in current density as a function of frequency, permeability and conductivity
$R_{AC}=R_{DC}   \frac{a}{2\delta}=\text{Resistance at AC}$

#### Example
Au(Gold) $\sigma_{Au}=48.544\times 10^6 \frac{S}{m}$
Remember $S=siemens=\frac{1}{\Omega}$
$f=10GHz$
$\mu_{r}=1.0$
$\delta=\frac{1}{\sqrt{ (10\times 10^9)(1.256\times 10^{-6})\pi(48.544\times 10^{6}) }}=7.22\times 10^{-7}m=0.7\mu m$
### Microstrip (Chapter 2)
![[Pasted image 20260831144958.png]]
You can call the Conducting Strip the "Top Conductor" and the Ground Plate as the "Bottom Conductor"

**Rule of Thumb #1**
- Best guess
- For Low-Loss RF operation. we need a minimum of 3 skin depths of metal
- $t\geq 3\delta$
So we are besically saying we need a $t$ of $3\delta$ of metal for the Top Conductor and Bottom Conductor to be Low-Loss

#### Example - calling back to earlier example
$t=3\delta=2(0.7\mu m)=2.1\mu m$ @ $f=10 GHz,\text{ Au metal}$

### Passive Components - Chapter 1.4
- Lumped Elements - R, L, C
	- Distributed Elements (TX Lines)
#### Resistor @ RF
![[Pasted image 20260831151629.png|531]]
R = Resistance
 L = Lead Inductance
$C_{a}$ = Change spearation effect
$C_{b}$ = Interlead Capacitance

#### Capacitor @ RF
Remeber $C=\frac{\epsilon A}{d}$
![[Pasted image 20260831152321.png|457]]
$C=\text{Capacitance}$
$R_{e}=\text{Dielectric Resistance}$
$R_{s}=\text{AC Resistance}$
$L=\text{Lead Inductance}$

![[Pasted image 20260831152955.png|440]]
$f_{r}={\text{Resonant Frequency}}$
$f_{r}$ is located on the large dip at the Real Capacitor impedance.
$\sum(X_{L}+X_{C})=0$
$\sum\left( j\omega L+\frac{{-i}}{\omega C} \right)=0$

**what is the best place to operate the capacitor in terms of frequency?**
	Below resonant frequency so it looks more like a capacitor!

**Homework: Solve for the resonant frequency in terms of L & C**

#### Inductors @ RF
![[Pasted image 20260831153749.png|447]]
$C_{s}=\text{Parasitic Shunt Capacitance}$
$R_{s}=\text{Series Resistance}$
$L=\text{Inductance}$

![[Pasted image 20260831154103.png|381]]
[[EE/4368 RF Principles/RF Circuit Design_ Theory & Applications (2nd Edition).pdf|RF Circuit Design_ Theory & Applications (2nd Edition).pdf#page=24]]
Striaght Wire Inductance (External Inductance)

[[filename.pdf#page=N]]