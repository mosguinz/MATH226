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
    % Shortcut for not implies
    \gdef\nimplies{\;\;\;\not\nobreak\!\!\!\!\implies\;}
    % Shortcuts for extended brackets
    \gdef\({\left(} \gdef\){\right)}
    % Shortcut for real number symbol
    \gdef\R{\mathbb{R}}
$$

# Review Problems for Exam 2

# Problem 1

Compute the derivative of $f(x) = e^{3x}\cdot\ln(5x+4)$.
$$
\begin{aligned}
    u &= e^{3x} &\implies u' &= e^{3x} \\
    v &= \ln(5x+4) &\implies v' &= \frac{5}{5x+4}
\end{aligned}
\\
\begin{aligned}
    f'(x) &= u'v+uv' \\
    &= e^{3x}\ln(5x+4) + \frac{5e^{3x}}{5x+4}
\end{aligned}
$$

# Problem 2

Compute the derivative of $f(x) = \tan^{-1}3x^2$.

Recall that:
$$
\diff{}{x}(\tan^{-1}x)=\frac{1}{x^2+1}.
$$

Then,
$$
\begin{aligned}
    f'(x) &= \frac{1}{(3x^2)^2 + 1}\cdot 6x \\
    &= \frac{6x}{9x^4+1}.
\end{aligned}
$$

# Problem 3
Given $2x^2-y=3xy^3+1$, find $\dydx$ using implicit differentiation.

First, differentiate both sides.
$$
4x-\dydx = \diff{}{x}(3x)y^3+\diff{}{y}(y^3)3x \\
4x-\dydx = 3y^3 + 3y^2\dydx\cdot3x
$$

Then, factor and isolate $\dydx$.
$$
4x-\dydx = 3y^3 + 9xy^2\dydx \\
-\dydx-9xy^2\dydx=-4x+3y^3 \\
\dydx(-1-9xy^2)=-4x+3y^3 \\
\begin{aligned}
    \dydx&=\frac{-4x+3y^3}{-1-9xy^2} \\[1em]
    &= \frac{4x-3y^3}{9xy^2+1}
\end{aligned}
$$


# Problem 4
Find the critical points of $f(x)=x^3-3x+1$ on the interval $[-3,2]$.

First, differentiate $f$.
$$
f'(x) = 3x^2 - 3
$$

Then, find the critical points by solving for $x$ at $f'(x)=0$.
$$
3x^2 - 3 = 0 \\
3(x^2-1) = 3(x+1)(x-1) = 0 \\
\therefore x=\pm1
$$

The extreme values of $f$ are at $x=-1$ and $x=1$, where $f(-1)=-3$ and $f(1)=-1$.

To determine if these are a minima or maxima, we can use the second derivative test.
$$
f'(x) = 3x^2 - 3 \implies f''(x) = 6x \\
f''(-1) = 6(-1) = -6 \implies \text{concave down, local max} \\
f''(1) = 6(1) = -6 \implies \text{concave up, local min}
$$

# Problem 5

Consider the function $f(x) = 3x^5-20x^3$.
1. Find the critical points.
2. Find the intervals where the function is increasing/decreasing.
3. Find out what extrema these critical points are.
4. Find all inflection points.

## Finding the critical points
$$
f(x)=3x^5-20x^3\implies f'(x)=15x^4-60x^2 \\
15x^4-60x^2 = 0 \\
15x^2(x^2-4) = 15x^2(x+2)(x-2) = 0 \\
\therefore x = -2,0,2
$$



## Finding the intervals where the function is increasing/decreasing

<center>

|  $x$  | $f'(x)$ |
| :---: | :-----: |
| $-3$  |  $675$  | $f'(x)>0$, increasing  |
| $-2$  |   $0$   | critical point, maxima |
| $-1$  |  $-45$  | $f'(x)<0$, decreasing  |
|  $0$  |   $0$   | critical point         |
|  $1$  |  $-45$  | $f'(x)<0$, decreasing  |
|  $2$  |   $0$   | critical point, minima |
|  $3$  |  $675$  | $f'(x)>0$, increasing  |

</center>

Therefore, we have that $f$ is increasing in the interval $(-\infty, -2)\cup(2,\infty)$ and is decreasing on the interval $(-2,0)\cup(0,2)$.

## Finding out what extrema these critical points are

We kind of already did that in the previous part.

The minima of $f$ is at $x=2$. The maxima of $f$ is at $x=-2$. And $x=0$ is neither a minima or maxima.

## Finding all inflection points

Find $f''(x)$ and find $x$ where $f''(x)=0$.

$$
f'(x)=15x^4-60x^2 \implies f''(x)=60x^3-120x \\
60x^3-120x = 0 \\
60x(x^2-2) = 0 \\
\therefore x = -\sqrt{2}, 0, \sqrt{2}
$$

The inflection points of $f$ are at $x = -\sqrt{2}, 0, \sqrt{2}$.
