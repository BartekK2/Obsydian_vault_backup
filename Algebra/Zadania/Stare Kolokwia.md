
### Bratusze :LiSkull:

#### Kolokwium 2, 2023-12-20

###### Zad 3. Oblicz $X=(\det A +r(B))\cdot C^{-1}$

$$\begin{gathered}
A=
\begin{bmatrix}
6&1&0&5&-1\\
0&1&-1&-1&0\\
1&0&1&2&1\\
2&-1&1&0&2\\
-1&1&0&1&0
\end{bmatrix}, \ \ \ 
B=
\begin{bmatrix}
1&0&-2&1&2&3\\
0&2&0&1&1&0\\
2&-1&-4&-1&2&6\\
3&1&-6&1&5&9
\end{bmatrix}, \ \ \ 
C=
\begin{bmatrix}
1&0&0\\
0&2&0\\
1&-1&3
\end{bmatrix}
\end{gathered}$$

$$\begin{gathered}
\det A:\\\\
A=
\begin{vmatrix}
6&1&0&5&-1\\
0&1&-1&-1&0\\
1&0&1&2&1\\
2&-1&1&0&2\\
-1&1&0&1&0
\end{vmatrix}=
\frac{1}{216}
\begin{vmatrix}
6&1&0&5&-1\\
0&1&-1&-1&0\\
6&0&6&12&6\\
12&-6&6&0&12\\
-6&6&0&6&0
\end{vmatrix}=\\\\=
-\frac{1}{648}

\begin{vmatrix}
6&1&0&-1&5\\
0&1&-1&0&-1\\
0&0&6&7&7\\
0&0&0&49&-17\\
0&0&0&0&18
\end{vmatrix}=-49\\\\
r(B):\\
B=
\begin{bmatrix}
1&0&-2&1&2&3\\
0&2&0&1&1&0\\
2&-1&-4&-1&2&6\\
3&1&-6&1&5&9
\end{bmatrix} \to 
\begin{bmatrix}
1&0&-2&1&2&3\\
0&-1&0&1&-2&0\\
0&0&0&0&1&0\\
0&0&0&0&0&0
\end{bmatrix}=3
\\\\
\end{gathered}$$
$$\begin{gathered}
C^{-1}:\\
\begin{bmatrix}
\begin{array}{ccc|ccc}
1&0&0&1&0&0\\
0&1&0&0&\frac{1}{2}&0\\
0&0&1&-\frac{1}{3}&\frac{1}{6}&\frac{1}{3}
\end{array}
\end{bmatrix}
\end{gathered}$$
$$\begin{gathered}
X=(\det A+r(B))\cdot C^{-1}=-46\cdot 
\begin{bmatrix}
1&0&0\\
0&\frac{1}{2}&0\\
-\frac{1}{3}&\frac{1}{6}&\frac{1}{3}
\end{bmatrix}=
\begin{bmatrix}
-46&0&0\\
0&-23&0\\
\frac{46}{3}&-\frac{46}{6}&-\frac{46}{3}
\end{bmatrix}
\end{gathered}$$---
$$\begin{bmatrix}
1&1&1&1\\
0&-1&-3&-2\\
0&0&13&8\\
0&0&0&9-\frac{8\cdot 11}{13}\\
\end{bmatrix}$$