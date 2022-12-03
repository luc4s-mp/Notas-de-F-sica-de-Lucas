# Máximo Común Divisor
Si $d$ es un entero tal que $d|a$ y $d|b$ decimos que $d$ es un *divisor común de $a$ y $b$*, por lo tanto el 1 es divisor común de todos los números enteros. Ya vimos por el apartado (7) de un lema (visto en [[Divisibilidad]]) que los divisores son menores o iguales que el módulo del número, entonces los divisores comunes entre dos números van a ser menores o iguales a $\mathrm{máx}(|a|,|b|)$. También, podemos deducir de esto que entre todos los divisores hay uno que es **el máximo** entre los otros. Este se llama **máximo común divisor** de $a$ y $b$, es un único $d = \mathrm{máx}(\mathrm{Div}_+(a) \cap \mathrm{Div}_+(b))$ que satiface

> #Definición  Sean $a, b \in \mathbb{Z}$ ([[Z]]) que no son simultaneamente nulos y se llama **máximo común divisor** de $a$ y $b$ a un número $d \in \mathbb{N}$ que satisface las siguientes propiedades:
> 1. $d|a$ y $d|b$. (así $d$ es un divisor común)
> 2. Si $c|a$ y $c|b \implies c|d, \; \forall \; c \in \mathbb{Z}$ (todos los divisores comunes entre $a$ y $b$ dividen a $d$)

Denotamos al mcd de a y b como $(a, b) = mcd(a, b)$ o simplemente $(a,b)$. 
Otra de las propiedades que debe cumplir el máximo común divisor es que tiene que ser **positivo**.

Una forma de encontrar el máximo común divisor es simplemente listando los divisores comunes de $a$ y $b$ y encontrando el mayor de ellos. Sin embargo, este método puede ser muy tedioso cuando $a$ y $b$ son valores muy grandes. Por ejemplo nos pueden preguntar $\mathrm{mcd}(87241,41041)$? Un método mucho más eficiente para estos casos es el **algoritmo de Euclides**. 

 > **Teorema (Unicidad del MCD)**. Sean $a, b \in \mathbb{Z}$ no simultáneamente nulos. Entonces existe un único $d \in \mathbb{N}$ que cumple (1) y (2) del MCD.

**Demostración.** Para comprobar la unicidad del MCD sabemos que $d_1$ es divisor de $a$ y $b$ y $d_2$ es el MCD de $a$ y $b \implies d_1|d_2 \implies d_1 \leq d_2$. Como $d_2$ es divisor de $a$ y $b$ y $d_1$ es el MCD de $a$ y $b \implies d_2|d_1 \implies d_2 \leq d_1$. Entonces, $d_1 = d_2$.

## Algoritmo de Euclides
Se basa en la siguiente simple observación:
> **Lema**. Si $a=bq+r$  entonces $\mathrm{mcd}(a,b)=\mathrm{mcd}(b,r)$.

**Demostración.** Por un colorario visto en [[Divisibilidad]] sabemos que $a=bq+r$ si $d$ es un común divisor de $a$ y $b$ entonces también tiene que ser un común divisor con $r$ (pues si $r=a-bq$ ,$d|a$ y $d|b$ entonces $d|r$). Luego, dos pares $a,b$ y $b,r$ tienen los mismos divisores comunes, y por lo tanto el mismo máximo común divisor.

El algoritmo de euclides utiliza esto muchas veces para simplificar el calculo del máximo común divisor y no cambiarlo. Tengamos en cuenta que si $a=0$ entonces $\mathrm{mcd}(a,b)= |b|$ y si $b=0$ tenemos $\mathrm{mcd}(a,b)=|a|$, así que ignorando los casos triviales y sabiendo que
$$\mathrm{mcd}(a,b)=\mathrm{mcd}(a,-b)=\mathrm{mcd}(-a,b)=\mathrm{mcd}(-a,-b)$$
Tomemos $a > b > 0$, dividimos a por b:
$$\exists q_r, r_1 / a = bq_1 + r_1, \; 0 \leq r_1 < b$$
- Si $r_1 = 0, \; b|a \implies (a,b) = b$ pues b cumple (1) y (2) de la definición de MCD.
- Si $r_1 \neq 0 \implies b = r_1q_2 + r_2,  \;\; 0 \leq r_2 < r_1$
- Si $r_2 = 0 \implies  r_1|b \implies (a, b) = (b, r_1) = r_1$
- Si $r_2 \neq 0 \implies r_1 = r_2q_3 + r_3, \;\; 0 \leq r_3 < r_2$
- $\vdots$
-  $r_{m-2} \neq 0 \implies r_{m-3} = r_{m-2}q_{m-1} + r_{m-1}, \;\; 0 \leq r_{m-1} < r_{m-2}$
-  $r_{m-2} = r_{m-1}q_m + 0$
-  Vemos que $(a, b) = r_{m-1}$ (el último resto no nulo encontrado).
---

