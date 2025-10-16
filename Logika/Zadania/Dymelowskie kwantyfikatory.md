
#### 1. Zapisać za pomocą kwantyfikatorów i podać zaprzeczenie.

##### a) Pomiędzy liczbami $n$ i $2n$ istnieje co najmniej jedna liczba pierwsza (tw. Czebyszewa)

$$\begin{gathered}
\forall n\in \mathbb{N}_+ \exists p \in \mathbb{P}: n\lt p\lt 2n\\\\
\text{ gdzie w sumie można od razu zdefiniować liczby pierwsze:}\\\\
p\in \mathbb{P}\implies \neg \exists a: \frac{p}{a}\in \mathbb{Z}\;\land a\notin \{1,a\}
\end{gathered}$$


#### 2. Znaleźć postać normalną wyrażeń:

##### a) $\forall x: A(x) \vee \forall x: B(x)$

$$\begin{gathered}
\forall x \forall y : (A(x)\vee B(y))
\end{gathered}$$

##### b) $\exists x: A(x) \vee \exists x: B(x)$

$$\begin{gathered}
\exists x: (A(x)\vee B(x))
\end{gathered}$$

##### c) $\forall x : A(x)\implies \exists x: B(x)$

$$\begin{gathered}
p\implies q \Leftrightarrow \neg p\vee q\\\\
\neg (\forall x: A(x))\vee \exists x: B(x)\\
\exists x: \neg A(x)\vee \exists x: B(x)\\
\exists x: (\neg A(x)\vee B(x))
\end{gathered}$$
##### d) $\forall x: A(x)\Leftrightarrow \exists x: B(x)$

$$\begin{gathered}
(A\Leftrightarrow B )\Leftrightarrow ((A\land B)\vee (\neg A\land \neg B))\\\\

\forall x: A(x)\Leftrightarrow \exists x: B(x)\\\\
(\forall x: A(x)\land \exists x: B(x)) \vee (\neg \forall x: A(x)\land \neg \exists x: B(x))\\\\

\forall x: A(x)\Leftrightarrow \exists x: B(x)\\\\

(\forall x: A(x)\land \exists x: B(x))\vee (\exists x: \neg A(x)\land \forall x: \neg B(x))\\\\


(\forall x: A(x)\land \exists y: B(y))\vee (\exists x: \neg A(x)\land \forall x: \neg B(x))\\\\
\forall x \exists y (A(x)\land B(y))\vee \exists u\forall z (\neg A(u)\land \neg B(z))\\\\

\forall x \exists y\exists u\forall z (A(x)\land B(y))\vee  (\neg A(u)\land \neg B(z))
\end{gathered}$$

##### e) $\neg \exists x: [A(x)\land \exists y: B(x,y)]$

$$\begin{gathered}
\forall x : \neg(A(x)\land \exists y: B(x,y))\\
\forall x: (\neg A(x) \vee \forall y:\neg B(x,y))\\
\forall x\forall y: (\neg A(x)\vee \neg B(x,y))
\end{gathered}$$

##### f) coś sie pomyliło dymelkowi

##### g) też chyba

##### h) znowu zepsute 

##### i) $\forall x: [\forall y : A(x,y)\implies \neg (\forall y: \exists z: B(x,y,z))]$

---
#### 3. Zapisz negację wyrażenia

##### a) $\exists x: (x\neq 0 \land \forall y: (y\gt 0\implies \forall z: (z\lt 0\implies x+y\neq z)))$

$$\begin{gathered}
\forall x: \neg (x\neq 0\land \forall y: (y\gt 0 \implies \forall z: (z\lt 0 \implies x+y\neq z)))\\\\

\forall x: x= 0\vee  \exists y: \neg (y\gt 0 \implies \forall z: (z\lt 0 \implies x+y\neq z)))\\\\


\forall x: x= 0\vee  \exists y: \neg (y\leq  0 \vee  \forall z: (z\lt 0 \implies x+y\neq z)))\\\\

\forall x: x= 0\vee  \exists y: (y\gt  0 \land \neg \forall z: (z\lt 0 \implies x+y\neq z)))\\\\


\forall x: x= 0\vee  \exists y: (y\gt  0 \land \exists z: \neg(z\geq 0 \vee x+y\neq z)))\\\\


