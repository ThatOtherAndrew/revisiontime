---
description: Answering questions about how hyperbolic functions relate to hyperbolae, where they come from, why e is involved, and more.
---

> [!quote]- Contribution by Lucilla
> This page is based on a document submitted by my very good (non-StA) friend and mathematician **Lucilla**.
> 
> Have something to contribute? Check out the **[[Contribution Guide]]**!

> [!warning] Beyond the module
> This page covers content which goes **beyond what is required** for the module. Read on, but don't worry if you don't recognise or understand all of it!
> 
> If you're looking for what's strictly covered under the module content, the following pages may be of interest to you:
> - [[Hyperbolic Function]]
> - [[Hyperbola]]
> - [[Unit Hyperbola]]

Okay, so you know the definitions of the [[Hyperbolic Function|hyperbolic functions]] and that they're supposed to relate to hyperbolae in the same way that [[Hyperbolic Function#Linking trigonometric and hyperbolic functions|trigonometric functions do to circles]].

But how exactly? And where did they come from? Who thought they were a good idea? And why are they defined with these silly equations involving $e^x$ rather than some cool geometric diagram?

"Well," you might answer, "just as parametrically plotting $(\cos t, \sin t)$ gives a circle, so does plotting $(\cosh t, \sinh t)$ give a hyperbola. Well, only the right half of it, but you get the idea."

But so what? The [[unit hyperbola]] is the set of points $(x, y)$ satisfying $x^2 - y^2 = 1$. So *any* pair of functions $(C(t), S(t))$ such that $S(t)$ spans the whole real line and $C(t)^2 - S(t)^2 = 1$ will *also* give a parameterisation of the unit hyperbola. For example, $(\sec t, \tan t)$. Or even $(\sqrt{t^2 + 1}, t)$!

<iframe src="https://www.desmos.com/calculator/qkkxyyipzv?embed" width="100%" style="min-height: 500px"></iframe>

Okay, okay. Parameterisations are too open-ended. But there's another analogy we can draw. $(\cos t, \sin t)$ are the coordinates of a point that has travelled from $(1, 0)$ counterclockwise along the unit circle by an angle of $t$ radians. Perhaps if we just switch out the word "circle" for "hyperbola" there, we'll get the hyperbolic functions?

Well, not quite. The unit hyperbola never really goes beyond 45 degrees: in fact, it's asymptotic to both the lines $y = x$ and $y = -x$. So if that was a defining property of the hyperbolic functions, then the graphs of $y = \cosh x$ and $y = \sinh x$ would need to have a huge vertical asymptote around the $\frac{1}{8} \cdot 2\pi$ mark. Not only that, but there's no point on the hyperbola at all that is 60 or 90 or 120 degrees counterclockwise from $(1, 0)$: there'd be blank space on the graph until $\frac{3}{8} \cdot 2\pi$, when the graph enters back into view from another vertical asymptote. And, anyway, such graphs'd need to repeat every $2\pi$ units. That's not at all what the graphs of $\cosh$ and $\sinh$ look like, so that can't be it.

Fortunately, that analogy is *almost* true. We just have to use a slightly different starting point: instead of characterising $(\cos t, \sin t)$ as the point you reach when the angle you've travelled is $t$, characterise it as the point you reach when the *area* of the subtended sector is $t/2$. *Now* the shift to the hyperbolic world works just as you'd expect:

<iframe src="https://www.desmos.com/calculator/cbacw5jac1?embed" width="100%" style="min-height: 500px"></iframe>

But why does that even work? Why would defining something with a weird combination of exponentials give you a function that tracks areas subtended by a hyperbola?

The path to explaining this is a long one, and it'll lead us to a bunch of pretty discoveries along the way as we get to the bottom of What Hyperbolic Functions Truly Are. And to start, let's go back to the very beginning: the exponential function.

## Derivatives all the way down

Think back in time to when you first learned how to differentiate. You probably recall the *power rule*, which, along with the fact that derivatives play nicely with sums and scalar multiples, lets you differentiate any polynomial. But now you want to spice it up a little. You're asking yourself a neat interesting question: is there a function which is *its own* derivative?

Well, the simplest function we can probably imagine is the constant zero function, which just takes the value 0 everywhere. That's a constant function, so its derivative is 0 everywhere, which is equal to the function itself, voilà! We found one.

