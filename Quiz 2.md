# Question 1
What is the Laplace Transform of this function?
$$
v(t)=18e^{-2t}u(t)
$$

$$
V(s)=\mathcal{L}[v(t)]=\frac{?}{s+?}
$$
## Answer
1. **Standard Laplace Transform Pair:**
    
    $$\mathcal{L}[e^{-at}u(t)] = \frac{1}{s + a}$$
    
2. **Linearity Property:**
    
    $$\mathcal{L}[a \cdot f(t)] = a \cdot F(s)$$
    
3. **Application:**
    
    Setting $a = 2$ and multiplying by $18$:
    
    $$V(s) = 18 \cdot \frac{1}{s + 2} = \frac{18}{s + 2}$$
# Question 2

$$
A\cos(\omega t)u(t)\leftrightarrow \frac{As}{s^2+\omega^2}
$$

$$
V(s)=\frac{10s}{s^2+16}
$$

$$
v(t)=?\cos(?t)u(t)
$$
## Answer
**Step-by-Step Solution**

Comparing $V(s) = \frac{10s}{s^2+16}$ to the standard transform pair $\mathcal{L}[A\cos(\omega t)u(t)] = \frac{As}{s^2+\omega^2}$:

1. **Amplitude ($A$):**
    
    Matching the numerator $10s = As \implies A = 10$
    
2. **Frequency ($\omega$):**
    
    Matching the denominator term $16 = \omega^2 \implies \omega = \sqrt{16} = 4$
    

**Missing Values:**

- **First `?` ($A$):** `10`
    
- **Second `?` ($\omega$):** `4`

# Question 3
The partial-fraction expansion of $F(s)=\frac{-4s+15}{s^3+8s^2+20s+16}$ is
$$
F(s)=\frac{?}{s+4}+\frac{?}{s+?}+\frac{?}{(s+?)^2}
$$
The time function (inverse Laplace transform} $f(t)$ is
$$
f(t)=(?e^{?t}-?e^{?t}+?te^{?t})u(t)
$$

## Answer
**Expected:**
$$F(s) = \frac{7.75}{s+4} + \frac{-7.75}{s+2} + \frac{11.5}{(s+2)^2}$$
$$f(t) = (7.75e^{-4t} - 7.75e^{-2t} + 11.5te^{-2t})u(t)$$

**Solution:** Factoring the denominator and expanding to partial-fractions:
$$F(s) = \frac{-4s + 15}{(s+4)(s+2)^2} = \frac{K_0}{s+4} + \frac{K_1}{s+2} + \frac{K_2}{(s+2)^2}$$

$$K_0 = (s+4) \cdot F(s) \Big|_{s=-4} = \left. \frac{-4s + 15}{(s+2)^2} \right|_{s=-4} = \frac{-4 \times (-4) + 15}{(-4+2)^2} = 7.75$$

$$K_2 = (s+2)^2 \cdot F(s) \Big|_{s=-2} = \left. \frac{-4s + 15}{s+4} \right|_{s=-2} = \frac{-4 \times (-2) + 15}{-2+4} = 11.5$$

$$K_1 = \left. \frac{d}{ds} \left[(s+2)^2 \cdot F(s)\right] \right|_{s=-2} = \left. \frac{d}{ds} \left( \frac{-4s + 15}{s+4} \right) \right|_{s=-2}$$

By the derivative quotient rule:
$$\begin{aligned}
\left. \frac{d}{ds} \left( \frac{-4s + 15}{s+4} \right) \right|_{s=-2} &= \left. \frac{(-4s + 15)'(s+4) - (-4s+15)(s+4)'}{(s+4)^2} \right|_{s=-2} \\
&= \frac{-4(-2+4) - (-4 \times (-2) + 15)}{(-2+4)^2} = -7.75
\end{aligned}$$

$$F(s) = \frac{7.75}{s+4} + \frac{-7.75}{s+2} + \frac{11.5}{(s+2)^2}$$
$$f(t) = (7.75e^{-4t} - 7.75e^{-2t} + 11.5te^{-2t})u(t)$$
# Question 4
The partial-fraction expansion of $F(s)$ is
$$
F(s)=\frac{116}{s^3+5s^2+4s+20}=\frac{?}{?}+\frac{?}{s+j 2}+\frac{?}{?}
$$

## Answer
**Expected:** $$F(s) = \frac{4}{s + 5} + \frac{-2 + j5}{s + j2} + \frac{-2 - j5}{s - j2}$$

