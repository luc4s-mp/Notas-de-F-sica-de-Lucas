No todas las sucesiones ([[Sucesión]]) convegen, existen algunas que no lo hacen por ejemplo $a_n = (-1)^n$ es obvio que diverge pero _¿Cómo lo demostramos?_ Existen diversos límites de divergen uno de ellos  es el límite al infinito positivo:
> #Definición Diremos que $\{a_n\}$ definida en [[R]] tiene a **infinito**,  y lo denotaremos por $$\lim_{n \rightarrow \infty} a_n = + \infty$$Si para todo $M > 0$ existe $N \in \mathbb{N}$ tal que $a_n > M$ para todo $n > N$.

Pero a diferencia de una sucesión arbitraria divergente, al menos podemos hacer una referencia del "comportamiento" de una sucesión que tiene límite infinito. En este caso, podemos decir de manera informal que *a medida que el índice n se hace cada vez más grande, entonces $a_n$ también se hace cada vez más grande*.
Podemos presentar la misma definición para cuando la sucesión hace más grande y negativa. Cambiando que ahora $a_n < - M$ para todo $n > N$. 
Es obvio que la sucesión $a_n = n$ tiene al infinito pues como vimos en [[Axiomas (Básicos) de los números reales]] los naturales no están acotados superiormente.
Por ejemplo la sucesión $\lim_{n \rightarrow \infty} \frac{n^4+ 3n^2}{3n^3-n^2-1} = + \infty$, analizandolo lógicamente  es obvio que esto ocurre pues el polinomio del numerador $n^4 + 3n^2$ crece más rápido que el polinomio denominador pues es de grado mayor. 

## El Lema del Sandwitch
Sería útil disponer de una herramienta que facilite encontrar la convergencia o divergencia de sucesiones más complicadas como $a_n = \frac{n}{2^n}$. Intuitivamente, veamos que las sucesiones divergen, pero $2^n$ crece mucho más rápido que $n$ (por ejemplo para $n = 20$ tenemos $\frac{20}{1048576}$). Podemos preguntarnos _¿En que momento se supera $2^n$ a $n$?_ se puede verificar por el [[Principio de la inducción]] que, $2^n > n^2$ para todo $n> 3$, por lo cual $\frac{1}{2^n} < \frac{1}{n^2}$ y tenemos que podemos acotar:
$$0 \leq \frac{n}{2^{n}} \leq \frac{n}{n^2} = \frac{1}{n} \quad \quad (\forall n > 3)$$
Entonces, para que nos quede para todo $n \in \mathbb{N}$ podemos hacer $$0 \leq \frac{n}{2^n}\leq\frac{n+3}{2^{n+3}} \leq \frac{1}{n+3}$$
Notemos que tenemos una sucesión que está acotada entre otras dos que a medida que $n \rightarrow \infty$ se acercan cada vez más a 0, entonces queda claro que para que se siga cumpliendo la desigualdad $a_n = n/2^n$ también tiene que estar acercandose a 0. De aquí sale un lema muy importante:
> **Lema del sandwich (o de las sucesiones encajadas).** Si $a_n \leq b_n \leq c_n$ para todo $n$ y $$\lim _{n \rightarrow \infty} a_n=\lim _{n \rightarrow \infty} c_n=\ell,$$entonces $\operatorname{lim}_{n \rightarrow \infty} b_n=l$.

**Demostración**. Sabemos que
$$
\lim _{n \rightarrow \infty} a_n=\lim _{n \rightarrow \infty} c_n=\ell,
$$
o sea,
$$
\begin{aligned}
&\forall \varepsilon_1>0 \exists N_1 \text { tal que }\left(n \geq N_1 \Rightarrow\left|a_n-\ell\right|<\varepsilon_1\right) .  & (4)\\
&\forall \varepsilon_2>0 \exists N_2 \text { tal que }\left(n \geq N_2 \Rightarrow\left|c_n-\ell\right|<\varepsilon_2\right) . & (5)
\end{aligned}
$$
Dado $\varepsilon>0$, buscamos $N=N(\varepsilon)$ tal que
$$
n \geq N \Rightarrow\left|b_n-\ell\right|<\varepsilon .
$$
Pero
$$
\begin{aligned}
&\left|a_n-\ell\right|<\varepsilon_1 \text { si y solo si } \quad \varepsilon_1<a_n-\ell<\varepsilon_1, \\
&\left|c_n-\ell\right|<\varepsilon_2 \text { si y solo si } \quad \varepsilon_2<c_n-\ell<\varepsilon_2 .
\end{aligned}
$$
Por hipótesis, $a_n \leq b_n \leq c_n$. Restamos miembro a miembro $\ell$ y usamos (4) y (5), obteniendo
$$
-\varepsilon_1<a_n-\ell \leq b_n-\ell \leq c_n-\ell<\varepsilon_2 . \quad (6)
$$
Podemos tomar $\varepsilon_1=\varepsilon_2=\varepsilon$ y $N=\operatorname{máx}\left\{N_1, N_2\right\}$. En efecto, si $n>N$, entonces $n>N_1$ y $n>N_2$. Luego valen la primera desigualdad y la última desigualdad en (6), y en particular,
$$
\varepsilon=\varepsilon_1<b_n-\ell<\varepsilon_2=\varepsilon,
$$
o equivalentemente,
$$
\left|b_n-\ell\right|<\varepsilon,
$$
como queríamos. $\blacksquare$ 

