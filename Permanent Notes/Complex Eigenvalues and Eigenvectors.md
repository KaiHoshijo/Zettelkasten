202210302106
Status: #permanent 
Tags: #LinearAlgebra #Eigenstuff #Complex #Vector

# Complex Eigenvalues and Eigenvectors
Building upon the concept of [[Eigenvalues and Eigenvectors]], complex eigenvaleus and eigenvalues add the concept of using the imaginary number *i* to find transformed vectors that stay on the original vector's span. 

Using the defintion from [[Eigenvalues and Eigenvectors]], we know that $$A\vec{x}=\lambda I$$
However, rotation matrices don't have any real vectors since the vectors are all being rotated, which means that imaginary numbers are necessary.
## Example
Let A be the transformation matrix that acts as pure rotation, which means there is no stretching or translation.
$$
A=\left[\begin{array}{rr}
0&-1\\
1&-1
\end{array}\right]
$$
### Find the complex eigenvalue
To find eigenvlaues, we know that we need to use $$det(A-\lambda I) \to 0$$ which can be rewritten as $$
\left[\begin{array}{rr}
-\lambda &-1\\
1&-\lambda
\end{array}\right]\to0
$$
then we can attempt to solve this [[Determinant|determinant]] and set it equal to zero 
$$
\begin{align}
\lambda ^2+1\to0\\
\lambda ^2 = -1\\
\lambda=\mathit{i}
\end{align}
$$
### Find the eigenvectors
Now that we know that $$\lambda=\mathit{i}$$, we can solve for the eigenvectors
$$
\lambda=\mathit{i}
A-\lambda I = A-\mathit{i}I
\left[\begin{array}{rr}
-i&-1\\
1&-i
\end{array}\right]
$$
To get rid of -i in both rows, we can multiply by the [[complex conjugate]], where $$\bar{\lambda}=a-b\mathit{i}$$
Thus we can use the complex conjugate of the first $$\mathit{i}$$ that appears, which means the conjugate is $$\bar{\lambda}=0-i$$
$$
R_1*\mathit{i}\\~
\left[\begin{array}{rr}
-i(i)&-1(i)\\
1&-i
\end{array}\right]=
\left[\begin{array}{rr}
1&-i\\
1&-i
\end{array}\right]=
-R_1+R_2\to R_2
\left[\begin{array}{rr}
1&-i\\
0&0
\end{array}\right]
$$
The bottom canceling out will always happen for eigenvectors.
This can be represented in parametric form as:
$$
\left[\begin{align}
x_1=ix_2\\
x_2=x_2\ \mathit{free}
\end{align}\right]
$$
Any multiple of $$\left[\begin{array}{r}i\\1\end{array}\right]$$ is an eigenvector of A with $$\lambda = \mathit{i}$$ 






---
# References