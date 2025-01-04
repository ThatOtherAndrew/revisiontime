A matrix is really just a **fancy way of arranging numbers** into a rectangular 2D array. Matrices are a very efficient and useful way of encoding information in certain cases, and are used extensively in linear algebra, computer graphics, machine learning, and more.

Here are some examples of some matrices:

$$
\begin{gathered}

\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix} &

\begin{bmatrix}
1 & 6 & 5 \\
9 & 2 & 3 \\
8 & 7 & 4
\end{bmatrix} &

\begin{pmatrix}
1
\end{pmatrix} \\

\begin{bmatrix}
9 & -\frac{3}{2} & 26
\end{bmatrix} &

\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix} &

\begin{pmatrix}
e \\
i \\
\pi
\end{pmatrix}

\end{gathered}
$$

Matrices can take any $m \times n$ rectangular shape, where $m$ and $n$ are positive integers describing the number of rows and columns respectively. Note how (parentheses) and \[square brackets\] are more or less interchangeable - it's just personal preference, really.

And if the last example there caught your eye for looking suspiciously like a vector, well spotted - that's because all vectors can be considered an $n \times 1$ matrix as well!

## Linear transformations

One of the things matrices are very good at describing is **linear transformations** - that being, some way to uniformly squash, stretch, scale or spin some space.

A two-dimensional linear transformation can be described in a $2 \times 2$ matrix, a three-dimensional transformation with a $3 \times 3$ matrix, and so on.

#todo 