The denominator is factored to $(s - p_0)(s - p_1)(s - p_2)$.

Then the numerator values $K_0, K_1, K_2$ for each partial-fraction denominator are found via
$$K_0, K_1, K_2 = (s - p_i) \cdot F(s) \Big|_{s=p_i}$$

$$F(s) = \frac{116}{s^3 + 5s^2 + 4s + 20} = \frac{116}{(s + 5)(s^2 + 4)} = \frac{K_0}{s + 5} + \frac{K_1}{s + j2} + \frac{K_2}{s - j2}$$

$$K_0 = (s + 5) \cdot F(s) \Big|_{s=-5} = 4$$

$$K_1 = (s + j2) \cdot F(s) \Big|_{s=-j2} = -2 + j5 \qquad K_2 = K_1^* = -2 - j5$$

$$F(s) = \frac{4}{s + 5} + \frac{-2 + j5}{s + j2} + \frac{-2 - j5}{s - j2} = \frac{4}{s + 5} + \frac{-4s + 20}{s^2 + 4}$$
# Question 5
For the differential equation
$$
6\frac{d^2}c(t){dt^2}+10c(t)=\frac{d^2r(t)}{dt^2}+4\frac{dr(t)}{dt}+2r(t) 
$$
The transfer function is:
$$
G(s)=\frac{s^2+?s+?}{?s^2+?}
$$

## Answer
### Derivation

1. **Take the Laplace Transform** of both sides (assuming zero initial conditions):
    
    $$\mathcal{L}\left[6\frac{d^2c(t)}{dt^2}+10c(t)\right] = \mathcal{L}\left[\frac{d^2r(t)}{dt^2}+4\frac{dr(t)}{dt}+2r(t)\right]$$
    
    $$(6s^2 + 10)C(s) = (s^2 + 4s + 2)R(s)$$
    
2. **Form the Transfer Function $G(s) = \frac{C(s)}{R(s)}$:**
    
    $$G(s) = \frac{C(s)}{R(s)} = \frac{s^2 + 4s + 2}{6s^2 + 10}$$
    

### Fill-in-the-Blank Values

- **Numerator:** $s^2 + \mathbf{4}s + \mathbf{2}$
    
- **Denominator:** $\mathbf{6}s^2 + \mathbf{10}$

# Question 6
Given step response 
$$
c(t)=8e^{-4t}\sin(2t)u(t)
$$
The transfer function is 
$$
G(s)=\frac{?s}{(s+?)^2+?}
$$

## Answer
### Step-by-Step Derivation

1. **Find the Laplace Transform of the Step Response $C(s)$:**
    
    Using the standard transform pair $\mathcal{L}[e^{-at}\sin(\omega t)u(t)] = \frac{\omega}{(s+a)^2 + \omega^2}$:
    
    $$C(s) = \mathcal{L}[c(t)] = 8 \cdot \frac{2}{(s+4)^2 + 2^2} = \frac{16}{(s+4)^2 + 4}$$
    
2. **Calculate the Transfer Function $G(s)$:**
    
    For a unit step input $r(t) = u(t)$, the input in the Laplace domain is $R(s) = \frac{1}{s}$.
    
    $$G(s) = \frac{C(s)}{R(s)} = s \cdot C(s) = \frac{16s}{(s+4)^2 + 4}$$
    

### Fill-in-the-Blank Values

- **Numerator multiplier:** $16$ (giving $16s$)
    
- **First denominator constant:** $4$ (giving $(s+4)^2$)
    
- **Second denominator constant:** $4$ (or $2^2$)

# Question 7
![[Pasted image 20260907234058.png]]

## Answer
$$V_{\text{out}} = \frac{16}{84s^2 + 80s}$$

### Step-by-Step Solution

1. **Set up the Mesh Equations:**
    
    - **Mesh 1 ($I_1$):**
        
        $$(R_1 + R_2)I_1 - R_2 I_2 = V_{\text{in}}(s)$$
        
        $$(8 + 4)I_1 - 4I_2 = \frac{1}{s} \implies 12I_1 - 4I_2 = \frac{1}{s}$$
        
    - **Mesh 2 ($I_2$):**
        
        $$-R_2 I_1 + (R_2 + sL + R_3)I_2 = 0$$
        
        $$-4I_1 + (4 + 7s + 4)I_2 = 0 \implies -4I_1 + (7s + 8)I_2 = 0 \implies I_1 = \frac{7s + 8}{4} I_2$$
        