## ¿Cómo encontramos si una sucesión es divergente?
Hagamos antes unos ejemplos por definición.

Ejemplo. Verificar que $\operatorname{lím}_{n \rightarrow \infty} \sqrt{n}=\infty$.
Dado $M>0$, buscamos $N=N(M)$ tal que
$$
n>N \Longrightarrow \sqrt{n}>M .
$$
Despejando $n$, vemos que podemos tomar $N=M^2$. En efecto, si $n>N=M^2$, tomando raíz cuadrada miembro a miembro, y usando que $0<x<y \Longrightarrow \sqrt{x}<\sqrt{y}$ (conocemos la implicación equivalente $a, b>0, a^2<b^2 \Longrightarrow a<b$ ) llegamos a que $\sqrt{n}>M$, como queríamos.

Ejemplo. Verificar por definición que
$$
\lim _{n \rightarrow \infty} \frac{n^3+n}{3 n+1}=\infty .
$$
Dado $M>0$, buscamos $N=N(M)$ tal que
$$
n>N \Longrightarrow \frac{n^3+n}{3 n+1}>M .
$$
Planteamos
$$
\frac{n^3+n}{3 n+1} \underset{(\leq)}{\geq} \frac{n^3}{3 n+n}=\frac{n^3}{4 n}=\frac{n^2}{4}>M .
$$
Despejando $n$, observamos que podemos tomar $N=\sqrt{4 M}=2 \sqrt{M}$.
Por ejemplo, si $M=10^4$, para $n>200$ tendremos 
$$
\frac{n^3+n}{3 n+1}>10^4
$$

Podemos definir de la misma manera al límite de $\lim_{n \rightarrow \infty} a_n = - \infty$  que dado un número muy grande $M > 0$ entonces la sucesión se hace cada vez más negativa tal que $a_n < - M$.  

Al igual que con los límites finitos si tenemos **dos sucesiones que divergen operar con ellas nos va a dar (casi siempre) otra sucesión divergente**. Es obvio que $n^3 + n$ diverge, para no tener que demostrarlo por definición si podemos probar que $n^3$ diverge, $n$ también diverge y que la suma de dos sucesiones divergentes diverge entonces listo. De esta manera nacen las siguientes proposiciones que nos enseñan como lidear con las sucesiones que tienden al infinito:

> **Proposición 1. (Criterios de Comparación para sucesiones)** Si $a_n \leq b_n$ para todo $n \in \mathbb{N}$ :
> 1. Si $\lim a_n = +\infty$, entonces $\lim b_n = +\infty$ 
> 2. Si $\lim b_n = - \infty$, entonces $\lim a_n = - \infty$.

Este criterio nos ayuda a encontrar la divergencia de sucesiones usando otras como por ejemplo $n < 2^n$ y como sabemos que $\lim n = + \infty$ entonces $\lim 2^n = + \infty$.

**Demostración.** Como $\lim_{n \rightarrow \infty} a_n = \infty$, para $M > 0$ existe $N \in \mathbb{N}$ tal que $n > N$ entonces $a_n > M$. A su vez $b_n \geq a_n$, entonces $b_n \geq a_n > M$ para todo $n > N$. Entonces, $b_n > M$ para todo $n > N$. Pero esto es la definición de $\lim_{n \rightarrow \infty} b_n = \infty$. La demostración para $- \infty$ es parecida $\blacksquare$  

