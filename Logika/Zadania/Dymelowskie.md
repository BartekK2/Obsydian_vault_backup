

## 1)

##### 1. Oceń prawdziwość wnioskowania:

###### 1. Jeśli jest późno, to dzieci śpią oraz nieprawdą jest, że słońce świeci. Dzieci śpią zawsze i tylko wtedy, gdy słońce nie świeci. Zatem jeśli dzieci nie śpią, to nie jest późno lub słońce świeci.

$$\begin{gathered}
\frac{p\implies (d\land \sim s), d\Leftrightarrow \sim s}{\sim d \implies \sim p \vee s}\\\\
1. p\implies (d\land \sim s)\\
2. d\Leftrightarrow \sim s\\
3. d\implies \sim s \text{ z 2.}\\
4. \sim s \implies d \text{ z 2.}\\
5. \sim d \implies s \text{ z 4.}\\
6. \sim d \text{ założenie do implikacji}\\
7. s \text{ z 5 i 6}\\
8. \sim p \vee s , \text{ dołączenie alternatywy}\\
9. \sim d\implies (\sim p \vee s)
\end{gathered}$$



## 2)

##### 3. Przedstaw w $APN$ i $KPN$ następujące formuły:

###### 1)
$$\begin{gathered}
\sim ((p \implies q)\land (q\implies p))\\
\sim (\sim (p\land \sim q)\land \sim (q\land \sim p))\\
(p\land \sim q)\vee (q\land \sim p) - APN\\
\\\\
[p\vee(q\land \sim p)]\land [\sim q \vee (q\land \sim p)]\\\\\
[(p\vee q)\land (p\vee \sim p))]\land [(\sim q \vee q)\land (q\vee \sim p)]\\\\\
(p\vee q)\land (q\vee \sim p) - KPN
\end{gathered}$$

###### 2. 

$$\begin{gathered}
\sim (p\implies \sim (q\vee p))\\
\sim (\sim (p\land \sim \sim (q\vee p)))\\
\sim (\sim (p\land (q\vee p)))\\
p\land (q\vee p)- KPN\\
(p\land q)\vee p - APN\\
\end{gathered}$$


###### 3. 

$$\begin{gathered}
(p\implies r)\implies (q\implies p)\\\\
\sim (p\land \sim r)\implies \sim (q\land \sim p)\\
(\sim p\vee r)\implies (\sim q\vee p)\\
\sim ((\sim p\vee r)\land \sim (\sim q\vee p))\\
\sim (\sim p \vee r)\vee (\sim q \vee p)\\
(p\land \sim r)\vee (\sim q \vee p)\\
(p\land \sim r)\vee \sim q \vee p - APN\\\\\
(p\land \sim r)\vee (\sim q \vee p)\\
(p\vee (\sim q\vee p))\land (\sim r \vee \sim q\vee p)\\
(p\vee \sim q)\land (\sim r \vee \sim q\vee p)- KPN\\
\end{gathered}$$

###### 4. 
$$\begin{gathered}
(p\implies r)\implies (p\implies q)\\
\sim (p\land \sim r)\implies \sim (p\land \sim q)\\
(\sim p \vee r)\implies (\sim p \vee q)\\
\sim ((\sim p \vee r)\land \sim (\sim p \vee q))\\
\sim (\sim p \vee r)\vee (\sim p \vee q)\\
(p\land \sim r)\vee (\sim p \vee q)\\
(p\land \sim r)\vee \sim p \vee q - APN\\\\\
(\sim p \vee q) \vee (p\land \sim r)\\
A\vee (B\land C)\\
(A\vee B)\land (A\vee C)\\
(\sim p \vee q \vee p)\land (\sim p \vee q \vee \sim r)\\
(\sim p \vee q\vee \sim r)\\
\end{gathered}$$

###### 5.
$$\begin{gathered}
(p\implies (r\implies q))\\
\sim (p\land \sim(r\implies q))\\
\sim(p\land \sim (\sim (r\land \sim q)))\\
\sim(p\land (r\land \sim q))\\
\sim p \vee \sim (r\land \sim q)\\
\sim p \vee \sim r\vee q- APN \ oraz \ KPN\\\\
(\sim p \vee \sim r \vee q) - (KPN)
\end{gathered}$$

###### 6.

$$\begin{gathered}
(p\implies r)\implies (r\implies q)\\
\sim ((p\implies r)\land \sim (r\implies q))\\
\sim ((p\land \sim r)\land \sim (r\land \sim q))\\
\sim (p\land \sim r)\vee (r\land \sim q)\\
p\vee r\vee (r\land \sim q) - APN\\
(r\land \sim q)\vee (r\vee p)\\

(A\land B)\vee C\\
(r\vee r\vee p)\land (\sim q\vee r \vee p)\\
(r\vee p)\land (\sim q\vee r \vee p) - KPN
\end{gathered}$$

###### 7.
$$\begin{gathered}
(p\implies \sim (r\vee q))\\
\sim (p\land (r\vee q))\\
\sim p \vee \sim (r\vee q)\\
\sim p \vee (\sim r \land \sim q) - APN\\
(\sim r \vee \sim p)\land (\sim q \vee \sim p) - KPN
\end{gathered}$$

###### 8.

$$\begin{gathered}
\sim ((p\implies q)\land (q\implies p))\implies (p\vee q)\\\\
\sim (\sim (p\land \sim q)\land \sim (q\land \sim p))\implies (p\vee q)\\
\sim (\sim ((p\land \sim q)\vee (q\land \sim p)))\implies (p\vee q)\\
((p\land \sim q)\vee (q\land \sim p))\implies (p\vee q)\\
\sim (((p\land \sim q)\vee (q\land \sim p))\land \sim (p\vee q))\\
\sim ((p\land \sim q)\vee (q\land \sim p))\vee (p\vee q)\\
\sim (p\land \sim q)\land \sim (q\land \sim p)\vee (p\vee q)\\
(\sim p \vee q)\land (\sim q\vee p)\vee (p \vee q)\\
(\sim p \vee q\vee \sim q)\land (\sim p \vee q\vee p)\vee (p \vee q)\\
(p \vee q) - APN/KPN
\end{gathered}$$

###### 10.

$$\begin{gathered}
(p\land r)\vee (p\land \sim q)\\
(p\vee (p\land \sim q))\land (r\vee (p\land \sim q))\\
((p\land p)\vee (\sim q\land p))\land ((p\vee r)\land (\sim q \vee r))\\
p\land (p \vee r)\land (\sim q \vee r) - KPN
\end{gathered}$$