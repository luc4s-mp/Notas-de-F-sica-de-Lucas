# Teorema Fundamental de la Aritmética
El teorema fundamental de la aritmética nos dice porque los [[Números primos]] son tan importantes, son la estructura básica de la que se construyen todos los enteros.

> **Teorema. (Fundamental de la Aritmética)** Para cada entero $n>1$ existe una fatorización en números primos $p_{1}^{e^1}p_2^{e^2} \dots p_k^{e^k}$ donde $p_1, p_2, \dots, pk$ son primos todos distintos entre sí y $e_1,e_2, \dots, e_k$ son enteros positivos. Esta factorización es única, aparte de permutaciones de los factores.

**Demostración**. 
- **Existencia:** Si $m$ es primo, $m \in \mathbb{N} \Rightarrow m = \prod_{j=1}^{1} p_j$. (O sea $p_1 = m, \; r = 1$); por lo tanto vale el resultado de la existencia. 
Supongamos $m$ no es primo, $m \in \mathbb{N}$. Definimos 
$$H = \{m \in \mathbb{N}-\{1\}: \; m \text{ NO es primo y } m \text{ no admite factorización en primos}\}$$
Queremos probar que $H = \emptyset$, vamos a suponer por el absurdo que $H \neq \emptyset$, luego $H$ tiene 1er elemento por el principio de la buena ordenación (visto en [[Principio de la inducción fuerte]], $h \in H$, $h$ no es primo $h = a \cdot b, \; a, b \in \mathbb{N}-\{1\} \text{ y } a < h, b < h$. Como ya hemos mostrado que debe tener un divisor primo, supongamos $a$ es primo. Luego $a, b \notin H$, como $b \notin H$, $b$ admite factorización en números primos:
$$h = a \cdot b = a \cdot \prod_{j=1}^{r} p_j$$
O sea $h \notin H$ pero se contradice porque empezamos con que $h \in H$. Luego $H = \emptyset$.
Otra forma de demostrar la existencia es utilizando el [[Principio de la inducción]].
- **Unicidad:** Sea $m \in \mathbb{N}- \{1\}$, entonces existen primos positivos $p_1, p_2, \dots, p_r$ tal que $m = \prod_{j=1}^{r} p_j$. Comprobemos la unicidad haciendo una prueba por **inducción** en la cantidad de factores $r$ . Tomemos entonces en la siguiente proposición sobre $\mathbb{N}$: 
 $P(n):$ Si $m \in \mathbb{N}-\{1\}$ y existe $p_1 \leq p_2 \leq \dots \leq p_n$ primos positivos tales que $m = \prod_{j=1}^n p_j$, y además existen primos positivos  $p_1' \leq p_2' \leq \dots \leq p_s'$ tal que $m = \prod_{j=1}^s p_j'$ entonces la cantidad de factores $s = n$ y  $(p_1', \; p_2', \; \dots, \; p_s') = (p_1, \; p_2, \; \dots, \; p_r)$.
	 -  (Caso Base) $P(1)$ es verdadera pues $m = \prod_{j=1}^1 = p_1$, entonces $m$ es primo.
	 - (Paso Inductivo) la hipótesis inductiva nos dice $P(k):$ si tenemos un $m \in \mathbb{N}-\{1\}$ que se factoriza con $k$ factores positivos, entonces dicha factorización es única salvo el orden el que escribimos los factores primos. 
		Queremos ver $P(k+1)$ verdadera. O sea si tenemos un natural que se factoriza con $k+1$ factores primos entonces esa factorización debe ser única. Sea entonces $p_1 \leq p_2 \leq \dots \leq p_k$ primos positivos tal que $m = \prod_{j=1}^{k+1} p_j$. Supongamos que tenemos primos positivos $p_1´ \leq p_2' \leq \dots \leq p_s'$ tal que $m= \prod^s_{j=1}p'_s = \prod_{j=1}^{k+1} p_j$ . En especial, $p_{k+1}|m$ entonces $p_{k+1}| \prod_{j=1}^s p_j'$ . Por una propiedad vista en [[Números primos]] $p_{k+1}$ divide a uno de los factores, digamos $p'_{j_0}$ , $p_{k+1}| p'_{j_0}$ entonces $p_{k+1} = p'_{j_0}$ . Luego tenemos que $p_{k+1}| m = \prod_{j=1}^k p_j = \underset{j \neq j_0}{\prod_{j=1}^s} p'_j$ . 
		Por HI se tiene que $p_{k+1}|m$ es única y por lo tanto $P(k+1)$ verdadera. Lo cual nos dice que $P(n)$ es verdadera, $\forall n \in \mathbb{N}$. 
	Falta considerar el caso $m < -1$ , si $m \in \mathbb{Z}$ luego $-m > 1$ entonces $-m$ se escribe de forma única como producto de primos positivos. $\blacksquare$     

O de otra forma también de demostrar la unicidad es al igualar $(p_1' \cdot p_2', \cdot \; \dots \; \cdot p_s') = (p_1 \cdot p_2 \cdot \; \dots \; \cdot p_r)$ simplificaremos todos los primos comunes, y observaremos que al hacer esto no nos sobra nada, es decir obtenemos $1 = 1$, es que todos los primos y todas las potencias coincidían. 
Si no pasa eso obtenemos que $p_r \neq p_s'$, supongamos que del lado izquierdo sobró un $p_r$, por la igualdad tenemos $p_r$ divide a lo que sobró del lado derecho o al 1 si no sobró nada. Debe existir un primo $p_s'$ que sea divisible por $p_r$ tal que $p_r|p_s'$ pero esto es una contradicción de suponer que sobró un primo de algún lado.

Este teorema nos permite usar las factorizaciones únicas de primos para calcular productos, cocientes, potencias, [[Máximo Común Divisor]] y el mínimo común múltiplo. Definiamos este último y intentemos calcularlo.

---

# Mínimo Común Múltiplo
Dados los múltiplos de dos enteros $a$ y $b$ (se suelen denotar los conjuntos como $\mathrm{Mult}(a)$ y $\mathrm{Mult}(b)$) el conjunto de múltiplos comunes entre ambos ($\mathrm{Mult}(a) \cap \mathrm{Mult}(b)$) debe tener un **primer elemento** por el principio de la buena ordenación (visto en [[Principio de la inducción fuerte]]), este primer elemento se llama **mínimo común múltiplo**. 

> #Definición Sean $a, b \in \mathbb{Z}$ ([[Z]]), no nulos. El **mínimo común múltiplo** entre a y b, que se nota $[a, b]$, es el menor número natural que es un múltiplo común de a y b. Para que sea un mcm de a y b se tienen que cumplir las condiciones:
> 1. $a|m$ y $b|m$
> 2. Si $n \in \mathbb{N}$ es múltiplo de a y de b, entonces $m|n$

> **Proposición.** Si $a, b \in \mathbb{Z}-\{0, 1, -1\} \Rightarrow a = \epsilon \prod_{j=1}^{r} p_j^{k_j}$ y $b = \epsilon' \prod_{j=1}^{r} p_j^{k_j}$, donde $\epsilon = 1$ o $\epsilon = -1$ y $p_1, p_2,  \dots, p_r$ primos positivos junto con $k_j \in \mathbb{N} \cup \{0\}, l_j \in \mathbb{N} \cup \{0\}, j \in \{1, \dots, r\}$. Entonces, $$[a, b] = \prod_{j=1}^r p_j^{\max\{k_j, l_j\}}$$

**Demostración.** En el [[Máximo Común Divisor]] realizamos la demostración de una proposición identica para el MCD.

> **Teorema (Otra forma de calcular el mcm)**  Sean $a, b \in \mathbb{Z} -\{0\}$. Entonces, $$[a,b] = \frac{|ab|}{(a,b)}$$

**Demostración.** Suponemos que $a, b \in \mathbb{N}$, vamos a ver si $\frac{ab}{(a,b)}$ cumple con las propiedades (1) y (2) de la definición del mcm. Notemos que $\frac{a}{(a,b)} \in \mathbb{N}$ y $\frac{b}{(a,b)} \in \mathbb{N}$, entonces:
$$\frac{ab}{(a,b)} = a \cdot \frac{b}{(a,b)} \implies a \Bigg| \frac{ab}{(a,b)}$$
$$\frac{ab}{(a,b)} = b \cdot \frac{a}{(a,b)} \implies b \Bigg| \frac{ab}{(a,b)}$$
Miremos ahora la condición (2) de la definición de mcm. Tomemos $n \in \mathbb{N}$, múltiplo de $a$ y $b$ o sea $a|n \wedge b|n \Rightarrow n = a \cdot x \wedge n = b \cdot y$. Luego, $\frac{a}{(a,b)} \cdot x = \frac{b}{(a,b)} \cdot y$. Además (gracias a el Teorema de Coprimización que vimos en [[Números primos]]) sabemos que $\big(\frac{a}{(a,b)}, \frac{b}{(a,b)} \big) = 1$.  Lo siguiente que concluimos es que $\frac{a}{(a,b)} \big| y$ y $\frac{b}{(a,b)} \big| x$. Teniendo otro número $z \in \mathbb{Z}$ tal que 
$$x = \frac{b}{(a,b)} \cdot z \Rightarrow n = a\cdot x = a \cdot \frac{b}{(a,b)} \cdot z = \frac{ab}{(a,b)} \cdot z$$ 
Por lo tanto, $\frac{ab}{(a,b)}|n$, que es a lo que queríamos llegar. 
Por último, nos queda comprobar que esta formula sirve para todo [[Z]], como $[a, b] = [|a|, |b|] = \frac{|a||b|}{(|a|,|b|)} = \frac{|ab|}{(a,b)}$. $\blacksquare$ 

--- 
Supongamos que tenemos dos enteros tal que $a = p_1^{e_1}p_2^{e_2} \cdots p_k^{e_k}$ y $b= q_1^{f_1}q_2^{f_2}\cdots q_k^{f_k}$ donde $e_i, f_i \geq 0$ tenemos que (supongamos que $p_i = q_i$ para todo $i \in \{1, \dots, k\}$): 
$$\begin{align}
ab\quad  & = \quad p_1^{e_1+f_1} \cdots p_k^{e_k + f_k} \\
a/b \quad & = \quad p_1^{e_1 - f_1} \cdots p_k^{e_k - f_k} \\
a^m \quad & = \quad p_1^{me_1} \cdots p_k^{me_k} \\
\mathrm{mcd}(a,b) \quad & = \quad p_1^{\mathrm{mín(e_1, f_1)}} \cdots p_k^{\mathrm{mín(e_k, f_k)}} \\
\mathrm{mcm}[a,b] \quad & = \quad p_1^{\mathrm{máx(e_1, f_1)}} \cdots p_k^{\mathrm{máx(e_k, f_k)}} 
\end{align}$$
Sin embargo, en algunas ocasiones ocurre que la factorización de primos puede ser muy larga y difícil de encontrar. Entonces, muchas veces conviene usar alguno de los otros métodos para encontrar el mcd o mcm. 

Una de las aplicaciones más interesantes del TFA es la de poder generalizar un resultado clasico probado por pitágoras en el siglo 5 AC, que es que $\sqrt{2}$ es irracional. Un número racional [[Q]] sabemos que es aquel tipo de número que se puede escribir como una división de dos números enteros $n$ y $m$ (para $m \neq 0$); todos los otros números que no se pueden escribir de esta manera son irracionales. 

> **Lema.** Si $m \in \mathbb{N}_0$ no es un cuadrado perfecto, entonces $\sqrt{m}$ es irracional.

**Demostración.** Basta con probar la contrarecíproca, supongamos que $\sqrt{m}$ es racional, entonces $m$ es un cudrado perfecto. Supongamos $\sqrt{m} = a/b$ para un $a,b \in \mathbb{Z}$ (ambos negativos o ambos positivos). Entonces, $m = a^2/b^2 \rightarrow mb^2 = a^2$ y ya que $a$ y $b$ son enteros podemos representarlos como la factorización de primos $a = p_1^{e_1}\cdots p_k^{e_k}$ y $b = p_1^{f_1} \cdots p_k^{f_k}$ como arriba entonces 
$$m = p_1^{2e_1 - 2f_1} \cdots p_k^{2e_k -2f_k}$$
tiene que ser una factorización de primos de $m$. Notemos que cada primo $p_i$ aparece un número par de veces en esta factorización, y $e_i - f_i \geq 0$ para cada $i$, entonces 
$$m = \Big(p_1^{e_1-f_1} \cdots p_k^{e_k - f_k} \Big)^2$$
es un cuadrado perfecto. $\blacksquare$ 

> **Teorema.** Existen infinitos primos.

Este teorema nos dice que si intentamos aplicar los métodos que vimos para encontrar [[Números primos]] para números muy grandes veremos que parecen que estos nunca terminan que siguien infinitamente, este teorema nos comprueba que efectivamente existen infinitos primos. 

**Demostración.** Supongamos por el absurdo que existen finitos primos, los únicos primos que existen son $p_1, p_2, \cdots, p_k$ luego tomemos $m= p_1p_2 \cdots p_k + 1$. Como nos dice el TFA, como $m$ es un número mayor que 1 debe ser divisible por un primo $p$, como los únicos primos que existen están en $p_1,p_2, \cdots, p_k$ entonces $p$ debe ser alguno de estos por lo cual $p|p_1p_2 \cdots p_k$. Como $p$ divide tanto a $m$ como a $p_1p_2 \cdots p_k$, $p$ divide a la resta $m- p_1p_2 \cdots p_k = 1$ lo cual es imposible, llegamos a una contradicción que viene de suponer que existen primos finitos. $\blacksquare$  