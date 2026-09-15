## Question 1
![[Pasted image 20260903220419.png|692]]




## Question 2
Given the transfer function G(s) = -24/(s+6)

Select ALL correct expressions for the unit step response in the s-domain C(s) and the time-domain step response c(t).

- C(s) = 4/s - 4/(s+6)

- c(t) = (-4 + 4e6t) u(t)

- **C(s) = -4/s + 4/(s+6)**

- **c(t) = (-4 + 4e-6t) u(t)**

### Work
To find the correct unit step response, we multiply the transfer function $G(s)$ by the unit step input $R(s) = \frac{1}{s}$ in the $s$-domain, then perform partial fraction expansion to solve for $c(t)$.

#### 1. $s$-Domain Response $C(s)$

The output $C(s)$ is given by:

$$C(s) = G(s) R(s) = \frac{-24}{s+6} \cdot \frac{1}{s} = \frac{-24}{s(s+6)}$$

Using partial fraction decomposition:

$$\frac{-24}{s(s+6)} = \frac{A}{s} + \frac{B}{s+6}$$

Solving for coefficients $A$ and $B$:

- $A = \lim_{s \to 0} s \cdot \frac{-24}{s(s+6)} = \frac{-24}{6} = -4$
    
- $B = \lim_{s \to -6} (s+6) \cdot \frac{-24}{s(s+6)} = \frac{-24}{-6} = 4$
    

Substituting these back in yields:

$$C(s) = -\frac{4}{s} + \frac{4}{s+6}$$

#### 2. Time-Domain Response $c(t)$

Taking the inverse Laplace transform of $C(s)$:

$$\mathcal{L}^{-1}\left\{ -\frac{4}{s} + \frac{4}{s+6} \right\} = \left(-4 + 4e^{-6t}\right) u(t)$$

#### Correct Selections

Based on the calculations above:

- **$C(s) = -4/s + 4/(s+6)$** is **CORRECT**
    
- **$c(t) = (-4 + 4e^{-6t}) u(t)$** is **CORRECT**
