Hyperbolic functions are like evil twins of trigonometric functions; just as trigonometric functions relate to circles, hyperbolic functions relate to [[Hyperbola|hyperbolae]]. In the mathematical family tree, they are closely related to **exponential functions** as well.

> [!tip] Curious about where this all comes from?
> Check out the *incredibly* written page on the [[Anatomy of a Hyperbola]], which dives deeper than the Mariana Trench on all the nitty-gritty workings of hyperbolae and hyperbolic functions.

Each trigonometric function's doppelganger can be obtained by slapping a fat $\text{h}$ after the function name:

| Trigonometric |  Hyperbolic   |
|:-------------:|:-------------:|
|    $\sin$     |    $\sinh$    |
|    $\cos$     |    $\cosh$    |
|    $\tan$     |    $\tanh$    |
|    $\sec$     | $\text{sech}$ |
|    $\csc$     | $\text{csch}$ |
|    $\cot$     |    $\coth$    |

Let's take a closer look at each of these hyperbolic functions individually.

## Function definitions

### sinh

The **hyperbolic sine** function is defined as follows:

$$
\sinh x = \frac{e^x-e^{-x}}{2}
$$

Why? ~~I dunno, go ask your mother.~~ Check out [[Anatomy of a Hyperbola]].[^1]

[^1]: Originally, this snarky response was because I had not the slightest of clues as to where this definition came from, and this footnote contained a link to the [BetterExplained article on hyperbolic functions](https://betterexplained.com/articles/hyperbolic-functions/). However, now there's an awesome page touching on the topic in this very wiki! Does this imply the author of the page is now our collective mothers? Let's not think about that!

The graph of $y = \sinh x$ looks something like this:

<iframe src="https://desmos.com/calculator/rfwkmbdhs8?embed" width="100%" style="min-height: 500px"></iframe>

Note how the function is asymptotic to both $\dfrac{e^{x}}{2}$ and $-\dfrac{e^{-x}}{2}$. This is because as $x$ gets really big (i.e. approaches $+\infty$), $e^{-x}$ gets really small and approaches zero, leaving behind just the other term - and inversely, when $x$ approaches $-\infty$ then $e^{x}$ gets really small.

### cosh

The **hyperbolic cosine** function is defined very similarly, but with a sign flipped:

$$
\cosh x = \frac{e^x+e^{-x}}{2}
$$

I still don't know why; go ask your father.

The graph of $y = \cosh x$ looks a bit like this:

<iframe src="https://desmos.com/calculator/dxfhgr0v6l?embed" width="100%" style="min-height: 500px"></iframe>

Note how again, the function is asymptotic to its two constituent exponential parts being summed together, for the same reason as with the [[#Function Definitions#sinh|sinh function]].

### tanh
Just like how $\tan=\dfrac{\sin}{\cos}$:

$$
\begin{aligned}
\tanh &= \frac{\sinh}{\cosh} \\
&= \frac{e^x-e^{-x}}{2} \div \frac{e^x+e^{-x}}{2} \\
&= \frac{e^x-e^{-x}}{\cancel{ 2 }} \times \frac{\cancel{ 2 }}{e^x+e^{-x}} \\
&= \frac{e^{x}-e^{-x}}{e^{x}+e^{-x}}
\end{aligned}
$$

The graph of $y = \tanh x$ looks a little like this:

<iframe src="https://desmos.com/calculator/94ruwrtkla?embed" width="100%" style="min-height: 500px"></iframe>

Note how the function is asymptotic to both $y = 1$ and $y = -1$. This property makes the function very useful for *interpolation* in applied mathematics, which is a fancy word which means smoothly filling in the space between two numbers.

### sech, csch, coth
Just as there exist **secant, cosecant and cotangent** functions which are the reciprocals of the **sine, cosine and tangent** functions respectively, there are also **hyperbolic equivalents**:

$$
\begin{aligned}
\color{#ed514c} \text{sech}\, x &= \frac{1}{\cosh x} = \frac{2}{e^x+e^{-x}} \\
\color{#3687d9} \text{csch}\, x &= \frac{1}{\sinh x} = \frac{2}{e^x-e^{-x}} \\
\color{#47b259} \coth x &= \frac{1}{\tanh x} = \frac{\cosh x}{\sinh x} = \frac{e^{x}+e^{-x}}{e^{x}-e^{-x}}
\end{aligned}
$$
Here's how the functions look when plotted:

<iframe src="https://desmos.com/calculator/0ltyed0ytb?embed" width="100%" style="min-height: 500px"></iframe>

## Linking trigonometric and hyperbolic functions

Okay, so clearly there's *some* sort of romantic tension between the trig and hyp families - from the similar naming and each function having a doppelganger, to the way in which their identities look so similar. But how do we actually, properly, relate the two?

### Parametric plots of cos/cosh, sin/sinh
If we were to parametrically plot $(\cos t, \sin t)$, we would get the following:

<iframe src="https://desmos.com/calculator/zkmbzoebfz?embed" width="100%" style="min-height: 500px"></iframe>

A lovely circle! :D

Now, what if we used $(\cosh t, \sinh t)$ instead?

<iframe src="https://desmos.com/calculator/kgov9btwf7?embed" width="100%" style="min-height: 500px"></iframe>

A-ha, there's half of our [[unit hyperbola]]!

> [!question]
> I wonder what happens when you plug in a complex value for $t$? Would that allow me to reach the other, dashed arm of the hyperbola?

### Using the imaginary unit
For some reason, bringing [[Imaginary Number|imaginary numbers]] into these functions bridges the gap between the circular trigonometric functions and the hyperbolic ones. It feels like a bridge from black magic!

Why does the following work? I have absolutely no clue, and wish I understood it better. There are proofs, but they don't sit quite right in my head yet.

#### cos and cosh
The hyperbolic cosine is actually equivalent to just **multiplying the inside of the cosine function by the [[Imaginary Number#Imaginary Unit|imaginary unit]]**:

$$
\cosh x = \cos {\color{magenta} i}x
$$

Surprisingly, this works the other way too!

$$
\cos x = \cosh {\color{magenta} i}x
$$

> [!question]
> I wonder if there's any way to visualise this as "remapping" the real and imaginary axes as inputs to the $\cos$ and $\cosh$ functions, and if there's any way to link that to conic sections.
> 
> If I had a plane intersecting a cone to create a circular intersection, I could rotate that plane by a right angle for it to intersect "vertically" with the cone instead, creating a hyperbolic intersection instead. Is that right-angle rotation possibly linked in any way to this multiplication by $i$?

#### sin and sinh
Unfortunately, bridging the gap between circular and hyperbolic sine functions isn't quite as pretty, but it's still doable. We just need to multiply the outside of the function by $-i$ as well:

$$
\begin{aligned}
\sinh x &= {\color{magenta} -i} \sin {\color{magenta} i}x \\
\sin x &= {\color{magenta} -i} \sinh {\color{magenta} i}x
\end{aligned}
$$

### Osborn's rule
Osborn's rule states that you can take "any" existing trigonometric identity, substitute $\sin$ with $\sinh$, $\cos$ with $\cosh$, as long as you *negate every product of sines* (i.e. $\sin^{2}x$ becomes $-\sinh ^{2}x$).

> [!warning] 
> Keep in mind that Osborn's rule is somewhat of a hand-wavey rule of thumb! Be careful, as equations can be rearranged and manipulated to disguise or spawn in $\sin^{2}$ terms.

For instance, if we were to take the trigonometric identity $\cos^{2} x + \sin^{2} x = 1$ (derived from Pythagoras' theorem), we get $\cosh^{2} x - \sinh^{2} x = 1$.

> [!important]
> This identity is **very useful** - make sure you know it!
> 
> Here it is again for good measure:
> 
> $$\cosh^{2} x - \sinh^{2} x = 1$$

## Inverse hyperbolic functions

So far, we've assembled a whole family of functions which map $a \to b$. But what if we wish to go the other way? We need to define some **inverse functions** which can map $b \to a$ instead.

However, since some of the hyperbolic functions don't have a $1:1$ mapping from input to output, we need to be a little careful and **restrict the domain** to avoid any "mapping conflicts".

### sinh⁻¹
#todo

### cosh⁻¹
#todo

### tanh⁻¹
#todo

## Calculus with hyperbolic functions
All of these hyperbolic functions are integratable and differentiable similarly to our regular ol' trigonometric functions, so we can do calculus with them!

### Differentiation
> [!summary]+ Summary of derivatives of hyperbolic functions
> 
> You do not need to know this table off by heart, but you should be able to work out the derivative on paper where necessary.
> 
> | $f(x)$ Function   | $f'(x)$ Derivative             | Domain (if applicable) |
> | ----------------- | ------------------------------ | ---------------------- |
> | $\sinh x$         | $\cosh x$                      |                        |
> | $\cosh x$         | $\sinh x$                      |                        |
> | $\tanh x$         | $\text{sech}^{2}\, x$          |                        |
> | $\text{sech}\, x$ | $-\tanh x\, \text{sech}\, x$   |                        |
> | $\text{csch}\, x$ | $-\coth x\, \text{csch}\, x$   |                        |
> | $\coth x$         | $-\,\text{csch}^{2}\, x$       |                        |
> | $\sinh^{-1} x$    | $\frac{1}{\sqrt{ x^{2} + 1 }}$ | $x \in \mathbb{R}$     |
> | $\cosh^{-1} x$    | $\frac{1}{\sqrt{ x^{2} - 1 }}$ | $x \in [1, \infty)$    |
> | $\tanh^{-1} x$    | $\frac{1}{1 - x^{2}}$          | $x \in (-1, 1)$        |

#### sinh
Given we [[#Function Definitions#sinh|know how to express]] $\sinh x$ exponentially, let's try differentiating that:

$$
\begin{aligned}
\frac{d}{dx}(\sinh x) &= \frac{d}{dx} \left( \frac{e^x-e^{-x}}{2} \right) \\
&= \frac{d}{dx} \left( \frac{1}{2}e^{x} - \frac{1}{2}e^{-x} \right) \\
&= \frac{1}{2}e^{x} + \frac{1}{2}e^{-x} \\
&= \frac{e^{x}+e^{-x}}{2} \\
&= \cosh x
\end{aligned}
$$

Woah, isn't that pretty! :O

The derivative of $\sinh$ is $\cosh$, just as the derivative of $\sin$ is $\cos$:

$$
\frac{d}{dx} \sinh x = \cosh x
$$

Maybe $e$ isn't such a scary monster after all. When working with calculus, $e$ is my friend. I like you now, $e$.

![[Hyperbolic Function 1.excalidraw.svg|sinh(x) differentiates to cosh(x).]]

#### cosh
Just as with $\sinh$ [[#Differentiation#sinh|above]], let's try differentiating $\cosh$'s [[#Function Definitions#cosh|exponential form]] to see what we get:

$$
\begin{aligned}
\frac{d}{dx}(\cosh x) &= \frac{d}{dx} \left( \frac{e^x+e^{-x}}{2} \right) \\
&= \frac{d}{dx} \left( \frac{1}{2}e^{x} + \frac{1}{2}e^{-x} \right) \\
&= \frac{1}{2}e^{x} - \frac{1}{2}e^{-x} \\
&= \frac{e^{x}-e^{-x}}{2} \\
&= \sinh x
\end{aligned}
$$

Woah, we've come full circle! The derivative of $\cosh$ is $\sinh$, not to be confused with the derivative of $\cos$ which gets its sign flipped to $-\sin$.

$$
\frac{d}{dx} \cosh x = \sinh x
$$

This completes the following "differentiation cycle" between $\sinh$ and $\cosh$:

![[Hyperbolic Function 2.excalidraw.svg|cosh(x) also differentiates to sinh(x).]]

> [!question]
> $\sinh x$ and $\cosh x$ both differentiate to each other, forming a "differentiation cycle" of two elements. $\sin x \to \cos x \to -\sin x \to -\cos x$ would form a cycle of four elements, and $e^{x}$ would be a cycle of one element as it differentiates to itself.
> 
> **Do there exist any other such cycles?**
> 
> If yes, how many are there? Is it possible to have multiple cycles with the same number of elements in it?
> 
> If no, how can we prove that there can be no more such cycles that exist?


#### tanh
We can use the **quotient rule** and our newfound knowledge of the **derivatives of [[#Differentiation#sinh|sinh]] and [[#Differentiation#cosh|cosh]]** to find the derivative of $\tanh x$:

$$
\frac{d}{dx}\left( \frac{{\color{dodgerblue} f(x)}}{{\color{orange} g(x)}} \right)
= \frac
    {
        {\color{dodgerblue} f'(x)}{\color{orange} g(x)}
        - {\color{dodgerblue} f(x)}{\color{orange} g'(x)}
    }
    {({\color{orange} g(x)})^{2}}
$$

$$
\begin{aligned}
\frac{d}{dx}(\tanh x) &= \frac{d}{dx} \left( \frac{\color{dodgerblue} \sinh x}{\color{orange} \cosh x} \right) \\
&= \frac{{\color{dodgerblue} \cosh x \color{orange} \cosh x} + {\color{dodgerblue} \sinh x \color{orange} \sinh x}}{({\color{orange} \cosh x})^{2}} \\
&= \frac{\cosh^{2}x - \sinh^{2}x}{\cosh^{2}x} \\
\end{aligned}
$$

Since we know from [[#Osborn's Rule]] that $\cosh^{2}x - \sin^{2}x = 1$, we can use this identity to simplify further:

$$
\begin{aligned}
& \frac{\cosh^{2}x - \sinh^{2}x}{\cosh^{2}x} \\
={}& \frac{1}{\cosh^{2}x} \\
={}& \text{sech}^{2}\,x
\end{aligned}
$$

And there we have it!

$$
\frac{d}{dx}(\tanh x) = \text{sech}^{2}\,x
$$

#### sech, csch, coth
The derivatives of the [[#Function Definitions#sech, csch, coth|hyperbolic secants, cosecants and cotangents]] can be worked out on the spot by rewriting them in terms of [[#Differentiation#sinh|sinh]], [[#Differentiation#cosh|cosh]] and [[#Differentiation#tanh|tanh]] and using the **quotient rule**:

> [!example]- Derivative of $\text{sech}\,x$
> $$
> \begin{aligned}
> \frac{d}{dx}(\text{sech}\, x) &= \frac{d}{dx}\left( \frac{1}{\cosh x} \right) \\
> &= \frac{-\frac{d}{dx}(\cosh x)}{\cosh^{2} x} \\
> &= \frac{-\sinh x}{\cosh^{2} x} \\
> &= - \left( \frac{\sinh x}{\cosh x} \right) \left( \frac{1}{\cosh x} \right) \\
> &= - \tanh x\ \text{sech}\,x
> \end{aligned}
> $$

> [!example]- Derivative of $\text{csch}\,x$
> $$
> \begin{aligned}
> \frac{d}{dx}(\text{csch}\, x) &= \frac{d}{dx}\left( \frac{1}{\sinh x} \right) \\
> &= \frac{-\frac{d}{dx}(\sinh x)}{\sinh^{2} x} \\
> &= \frac{-\cosh x}{\sinh^{2} x} \\
> &= - \left( \frac{\cosh x}{\sinh x} \right) \left( \frac{1}{\sinh x} \right) \\
> &= - \coth x\ \text{csch}\,x
> \end{aligned}
> $$

> [!example]- Derivative of $\coth x$
> $$
> \begin{aligned}
> \frac{d}{dx}(\coth x) &= \frac{d}{dx}\left( \frac{1}{\tanh x} \right) \\
> &= \frac{-\frac{d}{dx}(\tanh x)}{\tanh^{2} x} \\
> &= \frac{-\, \text{sech}^{2}\, x}{\tanh^{2} x} \\
> &= - \left( \frac{1}{\cosh^{2} x} \right) \left( \frac{\cosh^{2} x}{\sinh^{2} x} \right) \\
> &= - \frac{1}{\sinh^{2} x} \\
> &= -\,\text{csch}^{2}\, x
> \end{aligned}
> $$

#### sinh⁻¹
#todo 

#### cosh⁻¹
#todo 

#### tanh⁻¹
#todo 

### Integration

#### sinh
#todo

#### cosh
#todo

#### tanh
#todo
