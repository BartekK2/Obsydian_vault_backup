
### 1. Oblicz prawdopodobieństwo tego, że przypadkowo wybrany element jest $I$ gatunku, jeśli wiadomo, że $5\%$ wszystkich elementów stanowią braki, a $70\%$ niewybrakowanych elementów jest $I$ gatunku

$$\begin{gathered}
P(I)=(1-0.05)\cdot 0.7
\end{gathered}$$
### 2. Niech 
$$\begin{gathered}
\Omega=\{(x,y) \in \mathbb{R}^2: 0 \leq x \leq 4, 0 \leq y \leq 4\}\\
A=\{(x,y) \in \mathbb{R}^2: 0\leq x\leq
 4, 1 \leq y \leq 2\}\\
 
B=\{(x,y) \in \mathbb{R}^2: 0 \leq x \leq 4, 3 \leq y \leq 4\}\\
C=\{(x,y) \in \mathbb{R}^2: 3\leq x\leq
 4, 0 \leq y \leq 4\}
\end{gathered}$$

Zbadaj czy zdarzenia $A,B,C$ są:

- niezależne

- parami niezależne
$$\begin{gathered}
A \text{ oraz } B\\
\text{nie są niezależne ze względu na to że się wykluczają}\\\\
\text{A zdarzenia }A_1,\dots,A_k\\
\text{sa niezależne }\Leftrightarrow \\ \text{ wtedy kiedy są też parami niezalezne}
\end{gathered}$$

---
### 3. Wykaż, że jeżeli zdarzenia $A$ i $B$ są niezależne oraz $A \subset B$, to albo $P(A)=0$, albo $P(B)=1$

$$\begin{gathered}
\text{Warunkiem niezalezności A i B jest:}\\
P(A\cap B)=P(A)\cdot P(B)\\\\
\text{Jednakże tutaj:}\\
A \subset B \Leftrightarrow A\cap B =A\implies \\
\implies P(A \cap B)=P(A)\\\\\
P(A)=P(A)\cdot P(B)\\
1=P(B) \vee P(A)=0
\end{gathered}$$

---
### 4. Wykaż, że jeżeli zdarzenia $A$ i $B$ sa niezależne, to także zdarzenia $A'$ i $B'$ są niezależne.

$$\begin{gathered}
Zał:\\
P(A \cap B)=P(A)P(B)\\\\
Teza:\\
P(A'\cap B')=P(A')P(B')\\\\
A' \cap B'=\Omega \setminus (A \cup B)\\\\
P(\Omega \setminus (A\cup B))=1-P(A)-P(B)+P(A)P(B)=\\
=(1-P(A))(1-P(B))=P(A')P(B')
\end{gathered}$$

---
### 5. Prawdopodobieństwo trafienia w ruchomy cel przy jednym strzale wynosi $2/3$. $20$ osób strzela niezależnie do jednego ruchomego celu. Jakie jest prawdopodobieństwo tego, że cel zostanie trafiony?

$$\begin{gathered}
\text{Korzystając z własności udowodnionej }\\
\text{w poprzednim zadaniu:}\\
P(A' \cap B')=P(A')\cap P(B')\\\\
\text{Oraz wiedząc że jeśli zdarzenia }A_1,\dots,A_k \\
\text{są niezalezne to: }\\
P(A_1,\dots,A_k)=P(A_1)\dots P(A_k)\\\\
P(N)=1-2/3=1/3\\\\
P(N_1,\dots,N_{20})=\frac{1}{3^{20}}\\\\
\text{Otrzymaliśmy prawdopodobieństwo że nikt nie trafi}\\\\
\text{Zatem możemy z tego policzyć prawdopodobieństwo }\\
\text{że trafi ktokolwiek:}\\\\
P(T)=1-P(N_1,\dots,N_{20})=1-\frac{1}{3^20}
\end{gathered}$$

---
### 6. Trzy ściany czworościanu zostały pomalowane na, odpowiednio, biało, czerwono i zielono. Czwarta została pomalowana w biało-czerwono-zielone pasy. Doświadczenie polega na rzucaniu czworościanu na płaszczyzne i obserwowanie koloru ściany, na którą upadł. Zdarzenie $B$ oznacza upadek na ściane z kolorem białym, C - upadek na ścianę z kolorem czerwonym, a Z - upadek na ścianę z kolorem zielonym. Sprawdź, czy zdarzenia $B,C$ i $Z$ są:

a) niezależne
b) niezależne
$$\begin{gathered}
\Omega=\{S_b,S_c,S_z,S_p\}\\
P(B)=P(C)=P(Z)=\frac{2}{4}\\
P(B\cap C)=P(B\cap Z)=P(Z \cap C)=\frac{1}{4}=(\frac{2}{4})^2\\\\
\text{tak, te zdarzenia sa parami niezalezne}\\
\text{Ale nie są niezależne bo nie spełniają własności}\\
P(A,B,C)=P(A)P(B)P(C)\\
\text{ponieważ:}\\
L=\frac{1}{4}, R=\frac{1}{8}
\end{gathered}$$---
### 7. Niech $D$ będzie ograniczonym podzbiorem $\mathbb{R}^n$ i $S \subset D$, przy czym $0\lt |S| \lt |D|$. Algorytm przeszukiwania przypadkowego polega na wykonywaniu niezaleznych losowań po 1 punkcie ze zbioru $D$. Oblicz, ile losowań należy wykonać, żeby prawdopodobieństwo tego, że przynajmniej 1 z wylosowanych punktów należy do zbioru $S$ było nie mniejsze niż $\delta$ 


$$\begin{gathered}
\text{Zacznijmy od policzenia prawdopodobieństwa}\\
\text{że żaden z wylosowanych punktów }\\
\text{nie należy do S}\\\\
P(N_S)=1-\frac{|S|}{|D|}\\\\
\text{powtarzając to losowanie k razy:}\\\\
P(N_{S_k})=\left(1-\frac{|S|}{|D|}\right)^k\\\\
\text{teraz wystarczy wziąć zdarzenie przeciwne}\\
\text{otrzymujemy:}\\\\
P(T_{S_k})=1-\left(1-\frac{|S|}{|D|}\right)^k\geq \delta\\\\
1-\delta\leq (1-\frac{|S|}{|D|})^k\\\\
k\geq \frac{\ln{1-\delta}}{\ln{1-p}}
\end{gathered}$$