Fijemonos que repetimos el proceso hasta encontrar el $r_m = 0$ que termina el algoritmo. Vemos entonces que $r_{m-1}|a$ y $r_{m-1}|b$, esto lo obtenemos gracias a que $r_{m-1}|r_{m-2}$, luego $r_{m-1}$ divide también a todos los terminos de la penúltima ecuación, entonces $r_{m-1} | r_{m-3}$ y siguiendo de esta manera llego a la conclusión.

Usando el [[Teorema Fundamental de la Aritmética]] existe otra forma de calcular el MCD:
>  **Proposición.** Si $a, b \in \mathbb{Z}-\{0, 1, -1\} \Rightarrow a = \epsilon \prod_{j=1}^{r} p_j^{k_j}$ y $b = \epsilon' \prod_{j=1}^{r} p_j^{k_j}$, donde $\epsilon = 1$ o $\epsilon = -1$ y $p_1, p_2,  \dots, p_r$ primos positivos junto con $k_j \in \mathbb{N} \cup \{0\}, l_j \in \mathbb{N} \cup \{0\}, j \in \{1, \dots, r\}$. Entonces, $$(a, b) = \prod_{j=1}^r p_j^{\min\{k_j, l_j\}}$$

**Demostración.** Hay que probar que $p_{1}^{\min \left\{m_{1}, n_{1}\right\}} \cdots p_{r}^{\min \left\{m_{r}, n_{r}\right\}}$ es el mayor de los divisores comunes de $a$ y $b$. Investiguemos los divisores comunes (positivos) de a y $b$ :
$d \mid a \Longleftrightarrow d=p_{1}^{k_{1}} \cdots p_{r}^{k_{r}} \quad$ con $\quad 0 \leq k_{1} \leq m_{1}, \ldots, 0 \leq k_{r} \leq m_{r}$,
$d \mid b \Longleftrightarrow d=p_{1}^{k_{1}} \cdots p_{r}^{k_{r}} \quad$ con $\quad 0 \leq k_{1} \leq n_{1}, \ldots, 0 \leq k_{r} \leq n_{r} .$
Por lo tanto $d|a \quad y \quad d| b$ si y solo si
$$
d=p_{1}^{k_{1}} \cdots p_{r}^{k_{r}} \quad \text { con } \quad 0 \leq k_{1} \leq \min \left\{m_{1}, n_{1}\right\}, \ldots, 0 \leq k_{r} \leq \min \left\{m_{r}, n_{r}\right\}
$$
De esa forma el mayor de los divisores comunes es
$$
(a: b)=p_{1}^{\min \left\{m_{1}, n_{1}\right\}} \cdots p_{r}^{\min \left\{m_{r}, n_{r}\right\}}
$$
como se quería probar. $\blacksquare$ 

---

# MCD y combinación entera
La siguiente ecuación es conocida como **la Identidad de Bezout**.
> #Definición Sean $a, b \in \mathbb{Z}$ ([[Z]]), $s, t \in \mathbb{Z}$. Entonces el número $d = sa + tb$. Se denomina **Combinación Lineal** entera de a y b. 