2. **Solve for $I_2(s)$:**
    
    Substitute $I_1$ into the Mesh 1 equation:
    
    $$12\left(\frac{7s + 8}{4}I_2\right) - 4I_2 = \frac{1}{s}$$
    
    $$3(7s + 8)I_2 - 4I_2 = \frac{1}{s}$$
    
    $$(21s + 24 - 4)I_2 = \frac{1}{s}$$
    
    $$(21s + 20)I_2 = \frac{1}{s} \implies I_2 = \frac{1}{s(21s + 20)}$$
    
3. **Calculate $V_{\text{out}}(s)$:**
    
    $$V_{\text{out}}(s) = I_2 \cdot R_3 = \frac{4}{s(21s + 20)} = \frac{4}{21s^2 + 20s}$$
    
4. **Match Required Numerator ($16$):**
    
    Multiply the top and bottom by $4$:
    
    $$V_{\text{out}}(s) = \frac{4 \times 4}{4 \times (21s^2 + 20s)} = \frac{16}{84s^2 + 80s}$$
    

### Fill-in-the-Blank Values

- **First box ($s^2$ coefficient):** `84`
    
- **Second box ($s$ coefficient):** `80`
# Question 8
![[Pasted image 20260907234120.png]]

## Answer
**Expected:** $$\begin{bmatrix} 7 + 3s & -2 \\ -2 & 2 + 2/s \end{bmatrix} \begin{bmatrix} V_1 \\ V_2 \end{bmatrix} = \begin{bmatrix} 3 + 30/s \\ 0 \end{bmatrix}$$ $$V_2(s) = \frac{1s + 10.0}{s^2 + 2.67s + 2.33}$$ **Solution:** Writing KCL for currents exiting node $V_1$ : $$\frac{V_1 - V_a}{R_1} + \frac{V_1 - V_b}{1/(Cs)} + \frac{V_1 - V_2}{R_2} = 0$$ $$\frac{V_1 - 6/s}{0.2} + \frac{V_1 - 1/s}{0.333}s + \frac{V_1 - V_2}{0.5} = 0$$ which simplifies to: $$(7 + 3s)V_1 - 2V_2 = 3 + 30/s$$ KCL at node $V_2$ : $$\frac{V_2 - V_1}{R_2} + \frac{V_2}{Ls} = 0$$ $$\frac{V_2 - V_1}{0.5} + \frac{V_2}{0.5s} = 0$$ which simplifies to: $$-2V_1 + (2 + 2/s)V_2 = 0$$ Solution by hand or by MATLAB :
# Question 9
![[Pasted image 20260907234142.png]]

## Answer
Expected: $G(s) = \frac{-20}{s + 8}$, $\quad v_o(t) = -20e^{-8t}u(t)$

Solution:
The feedback impedance is:
$$Z_2 = R_f \parallel \frac{1}{Cs} = \frac{\frac{R_f}{Cs}}{R_f + \frac{1}{Cs}} = \frac{\frac{R_f}{Cs}}{R_f + \frac{1}{Cs}} \cdot \frac{\frac{s}{R_f}}{\frac{s}{R_f}} = \frac{\frac{1}{C}}{s + \frac{1}{R_f C}}$$

resulting in the inverting amp transfer function:
$$\begin{aligned}
G(s) &= \frac{V_o(s)}{V_i(s)} = -\frac{Z_2}{R_i} = -\frac{\frac{1}{R_i C}}{s + \frac{1}{R_f C}} \\
&= -\frac{\frac{1}{(4\text{ k}\Omega)(12.5\ \mu\text{F})}}{s + \frac{1}{(10\text{ k}\Omega)(12.5\ \mu\text{F})}} \\
&= \frac{-20}{s + 8}
\end{aligned}$$

Thus, by $B e^{-at} u(t) \Leftrightarrow \frac{B}{s + a}$, the impulse response is:
$$v_o(t) = \mathcal{L}^{-1}[G(s)] = -20e^{-8t}u(t)$$
# Question 10
![[Pasted image 20260907234158.png]]

## Answer
$$G(s) = \frac{X(s)}{F(s)} = \frac{1}{15s^2 + 2s + 16}$$

### Step-by-Step Solution

