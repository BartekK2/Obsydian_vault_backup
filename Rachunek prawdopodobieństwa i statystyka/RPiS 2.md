### Prawdopodobieństwo warunkowe

Niech $(\Omega,\Sigma,P)$ będzie przestrzenią probabilistyczną.

**Definicja**

Niech $A,B \subset \Omega$ będą zdarzeniami, przy czym zakładamy, że $P(B)\gt 0$. **Prawdopodobieństwem $A$ pod warunkiem $B$** nazywamy liczbę nieujemną.

$$\begin{gathered}
P(A|B)=\frac{P(A \cap B)}{P(B)}
\end{gathered}$$
#### Własności 
Zakładając że $B$ jest dowolnym zdarzeniem takim, że $P(B)\gt 0$. 
1. Dla dowolnego zdarzenia $A$ 
   $P(A\cap B)=P(A|B)P(B)$
2. Jeśli dodatkowo $P(A)\gt 0$, to
   $P(A\cap B)=P(B|A)P(A)$
3. Dla dowolnego zdarzenia $A$
   $0\leq P(A|B)\leq 1$
4. Dla dowolnego zdarzenia $A$
   $P(A|\Omega)=P(A)$
5. $P(\emptyset|B)=0$ i $P(B|B)=1$
6. Jeśli zdarzenia $A_1,A_2,\dots$ się wykluczają to:
   $P \left( \bigcup^\infty_{i=1} A_i|B\right)=\sum^{\infty}_{i=1}P(A_i|B)$

---
### Oznaczenia 

$$\begin{gathered}
P(A_1,\dots,A_k)=P(A_1 \cap \dots \cap A_k)\\
P(A_1,\dots,A_k|B)=P(A_1 \cap \dots \cap A_k|B)\\
P(B|A_1,\dots,A_k)=P(B|A_1 \cap \dots \cap A_k)
\end{gathered}$$

---
### Reguła wielokrotnego warunkowania

Indukcyjnie pokazujemy że można przekształcić:
własność 1
$$\begin{gathered}
P(A\cap B)=P(A|B)P(B)
\end{gathered}$$


$$\begin{gathered}
P(A_1,\dots,A_k)=P(A_1|A_2,\dots,A_k)P(A_2|A_3,\dots,A_k)\dots P(A_{k-1}|A_k)P(A_k)
\end{gathered}$$

---
### Układ zupełny zdarzeń

Ciąg (skończony lub nieskończony) zdarzeń $A_1, A_2, \dots$ nazywamy
układem zupełnym zdarzeń (lub podziałem przestrzeni $\Omega$) jeśli
zdarzenia w ciągu parami wzajemnie się wykluczają, tzn

$$\begin{gathered}
A_i \cap A_j = \emptyset \text{ dla }i\neq j
\end{gathered}$$
oraz zachodzi równość:
$$\begin{gathered}
\Omega=\bigcup_i A_i
\end{gathered}$$

---
### Twierdzenie o prawdopodobienstwie całkowitym 

Jeśli zdarzenia $A_1,A_2,\dots$ tworzą układ zupełny oraz $P(A_i)\gt 0$ dla każdego $i$, to dla dowolnego zdarzenia $B$ zachodzi równość
$$\begin{gathered}
P(B)=\sum_iP(B|A_i)P(A_i)
\end{gathered}$$

---
### Twierdzenie Bayesa 

Jeśli zdarzenia $A$ i $B$ mają dodatnie prawdopodobieństwo, to
$$\begin{gathered}
P(A|B)=\frac{P(B|A)P(A)}{P(B)}
\end{gathered}$$

W pudełku są 3 monety normalne i jedna fałszywa, która ma dwie reszki. Wyciągamy jedną monetę i rzucamy nią otrzymując reszkę. Jakie jest prawdopodobieństwo tego, że wybrana moneta jest fałszywa?

$$\begin{gathered}
R - reszka\\
F - falszywa\\\\
P(R|F)=1\\
P(F)=\frac{1}{4}\\\
P(R)=\frac{3}{4}\cdot \frac{1}{2}+\frac{1}{4}=\frac{5}{8}\\
\\\
P(F|R)=\frac{P(R|F)P(F)}{P(R)}=\frac{\frac{1}{4}}{\frac{5}{8}}=\frac{2}{5}\\
\end{gathered}$$
Jeśli zdarzenia $A_i$ tworzą układ zupełny taki, że $P(A_i)\gt 0$ dla każdego $i$, a $B$ jest zdarzeniem takim, że $P(B)\gt 0$, to dowolnego $k$ zachodzi równość
$$\begin{gathered}
P(A_k|B)=\frac{P(B|A_k)P(A_k)}{\sum_iP(B|A_i)P(A_i)}
\end{gathered}$$
---
### Niezależność zdarzeń

**Definicja**
Zdarzenia $A$,$B$ nazywamy **niezależnymi** jeśli
$$\begin{gathered}
P(A\cap B)=P(A)P(B)
\end{gathered}$$
Czyli wiedza o tym że wylosowaliśmy $B$ nie sprawia że szansa na $A$ nam sie zmieniła.
$$\begin{gathered}
P(A|B)=\frac{P(A \cap B)}{P(B)}=P(A)
\end{gathered}$$
Zdarzenia $A_1,A_2,\dots,A_k$ nazwiemy **niezależnymi** jeśli dla dowolnych $i_1,\dots,i_m$ takich że $i_j\in \{1,\dots,k\}$ zachodzi równość 
$$\begin{gathered}
P(A_{i_1},\dots,A_{i_m})=P(A_{i_1})\dots P(A_{i_m})
\end{gathered}$$

#### Własności niezależności

1. Każde zdarzenie jest niezależne od $\emptyset$
2. Każde zdarzenie jest niezależne od $\Omega$ 
3. Jeśli zdarzenia $A$ i $B$ o **dodatnich prawdopodobieństwach** się wzajemnie wykluczają to są **zależne**
4. Jeśli zdarzenia $A$ i $B$ są niezależne oraz $P(B)\gt 0$, to
$$\begin{gathered}
P(A|B)=P(A)
\end{gathered}$$
5. Jeśli zdarzenia $A$ i $B$ są niezależne oraz $P(A)\gt 0$, to 
$$\begin{gathered}
P(B|A)=P(B)
\end{gathered}$$
6. Jesli zdarzenia $A_1, \dots, A_k$ są niezależne, to sa **parami niezależne** tzn. dla każdych $i,j \in \{1,\dots,k\}$ zachodzi równość
$$\begin{gathered}
P(A_i\cap A_j) = P(A_i)P(A_j)
\end{gathered}$$
7. Jeśli zdarzenia $A_1,\dots, A_k$ są niezależne to 
$$\begin{gathered}
P(A_1,\dots,A_k)=P(A_1)\dots P(A_k)
\end{gathered}$$

---
### Niezależność warunkowa 

Niech $C$ będzie zdarzeniem o dodatnim prawdopodobieństwie 

**Definicja**
Zdarzenia $A$ i $B$ są **warunkowo niezależne względem** $C$ jeśli:

$$\begin{gathered}
P(A \cap B|C)=P(A|C)P(B|C)
\end{gathered}$$
Zdarzenia $A_1,\dots, A_k$ są **warunkowo niezależne względem** $C$ jeśli dla dowolnych $i_1,\dots,i_m$ takich, że $i_j \in \{1,\dots,k\}$ zachodzi równość:
$$\begin{gathered}
P(A_{i_1},\dots,A_{i_m}|C)=P(A_{i_1}|C)\dots P(A_{i_m}|C)
\end{gathered}
$$

