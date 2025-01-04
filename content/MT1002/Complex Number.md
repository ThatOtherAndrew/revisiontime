A complex number is a **number with real and [[Imaginary Number|imaginary]] parts**. They can be expressed in the following **general form**, where $a$ and $b$ are real numbers:

$$
a {\color{magenta} {}+ bi}
$$

>[!info]- Magenta colour-coding
>All imaginary parts in expressions on this page will be highlighted a lovely shade of <span style="color: magenta">magenta</span>, to make them easier to follow.
>
><sub>Yes, this took way too long to typeset.</sub>

The set of all complex numbers is denoted by the symbol $\mathbb{C}$. Yes, with the funny font and all. What next, will the [cool S](https://en.wikipedia.org/wiki/Cool_S) become a maths symbol as well?

If $a$ is $0$, then the complex number can be expressed as just $bi$. Just like my chances of graduating with a first class degree, this number is considered **purely imaginary**.

A letter commonly used to represent a complex variable is the letter $z$. Why? It's convention or something, I dunno.

## Real and imaginary parts

Given some complex number:

$$
z = a \color{magenta} + bi
$$

To get just $a$ or $b$ from a complex number, we use the $\mathrm{Re}$ and $\mathrm{Im}$ functions:

$$
\begin{aligned}
\mathrm{Re}(z) = a \\
\mathrm{Im}(z) = b
\end{aligned}
$$

## Modulus-argument form

An alternative form of expressing complex numbers, if you're too cool for boring ol' $a \color{magenta} + bi$ form, is **modulus-argument form** (also known as **polar form**). This, unsurprisingly, is composed of a modulus and argument - but what the heck are they?

A good intuition for understanding modulus-argument form is thinking about plotting complex numbers on an [[Argand diagram]]. Using the general $a \color{magenta} + bi$ form above is like plotting a point on a rectangular coordinate system. Nothing special there, we simply encode $a$ and $b$ as a horizontal and vertical position respectively. However, that's not the only way to describe a point on a 2D plane - we could also borrow a leaf out of **polar plotting**'s book and describe a point as an **angle** and a **distance from the origin**.

Here's an analogy: imagine giving directions to a lost stranger. Since you're a huuuuge nerd, you decide there are two ways to tell them the directions to where they're trying to get. You could either tell them to walk a certain distance north/south then a certain distance east/west, or you could simply point in a direction and tell them to walk a certain distance that way. Both ways can uniquely identify a location, and the latter is what polar plotting and modulus-argument form is like.

![[Complex Number 1.excalidraw.svg|A visual comparison between general form and polar form on an Argand diagram.]]

As hinted at by the diagram above, modulus-argument form takes the following algebraic shape:

$$
r(\cos \theta {\color{magenta} {}+ i \sin \theta})
$$

It looks a little scary at first, but it just comes from right triangle trigonometry (SOHCAHTOA). If the hypotenuse has length $r$, then the two other sides of the triangle have lengths $r \cos \theta$ and $r \sin \theta$:

![[Complex Number 2.excalidraw.svg]]


#todo ==Explain where the expression comes from==

%%
#todo ask at tutorial: where does $e^{i\theta}$ come into all of this?
%%

### Modulus
#todo 

### Argument
#todo 
