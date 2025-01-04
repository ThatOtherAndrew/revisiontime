> "If maths is so great, why isn't there a Maths 2?"

<sup>- some silly goose who didn't anticipate *complex arithmetic*</sup>

It's the counting you know and love, but now *even more* [[Imaginary Number|imaginary]] than before! Instead of simple, boring, real-number land, we're venturing into the funky terrain of manipulating [[Complex Number|complex numbers]] now, woohoo!

For the most part, arithmetic with complex numbers can be performed just by considering the imaginary unit $i$ to be like any other old variable, then sprinkling in a bit of algebra to push things around.

>[!info]- Magenta colour-coding
>All imaginary parts in expressions on this page will be highlighted a lovely shade of <span style="color: magenta">magenta</span>, to make them easier to follow.
>
><sub>Yes, this took way too long to typeset.</sub>

## Addition

### Real
Add the real number to the real part. That's it.
$$
\begin{aligned}
& (a {\color{magenta} {}+ bi}) + c \\
={} & (a + c) {\color{magenta} {}+ bi}
\end{aligned}
$$

### Complex
To add two complex numbers together, you simply **add the real and imaginary parts separately**. Simples!

$$
\begin{aligned}
& (a {\color{magenta} {}+ bi}) + (c {\color{magenta} {}+ di}) \\
={} & (a + c) {\color{magenta} {}+ (b + d)i}
\end{aligned}
$$

> [!example]
> #todo 

## Subtraction

### Real
I'm not gonna insult your intelligence by explaining this to you.[^1] Go on, click the link. You'll figure it out. I believe in you.
[[Complex Arithmetic#Addition#Real]]

[^1]: That was a lie; I'd *absolutely* insult your intelligence. Many times over. Adding a sprinkle of snarkiness to these notes gives it a unique flair and makes them more fun to write, you see.

### Complex
Just like with the [[#addition]] of complex numbers shown above, we can **subtract the real and imaginary parts separately**:

$$
\begin{aligned}
(a {\color{magenta} {}+ bi}) & {\color{yellow} {}-{}} (c {\color{magenta} {}+ di}) \\
=(a {\color{yellow}{}-{}} c) & {\color{magenta} {}+ (b {\color{yellow} {}-{}} d)i}
\end{aligned}
$$

> [!example]
> #todo 

## Multiplication

### Real
Multiplying a complex number by a real number is dead simple - just multiply out the brackets! Even a toddler can do this while blindfolded and suspended upside down, so you have no excuse here.

$$
\begin{aligned}
& (a {\color{magenta} {}+ bi}) \times c \\
={} & ca {\color{magenta} {}+ cbi}
\end{aligned}
$$

### Complex
When multiplying two complex numbers, we take a very similar approach of multiplying everything out:

$$
\begin{aligned}
& (a+{\color{magenta} bi})(c+{\color{magenta} di}) \\
={}& a(c+{\color{magenta} di}) + {\color{magenta} bi}(c+{\color{magenta} di}) \\
={}& ac + {\color{magenta} adi} + {\color{magenta} bci} + bdi^2
\end{aligned}
$$

Since we know that $i^2 = -1$, the last term can be simplified:

$$
\begin{aligned}
& ac + {\color{magenta} adi} + {\color{magenta} bci} - bd \\
={}& (ac - bd) {\color{magenta} {}+ (ad + bc)i}
\end{aligned}
$$

Some people like to memorise the last step of the working above as a formula. I'm not a fan of that. Just do the middle-school algebra please.

> [!example]
> #todo 

## Division
A-ha! Addition, subtraction and multiplication of complex numbers has been mere child's play; division is our first taste of things starting to get slightly *spicy*~

### Real
Just like with addition and subtraction, dividing a complex number by a real number isn't too different from multiplication - we can still just distribute the operation across the real and imaginary parts. After all, division is the same as multiplying by the <abbr title="1 divided by the number">reciprocal</abbr>:

$$
\begin{aligned}
& \frac{a {\color{magenta} {}+ bi}}{c} \\
={} & \frac{1}{c}(a {\color{magenta} {}+ bi}) \\
={} & \frac{a}{c} {\color{magenta} {}+ \frac{b}{c}i}
\end{aligned}
$$

> [!warning]
> make sure $c \neq 0$ or Bad Things™️ will happen!

### Complex
Let's try to do the same thing as if we were [[#Division#Real|dividing by a real number]]:

$$
\begin{aligned}
& \frac{a {\color{magenta} {}+ bi}}{c {\color{magenta} {}+ di}} \\
={} & \frac{a}{c {\color{magenta} {}+ di}} + \frac{\color{magenta} bi}{c {\color{magenta} {}+ di}}
\end{aligned}
$$

...aaaaand we're stuck. This is no good; we can't simplify this into $a {\color{magenta} {}+ bi}$ form!

Instead, let's introduce a new tool from our mathematical toolbox: the [[complex conjugate]]. This tool is powerful, because when multiplied, it can **turn any complex number into a real number**. As such, we can use it to make the denominator real!

![[get_real.png|Sorry, I just couldn't resist.|300]]

$$
\begin{aligned}
& \frac{a {\color{magenta} {}+ bi}}{c {\color{magenta} {}+ di}} \\
={} & \frac{a {\color{magenta} {}+ bi}}{c {\color{magenta} {}+ di}} \color{yellow} \times \frac{c - di}{c - di} \\
={} & \frac{(a {\color{magenta} {}+ bi})(c {\color{magenta} {}- di})}{c^{2} + d^{2}}
\end{aligned}
$$
From here, we can [[#Multiplication#Complex|multiply out the numerator]]:

$$
= \frac{(ac + bd) {\color{magenta} {}+ (bc - ad)i}}{c^{2} + d^{2}}
$$

Then finally, we can [[#Division#Real|divide the complex numerator by the real denominator]] to get our nice and pretty $a \color{magenta} {}+ bi$ form:

$$
= \frac{ac + bd}{c^{2} + d^{2}}
\color{magenta} + \frac{bc - ad}{c^{2} + d^{2}}i
$$

"Nice and pretty"...

The algebra looks horrible, but it's cleaner with actual numbers; I promise. Again, you'd be a couple backslashes short of a LaTeX expression to memorise the above result as a formula instead of just using the intuitive method demonstrated above.

> [!example]
> #todo 