Una de las propiedades del máximo común divisor es de ser el **menor** número posible de escribir en una combinación posible entre dos números, es decir $(a,b) = \mathrm{mín}\{x \in \mathbb{N} : x = ra+sb \text{ con } r,s \in \mathbb{Z}$.

 > **Teorema.** Sean $a, b \in \mathbb{Z}$, no ambos nulos. Entonces existen $s, t \in \mathbb{Z}$ tales que $$(a, b) = s \cdot a + t \cdot b$$

**Demostración.** Este resultado se demuestra con el **Esquema de Euclides Extendido**. Se miran de atrás para adelante las sucesivas divisiones hasta la que da al máximo común divisor como último resto no nulo, y, poniendo en factor común los sucesivos divisores y restos y reagrupando, se obtiene una escritura entera de $(a, b)$ como combinación entera de $a$ y $b$. (Luego, si habíamos —para simplificar las divisiones- cambiado los signos de los a y $b$ originales, se modifican los signos para escribir $(a, b)$ como combinación entera de los $a$ y $b$ originales.) Si $r_{\ell}=(a, b)$,
$r_{\ell-2}=k_{\ell} r_{\ell-1}+r_{\ell} \quad \Rightarrow r_{\ell}=r_{\ell-2}-k_{\ell} r_{\ell-1}$
$r_{\ell-3}=k_{\ell-1} r_{\ell-2}+r_{\ell-1} \Rightarrow r_{\ell}=r_{\ell-2}-k_{\ell}\left(r_{\ell-3}-k_{\ell-1} r_{\ell-2}\right)$
$=\left(1+k_{\ell} k_{\ell-2}\right) r_{\ell-2}-k_{\ell} r_{\ell-3}$
:
$r_{1}=k_{3} r_{2}+r_{3} \quad \Longrightarrow \quad r_{\ell}=* r_{1}+*^{\prime} r_{2}$
$b=k_{2} r_{1}+r_{2} \quad \Longrightarrow r_{\ell}=* r_{1}+*^{\prime}\left(b-k_{2} r_{1}\right)$
$a=k_{1} b+r_{1} \quad \Longrightarrow r_{\ell}=\left(*-k_{2} *^{\prime}\right)\left(a-k_{1} b\right)+*^{\prime} b$
$=s a+t b$,
donde las estrellitas simbolizan los números que se obtuvieron como coeficientes al llegar a ese paso. Así, $(a: b)=r_{\ell}=s a+t b$ donde claramente $s, t \in \mathbb{Z}$ ya que son obtenidos sumando y multiplicando enteros. $\blacksquare$ 

Veamos que tiene sentido que el número más chico que podamos escribir como una combinación lineal de dos números sea el máximo común divisor. Este teorema nos ayuda a resolver ecuaciones del tipo $ax+by=c$ ($a,b,c$ dados) en los **números enteros**. 

>**Teorema.** Sean $a$ y $b$ enteros (no nulos) con $d=(a,b)$. Entonces, el entero $c$ tiene la forma $ax+by$ para algún $x,y \in \mathbb{Z}$ si y solo si $c$ es múltiplo de $d$. En particular, $d$ es el número entero positivo más chico que se puede escribir de la forma $ax+by$. 

**Demostración.** Si $c=ax+by$ donde $x,y \in \mathbb{Z}$, entonces como $d|a$ y $d|b$, por el colorario visto en [[Divisibilidad]], entonces $d|c$. En consecuencia, si $c=dq$ para un $q \in \mathbb{Z}$, entonces escribiendo $d=au+bv$ (como nos dice el teorema anterior) obtenemos que $c= auq + bvq = ax+by$ donde $x = uq$ y $y=vq$ . Entonces, los enteros de la forma $ax+by$ son múltiplos de $d$, el entero positivo más chico que sea múltiplo de $d$ es $d$ en sí mismo. $\blacksquare$

> #Definición Decimos que $a,b \in \mathbb{Z}$ son **números coprimos** si $\mathrm{mcd}(a,b)=1$.

Por ejemplo, 10 y 21 son coprimos, pues no comparten ningún divisor en común. A partir de esto podemos obtener 3 colorarios del teorema anterior.

> **Colorario. (1)** Sean $a,b \in \mathbb{Z}$ son **coprimos** si existen dos números $x,y \in \mathbb{Z}$ tales que $ax+by=1$.

> **Colorario. (2)** Si $\mathrm{mcd}(a,b)=d$ entonces $\mathrm{mcd}(ma,mb)=md$ para cada entero $m>0$, y $\mathrm{mcd}(\frac{a}{d},\frac{b}{d})=1$. 

**Demostración.** Por el teorema anterior, $\mathrm{mcd}(ma,mb)$ es el número entero positivo tal que $max+mby=m(ax+by)$, donde $x,y \in \mathbb{Z}$, mientras que $d$ es el menor entero positivo que se puede escribir como $ax+by$, entonces $\mathrm{mcd}(ma,mb)=md$. Luego, escribiendo $d=as+bt$ y luego dividiendo por $d$ obtenemos $\frac{a}{d}s + \frac{b}{d}t=1$ y por el colorario 1, $(\frac{a}{d},\frac{b}{d})=1$ son coprimos. $\blacksquare$ 

> **Colorario (3)**. Sea $a, b \in \mathbb{Z}$ son coprimos, entonces
> 1. Si $a|c$ y $b|c$ entonces $ab|c$.
> 2. Si $a|bc$ luego $a|c$.

**Demostración.** (1) Tenemos que $c=aq$ para un $q \in \mathbb{Z}$ y $c=bk$ para un $k \in \mathbb{Z}$, luego sabemos que para un par $x,y \in \mathbb{Z}$ tenemos $cax + cby = c$ reemplazamos $(bk)ax + (aq)by = c$ luego $(ab)kx + (ab)qy=c \rightarrow ab(kx+qy)=c \rightarrow ab|c$ ya que $kx+qy$ es un entero. 
(2) Sabemos que $c=cax + cby$ como en (1). Como $a|bc$ y $a|a$, por el colorario visto en [[Divisibilidad]] resulta $a|(cax+cby)=c$. $\blacksquare$ 

---

## Esquema extendido de Euclides
Sirve para escribir el máximo común divisor $(a, b)$ como una combinación entera entre $a$ y $b$. 
- Comenzar con $r_1 = a$, $r_2 = b$, $s_1 = 1$, $t_1 = 0$, $s_2 = 0, \; t_2 = 1$.
- Mientras $r_2 \neq 0$:
	- Calcular el cociente $q$ y el resto $r$ de la división de $r_1$ por $r_2$.
	- Calcular $s = s_1 - k \cdot s_2$ y $t = t_1 - k \cdot t_2$
	- Reemplazar
		- $r_1 \leftarrow r_2$
		- $r_2 \leftarrow r$
		- $s_1 \leftarrow s_2, \; t_1 \leftarrow t_2$
		- $s_2 \leftarrow s, t_2 \leftarrow t$
- Dar como respuesta $r_1$, $s_1$, $t_1$ (que satisfacen $(a, b) = r_1 = s_1a+ t_1b$)
	
#Matemática #Primer-año 