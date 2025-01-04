Consider the following equation:

$$
x^2 - y^2 = 1
$$

> [!note]
> Notice how the equation compares to the equation of a unit circle, $x^2 + y^2 = 1$.

Spoiler alert: This is the equation of the **unit hyperbola**.

We can rearrange this to make $y$ the subject:

$$
y^2 = x^2 - 1
$$

$$
y = \pm\sqrt{x^2 - 1}
$$

Consider how the function would behave as we make the value of $x$ very big in either the positive or negative direction. The $- 1$ alongside it under the square root becomes near-insignificant, leaving the square and square root to cancel out:

$$
\begin{gathered}
y \approx \pm \color{red} \sqrt{
	\color{lightgrey} (\text{really big }x)^{\color{red} 2}
} \\
y \approx \pm\ \text{really big }x
\end{gathered}
$$

We know that **as $x$ approaches $\pm\ \infty$, the function approaches $y = \pm\ x$**, meaning there are **asymptotes** of $y = x$ and $y = -x$. We also know that the function is **symmetric across the x-axis** (because of the $\pm$).

Now consider what has to happen for $y$ to be zero, to figure out where this function would cross the x-axis:

$$
\begin{gathered}
0 = \pm \sqrt{ x^2 - 1 } \\
x^2 - 1 = 0 \\
x^2 = 1 \\
x = \pm\ 1
\end{gathered}
$$

We now know that the function must also pass through the points $(1, 0)$ and $(-1, 0)$ as well.

This is enough to provide a basic intuition for the shape of the graphed function:

<iframe src="https://desmos.com/calculator/5aqlpv2t3c?embed" width="100%" style="min-height: 500px"></iframe>

Let's finally take a look at the function in all its hyperbolic glory:

<iframe src="https://desmos.com/calculator/fcebs8loxj?embed" width="100%" style="min-height: 500px"></iframe>

Yippee!
