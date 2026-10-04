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
Remember
$$
\cos(\omega t)=\frac{e^{j\omega t}+e^{-j\omega t}}{2}
$$

$$
j=\sqrt{ -1 }
$$

$$v(t) = \frac{A}{2} e^{j\omega t} u(t) + \frac{A}{2} e^{-j\omega t} u(t)$$
so you can work this out but were already given the equations so the answer is
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

1. **Factor the Denominator: Rational Root Theorem**
    
    $$s^3 + 20s^2 + 125s + 250 = (s + 10)(s + 5)^2$$
    
2. **Set Up Partial Fractions:**
    
    $$F(s) = \frac{8s + 4}{(s + 10)(s + 5)^2} = \frac{A}{s + 10} + \frac{B}{s + 5} + \frac{C}{(s + 5)^2}$$
    **Multiply both sides by $(s+10)(s+5)^2$ to clear the fractions:

$$8s + 4 = A(s+5)^2 + B(s+10)(s+5) + C(s+10)$$
  ### Step 3: Solve for $A$ and $C$ Using Roots (Cover-Up Method)

Plug in the roots of the denominator terms to isolate individual coefficients.

- **Find $A$ by setting $s = -10$:**
    
    $$8(-10) + 4 = A(-10 + 5)^2 + B(0) + C(0)$$
    
    $$-76 = 25A \implies A = -\frac{76}{25} = -3.04$$
    
- **Find $C$ by setting $s = -5$:**
    
    $$8(-5) + 4 = A(0) + B(0) + C(-5 + 10)$$
    
    $$-36 = 5C \implies C = -\frac{36}{5} = -7.2$$
	Step 4: Solve for $B$

Since no un-used roots remain, pick an easy value for $s$ (such as $s = 0$) and substitute the values for $A$ and $C$:

$$8(0) + 4 = A(5)^2 + B(10)(5) + C(10)$$

$$4 = 25A + 50B + 10C$$

Substitute $25A = -76$ and $10C = -72$:

$$4 = -76 + 50B - 72$$

$$4 = -148 + 50B$$

$$152 = 50B \implies B = \frac{76}{25} = 3.04$$



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
For the differential equation
$$
3\frac{d^2c(t)}{dt^2}+7c(t)=\frac{d^2r(t)}{dt^2}+2\frac{dr(t)}{dt}+5r(t)
$$
The transfer function is:
$$
G(s)=\frac{s^2+?s+?}{?s^2+?}
$$


## Answer
To find the transfer function $G(s) = \frac{C(s)}{R(s)}$, take the Laplace transform of both sides, assuming all initial conditions are zero.

### Step 1: Take the Laplace Transform

Using the property $\mathcal{L}\left\{\frac{d^n y(t)}{dt^n}\right\} = s^n Y(s)$ for zero initial conditions:

- **Left side:**
    
    $$\mathcal{L}\left\{3\frac{d^2c(t)}{dt^2} + 7c(t)\right\} = 3s^2C(s) + 7C(s) = (3s^2 + 7)C(s)$$
    
- **Right side:**
    
    $$\mathcal{L}\left\{\frac{d^2r(t)}{dt^2} + 2\frac{dr(t)}{dt} + 5r(t)\right\} = s^2R(s) + 2sR(s) + 5R(s) = (s^2 + 2s + 5)R(s)$$
    

### Step 2: Form the Ratio $\frac{C(s)}{R(s)}$

Rearrange the equation to isolate $G(s) = \frac{C(s)}{R(s)}$:

$$(3s^2 + 7)C(s) = (s^2 + 2s + 5)R(s)$$

$$G(s) = \frac{C(s)}{R(s)} = \frac{s^2 + 2s + 5}{3s^2 + 7}$$

### Completed Transfer Function

$$G(s) = \frac{s^2 + 2s + 5}{3s^2 + 7}$$

- **Numerator missing values:** $2$ and $5$
    
- **Denominator missing values:** $3$ and $7$