> **Proposición 2.** Si $$\lim _{n \rightarrow \infty} a_n=\infty, \quad \lim _{n \rightarrow \infty} b_n=\infty \quad \text { y } \quad \lim _{n \rightarrow \infty} c_n=\ell \neq 0,$$entonces
> 1. $\lim _{n \rightarrow \infty} a_n+b_n=\infty$,
> 2. $\operatorname{lim}_{n \rightarrow \infty} a_n b_n=\infty$,
> 3. $\lim _{n \rightarrow \infty} a_n+c_n=\infty$,
> 4. $\lim _{n \rightarrow \infty} \frac{1}{a_n}=0$,
> 5. $\lim _{n \rightarrow \infty} a_n c_n=\infty, \quad$ si $\ell>0$
> 6. $\lim _{n \rightarrow \infty} a_n c_n=-\infty$, si $\ell<0$.

**Demostración.** 
1.  Por definición tenemos que 
$$
\begin{aligned}
&\forall M_1>0 \exists N_1 \text { tal que }\left(n>N_1 \Longrightarrow a_n>M_1\right), & (1) \\
&\forall M_2>0 \exists N_2 \text { tal que }\left(n>N_2 \Longrightarrow b_n>M_2\right) . & (2)
\end{aligned}
$$
Debemos mostrar que
$$
\forall M>0 , \; \exists N \text { tal que }\left(n>N \Longrightarrow a_n +b_n>M\right) .
$$
Supongamos que nos dan un $M_1$ y un $M_2$ tal que se cumple (1) y (2) para algún $N_1$ y $N_2$, entonces $a_n +b_n > M_1 + M_2$. Si elegimos tomar $M_1 = M_2 = \frac{M}{2}$ nos queda  $a_n + b_n > \frac{M}{2} + \frac{M}{2} = M$ eligiendo $N = \frac{M}{2} \mathrm{máx}\{N_1, N_2\}$, lo que queriamos.
2. De nuevo tenemos (1) y (2) y queremos probar que 
$$\forall M>0 , \; \exists N \text { tal que }\left(n>N \Longrightarrow a_nb_n>M\right) .$$
Sea $M>0$. Planteamos
$$
a_n b_n>M_1 M_2=M
$$
Luego podemos tomar $M_1=M_2=\sqrt{M}$. Si $n>N_1(\sqrt{M})$ y $n>N_2(\sqrt{M})$, entonces
$$
a_n b_n>\sqrt{M} \sqrt{M}=M
$$
Así $N=\operatorname{máx}\left\{N_1(\sqrt{M}), N_2(\sqrt{M})\right\}$. 
3. Tenemos ahora como hipótesis (1) y 
$$\begin{align}
\forall \epsilon_3 > 0, \exists N_3 \text{ tal que } (n > N_3 \implies |c_n - l| < \epsilon && (3)\end{align}
$$
Como $\lim _{n \rightarrow \infty} c_n=l$, para $\epsilon=1$, existe $N \in \mathbb{N}$ tal que $\left|c_n-l\right|<1$ para todo $n>N$. O bien, $-1<c_n-l<1$ para todo $n>N$. Luego, $l-1<c_n<l+1$ para todo $n>N$. Por lo tanto
$$
a_n+(l-1)<a_n+c_n \quad \text { para todo } n>N \text {. }
$$
Ahora, el límite de una sucesión que tiende al infinito más una constante es infinito, $\lim _{n \rightarrow \infty} a_n+(l-1)=\infty$. Pero usando el inciso (1) de la Proposición anterior resulta que $\lim _{n \rightarrow \infty} b_n+a_n=\infty$.
4. Como hipótesis sabemos (1), supongamos que existe un $\epsilon > 0$ tal que $M = \frac{1}{\epsilon}$, existe un $N \in \mathbb{N}$ tal que si $n > N$ entonces $a_n > M = \frac{1}{\epsilon}$. Por lo tanto, para $\epsilon$ dado, si $n > N$ se cumple $\frac{1}{a_n} < \epsilon$ siempre que $a_n \neq 0$. Pero esto es la definición de $\lim_{n \rightarrow \infty} \frac{1}{a_n} = 0$. 
Las demostraciones de (5) y (6) son parecidas, para (5) si tomamos $\epsilon = \frac{l}{2} > 0$, $|c_n - l | < \epsilon \rightarrow l - \epsilon < c_n < l + \epsilon$ entonces $a_nc_n < (l+\epsilon)M$ si $l > 0$, entonces $(l+\epsilon) > 0$ y nos queda que $(l+\epsilon)M > 0$ y se cumple la definici´pon de límite al infinito positivo. $\blacksquare$ 