1. **Write the Differential Equation of Motion:**
    
    Applying Newton's second law ($\sum F = M\ddot{x}$) to mass $M$:
    
    $$f(t) - f_v \dot{x}(t) - K_1 x(t) - K_2 x(t) = M \ddot{x}(t)$$
    
    $$M \ddot{x}(t) + f_v \dot{x}(t) + (K_1 + K_2)x(t) = f(t)$$
    
2. **Substitute System Parameters:**
    
    - $M = 15\text{ kg}$
        
    - $f_v = 2\text{ N}\cdot\text{s/m}$
        
    - $K_1 = 10\text{ N/m}$
        
    - $K_2 = 6\text{ N/m} \implies K_{\text{eq}} = K_1 + K_2 = 16\text{ N/m}$
        
    
    $$15 \ddot{x}(t) + 2 \dot{x}(t) + 16 x(t) = f(t)$$
    
3. **Take the Laplace Transform:**
    
    Assuming zero initial conditions:
    
    $$(15s^2 + 2s + 16)X(s) = F(s)$$
    
4. **Form the Transfer Function $G(s)$:**
    
    $$G(s) = \frac{X(s)}{F(s)} = \frac{1}{15s^2 + 2s + 16}$$
    

### Fill-in-the-Blank Values

- **First box ($s^2$ coefficient):** `15`
    
- **Second box ($s$ coefficient):** `2`
    
- **Third box (constant term):** `16`


# Question 1
What is the Laplace Transform of this function?
$$
v(t)=3e^{2t}u(t)
$$

$$
V(s)=\mathcal{L}[v(t)]=\frac{?}{s+?}
$$
## Answer
$\mathcal{L}[f(t)]=F(s)=\int^{\infty}_{{0}}e^{-st}f(t)dt$

| Function $f(t)$ | Laplace Transform $\mathcal{L}[f(t)]=F(s)$ |
| --------------- | ------------------------------------------ |
| 1 Constant      | $\frac{1}{s}, (s> 0)$                      |
| $e^{at}$        | $\frac{1}{s-a}, (s> a)$                    |
| $t^n$           | $\frac{n!}{s^{n+1}}, (s> 0)$               |
| $\sin(at)$      | $\frac{a}{s^2+a^2}, (s>0)$                 |
| $\cos(at)$      | $\frac{s}{s^2+a^2}, (s>0)$                 |


$$3\int_{0}^{\infty} e^{-st} e^{2t} u(t) \, dt = \frac{3}{s-2}, \quad \text{for } \text{Re}(s) > 2$$

**Step-by-Step Evaluation**

1. **Apply $u(t)$ and Combine Exponents:**
    
    Since $u(t) = 1$ for $t \ge 0$, simplify the integrand:
    
    $$3\int_{0}^{\infty} e^{-st} e^{2t} \, dt = 3\int_{0}^{\infty} e^{-(s-2)t} \, dt$$
    
2. **Evaluate the Definite Integral:**
    
    $$\begin{aligned} 3\int_{0}^{\infty} e^{-(s-2)t} \, dt &= 3 \left[ \frac{e^{-(s-2)t}}{-(s-2)} \right]_{0}^{\infty} \\ &= -\frac{3}{s-2} \left( \lim_{t \to \infty} e^{-(s-2)t} - e^0 \right) \end{aligned}$$
    
3. **Convergence Condition ($\text{Re}(s) > 2$):**
    
    The limit $\lim_{t \to \infty} e^{-(s-2)t} = 0$ provided that $\text{Re}(s - 2) > 0 \implies \text{Re}(s) > 2$:
    
    $$-\frac{3}{s-2} (0 - 1) = \frac{3}{s-2}$$

# Question 2
$$
A\cos(\omega t)u(t)\leftrightarrow \frac{As}{s^2+\omega^2}
$$

$$
V(s)=\frac{14s}{s^2+100}
$$

$$
v(t)=?\cos(?t)u(t)
$$
## Answer
$$
v(t)=14s\cos(10t)u(t)
$$

# Question 3
The partial-fraction expansion of 
$$
F(s)=\frac{8s+4}{s^3+20s^2+125s+250}
$$
is
$$
F(s)=\frac{?}{s+10}+\frac{?}{s+?}+\frac{?}{(s+?)^2}
$$
The time function (inverse Laplace transform} $f(t)$ is
$$
f(t)=(?e^{?t}+?e^{?t}-?te^{?t})u(t)
$$

## Answer
**Partial Fraction Expansion**

1. **Factor the Denominator:**
    
    $$s^3 + 20s^2 + 125s + 250 = (s + 10)(s + 5)^2$$
    