# Question 6
Given step response 
$$
c(t)=9e^{-2t}\sin(5t)u(t)
$$
The transfer function is 
$$
G(s)=\frac{?s}{(s+?)^2+?}
$$
## Answer
To find the transfer function $G(s)$ from the step response $c(t)$, use the relationship:

$$G(s) = \frac{C(s)}{R(s)}$$

Since $c(t)$ is the **step response**, the input is a unit step function $r(t) = u(t)$, which has the Laplace transform:

$$R(s) = \frac{1}{s}$$

Therefore:

$$G(s) = s \cdot C(s)$$

### Step 1: Find $C(s)$

Take the Laplace transform of $c(t) = 9e^{-2t}\sin(5t)u(t)$.

Using the damped sine transform pair $\mathcal{L}\left\{e^{-at}\sin(\omega t)u(t)\right\} = \frac{\omega}{(s+a)^2 + \omega^2}$:

$$C(s) = 9 \cdot \frac{5}{(s+2)^2 + 5^2} = \frac{45}{(s+2)^2 + 25}$$

### Step 2: Calculate $G(s)$

Multiply $C(s)$ by $s$:

$$G(s) = s \cdot \left(\frac{45}{(s+2)^2 + 25}\right) = \frac{45s}{(s+2)^2 + 25}$$

### Completed Transfer Function

$$G(s) = \frac{\mathbf{45}s}{(s + \mathbf{2})^2 + \mathbf{25}}$$

- **Numerator multiplier:** $45$
    
- **Pole shift ($a$):** $2$
    
- **Frequency squared ($\omega^2$):** $25$


# Question 7

| $\rightarrow$                         | $\rightarrow$ | $R_{1}(3\Omega)$ | $\rightarrow$    | $L(6H)$      | $\rightarrow$    | $\rightarrow+$ |           |
| ------------------------------------- | ------------- | ---------------- | ---------------- | ------------ | ---------------- | -------------- | --------- |
| $\uparrow$                            |               |                  | $\downarrow$     |              | $\downarrow$     |                |           |
| $V(s)(\pm)\left( \frac{1}{s} \right)$ |               |                  | $R_{2}(7\Omega)$ |              | $R_{3}(7\Omega)$ |                | $V_{out}$ |
| $\uparrow$                            |               |                  | $\downarrow$     |              | $\downarrow$     |                |           |
| $\leftarrow$                          | $\leftarrow$  | $\leftarrow$     | $\leftarrow$     | $\leftarrow$ | $\leftarrow$     | $\rightarrow-$ |           |

$$
V_{out}=\frac{49}{?s^2+?s}
$$
## Answer

**1. Mesh Equations:**

  

- **Mesh 1 ($I_1$):**
    
      
    
    $$(R_1 + R_2)I_1 - R_2 I_2 = V_{\text{in}}(s)$$
    
    $$(3 + 7)I_1 - 7I_2 = \frac{1}{s} \implies 10I_1 - 7I_2 = \frac{1}{s}$$
    
- **Mesh 2 ($I_2$):**
    
      
    
    $$-R_2 I_1 + (R_2 + R_3 + sL)I_2 = 0$$
    
    $$-7I_1 + (7 + 7 + 6s)I_2 = 0 \implies 7I_1 = (6s + 14)I_2$$
    

**2. Solve for $I_2(s)$:**

Substitute $I_1 = \frac{6s + 14}{7}I_2$ into the Mesh 1 equation:

  

$$10\left(\frac{6s + 14}{7}\right)I_2 - 7I_2 = \frac{1}{s}$$

$$\left(\frac{60s + 140}{7} - \frac{49}{7}\right)I_2 = \frac{1}{s}$$

$$\left(\frac{60s + 91}{7}\right)I_2 = \frac{1}{s} \implies I_2(s) = \frac{7}{s(60s + 91)}$$

**3. Calculate $V_{\text{out}}(s)$:**

The output voltage is measured across resistor $R_3$:

