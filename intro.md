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


<h1>Menghitung determinan matrik dengan menggunakan rumus expansi baris</h1>

$\[
\sum_{k=1}^{n} (-1)^{i+k} a_{ik} M_{ik}
\]$

<br>dengan \( M_{ij} \) adalah minor dari matriks \( A \) dan

$\[
M_{ij} = \det A_{ij}
\]$

<br>\( A_{ij} \) adalah submatrik dengan menghapus baris \( i \) dan kolom \( j \) dari matriks \( A_{m \times n} \) dengan \( 1 \le i,j \le n \).

\end{document}
    
<h2>1. Determinan Matriks 2x2</h2>
    
<p>
$\[
A=\begin{pmatrix}-7 & -5 \\ 1 & 4\end{pmatrix}
\]$
</p>

<p>Rumus:</p>
<p>
$\[
\det(A)=ad-bc
\]$
</p>

<p>Perhitungan:</p>
<p>
$\[
\det(A)=(-7)(4)-(-5)(1)
\]
$</p>

<p>
$\[
=-28+5=-23
\]
$</p>

<h2>2. Determinan Matriks 3x3</h2>   
    
<p>
$\[
A=\begin{pmatrix}
0 & 2 & -3\\
1 & -2 & -1\\
0 & 0 & 1
\end{pmatrix}
\]$
</p>

<p>Ekspansi baris pertama:</p>

<p>
$\[
\det(A)=0 + (-1)^{1+2}(2)
\begin{vmatrix}1 & -1\\0 & 1\end{vmatrix}
+ (-1)^{1+3}(-3)
\begin{vmatrix}1 & -2\\0 & 0\end{vmatrix}
\]$
</p>

<p>Hitung minor:</p>

<p>
$\[
= (-1)(2)(1\cdot1-(-1)\cdot0) + (1)(-3)(0)
\]
$</p>

<p>
$\[
=-2
\]$
</p>

<h2>3. Determinan Matriks 4x4</h2>

<p>
$\[
A=
\begin{pmatrix}
1 & -3 & 1 & 1\\
-3 & 1 & 1 & 1\\
1 & 1 & -3 & 1\\
1 & 1 & 1 & -3
\end{pmatrix}
\]
$</p>

<p>Jumlah setiap baris:</p>

<p>
$\[
1-3+1+1=0
\]$
</p>

<p>Karena ada baris yang saling bergantung (linear dependent):</p>

<p>
$\[
\det(A)=0
\]
$</p>

<p><b>Sifat Determinan: Kalau ada baris/kolom yang saling bergantung (linear dependent) → determinan = 0</b></p>
<p>Baris 1:  1−3+1+1=0</p>
<p>Baris 2:  −3+1+1+1=0</p>
<p>Baris 3:   1+1−3+1=0</p>
<p>Baris 4: 1+1+1−3=0</p>
<p>Semua baris jumlahnya 0</p>
<p>Jadi det(A) = 0</p>   
<h1>Menggunakan rumus matriks adjoin untuk menghitung invers dari matriks berikut dengan rumus</h1>

<p>
$\[
(\mathrm{adj}\, A)_{ij} = (-1)^{i+j} M_{ji}
\]$
</p>

<p>
$\[
A^{-1} = \frac{1}{\det A} \, \mathrm{adj}\, A
\]$
</p>

<h2>4. Invers Matriks 2x2 (Metode Adjoin)</h2>

<p>
$\[
A=\begin{pmatrix}-7 & -5 \\ 1 & 4\end{pmatrix}
\]$
</p>

<p>Langkah 1: Determinan</p>
<p>
$\[
\det(A)=(-7)(4)-(-5)(1)=-28+5=-23
\]$
</p>

<p>Langkah 2: Minor</p>
<p>
$\[
M_{11}=4,\quad M_{12}=1,\quad M_{21}=-5,\quad M_{22}=-7
\]$
</p>

<p>Langkah 3: Kofaktor</p>
<p>
$\[
C_{11}=4,\quad C_{12}=-1,\quad C_{21}=5,\quad C_{22}=-7
\]$
</p>

<p>Langkah 4: Adjoin (transpose kofaktor)</p>
<p>
$\[
\text{adj}(A)=\begin{pmatrix}4 & 5 \\ -1 & -7\end{pmatrix}
\]$
</p>

<p>Langkah 5: Invers</p>
<p>
$\[
A^{-1}=\frac{1}{-23}
\begin{pmatrix}4 & 5 \\ -1 & -7\end{pmatrix}
\]$
</p>

<h2>5. Invers Matriks 3x3 (Metode Adjoin)</h2>

<p>
$\[
A=\begin{pmatrix}
0 & 2 & -3\\
1 & -2 & -1\\
0 & 0 & 1
\end{pmatrix}
\]
$</p>

<p>Langkah 1: Determinan</p>
<p>
$\[
\det(A)=-2
\]
,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,$</p>

<p>Langkah 2: Matriks Minor</p>

<p>\[
M_{11}=\begin{vmatrix}-2 & -1\\0 & 1\end{vmatrix}=-2
\]</p>

<p>\[
M_{12}=\begin{vmatrix}1 & -1\\0 & 1\end{vmatrix}=1
\]</p>

<p>\[
M_{13}=\begin{vmatrix}1 & -2\\0 & 0\end{vmatrix}=0
\]</p>

<p>Langkah 3: Matriks Kofaktor</p>

<p>\[
C=
\begin{pmatrix}
-2 & -1 & 0\\
2 & 0 & 0\\
-5 & -3 & -2
\end{pmatrix}
\]</p>

<p>Langkah 4: Adjoin (transpose)</p>

<p>\[
\text{adj}(A)=
\begin{pmatrix}
-2 & 2 & -5\\
-1 & 0 & -3\\
0 & 0 & -2
\end{pmatrix}
\]</p>

<p>Langkah 5: Invers</p>

<p>\[
A^{-1}=\frac{1}{-2}
\begin{pmatrix}
-2 & 2 & -5\\
-1 & 0 & -3\\
0 & 0 & -2
\end{pmatrix}
\]</p>

<p>\[
=
\begin{pmatrix}
1 & -1 & \frac{5}{2}\\
\frac{1}{2} & 0 & \frac{3}{2}\\
0 & 0 & 1
\end{pmatrix}
\]</p>

<h2>6. Invers Matriks 4x4</h2>

<p>\[
A=
\begin{pmatrix}
1 & -3 & 1 & 1\\
-3 & 1 & 1 & 1\\
1 & 1 & -3 & 1\\
1 & 1 & 1 & -3
\end{pmatrix}
\]</p>

<p>Langkah 1: Cek determinan</p>

<p>\[
1-3+1+1=0
\]</p>

<p>Baris saling bergantung (linear dependent)</p>

<p>\[
\det(A)=0
\]</p>

<p>Langkah 2: Kesimpulan</p>

<p>\[
A^{-1} \text{ tidak ada karena determinan = 0}
\]</p>



	​