2. **Set Up Partial Fractions:**
    
    $$F(s) = \frac{8s + 4}{(s + 10)(s + 5)^2} = \frac{A}{s + 10} + \frac{B}{s + 5} + \frac{C}{(s + 5)^2}$$
    
3. **Calculate Coefficients:**
    
    - **$A$ (for pole at $s = -10$):**
        
        $$A = \left. \frac{8s + 4}{(s + 5)^2} \right\vert{}_{s = -10} = \frac{8(-10) + 4}{(-10 + 5)^2} = \frac{-76}{25} = -3.04$$
        
    - **$C$ (for pole at $s = -5$):**
        
        $$C = \left. \frac{8s + 4}{s + 10} \right\vert{}_{s = -5} = \frac{8(-5) + 4}{-5 + 10} = \frac{-36}{5} = -7.2$$
        
    - **$B$ (for repeated pole at $s = -5$):**
        
        $$B = \left. \frac{d}{ds} \left( \frac{8s + 4}{s + 10} \right) \right\vert{}_{s = -5} = \left. \frac{8(s + 10) - (8s + 4)(1)}{(s + 10)^2} \right\vert{}_{s = -5} = \frac{76}{25} = 3.04$$
        

**Inverse Laplace Transform**

Taking the inverse Laplace transform term-by-term:

$$f(t) = \left( \frac{76}{25} e^{-5t} - \frac{76}{25} e^{-10t} - \frac{36}{5} t e^{-5t} \right) u(t)$$

**Fill-in-the-Blank Values**

**Partial Fraction Expansion:**

- $F(s) = \frac{\mathbf{-76/25}}{s+10} + \frac{\mathbf{76/25}}{s+\mathbf{5}} + \frac{\mathbf{-36/5}}{(s+\mathbf{5})^2}$
    
    _(in decimals: $-3.04$, $3.04$, $5$, $-7.2$, $5$)_
    

**Time Function $f(t)$:**

- $f(t) = \left( \mathbf{\frac{76}{25}} e^{\mathbf{-5}t} - \mathbf{\frac{76}{25}} e^{\mathbf{-10}t} - \mathbf{\frac{36}{5}} t e^{\mathbf{-5}t} \right) u(t)$
    
    _(in decimals: $3.04$, $-5$, $3.04$, $-10$, $7.2$, $-5$)_

# Question 4
The partial-fraction expansion of $F(s)$ is
$$
F(s)=\frac{150}{s^3+4s^2+9s+36}=\frac{?}{?}+\frac{?}{s+j 3}+\frac{?}{?}
$$

## Answer
**Partial Fraction Expansion**

1. **Factor the Denominator:**
    
    $$s^3 + 4s^2 + 9s + 36 = s^2(s + 4) + 9(s + 4) = (s + 4)(s^2 + 9)$$
    
    Factoring over complex roots yields poles at $s = -4$, $s = -j3$, and $s = j3$:
    
    $$s^3 + 4s^2 + 9s + 36 = (s + 4)(s + j3)(s - j3)$$
    
2. **Set Up the Expansion:**
    
    $$F(s) = \frac{150}{(s+4)(s+j3)(s-j3)} = \frac{A}{s+4} + \frac{B}{s+j3} + \frac{C}{s-j3}$$
    
3. **Calculate the Residues:**
    
    - **For $A$ (pole at $s = -4$):**
        
        $$A = \left. \frac{150}{s^2+9} \right\vert{}_{s=-4} = \frac{150}{(-4)^2+9} = \frac{150}{25} = 6$$
        
    - **For $B$ (pole at $s = -j3$):**
        
        $$B = \left. \frac{150}{(s+4)(s-j3)} \right\vert{}_{s=-j3} = \frac{150}{(-j3+4)(-j6)} = \frac{150}{-18 - j24} = -3 + j4$$
        
    - **For $C$ (pole at $s = j3$):**
        
        $$C = B^* = -3 - j4$$
        

**Final Expansion**

$$F(s) = \frac{6}{s+4} + \frac{-3 + j4}{s+j3} + \frac{-3 - j4}{s-j3}$$

**Fill-in-the-Blank Values:**

- First term: $\frac{\mathbf{6}}{\mathbf{s+4}}$
    
- Second term (over $s+j3$): $\frac{\mathbf{-3+j4}}{s+j3}$
    
- Third term: $\frac{\mathbf{-3-j4}}{\mathbf{s-j3}}$

# Question 5