$$V_{\text{out}}(s) = R_3 \cdot I_2(s) = 7 \cdot \frac{7}{s(60s + 91)} = \frac{49}{60s^2 + 91s}$$



# Question 8
| $\rightarrow$                         | $R_{1}(0.4\Omega)$ | $\rightarrow$ | $V_{1}$                                | $\rightarrow$ | $R_{2}(0.2\Omega)$ | $\rightarrow$ | $V_{1}$      |
| ------------------------------------- | ------------------ | ------------- | -------------------------------------- | ------------- | ------------------ | ------------- | ------------ |
| $\uparrow$                            |                    |               | $\downarrow$                           |               |                    |               | $\downarrow$ |
| $\uparrow$                            |                    |               | $C(1F)$                                |               |                    |               | $\downarrow$ |
| $V(s)(\pm)\left( \frac{6}{s} \right)$ |                    |               | $\downarrow$                           |               |                    |               | $L(0.25H)$   |
| $\uparrow$                            |                    |               | $V_{b}(\pm)\left( \frac{3}{s} \right)$ |               |                    |               | $\downarrow$ |
| $\uparrow$                            |                    |               | $\downarrow$                           |               |                    |               | $\downarrow$ |
| $\uparrow$                            | $\leftarrow$       | $\leftarrow$  | $\leftarrow$                           | $\leftarrow$  | $\leftarrow$       | $\leftarrow$  | $\leftarrow$ |
What are the nodal analysis matrix equations and voltage $V_{2}(s)$


$$ \begin{bmatrix} ?+?s & -5  \\ -5 & ?+\frac{?}{s}  \end{bmatrix} \begin{bmatrix} V_{1}\\ V_{2} \end{bmatrix} = \begin{bmatrix} ?+\frac{?}{s}\\ ? \end{bmatrix}  $$


$$
V_{2}(s)=\frac{?s+?}{s^2+?s+?}
$$
## Answer
Nodal analysis. Write KCL Equations from nodes

$V_{1}$:

$$
 \frac{V_{1}-V_{a}}{R_{1}}+\frac{V_{1}-V_{b}}{\frac{1}{Cs}}+\frac{V_{1}-V_{2}}{R_{2}}=0
$$
$$
 \frac{V_{1}-\frac{6}{s}}{0.4}+\frac{V_{1}-\frac{3}{s}}{\frac{1}{s}}+\frac{V_{1}-V_{2}}{0.2}=0
$$
	simplies to

$$(2s^2 + 15s)V_1 - 10sV_2 = 6s + 30$$
$V_{2}$:

$$
\frac{V_{2}-V_{1}}{R_{2}}+\frac{V_{2}}{Ls}=0
$$

$$
\frac{V_{2}-V_{1}}{0.2}+\frac{V_{2}}{0.25s}=0
$$
	simplifies to

$$-5 V_1 + \left( 5 + \frac{4}{s} \right)V_2 = 0$$

- **Top Row (Row 1):** Comes entirely from **Node 1's KCL Equation**.
    
- **Bottom Row (Row 2):** Comes entirely from **Node 2's KCL Equation**.
    
- **Column 1:** The total coefficients multiplying **$V_1$**.
    
- **Column 2:** The total coefficients multiplying **$V_2$**.
    
- **Right-Hand Side Vector ($\mathbf{B}$):** Contains all the **independent source/constant terms** (moved to the right side of the equal sign).

It looks like I need to divide the $V_{1}$ equation by $2s$ to match the example from the question. And the right hand side is what is after the equal sign.

$V_{1}$:

$$
\frac{(2s^2 + 15s)V_1}{2s} - \frac{10sV_{2}}{2s} = \frac{6s + 30}{2s}
$$

$$
(s+7.5)V_{1}-5V_{2}=3+\frac{15}{s}
$$
Now set up the matrix
$$
 \begin{bmatrix} 7.5+s & -5  \\ -5 & 5+\frac{4}{s}  \end{bmatrix} \begin{bmatrix} V_{1}\\ V_{2} \end{bmatrix} = \begin{bmatrix} 3+\frac{15}{s}\\ 0 \end{bmatrix}  
