The complex conjugate of a [[Complex Number|complex number]] simply has its **[[Imaginary Number|imaginary]] part negated**.

The following complex numbers are complex conjugates of each other:

$$
\begin{aligned}
a {\color{magenta} {}+ bi} \\
a {\color{magenta} {}- bi}
\end{aligned}
$$

>[!info]- Magenta colour-coding
>All imaginary parts in expressions on this page will be highlighted a lovely shade of <span style="color: magenta">magenta</span>, to make them easier to follow.
>
><sub>Yes, this took way too long to typeset.</sub>

The complex conjugate of a variable is usually denoted by a horizontal line above the variable. For example, a complex number $z$ would have a complex conjugate $\bar{z}$.

A real number is equal to its complex conjugate, as adding or subtracting the complex part makes no difference.

## Multiplying conjugates

If you multiply a complex number by its conjugate, following the process of [[Complex Arithmetic#Multiplication#Complex|multiplying two complex numbers together]] it simplifies as follows:

$$
\begin{aligned}
& (a {\color{magenta} {}+ bi})(a {\color{magenta} {}- bi}) \\
={}& a^{2} {\color{magenta} {}+ abi} {\color{magenta} {}- abi} - b^{2}i^2
\end{aligned}
$$

Notice how the imaginary terms cancel out, and that $i^2$ is $-1$:

$$
\begin{aligned}
={}& a^{2} \cancel{ {\color{magenta} {}+ abi} {\color{magenta} {}- abi} } + b^{2} \\
={}& a^2 + b^{2}
\end{aligned}
$$

Now isn't that pretty!

> [!tip]
> Multiplying a complex number by its conjugate is a **reliable way to make it real** (i.e. get rid of the imaginary part).
> 
> In fancy maths notation:
> 
> $$
> z \bar{z} \in \mathbb{R}
> $$

## Adding and subtracting conjugates

Less useful than multiplying conjugates, but still good to know.

If you add a complex number with its conjugate, the ${\color{magenta} +bi}$ and ${\color{magenta} -bi}$ cancel out, leaving just two times the real part left behind:

$$
\begin{aligned}
& (a {\color{magenta} {}+ bi}) + (a {\color{magenta} {}- bi}) \\
={} & a + a \cancel{\color{magenta} + bi - bi} \\
={} & 2a
\end{aligned}
$$

If you subtract the conjugate instead, you get two times the imaginary part left behind instead:

$$
\begin{aligned}
& (a {\color{magenta} {}+ bi}) - (a {\color{magenta} {}- bi}) \\
={} & \cancel{a - a} \color{magenta} + bi + bi \\
={} & \color{magenta} 2bi
\end{aligned}
$$
