### Wstęp
#### 2025-04-22
##### Poprzednia: [[Logika 1]]
##### Następna: [[Logika 3]]
##### Zadania: [[]]

#APN #KPN #postać_normalna

---
### Postać normalna

Formuły $p$ i $\sim p$ nazywamy **literałami**, p jest lierałem **pozytywnym** a $\sim p$ literałem **negatywnym**.

Literały $p, \sim p$ są przeciwne.

Klauzula (alternatywa elementarna) jest to alternatywa skończenie wielu literałów, np. $p\vee \sim q\vee r, \sim q$

Koniunkcja elementarna jest to koniunkcja skończenie wielu literałów, np $p\land \sim q\land r, \sim q$

Formuła w **koniunkcyjnej postaci normalnej** (kpn) jest to koniunkcja skończenie wielu klauzul, np:
$(p\vee \sim q \vee r) \land (\sim p \vee \sim r)$

Formuła w **alternatywnej postaci normalnej** (apn) jest to alternatywa skończenie wielu koniunkcji elementarnych np:
$(p\land \sim q \land r) \vee (\sim p \land \sim r)$

**Twierdzenie 1**:
Każda formuła **KRZ*** (klasycznego rachunku zdań) jest logicznie równoważna pewnej formule w **KPN** i pewnej formule w **APN**

---
### KPN oraz APN

**Przykład APN**
$A=p\vee q\Leftrightarrow q \land \sim r$

$$\begin{vmatrix}
\begin{array}{c|c}
p&q&r&p\vee q&\sim r&q\land \sim r&A&APN\\
1&1&1&1&0&0&0&\\
1&1&0&1&1&1&1&p\land q\land \sim r\\
1&0&1&1&0&0&0\\
1&0&0&1&1&0&0\\
0&1&1&1&0&0&0\\
0&1&0&1&1&1&1&\sim p \land q \land \sim r\\
0&0&1&0&0&0&1&\sim p \land \sim q \land r\\
0&0&0&0&1&0&1&\sim p \land \sim q \land \sim r
\end{array}
\end{vmatrix}$$

$$\begin{gathered}
\text{APN}:\\
(p\land q\land \sim r)\vee (\sim p \land q\land \sim r)\vee\\ (\sim p \land \sim q \land r)\vee (\sim p \land s\sim q \land \sim r)
\end{gathered}$$

**Przykład KPN**
$A=p\vee q\Leftrightarrow q \land \sim r$

$$\begin{vmatrix}
\begin{array}{c|c}
p&q&r&p\vee q&\sim r&q\land \sim r&A&KPN\\
1&1&1&1&0&0&0&\sim p \vee \sim q \vee \sim r\\
1&1&0&1&1&1&1\\
1&0&1&1&0&0&0&\sim p \vee q \vee \sim r\\
1&0&0&1&1&0&0&\sim p \vee q \vee r\\
0&1&1&1&0&0&0&p\vee \sim q \vee \sim r\\
0&1&0&1&1&1&1&\\
0&0&1&0&0&0&1&\\
0&0&0&0&1&0&1&
\end{array}
\end{vmatrix}$$

$$\begin{gathered}
\text{KPN}:\\
(\sim p \vee \sim q \vee \sim r) \land (\sim p \vee q\vee \sim r)\land (\sim p \vee q\vee r)\land\\ (p\vee \sim q \vee \sim r)
\end{gathered}$$

---
**Metoda przekształceń**:

Sprowadź formułe $A=p\vee q\Leftrightarrow q\land \sim r$ do **KPN** za pomocą przekształceń:

$$\begin{gathered}
(p\vee q \implies q \land \sim r)\land (q\land \sim r\implies p\vee q)\\\\
[\sim (p\vee q)\vee (q\land \sim r)]\land [\sim (q\land \sim r)\vee (p\vee q)]\\\\
[(\sim p\land \sim q)\vee (q\land \sim r)]\land [\sim q\vee r\vee p \vee q]\\\\
[(\sim p\land \sim q)\vee q] \land [(\sim p\land \sim q)\vee \sim r]\land [\sim q \vee r \vee p \vee q]\\\\
[\sim (p\vee q)\vee q] \land [\sim (p\vee q)\vee \sim r]\land [\sim q\vee r\vee p\vee q]\\\\
(\sim p \vee q)\land (\sim q \vee q)\land (\sim p \vee \sim r)\land (\sim q \vee \sim r)\land (\sim q \vee r\vee p \vee q)
\end{gathered}$$