But that's hardly interesting; we want a function with some really funky behavior that still manages to be equal to its own derivative everywhere. Let's say that in order to explicitly exclude the constant zero function, we'll additionally require our target function to take the value 1 at 0. So we're looking for a function $f$ that satisfies $f' = f$ and $f(0) = 1$.

Okay, what's the simplest function we can imagine that takes the value 1 at 0? The constant 1 function! Alright, that one doesn't work; being constant, its derivative is still 0, which this time isn't equal to the function itself. We need its derivative to be 1.

Let's not give up. We can fix the discrepancy by adding a linear term, $ax$ for some constant $a$: this term would vanish at 0, so it wouldn't break $f(0) = 1$; and it's non-constant, so it could help us set the derivative at 0 to be 1. Since $ax$ differentiates to $a$, this means $a$ needs to be 1; so now $f(x) = 1 + x$ and its derivative is 1.

But wait! While we worked on fixing the discrepancy, the goalposts themselves moved by one step! Now we need the derivative to be $1 + x$, not just 1. We can keep going and add a quadratic term whose derivative is $x$; that'd be $\frac{1}{2} x^2$, if you remember your calculus, so now $f(x) = 1 + x + \frac{1}{2} x^2$ and its derivative is $1 + x$. Agh, but now $f$ itself is again one step ahead, now we need the derivative to have that $\frac{1}{2} x^2$ term! And it'll keep doing that forever, because every time we want to add a term to fix $f'$, that same term will move the goalposts away by one step.

But all hope is not lost. Maybe if we do this for *infinitely many* steps, then we will indeed get a function whose derivative is itself: when differentiating, the constant 1 term would vanish, and the $(n + 1)$-th power term would turn into the $n$-th power term; ordinarily that would leave a gap at the end, but since with infinity there *is* no end, everything works out perfectly, [Hilbert's Hotel](https://en.wikipedia.org/wiki/Hilbert's_paradox_of_the_Grand_Hotel) style.

$$
\small
\begin{array}{rrcrcrcrcrcl}
f(x) = & & & 1 & & +\ x & & +\ \frac{1}{2} x^2 & & +\ \frac{1}{6} x^3 & & +\ \ldots \\
& & \swarrow & & \swarrow & & \swarrow & & \swarrow & & \swarrow \\
f'(x) = & 0 & & +\ 1 & & +\ x & & +\ \frac{1}{2} x^2 & & +\ \frac{1}{6} x^3 & & +\ \ldots
\end{array}
$$

> [!question]
> What is the sequence of denominators here? In other words, if the $n$-th power term of $f$ is $\frac{1}{a_n} x^n$, what is $a_n$?

Nice, so if we put aside the question of whether this sum converges,[^1] we actually did find a function $f$ which takes the value 1 at 0 and equals its own derivative! And clearly it's doing something funkier than just constant zero.

