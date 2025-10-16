### Wstęp
#### 2025-03-07
##### Następna: [[]]
##### Zadania: [[]]

#tautologia #kontrtautologia 

---
### Definicje:

#### **Tautologia:**

Formuła jest tautologią KRZ (klasycznym rachunku zdań) wtedy i tylko wtedy, gdy przy każdym wartościowaniu przyjmuje wartość 1.

Tautologią nazywamy formułe $\alpha$ taką, że $w^*(\alpha)=1$ dla dowolnego wartościowania $w$.

##### **Ważne tautologie:**

Prawo wyłączonego środka: $p\ \vee \sim p$

Prawo sprzeczności: $\sim (p\land \sim p)$

Prawo podwójnej negacji: $\sim (\sim p)\Leftrightarrow p$

Prawa idempotentności koniunkcji i alternatywy: $(p \land p)\Leftrightarrow p, \ \ (p\vee p)\Leftrightarrow p$

...

**Prawa De Morgana:** 

$$\begin{gathered}
\sim (p\land q) \Leftrightarrow\sim  p\ \vee \sim q\\
\sim (p \vee q)\Leftrightarrow \sim p\  \land \sim q
\end{gathered}$$
**Prawo zaprzeczenia implikacji:**
$$\begin{gathered}
\sim (p\implies q)\Leftrightarrow (p\ \land \sim q)
\end{gathered}$$
**Prawo transpozycji:**
$$\begin{gathered}
(p\implies q)\Leftrightarrow (\sim q\implies \sim p)
\end{gathered}$$
**Prawa łączności koniunkcji, alternatywy i równoważności:**
$$\begin{gathered}
(p\land q)\land r \Leftrightarrow p\land (q\land r)\\
(p\vee q)\vee r \Leftrightarrow p\vee (q\vee r)\\
[(p\Leftrightarrow q)\Leftrightarrow r]\Leftrightarrow [p\Leftrightarrow (q\Leftrightarrow r)]
\end{gathered}$$
**Prawa rozdzielności koniunkcji względem alternatywy i alternatywy względem koniunkcji:
$$\begin{gathered}
p\land(q\vee r)\Leftrightarrow (p\land q)\vee (p\land r)\\
p\vee (q\land r)\Leftrightarrow (p\vee q)\land (p\vee r)
\end{gathered}$$

**Bardzo ważne:**

Modus ponendo ponens (reguła odrywania) $[p \land (p\implies q)]\implies q$
Modus tollendo tollens $[(p\implies q)\land  \sim q]\implies \sim p$
Prawo kompozycji $(p\vee q\implies r) \implies (p\implies r)$
Prawo symplifikacji: $(p\land q)\implies p$
Prawo symplifikacji $q\implies (p\vee q)$
Prawo symplifikacji $(p\implies q)\implies p$
Prawo Dunsa Szkota $\sim p \implies (p\implies q)$
Prawo dylematu konstrukcyjnego:
$[(p\implies r) \land (q\implies r) \land (p\vee q)] \implies r$
Prawo eksportacji $(p\land q \implies r)\implies p \implies q\implies r$
Prawo importacji $(p\implies q \implies r)\implies p\land q \implies r$
Prawo redukcji do absurdu $(p\implies \sim p)\implies \sim p$
Prawo sylogizmu hipotetycznego $[(p\implies q)\implies (q\implies r)]\implies (p\implies r)$
Prawo Peirce'a $((p\implies q)\implies p)\implies p$
Prawo Claviusa $(\sim p \implies p)\implies p$


**Ważne funktory**:
$\oplus$ - alternatywa wykluczająca
$\downarrow$ - negacja alternatywy (**binegacja**)
$\mid$ - negacja koniunkcji (**dysjunkcja**)

---