\forall x: x= 0\vee  \exists y: (y\gt  0 \land \exists z: (z\lt 0 \land x+y= z)))\\\\
\end{gathered}$$

##### b) $\forall x: (x\gt 0 \implies \forall y: (y\lt 0\implies \exists z: (z\lt 0 \land 2x+y\gt z)))$

$$\begin{gathered}
\exists x: \neg (x\gt 0 \implies \forall y: (y\lt 0\implies \exists z: (z\lt 0 \land 2x+y\gt z)))\\\\

\exists x: \neg (x\leq 0 \vee \forall y: (y\lt 0\implies \exists z: (z\lt 0 \land 2x+y\gt z)))\\\\

\exists x:  (x\gt 0 \land \exists y: \neg (y\lt 0\implies \exists z: (z\lt 0 \land 2x+y\gt z)))\\\\

\exists x:  (x\gt 0 \land \exists y: \neg (y\geq 0\vee \exists z: (z\lt 0 \land 2x+y\gt z)))\\\\

\exists x:  (x\gt 0 \land \exists y:  (y\lt 0\land \forall  z: \neg(z\lt 0 \land 2x+y\gt z)))\\\\


\exists x:  (x\gt 0 \land \exists y:  (y\lt 0\land \forall  z: (z\geq 0 \vee 2x+y\leq z)))\\\\
\end{gathered}$$
##### c) $\forall x: (x\lt 0 \implies \exists y: (y\lt 0 \land \forall z: (z\lt 0 \implies 2x+y\lt z)))$

$$\begin{gathered}
\exists x: \neg (x\lt 0 \implies \exists y: (y\lt 0 \land \forall z: (z\lt 0 \implies 2x+y\lt z)))\\\\
\exists x: \neg (x\geq 0 \vee \exists y: (y\lt 0 \land \forall z: (z\lt 0 \implies 2x+y\lt z)))\\\\

\exists x: (x\lt 0 \land \forall y: \neg (y\lt 0 \land \forall z: (z\lt 0 \implies 2x+y\lt z)))\\\\


\exists x: (x\lt 0 \land \forall y:(y\geq 0 \vee \exists z: \neg (z\lt 0 \implies 2x+y\lt z)))\\\\


\exists x: (x\lt 0 \land \forall y:(y\geq 0 \vee \exists z: \neg (z\geq 0 \vee 2x+y\lt z)))\\\\


\exists x: (x\lt 0 \land \forall y:(y\geq 0 \vee \exists z: (z\lt 0 \land 2x+y\geq z)))\\\\

\end{gathered}$$

---
#### 4. Symbolom predykatów $P$ i $R$ przypisujemy znaczenia: $P$ - jest płytą winylową, $R$ - jest nośnikiem audio. Jak można odczytać zapisane symbolicznie wyrażenie:

##### a) $\neg \forall x: (P(x)\implies \neg R(x))$?

$$\begin{gathered}
\exists x: \neg (\neg P(x)\vee \neg R(x))\\
\exists x: (P(x)\land R(x))\\\\
\text{Istnieje coś co jest płytą winylową i jednocześnie jest nośnikiem audio.}
\end{gathered}$$

##### b) $\neg \forall x: (\neg P(x)\land R(x))$?

$$\begin{gathered}
\exists x: \neg (\neg P(x)\land R(X))\\
\exists x: (P(x)\vee \neg R(X))\\
\text{Istnieje coś co jest płytą winylową lub nie jest nośnikiem audio.}

\end{gathered}$$

---
#### 5. Symbolem predykatów $P$ i $R$ przypisujemy znaczenia $P$ - jest stołem, $R$ - jest drewniany. Zapisz symbolicznie zdania.

##### Nie każdy stół jest drewniany.

$\exists x: (P(x)\land \neg R(x))$

##### Żaden stół nie jest drewniany

$\forall x: (P(x)\implies \neg R(x))$

##### Istnieją stoły, które nie są drewniane.

$\exists x: (P(x)\land \neg R(x))$

---
#### 6. Symbolowi predykatu $P$ przypisujemy znaczenie: $P(x,y)$ - $x$ lubi $y$. Jak można zapisać symbolicznie wyrażenie:

##### Pewien deser lubią wszystkie dzieci.

