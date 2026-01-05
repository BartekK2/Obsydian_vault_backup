
## Metoda elementów skończonych

Zaczynając od równania:
$$\begin{gathered}
-ku''(x)=0&x \in [0,1] &u(0)=u_0&ku'(1)=u_z
\end{gathered}$$

Obie strony równania mnożymy przez funkcje testującą $v(x)$ a następnie całkujemy obustronnie:

$$\begin{gathered}
-k \int^{1}_{0}u''(x)v(x)dx=0
\end{gathered}$$
przekształcamy z całki przez części:
$$\begin{gathered}
k \int^{1}_{0}{u'(x)v'(x)dx}- ku'(1)v(1)+ku'(0)v(0)=0
\end{gathered}$$
Podstawiając warunki:
$$\begin{gathered}
k \int^{1}_{0}{u'(x)v'(x)dx}- u_zv(1)+ku'(0)v(0)=0
\end{gathered}$$
Następnie przenosimy na prawą strone $u_zv(1)$ i otrzymujemy:
$$\begin{gathered}
k \int^{1}_{0}{u'(x)v'(x)dx}+ku'(0)v(0)=u_zv(1)
\end{gathered}$$
Następnie analogicznie do metody różnic skończonych dokonamy "shiftu" warunku dirichleta:
$$\begin{gathered}
u=w+\overline{u}\\
w(0)=0\\
\overline{u}(0)=u_0\\
\overline{u}=(1-x)u_0\\\\
u'=w'-u_0
\end{gathered}$$

Podstawiając do równania dostajemy:

