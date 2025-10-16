### Systemy założeniowe
#### 2025-04-23
##### Poprzednia: [[Logika 2]]
##### Następna: [[Logika 4]]
##### Zadania: [[]]

#systemy_zalozeniowe 

---
### Systemy założeniowe

**wnioskowanie** - proces, w którym na podstawie pewnych uznanych formuł (przesłanek) dochodzimy do uznania innej formuły (wniosku)

**Przykład:**
$$\begin{gathered}
\frac{\text{Dziś jest sobota}}{\text{Jutro będzie niedziela}}
\end{gathered}$$

**wnioskowanie dedukcyjne** - o przyjęciu wniosku nie decydujemy na podstawie jego treści czy też treści przesłanek, a na podstawie ich postaci

schemat wnioskowania jest *niezawodny* $\Leftrightarrow$ nie da się w nim z prawdziwych przesłanek dojść do fałszywego wniosku

### Reguły wnioskowania

**reguła wnioskowania** - sposób przekształcenia ciągu formuł $\alpha_1,\alpha_2,\dots$ (przesłanek) w formułe $\beta$ (wniosek) w którym jeśli przesłani są prawdziwe to wniosek też jest prawdziwy:

$$\begin{gathered}
\begin{vmatrix}
\begin{array}{c|c|c}
RO&\text{Reguła odrywania (modus ponens)}&\frac{\alpha, \alpha \implies \beta}{\beta}\\
&\text{Reguła podstawiania}&\frac{\alpha}{\alpha[k\setminus\beta ]}\\
DK&\text{Reguła dołączania koniunkcji}&\frac{\alpha_1,\alpha_2}{\alpha_1\land \alpha_2}\\
OK&\text{Reguła opuszczania koniunkcji}&\frac{\alpha_1 \land \alpha_2}{\alpha_1, \alpha_2}\\
DA &\text{Reguła dołączania alternatywy}&\frac{\alpha}{\alpha \vee \beta }\\
OA &\text{Reguła opuszczania alternatywy}&\frac{\alpha \vee \beta, \sim \alpha}{\beta}\\
MT&\text{Reguła modus tollens}&\frac{\alpha \implies\beta, \sim \beta}{\sim \alpha}\\
&\text{Reguła transpozycji}&\frac{\alpha \implies \beta}{\sim \beta \implies \sim \alpha}\\
ON&\text{Reguła opuszczania negacji}&\frac{\sim \sim \alpha}{\alpha}\\
\end{array}
\end{vmatrix}
\end{gathered}$$

---
### Tezy rachunku logicznego

**tezy** rachunku logicznego: formuły, które na gruncie systemu posiadają *dowód*

Niech $A$ będzie skończonym zbiorem formuł $\{\alpha_1,\alpha_2, \dots, \alpha_n\}$, a $\beta$ będzie formuła języka rachunku logicznego. $A ⊢ \beta$ wtw. gdy istnieje dowód $\beta$ w oparciu o formuły zbioru $A$ oraz przyjęte w systemie reguły wnioskowania - formuła $\beta$ jest *dowodliwa* (wprowadzalna) z $A$.

---
### Założeniowy system rachunku zdań

Systemy założeniowe są oparte na regułach wnioskowania - przyjmuje się pewne **niezawodne pierwotne reguły wnioskowania** (jak wyżej). Z nich można wnioskować **reguły wtórne** (własne na podstawie pierwotnych). Czyli jeśli udowodnimy że $\alpha \implies \beta$, można wprowadzić nową regułe $\frac{\alpha}{\beta}$. Późniejsze dowody można oprzeć o wcześniej udowodnione wyrażenia. Proces wnioskowania można zatem traktować jako dowód.

Do budowy takiego systemu potrzebujemy też **języka formalnego** i **zasad konstrukcji dowodu**.

**Przykład**: Poniższe zdania są sobie równoważne:

$$\begin{gathered}
\{\alpha_1, \alpha_2, \alpha_3\}⊢\beta\\
\{\alpha_1, \alpha_2\}⊢\alpha_3\implies \beta\\
\{\alpha_1\}⊢\alpha_2\implies (\alpha_3\implies \beta)\\

\emptyset⊢\alpha_1 \implies (\alpha_2\implies (\alpha_3\implies \beta))\\
\end{gathered}$$

**Dowód założeniowy wprost** to ciąg formuł logicznych spełniający następujące warunki:

1. Pierwszymi formułami dowodu są założenia
2. Każda następna formuła jest otrzymana z poprzedzających ją formuł, przy użyciu reguł wnioskowania lub wcześniej udowodnionego twierdzenia.
3. Ostatnią formułą dowodu jest wniosek.


#### Przykłady:

$$\begin{gathered}
\frac{p\implies q, q\implies r}{p\implies r}\\
założenia - \left\{

\begin{matrix}
1. p\implies q\\
2. q\implies r
\end{matrix}
\right.\\
3. p\ \text{(poprzednik wniosku)}\\
4. q, RO. 1,3\\
5. r RO. 2,4
\end{gathered}$$


$$\begin{gathered}
\frac{\alpha \implies (\beta \implies \delta)}{\beta \implies (\alpha \implies \delta)}\\\\
założenia - \left\{

\begin{matrix}
1.\alpha\implies (\beta\implies \delta)\\
2. \beta \\
3. \alpha 
\end{matrix}
\right.\\
4. \beta \implies \delta  \ RO. 1,3\\
5. \delta \ RO. 2,4
\end{gathered}$$



