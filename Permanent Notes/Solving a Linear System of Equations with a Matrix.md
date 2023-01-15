202208290806
Status: #permanent 
Tags: #LinearAlgebra #Matrix

# Solving a Linear System of Equations with a Matrix

There are some row operations allowed:
    1. Swap rows, which means to move around the equations within the system. This doesn't *change* anything about the matrix, but it makes it more readable and can help put the matrix in [[Fundamentals of Echelon Form | Echelon Form]] and (hopefully) [[Fundamentals of Reduced Echelon Form | Reduced Echelon Form]].
    2. Multiply the row by a nonzero constant. This doesn't change the row since both the variables and the constants will scale accordingly.
    3. Replace a row with the sum of itself and a multiple of another row. An example of this would be to add R$_1$ + 5R$_2$ to R$_1$. 
        a. Don't replace an unused row or the row being used as a multiple.
        
The matrix being solved is:
$$
\left[\begin{array}{rrr|r}
1&-3&-3&-8\\
0&1&2&7\\
0&1&1&4
\end{array}\right]
$$

This matrix is an **augmented matrix**, which is a *coefficient matrix* with a *right-hand-side-vector*. The augmented matrix is a matrix that holds on the variables on the **left** side while the constants are on the **right** side.

The row operations are allowed on the matrix as long as **equivalency** , which means both matrices have the *same solution*.

The goal is to get a matrix that looks like below:
$$
\left[\begin{array}{rrr|r}
1&0&0&4\\
0&1&0&1\\
0&0&1&3
\end{array}\right]
$$

This goal is to get each leading nonzero entry to be the only one and has the value one in the variable side of the matrix in its column. This means that each nonzero term in the matrix on the variable side should be the only nonzero term in its column.

The first step is to eliminate x$_2$ from row 3 to isolate x$_3$. A row operation that will help with this is row operation 3 with row 2 and row 3 because it will eliminate column 2 in row 3.
$$
-R_2+R_3 \to R_3
$$
The result is the vector below:
$$
\left[\begin{array}{rrr|r}
1&-3&-3&-8\\
0&1&2&7\\
0&0&-1&-3
\end{array}\right]
$$

To finish this operation off, row 3 should have a positive variable since we want to know what x$_3$ is not -x$_3$. Row operation 2 should help by multiplying -1 to row 3.
$$
-R_3 \to R_3\\
$$
$$
\left[\begin{array}{rrr|r}
1&-3&-3&-8\\
0&1&2&7\\
0&0&1&3
\end{array}\right]
$$

A note is that multiple row operations can be applied at once, but this should be used sparingly as it can be easy to mix up rows. With that in mind, we can eliminate the variable x$_3$ from row 1 and row 2 since we have successfully isolated x$_3$ in row 3. This will also isolate x$_2$ in row 2, which will allow us to finish this off in the next step.
$$
\begin{aligned}
-2R_3+R_2 \to R_2\\
3R_3+R_1 \to R_1
\end{aligned}
$$
$$
\left[\begin{array}{rrr|r}
1&-3&0&1\\
0&1&0&1\\
0&0&1&3
\end{array}\right]
$$

The next step is to isolate x$_1$ in row 1, so row operation 3 should help by adding a multiple of row 2 to row 1.
$$
3R_2+R_1 \to R_1
$$
$$
\left[\begin{array}{rrr|r}
1&0&0&4\\
0&1&0&1\\
0&0&1&3
\end{array}\right]
$$

This has given us the solution to the system as shown below:
$$
\begin{aligned}
x_1=4\\
x_2=1\\
x_3=3
\end{aligned}
$$




---
# References
1. [[Solving a Linear System of Equations]]