$$
So now we have to solve for $V_{2}(s)$
if you were solving for $V_1$, Cramer's Rule gives:

$$V_1(s) = \frac{\Delta_1}{\Delta}$$

where $\Delta_1$ is the determinant of matrix $\mathbf{A}$ with its **1st column** replaced by vector $\mathbf{B}$.
Substituting $\Delta$ and $\Delta_2$ back into the isolated $V_2$ expression yields:

$$V_2(s) = \frac{\Delta_2}{\Delta}$$
**The Denominator ($\Delta$):**

$$\Delta = \det(\mathbf{A}) = \det \begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix} = a_{11} a_{22} - a_{21} a_{12}$$

**The Numerator ($\Delta_2$):**

If you replace the **2nd column** of $\mathbf{A}$ (the $V_2$ coefficients) with the right-hand side vector $\mathbf{B}$:

$$\mathbf{A}_2 = \begin{bmatrix} a_{11} & b_1 \\ a_{21} & b_2 \end{bmatrix}$$

Taking its determinant gives:

$$\Delta_2 = \det(\mathbf{A}_2) = a_{11} b_2 - a_{21} b_1$$
$$V_2(s) = \frac{\frac{15s + 75}{s}}{\frac{5s^2 + 16.5s + 30}{s}}$$

Cancel the common denominator $s$:

$$V_2(s) = \frac{15s + 75}{5s^2 + 16.5s + 30}$$

Divide both the numerator and denominator by $5$ to normalize the leading $s^2$ coefficient to $1$:

$$V_2(s) = \frac{3s + 15}{s^2 + 3.3s + 6}$$


# Question 9
The transfer function is:
$$
G(s)=\frac{?}{s+?}
$$
The impulse response is:
$$
v_{o}(t)=?e^{?t}u(t)
$$
![[Pasted image 20260908150927.png]]


## Answer
The feedback impedance is:
$$Z_2 = R_f \parallel \frac{1}{Cs} = \frac{\frac{R_f}{Cs}}{R_f + \frac{1}{Cs}} = \frac{\frac{R_f}{Cs}}{R_f + \frac{1}{Cs}} \cdot \frac{\frac{s}{R_f}}{\frac{s}{R_f}} = \frac{\frac{1}{C}}{s + \frac{1}{R_f C}}$$

resulting in the inverting amp transfer function:
$$\begin{aligned}
G(s) &= \frac{V_o(s)}{V_i(s)} = -\frac{Z_2}{R_i} = -\frac{\frac{1}{R_i C}}{s + \frac{1}{R_f C}} \\
&= -\frac{\frac{1}{(2\text{ k}\Omega)(31.25\ \mu\text{F})}}{s + \frac{1}{(4\text{ k}\Omega)(31.25\ \mu\text{F})}} \\
&= \frac{-16}{s + 8}
\end{aligned}$$

Thus, by $B e^{-at} u(t) \Leftrightarrow \frac{B}{s + a}$, the impulse response is:
$$v_o(t) = \mathcal{L}^{-1}[G(s)] = -16e^{-8t}u(t)$$


# Question 10
The transfer function is
$$
G(s)=\frac{X(s)}{F(s)}=\frac{1}{?s^2+?s+?}
$$
![[Pasted image 20260908150912.png]]

## Answer
Solution: The total spring force is $(K_1 + K_2)X(s) = (4 + 7)X(s) = 11X(s)$, the damper friction force is $f_v s X(s) = 3s X(s)$, and the mass acceleration force is $M s^2 X(s) = 13s^2 X(s)$.

Summing forces in the $s$-domain gives $F(s) = (13s^2 + 3s + 11)X(s)$. The transfer function is the ratio of displacement $X(s)$ to force $F(s)$ :

$$G(s) = \frac{X(s)}{F(s)} = \frac{1}{13s^2 + 3s + 11}$$