[^1]: This sum does indeed converge for every $x$, so this function is indeed well-defined for all real numbers. There's probably several ways to verify this: here's one I came up with. First, I gotta spoil that those denominators are factorials: the summands are $\frac{x^n}{n!}$ for $n$ from 0 to infinity. (The factorials come from repeatedly applying the power rule; you multiply by $n$ but lower the exponent to $n - 1$, so next time you'll multiply by $n - 1$, and so on.) Note that $n!$, being $1 \cdot 2 \cdot 3 \cdot \ldots \cdot n$, is the same as the geometric mean of all the numbers from 1 to $n$, raised to the power $n$. As $n$ increases, that geometric mean increases without bound; in particular, it always eventually exceeds any fixed $x$. In fact, it even eventually exceeds $2x$; from that point onwards, $\frac{x^n}{n!}$ is always less than $\frac{x^n}{(2x)^n} = \left( \frac{1}{2} \right)^n$, so the rest of the terms from that point onwards are bounded from above by a geometric series with common ratio $\frac{1}{2}$. And we know that that series converges, so our original series also does. For large $x$ it can converge to something very big; after all, all we know is that *eventually* it'll turn to something smaller than a geometric series, and that "eventually" could take a very long time. But it will always be finite: the part before the Eventually will always have finitely many terms, and the part after the Eventually is always bounded by a geometric series.

## Is Its Own Derivative

So, we found a function equal to its own derivative which takes the value 1 at 0. Big deal, right? There's probably thousands of such functions.

Well, the interesting thing is, no, actually! The function we constructed, by constantly "moving the goalposts", is the *only* one.

Let's think about it again. The constant term couldn't have been anything other than 1, since all the higher terms will vanish at zero, and we want $f(0) = 1$. Now because $f' = f$, we also need $f'(0) = 1$; but the constant term obviously has zero derivative, and the quadratic and all higher terms will differentiate to at least linear terms, which, again, will vanish at zero. So the *only* term capable of controlling the value of the derivative at zero is the linear term: so that one also *has* to be $1x$.

The same argument can keep going: the value of the $n$-th derivative at 0 can be controlled *only* by the $n$-th power term, since all lower ones will have zero $n$-th derivative everywhere, and all higher ones will differentiate to at least something linear, and so will have zero $n$-th derivative at 0. And so, because we've specified the value of *every* order derivative at 0 (namely, all of them must be 1), we've uniquely determined the value of every power term.

This means our silly infinite polynomial is actually quite an important function indeed! Let's name it $\text{\color{lightblue}IIOD}(x)$, for "*Is Its Own Derivative* \[and, at 0, takes the value 1\]". Again, **it's the *unique* function with those two properties**.

Now the interesting thing is that we can generalise this a little. Since derivatives play along nicely with scalar multiplication, the derivative of $C \cdot \text{\color{lightblue}IIOD}(x)$ is also $C \cdot \text{\color{lightblue}IIOD}(x)$ for any real number $C$; and clearly such a function would take the value $C$ at 0. Also, by the chain rule, the derivative of $\text{\color{lightblue}IIOD}(\lambda \cdot x)$ is $\lambda \cdot \text{\color{lightblue}IIOD}(\lambda \cdot x)$; so such a function has the property that its derivative is $\lambda$ times itself. And in the same fashion as before, it turns out that $C \cdot \text{\color{lightblue}IIOD}(\lambda \cdot x)$ is the *unique* function whose derivative is $\lambda$ times itself and which takes the value $C$ at 0.[^2]

Keep this in mind. I'm gonna repeat it again for importance's sake:

> **The *only* function whose derivative is $\lambda$ times itself and which takes the value $C$ at 0 is $f(x) = C \cdot \text{\color{lightblue}IIOD}(\lambda \cdot x)$**.

With that in mind, we can try to figure out more about this mysterious function.

[^2]: You could prove this by either repeating the argument from above with these generalisations, or with a neat succinct indirect proof: suppose there existed another function $f$ whose derivative was $\lambda$ times itself and which took the value $C$ at 0; then $\frac{1}{C} f(x/\lambda)$ would be a function other than $\text{\color{lightblue}IIOD}$ equal to its own derivative and taking the value 1 at 0, a contradiction.

## Exponents all along?

Let's see just how much more we can find out about $\text{\color{lightblue}IIOD}$ just from its characteristic property of being equal to its own derivative.

We know the product rule says that the derivative of $f(x) \cdot g(x)$ is $f'(x) \cdot g(x) + f(x) \cdot g'(x)$. Let's see what happens when we apply the product rule to two differently scaled versions of $\text{\color{lightblue}IIOD}$:

$$
\begin{array}{cl}
& \big( \text{\color{lightblue}IIOD}(Ax) \cdot \text{\color{lightblue}IIOD}(Bx) \big)' \\[1ex]
= & \text{\color{lightblue}IIOD}(Ax)' \cdot \text{\color{lightblue}IIOD}(Bx) + \text{\color{lightblue}IIOD}(Ax) \cdot \text{\color{lightblue}IIOD}(Bx)' \\[1ex]
= & A \cdot \text{\color{lightblue}IIOD}(Ax) \cdot \text{\color{lightblue}IIOD}(Bx) + \text{\color{lightblue}IIOD}(Ax) \cdot B \cdot \text{\color{lightblue}IIOD}(Bx) \\[1ex]
= & (A + B) \cdot (\text{\color{lightblue}IIOD}(Ax) \cdot \text{\color{lightblue}IIOD}(Bx))
\end{array}
$$

Huh! So $\text{\color{lightblue}IIOD}(Ax) \cdot \text{\color{lightblue}IIOD}(Bx)$ has a derivative equal to $A + B$ times itself. But wait, we deduced earlier that the *only* such function is $\text{\color{lightblue}IIOD}((A + B)x)$. So they must be equal! Specifically, setting $x = 1$, we get:

$$
\text{\color{lightblue}IIOD}(A + B) = \text{\color{lightblue}IIOD}(A) \cdot \text{\color{lightblue}IIOD}(B).
$$

How peculiar! This $\text{\color{lightblue}IIOD}$ function has a property reminiscent of exponents.

What about the power rule? What if we try differentiating $\text{\color{lightblue}IIOD}(x)^n$?

$$
\begin{array}{cl}
& \big( \text{\color{lightblue}IIOD}(x)^n \big)' \\[1ex]
= & n \cdot \text{\color{lightblue}IIOD}(x)^{n - 1} \cdot \text{\color{lightblue}IIOD}(x)' \\[1ex]
= & n \cdot \text{\color{lightblue}IIOD}(x)^{n - 1} \cdot \text{\color{lightblue}IIOD}(x) \\[1ex]
= & n \cdot \text{\color{lightblue}IIOD}(x)^n
\end{array}
$$

So $\text{\color{lightblue}IIOD}(x)^n$ is a function whose derivative is $n$ times itself! And again, we know the *only* such function is $\text{\color{lightblue}IIOD}(n \cdot x)$, so:

$$
\text{\color{lightblue}IIOD}(x)^n = \text{\color{lightblue}IIOD}(n \cdot x)
$$

Again, just like exponents!

Perhaps you even know that the power rule works for all real exponents, not just natural-number ones. But if you don't, we can still extend that second property of $\text{\color{lightblue}IIOD}$ to at least all rational exponents.[^3] The property $\text{\color{lightblue}IIOD}(0) = 1$ plays along very nicely with all this; it implies the identity works for negative integers, since $1 = \text{\color{lightblue}IIOD}(0) = \text{\color{lightblue}IIOD}(n - n) = \text{\color{lightblue}IIOD}(n) \cdot \text{\color{lightblue}IIOD}(-n)$, so that $\text{\color{lightblue}IIOD}(-n)$ must be the reciprocal of $\text{\color{lightblue}IIOD}(n)$. And $\text{\color{lightblue}IIOD}(p/q)$ must be the $q$-th root of $\text{\color{lightblue}IIOD}(p)$, since $\text{\color{lightblue}IIOD}(p) = \text{\color{lightblue}IIOD}(p/q \cdot q) = \text{\color{lightblue}IIOD}(p/q)^q$.

[^3]: Exponentiation with a rational number can be defined relatively simply as $x^{p/q} = \sqrt[q]{x^p}$. Exponentiation with arbitrary *real* numbers, on the other hand, is a lot trickier to define. It basically requires proving that exponentiation is a continuous function (at every point except (0, 0)), and then "filling in the gaps". Illustratively, if for, say, $\sqrt{2}$, we pick some sequence $q_n$ of rational numbers that converges to it (say, 1, 1.4, 1.41, 1.414, ...), then the sequence $2^{q_n}$ will always converge to the same value no matter which sequence $q_n$ we picked: we define $2^{\sqrt{2}}$ to be that value.

## Always has been

Indeed, in this identity we can set $x = 1$ as well, and get the following:

$$
\text{\color{lightblue}IIOD}(\alpha) = \text{\color{lightblue}IIOD}(1)^{\alpha}
$$

Aha! So it *was* exponents all along! Amazingly, starting from just the requirement of being its own derivative, we found that $\text{\color{lightblue}IIOD}(\alpha)$ is secretly just the operation of raising $\text{\color{lightblue}IIOD}(1)$ to the power of $\alpha$.

So whatever this $\text{\color{lightblue}IIOD}(1)$ is, it must be a really important number! Let's try to find out what it is.

Since we know the infinite polynomial that defines $\text{\color{lightblue}IIOD}$, let's just plug in 1 and see what we get:

$$
\text{\color{lightblue}IIOD}(1) = 1 + 1 + \frac{1}{2} + \frac{1}{6} + \frac{1}{24} + \ldots
$$

$$
\begin{array}{rrrrrl}
1 & & & & & = 1 \\[1ex]
1 & +\ 1 & & & & = 2 \\[1ex]
1 & +\ 1 & +\ \frac{1}{2} & & & = 2.5 \\[1ex]
1 & +\ 1 & +\ \frac{1}{2} & +\ \frac{1}{6} & & = 2.666\ldots \\[1ex]
1 & +\ 1 & +\ \frac{1}{2} & +\ \frac{1}{6} & +\ \frac{1}{24} & = 2.708333\ldots
\end{array}
$$

So it's some number between 2 and 3, somewhere around 2.7.

By this point you're probably screaming at me. "Of course it's $e$! We knew it all along! We knew $e^x$ was its own derivative! We knew $\text{\color{lightblue}IIOD}$ was just $e^x$ all along!"

Yes, I admit, I made it excessively cryptic on purpose. I did that to drive the point home: *This* is what the place of $e$ in calculus is all about. $e$ is not about compound interest, or the limit of $(1 + \frac{1}{n})^n$, or, heck, even a raw dry definition of $e$ as that sum $1 + 1 + \frac{1}{2} + \frac{1}{6} + \ldots$ doesn't fully do it justice. **The true meaning of $e$ is that it is the value of $\text{\color{lightblue}IIOD}(1)$.** We were able to find the function equal to its own derivative without knowing about $e$ at all; $e$ derives from $\text{\color{lightblue}IIOD}$, not the other way around.

## Euler's formula

Remember that $\text{\color{lightblue}IIOD}$ is just a funky polynomial. An infinite one, true, but still just a function that involves only the four elementary operations.

And, hey, we know how to do the four elementary operations on complex numbers, too! There should be no harm in, say, plugging in $i$:

$$
\begin{array}{rrrrrrr}
\text{\color{lightblue}IIOD}(i) & = 1 & +\ i & +\ \frac{i^2}{2} & +\ \frac{i^3}{6} & +\ \frac{i^4}{24} & +\ \ldots \\[1.5ex]
& = 1 & +\ i & -\ \frac{1}{2} & -\ \frac{i}{6} & +\ \frac{1}{24} & +\ \ldots
\end{array}
$$

So the end result would be something like:

$$
\begin{array}{rl}
\text{\color{lightblue}IIOD}(i) & = \left( 1 - \frac{1}{2} + \frac{1}{24} - \ldots \right) + \left( 1 - \frac{1}{6} + \frac{1}{120} - \ldots \right) \cdot i \\[1.5ex]
& = 0.540302\ldots + 0.841471\ldots i
\end{array}
$$

The numbers are unusual, but the principle itself isn't strange: we're just plugging in complex numbers into a polynomial.

Here's something entirely different, for a change: what's the derivative of $\cos x + i \sin x$?

$$
\begin{array}{rl}
& \big( \cos x + i \sin x \big)' \\[1ex]
= & (\cos x)' + i (\sin x)' \\[1ex]
= & -\sin x + i \cos x \\[1ex]
= & i^2 \sin x + i \cos x \\[1ex]
= & i \cdot \big( \cos x + i \sin x \big)
\end{array}
$$

Aha! It's $i$ times itself! But what do we know about such functions? They're just secretly scaled and stretched copies of $\text{\color{lightblue}IIOD}$, aren't they? And because $\cos x = 1$ and $\sin x = 0$, this function already has the value 1 at 0, so no scaling is necessary. So in conclusion:

$$
\text{\color{lightblue}IIOD}(ix) = \cos x + i \sin x
$$

You've more than likely come across *this* formula at some point in your maths-curiosity-filled life:

$$
e^{ix} = \cos x + i \sin x
$$

**It's the same formula.**

## The mirrors of Euler's formula

Perhaps you remember from physics that circular motion has the defining property that the acceleration vector is proportional to the displacement vector with a negative proportionality factor. That makes sense: in a circle, acceleration always points towards the centre, whereas displacement is, well, away from the centre. The cool thing is that this property also *characterises* circular motion: as long as both the horizontal and vertical velocities are nonzero, such motion will *always* follow a circle.

And, hey, circles! Sine and cosine! Maybe there's a connection there!

The displacement in circular motion follows $(\cos t, \sin t)$, where $t$ is time. But what if we tried to find out what functions describe circular motion not through a geometric approach, but through a differential one? What if we tried to analyse circular motion through this idea of acceleration being negatively proportional to displacement?

So we have a new wishlist: we want functions $(x, y) = (C(t), S(t))$ such that

- $C(0) = 1$, $C'(0) = 0$, and $C''(x) = -C(x)$;
- $S(0) = 0$, $S'(0) = 1$, and $S''(x) = -S(x)$.

In other words, we're specifying how we want our circular motion to start (namely, one unit to the right from the origin, and with a derivative pointing upwards), and having the characteristic property: their second derivative (acceleration) is equal to the displacement with a negative sign.

How can the *second* derivative of a function be equal to $\lambda$ times itself? Well, one easy way is for its *first* derivative to be $\sqrt{\lambda}$ times itself; then differentiating it twice will give us $\lambda$ back. Naturally, another way is $-\sqrt{\lambda}$, since every number has two square roots. Also, any sum of such functions will still have a second derivative equal to $\lambda$ times itself, and any scalar multiple still will.

And in fact, the theory of differential equations tells us that *that's all of them*. **The *only* functions whose second derivative is $\lambda$ times itself are functions of the form $A \cdot f(x) + B \cdot g(x)$, where $A$ and $B$ are constants, and $f$ and $g$ are functions whose derivative is $\sqrt{\lambda}$ and $-\sqrt{\lambda}$ times itself, respectively.**[^4]

[^4]: I don't have a handy, easy-to-understand proof for this, sadly, you'll have to take my word for it or look it up yourself if you feel up to it. It's basically a generalisation of what we saw above with $\text{\color{lightblue}IIOD}$, though, so you're not missing out on much.

And we *already know* what function differentiates to $\pm \sqrt{\lambda}$ times itself: it's $\text{\color{lightblue}IIOD}(\pm \sqrt{\lambda} \cdot x)$! And in our case, $\lambda$ was $-1$, so $\pm \sqrt{\lambda}$ is $\pm i$. So both $C(x)$ and $S(x)$ are some combination of scalar multiples of $\text{\color{lightblue}IIOD}(ix)$ and $\text{\color{lightblue}IIOD}(-ix)$.

Rings a bell?

If $C(x) = A \cdot \text{\color{lightblue}IIOD}(ix) + B \cdot \text{\color{lightblue}IIOD}(-ix)$, all that's left is to solve for $A$ and $B$. We want:

$$
\begin{array}{rlll}
1 & = C(0) & = A \cdot \text{\color{lightblue}IIOD}(i \cdot 0) + B \cdot \text{\color{lightblue}IIOD}(-i \cdot 0) & = A + B\\[1ex]
0 & = C'(0) & = A \cdot i \cdot \text{\color{lightblue}IIOD}(i \cdot 0) - B \cdot i \cdot \text{\color{lightblue}IIOD}(-i \cdot 0) & = (A - B) \cdot i
\end{array}
$$

So $A + B = 1$ and $A - B = 0$, giving $A = \frac{1}{2}$ and $B = \frac{1}{2}$, so that:

$$
C(x) = \frac{\text{\color{lightblue}IIOD}(ix) + \text{\color{lightblue}IIOD}(-ix)}{2}
$$

Repeating this with $S(x)$, we get $A + B = 0$ and $(A - B) \cdot i = 1$, so $A = \frac{1}{2i}$ and $B = -\frac{1}{2i}$, and we get:

$$
S(x) = \frac{\text{\color{lightblue}IIOD}(ix) - \text{\color{lightblue}IIOD}(-ix)}{2i}
$$

And, of course, I cleverly picked the initial conditions so that the circular motion functions $C(x)$ and $S(x)$ are just $\cos x$ and $\sin x$: at time 0, a point tracing out $(\cos t, \sin t)$ would be one unit to the right of the origin and its velocity would be upwards. Switching out $\text{\color{lightblue}IIOD}$ for that scary, scary $e^x$ notation gives us the "mirrors" of Euler's Formula:

$$
\cos x = \frac{e^{ix} + e^{-ix}}{2} \qquad \text{and} \qquad \sin x = \frac{e^{ix} - e^{-ix}}{2i}
$$

This usual notation of $\text{\color{lightblue}IIOD}$ as $e^x$, even when its argument is a complex number, can be crazy confusing if not outright intimidating: what's it even *mean* to raise a number to an imaginary power? The answer: this isn't *about* raising anything to a power at all! It's an [abuse of notation](https://en.wikipedia.org/wiki/Abuse_of_notation); what we *mean* by $e^{ix}$ is $\text{\color{lightblue}IIOD}(ix)$.[^5]

[^5]: Heck, this only gets worse: the same abuse of notation is used to take [matrix exponents](https://en.wikipedia.org/wiki/Matrix_exponential) and even [exponential derivatives](https://youtu.be/VI6ZlnkuxuA).

So sine and cosine can be characterised by their geometric meaning just as well as their property that their second derivatives are equal to their own negation, and the connection between the two approaches lies in how circular motion works. This means sine and cosine are not-so-distant cousins of exponentials! In fact, for a brief time before the discovery of logarithms, people used sines and cosines to turn multiplication into addition: [sines and cosines were makeshift logarithms](https://en.wikipedia.org/wiki/Prosthaphaeresis).

And, hey, bring up those formulae above one more time:

$$
\cos x = \frac{e^{ix} + e^{-ix}}{2} \qquad \text{and} \qquad \sin x = \frac{e^{ix} - e^{-ix}}{2i}
$$

Doesn't this look a whole lot like the definition of $\cosh$ and $\sinh$?

## IIOD's slightly less outlandish cousins

What if we go back to the defining characteristic of circular motion, but get rid of that pesky negative sign this time? Instead of looking for functions whose second derivative equals *minus* themselves; let's look for some whose second derivative equals... themselves, period.

Obviously, $\text{\color{lightblue}IIOD}(x)$ is such a function. So is $\text{\color{lightblue}IIOD}(-x)$, since differentiating it once negates it, and differentiating it a second time negates *that*, landing us back at the beginning. And since 1 and -1 are the only two square roots of 1, by the same reasoning as above, ***all* such functions are the sums and scalar multiples of $\text{\color{lightblue}IIOD}(x)$ and $\text{\color{lightblue}IIOD}(-x)$.**

Just for fun, let's give them the same starting conditions as we did above: $C(x) = 1, C'(x) = 0, S(x) = 0, S'(x) = 1$; and give the resulting functions $C$ and $S$ the names $\cosh$ and $\sinh$. Just for fun. Then we get slightly less outlandish counterparts of the mirrors of Euler's Formula:

$$
\cosh x = \frac{e^x + e^{-x}}{2} \qquad \text{and} \qquad \sinh x = \frac{e^x - e^{-x}}{2}
$$

And, by adding them, a slightly less outlandish counterpart of Euler's Formula itself:

$$
e^x = \cosh x + \sinh x
$$

That's right, $\cosh$ and $\sinh$ are the [even part and odd part](https://en.wikipedia.org/wiki/Even_and_odd_functions#Even%E2%80%93odd_decomposition) of $e^x$, respectively.

And by the way, with those definitions, it's easy to verify that $\cosh^2 x - \sinh^2 x = 1$; and because the unit hyperbola includes the point $(1, 0)$ and is tangent to a vertical line at that point, that means $(\cosh t, \sinh t)$ traces out (half of) the unit hyperbola, just like $(\cos t, \sin t)$ traces out the unit circle.[^6] But this isn't what $\cosh$ and $\sinh$ are *about*: that's just a consequence of the fact that they satisfy $\cosh^2 x - \sinh^2 x = 1$. Their real significance is in their differential properties. Ironically, their names are kind of a misnomer: they really aren't all that much about hyperbolae. Like, sure, the connection is there, but it sorta distracts from the more important stuff about them, you know?

[^6]: So maybe motion in which acceleration is proportional to displacement with a *positive* proportionality factor should be called "hyperbolic motion".

## Not really about hyperbolae

Let's go back all the way to the beginning, to how we characterised the hyperbolic functions through their connection to spanning areas in hyperbolae. Here's that diagram again, for reference:

<iframe src="https://www.desmos.com/calculator/clk4iqpvbf?embed" width="100%" style="min-height: 500px"></iframe>

Now we have everything we need to actually show that this is true.

We want to find a parameterisation of the unit hyperbola with a function $f(t)$, which will serve as the vertical coordinate (so the horizontal coordinate will be $\sqrt{f(t)^2 + 1}$), such that when the vertical coordinate is $f(t)$, the area of the subtended sector will be $t/2$. Our task is to determine what $f$ is.

We can find the area of this sector using calculus, if we rotate this diagram by 90 degrees:

<iframe src="https://www.desmos.com/calculator/czxssbbnww?embed" width="100%" style="min-height: 500px"></iframe>

It basically amounts to finding the integral $\displaystyle \int \sqrt{x^2 + 1} \ dx$.

This integral isn't easy! Right off the bat, if we substituted $u = x^2 + 1$ or something, there'd be no good way to get $dx$ to turn into $du$. The answer will probably not just be a simple polynomial.

Let's try to put our hyperbolic functions (the ones with the exponential definitions) to the rescue. Since $\cosh^2 \theta - \sinh^2 \theta = 1$, let's try to substitute $x = \sinh \theta$. Doing so will give us $dx = \cosh \theta \ d\theta$ and $\sqrt{x^2 + 1} = \cosh \theta$, so the integral becomes $\displaystyle \int \cosh^2 \theta \ d\theta$.

To continue, we can rewrite $\cosh^2 \theta$ as $\dfrac{\cosh(2\theta) + 1}{2}$ (which is pretty much just the first binomial formula, quite neatly). This gives us

$$
\int \frac{\cosh(2\theta) + 1}{2} \ d\theta = \frac{\sinh(2\theta)}{4} + \frac{\theta}{2}
$$

(Plus $C$, but shush, we'll want a definite integral in the end.)

Okay, but we're not quite there yet; we can't convert back anymore. We started with $x = \sinh(\theta)$, and now we have $\sinh(2\theta)$. That's okay though; we can use a similar identity to go back: $\sinh(2\theta) = 2 \cdot \sinh(\theta) \cdot \cosh(\theta)$. (Pretty much just the *third* binomial formula.) Then $\sinh(\theta)$ becomes $x$, and $\cosh(\theta)$ becomes $\sqrt{x^2 + 1}$, and we get our final answer:

$$
\int \sqrt{x^2 + 1} \ dx = \frac{x \cdot \sqrt{x^2 + 1}}{2} + \frac{\sinh^{-1}(x)}{2}
$$

What a funky integral indeed! Who would've thought that the integral of $\sqrt{x^2 + 1}$ would have *inverse hyperbolic sine* in it.

So that's the area between the unit hyperbola and the $y$-axis. To get our desired sector, we need to subtract the bit subtended by a straight line directly from $(0, 0)$ to a point on the hyperbola, namely $(\sqrt{f(t)^2 + 1}, f(t))$. That's just a right triangle, and the area of a triangle is half base times height, where the base is the $y$-coordinate, $f(t)$, and the height is the $x$-coordinate, $\sqrt{f(t)^2 + 1}$. Putting it all together:

$$
\begin{array}{l}
\text{area of arc} \\[1ex]
= \text{area under hyperbola} - \text{area of triangle} \\[1ex]
= \displaystyle \int \sqrt{x^2 + 1} \ dx \Bigg|_0^{f(t)} \ - \frac{f(t) \cdot \sqrt{f(t)^2 + 1}}{2} \\[4ex]
= \displaystyle \frac{f(t) \cdot \sqrt{f(t)^2 + 1}}{2} + \frac{\sinh^{-1}(f(t))}{2} - \frac{f(t) \cdot \sqrt{f(t)^2 + 1}}{2} \\[4ex]
= \displaystyle \frac{\sinh^{-1}(f(t))}{2}
\end{array}
$$

And since we want it to be equal to $t/2$, that means our $f$ must be $\sinh$. That exponential one.

So, yes, the "hyperbolic" functions with those weird combinations of $e^x$ and $e^{-x}$ do really characterise a hyperbola. But the fact that they do is little more than an exercise in calculus as a consequence of their real significance: that they're their own second derivatives.

Thank you for reading.
