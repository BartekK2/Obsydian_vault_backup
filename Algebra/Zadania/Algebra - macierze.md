##### Lekcja: [[Algebra - 9]]
#algebra  #macierze 
###### 15.12.2024
---
###### 5. Niech $A$ będzie macierzą kwadratową. Udowodnij że:

a) Jeżeli $A^2-A+I=0$, to $A$ jest nieosobliwa i $A^{-1}=I-A$

$$\begin{gathered}
A\cdot A^{-1}=I \ \land \ A^{-1}=I-A\\
A\cdot (I-A)=I\\
-A^2+IA=I\\
-A^2+I(A-1)=0\\
A^2+I-IA=0\\
\land \\
A^2-A+I=0\\
A^2+I-IA=A^2-A+I\\
-IA=-A\\
c.k.d
\end{gathered}$$

b) jeżeli $A^k=0$, to $(I-A)^{-1}=I+A+A^2+\dots+A^{k-1}, k\geq 1$
$$\begin{gathered}
I+A+A^2+\dots+A^{k-1}=S\\\\
(I-A)S=(I-A)(I+A+A^2+\dots+A^{k-1})=\\ =I+A+A^2+\dots+A^{k-1}-A-A^2-A^3-\dots-A^k=\\
=I-A^k=I \implies S=(I-A)^{-1}
\end{gathered}$$
---
###### 6. Jakie są możliwe wartości wyznacznika macierzy rzeczywistej A stopnia $n$, jeżeli:

a) $A^2=A^T$ 

Skoro $A^2=A^T \implies \det A^2 = \det A^T$ 
Wiemy z własności wyznaczników że:
1. $\det (A\cdot B)=\det A \cdot \det B$ co implikuje że $\det A^2=(\det A)^2$
2. $\det A^T=\det A$

Zatem podstawiając $a=\det A$:
$$\begin{gathered}
a^2=a \ \ /-a\\
a^2-a=0\\
a(a-1)=0\\
\end{gathered}$$
Zatem wyznacznik równy 0 albo 1.

---
b) $A^T-A^{-1}=\boldsymbol{0}$

Czyli $A^T=A^{-1}$:

$\det A^T=\det A \ \land \ \det A^{-1}=(\det A)^{-1}$

Podstawiając $a=\det A$

$$\begin{gathered}
a=a^{-1}\\
a=\frac{1}{a}\\
a^2=1\\
a=1 \vee a=-1
\end{gathered}$$
---
c) $A^2+A^{-1}=\boldsymbol{0}$

Czyli $A^2=-A^{-1}$

$(\det A)^2=-(\det A)^{-1}$ 

Podstawiając $a=\det A$

$$\begin{gathered}
a^2=-\frac{1}{a}\\
a^3=-1\\
\end{gathered}$$
---
