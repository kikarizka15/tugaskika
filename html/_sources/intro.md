# INVERS
## Diketahui:
$A =
\begin{bmatrix}
1 & 1 & 1 & 1 \\
2 & -1 & 1 & -1 \\
1 & 2 & -1 & 1 \\
3 & -1 & 2 & 1
\end{bmatrix}
\quad
B =
\begin{bmatrix}
10 \\
-1 \\
6 \\
11
\end{bmatrix}
$

## Mencari Invers Matriks A
### Langkah 1 Rumus Invers
$A^{-1} = \frac{1}{\det(A)} \cdot \text{adj}(A)$

### Langkah 2 Hitung Determinan
### Kita ekspansi baris pertama:
det(A)=1C11​+1C12​+1C13​+1C14​

dengan

Cij​=(−1)i+jMij​

di mana Mij​ adalah minor.

Jadi kita cari minor satu-satu dari baris pertama.

## Cari determinan dari baris pertama
det(A)=−3+9+11−4=13

## Minor
$
\text{Minor } M_{11}
$

$
M_{11}=
\begin{vmatrix}
-1 & 1 & -1\
2 & -1 & 1\
-1 & 2 & 1
\end{vmatrix}
$

# $

-1
\begin{vmatrix}
-1 & 1\
2 & 1
\end{vmatrix}
-1
\begin{vmatrix}
2 & 1\
-1 & 1
\end{vmatrix}
+(-1)
\begin{vmatrix}
2 & -1\
-1 & 2
\end{vmatrix}
$

$
\begin{vmatrix}
-1 & 1\
2 & 1
\end{vmatrix}
=(-1)(1)-(1)(2)=-3
$

$
\begin{vmatrix}
2 & 1\
-1 & 1
\end{vmatrix}
=(2)(1)-(1)(-1)=3
$

$
\begin{vmatrix}
2 & -1\
-1 & 2
\end{vmatrix}
=(2)(2)-(-1)(-1)=3
$

$
M_{11}=(-1)(-3)-1(3)+(-1)(3)=3-3-3=-3
$

$
C_{11}=(+),M_{11}=-3
$

$
\det(A)=1(C_{11})+1(C_{12})+1(C_{13})+1(C_{14})
$

$
\det(A)=-3+9+11-4=13
$

$
\det(A)=13
$

$
A^{-1}=\frac{1}{\det(A)},\operatorname{adj}(A)
$

$
\text{karena } \det(A)=13
$

$
A^{-1}=\frac{1}{13}
\begin{pmatrix}
-3 & 3 & 4 & 2\
9 & 4 & 1 & -6\
11 & 2 & -6 & -3\
-4 & -9 & 1 & 7
\end{pmatrix}
$

$
A^{-1}=
\begin{pmatrix}
-\frac{3}{13} & \frac{3}{13} & \frac{4}{13} & \frac{2}{13}\
\frac{9}{13} & \frac{4}{13} & \frac{1}{13} & -\frac{6}{13}\
\frac{11}{13} & \frac{2}{13} & -\frac{6}{13} & -\frac{3}{13}\
-\frac{4}{13} & -\frac{9}{13} & \frac{1}{13} & \frac{7}{13}
\end{pmatrix}
$


	​
