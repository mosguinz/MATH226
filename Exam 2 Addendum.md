---
    print_background: true
    export_on_save:
        html: true
    puppeteer:
        format: "Letter"
        timeout: 3000
---

$$
    % Differentials d[something]/d[something]
    \gdef\diff#1#2{\frac{\mathrm{d}#1}{\mathrm{d}#2}}
    % Shortcut for dy/dx
    \gdef\dydx{\diff{y}{x}}
    % Differential letter "d" with a thin space before it
    \gdef\dd{\mathop{}\!\mathrm{d}}
    % Shortcut for not implies
    \gdef\nimplies{\;\;\;\not\nobreak\!\!\!\!\implies\;}
    % Shortcuts for extended brackets
    \gdef\({\left(} \gdef\){\right)}
    % Shortcut for real number symbol
    \gdef\R{\mathbb{R}}
$$

# Exam 2 Addendum

> Kullathon "Mos" Sitthisarnwattanachai
> **MATH022613-S21R-7307**

# Question 3

In this question, it was provided that $f(1)=4$ and $f'(1)=10$. All else not relevant for \(c\).

## Part C
Let $j(x)=xe^{f(x)}$. Find $j'(1)$.

### Original answer
$\displaystyle j'(1)=10e^4$
The original answer was incorrect due to a typo.

### Correction
$$
\begin{aligned}
    j'(x) &= \diff{}{x}(x)e^{f(x)} + x\diff{}{x}\(e^{f(x)}\) \\[1.0em]
    &= e^{f(x)} + xf'(x)\cdot e^{f(x)} \\[.5em]
    &= e^{f(x)}(xf'(x) + 1) \\[1.5em]
    \therefore j'(1) &= e^{f(1)}(1\cdot f'(1) + 1) \\
    &= e^4(1\cdot 10+1) \\
    &= 11e^4 \\
    &\approx 600.6\quad\text{(1 d.p.)}
\end{aligned}
$$

# Question 4

## Second part
Find the equation of the tangent line to $-42x^8+9x^{56}y+y^5=-32$.

### Original answer
$\displaystyle y=-\frac{56}{15}\left(x-1\right)+1$
Error carried forward during previous calculations.

### Correction
The derivative of the function was calculated from the first part.
$$
-42x^8+9x^{56}y+y^5=-32 \implies \dydx=\frac{168x^7\left(2-3x^{48}y\right)}{9x^{56}+5y^4}
$$

Then, find the slope at $(1,1)$.
$$
\begin{aligned}
    \frac{168(1^7)\left(2-3(1^{48})(1)\right)}{9(1^{56})+5(1^4)} &= \frac{168(-1)}{9+5} \\[1em]
    &= \frac{-168}{14} \\[1em]
    &= -12
\end{aligned}
$$

Applying the formula for the equation of the tangent, we have that
$$
y=-12(x-1)+1 \\
\therefore y = -12x+13.
$$

# Question 8

## Part A
Find the intervals for which the function $f(x)=x^4-6x^2$ is concave up.

### Original answer
$(-\infty, -1), (1, \infty)$
The provided answer is correct.

$(-\infty, -1), (1, \infty)$ was used to denote the union $(-\infty, -1)\cup (1, \infty)$. This was consistent with the directions provided in the previous question and did not result in an error message.

As noted in previous correspondence, the system's input validation failed when the answer was provided in either the requested format, `(-oo,-1)U(1,oo)`, or the proper interval notation, $(-\infty, -1)\cup (1, \infty)$.

### Correction
For the sake of completeness, below is the working for this part.

First, find $f''$.
$$
f(x)=x^4-6x^2\implies f'(x)=4x^3-12x\implies f''(x)=12x^2-12
$$

Then, find the inflection points.
$$
12x^2-12=0 \\
x^2 = 1 \\
\therefore x=\pm1
$$

Then, check the values of $f''(x)$ before and after the inflection points.

<center>

|  $x$  | $f''(x)$ |
| :---: | :------: |
| $-2$  |   $36$   |
| $-1$  |   $0$    |
|  $0$  |  $-12$   |
|  $1$  |   $0$    |
|  $2$  |   $36$   |

</center>

Since $f$ is continuous and is defined for all $x\in\R$, the positive values of $f''(x)$ from the table indicates that $f$ is concave up before $x=-1$ exclusive and after $x=1$ exclusive.

As such, we conclude that $f$ is concave up on the interval $(-\infty, -1)\cup (1, \infty)$.

