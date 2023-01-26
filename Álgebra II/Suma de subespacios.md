# Suma de subespacios
Ya probamos en [[Subespacios]], que la unión de subespacios no es un subespacio necesariamente. Sin embargo, sería muy útil tener una herramienta parecida a la unión que me permita combinar dos subespacios en uno. De esta manera podemos definir la suma de subespacios.

> [!Suma de subespacios]
> #Definición Supongamos $U_1, \dots, U_m$ son subespacios de $V$. La _suma_ de $U_1 + \cdots + U_m$, es el conjunto de todas las posibles sumas de elementos de $U_1, \dots, U_m$. Más precisamente, 
> $$U_1+ \cdots + U_m = \{u_1 + \cdots + u_m : u_1 \in U_1, \dots, u_m \in U_m\}$$ 

Un ejemplo de porque la suma de subespacios es útil, es por ejemplo si tenemos $V = \mathbb{K}^2$ y $U = \{(x,0) \in \mathbb{K}^2 : x \in \mathbb{K}\}$ que es el eje "x" en el sistema cartesiano y $W = \{(0,y) \in \mathbb{K}^2: y \in \mathbb{K}\}$ que es el eje "y". Entonces tenemos que $U + W = \{(x,0) + (y, 0) : x,y \in \mathbb{K}\} = \{(x,y): x,y \in \mathbb{K}\} = \mathbb{K}^2$. Podrá notar entonces, que si entendemos cada uno de los subespacios por separado, entonces podemos entender es espacio vectorial ([[Espacios Vectoriales]]) en su conjunto. 

> [!Lema 1. Suma de subespacios es el subespacio más chico conteniendo los subespacios]
> Sea $U$ y $W$ subespacios vectorial de un $\mathbb{K}$-espacio vectorial $V$. Se cumple:
> 1. $U+W$ es un subespacio.
> 2. $U+W$ es el menor subespacio que contiene a $U$, $W$ y $U \cup W$.
> 3. Si $\{u_1, \dots, u_m\}$ es un sist. de generadores de $U$ y $\{w_1, \dots, w_n\}$ es un sist. de generadores de $W$, entonces $\{u_i\}_{i=1,\dots,m} \cup \{t_j\}_{j=1, \dots, n}$ es un sist. de generadores de $U+W$.

**Demostración.** 
1. Probemos los 3 requisitos de la proposición 1 de [[Subespacios]]. $0 \in U$ y $0 \in W$, entonces $0 = 0+0 \in U+W$. Luego, si $u, u' \in U$ y $w, w' \in W$ entonces es claro que si $v = u+w$ y $v' = u'+w'$ entonces $v+v' \in U+W$. Sea $v \in U+W$ y $\lambda \in \mathbb{K}$, para $v$ existen $u \in U$ y $w \in W$ tal que $v = u+w$, entonces $\lambda v = \lambda u + \lambda w$. Luego, $\lambda u \in U$  y $\lambda w \in W$ por lo tanto $\lambda v \in U+W$. En consecuencia, $U+W$ es un subespacio de $V$.
2. Notemos que basta con probar que $U+W$ es el menor subespacio que contiene a $U \cup W$. Entonces, supongamos el subespacio de $V$, $S$, tal que $U \cup W \subseteq S$. Queríamos ver que $S \subseteq U + W$ para todo subespacio $S$.  Si $v \in U+W$ entonces existen $u \in U$ y $w \in W$ tal que $v = u+w$. Notemos $U \subseteq U \cup W \subseteq S$ y $W \subseteq U \cup W \subseteq S$, entonces $u \in S$ y $w \in S$. Por hipótesis, $S$ es un subespacio entonces $v = u+w \in S$. Luego, $U+W \subseteq S$. 
3. Por la proposición 1 en [[Independencia Lineal]], esto es lógico. Pues $U$ es el subespacio más chico que contiene a los vectores $\{u_1, \dots, u_m\}$ y $W$ es el subespacio más chico que contiene a los vectores $\{w_1, \dots, w_n\}$, entonces como $U+W$ es el subespacio más chico que contiene a $U$ y $W$ entonces tiene sentido que $\{u_1, \dots, u_m\} \cup \{w_1, \dots, w_n\}$ sea un conjunto de generadores de $U+W$. Pero probándolo, sea $v \in U+W$ entonces existen $u \in U$ y $w \in W$ tales que $v = u+w$, pero luego existen $\alpha_1, \dots, \alpha_m \in \mathbb{K}$ tales que $u = \sum_{i=1}^m \alpha_i u_i$ y existen $\beta_1, \dots, \beta_m \in \mathbb{K}$ tales que $w = \sum_{j=1}^n \beta_j w_j$, entonces $v = \sum_{i=1}^m \alpha_i u_i + \sum_{j=1}^n \beta_j w_j$. Tal que $U+W = < u_1, \dots, u_m, v_1, \dots, v_n>$. $\blacksquare$ 

En cierta forma, se puede ver a la suma de subespacios como la equivalencia a la unión para los conjuntos. 

El siguiente resultado nos da una formula para la dimensión de la suma de dos espacios vectorial de un espacio vectorial finito. Esta formula se puede razonar lógicamente, el número de elementos de la unión de dos conjunto de elementos finitos es la suma de los elementos del primer conjunto con los del segundo menos  el número de elementos en la intersección de ambos. 

> [!Teorema 2. Dimensión de la suma]
> Sean $U$ y $W$ subespacios de $V$ que es un $\mathbb{K}$-espacio vectorial finito, entonces $$\dim (U+W) = \dim U + \dim W - \dim (U \cap W)$$

**Demostración.** Si $U = \{0\}$ ó $W = \{0\}$ listo. Si $u_1, \dots, u_m$ es una base de $U \cap W$, entonces $\dim(U \cap W) = m$. $u_1, \dots, u_m$ es linealmente independiente en $U$. Entonces este conjunto puede ser extendido a una base gracias a la proposición 4 de [[Independencia Lineal]], tal que $u_1, \dots, u_m,v_1, \dots, v_j$ de $U$. Entonces $\dim U = m + j$. Podemos hacer lo mismo con $W$ tal que una base de esta sería $u_1, \dots, u_m, w_1, \dots, w_k$, entonces $\dim W = m+k$. Mostremos ahora que $$u_1, \dots, u_m, v_1, \dots, v_j, w_1, \dots, w_k $$
es una base de $U+W$. Esto va a completar la prueba, pues después tendremos que 
$$\dim (U+W) = m+j+k = (m+j) + (m+k)-m = \dim U + \dim W - \dim(U \cap W)$$
Claramente $<u_1, \dots, u_m, v_1, \dots, v_j, w_1, \dots, w_k>$ contiene a $U$ y $W$, y por lo tanto es igual a $U+W$ (por la proposición 1.3). Así que para probar que es una base, tenemos que probar que es LI. Para probar esto, supongamos
$$a_1u_1+ \cdots +a_mu_m + b_1 v_1 + \cdots + b_j v_j + c_1 w_1 + \cdots + c_k w_k = 0$$
donde todos los $a$'s, $b$'s y $c$'s son escalares de $\mathbb{K}$. Necesitamos probar que todos los $a$'s, $b$'s y $c$'s son igual a 0. La ecuación de arriba puede ser reescrita de la siguiente manera
$$c_1w_1+ \dots + c_k w_k = -a_1u_1 - \dots - a_mu_m-b_1v_1 - \cdots - b_jv_j$$
el cual muestra que $c_1w_1 + \dots + c_k w_k \in U$. Todos los $w$'s son $W$, esto implica que $c_1w_1 + \dots + c_k w_k \in U \cap W$. Como $u_1, \dots, u_m$ es una base de $U \cap W$, podemos escribir $$c_1 w_1 + \cdots + c_kw_k = d_1 u_1 + \cdots+ d_m u_m$$
para algunos escalares $d_1, \dots, d_m$. Pero $u_1, \dots, u_m, w_1, \dots, w_k$ es linealmente independientes, entonces por la ecuación de arriba esto implica que todos los $c$'s (y los $d$'s) son iguales 0. Entonces nuestra ecuación original que tiene a los $a$'s, $b$'s y $c$'s resulta en
$$a_1u_1 + \cdots + a_m u_m + b_1 v_1 + \dots + b_j v_j = 0$$
Como la lista $u_1, \dots, u_m, v_1, \dots, v_j$ es LI, la ecuación implica que todos los $a$'s y $b$'s son 0. Entonces, tenemos que la lista $u_1, \dots, u_m, v_1, \dots, v_j, w_1, \dots, w_k$ es LI por lo que es una base de $U+W$. $\blacksquare$ 

Notemos que existen subespacios $U+W$ en los cuales $\dim (U \cap W) = 0$. En ese caso, podemos sumar $\dim U + \dim W$ tranquilamente. Por ejemplo, sea $\mathbb{R}^2$ el espacio vectorial y las rectas generadas por $<(1,1)>$ y $< (-1,1)>$ que la única intersección es el vector $(0,0)$ por lo tanto $\dim (U \cap W) = 0$ y $\dim U+W = \dim U + \dim W = 2$ que nos dice que genera todo $\mathbb{R}^2$. 

> [!Suma Directa]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial y sean $U$ y $W$ subespacios de $V$. Entonces, $V$ es una suma directa $V = U+W$ y $U \cap W = \{0\}$. Se denota $V = U \oplus W$ 

Una de las propiedades más interesantes es que la suma directa es la capacidad de poder escribir cada elemento de forma **única** como la suma de otros dos $v = u +w$ con únicos $u \in U$ y $w \in W$. 

> [!Proposición 3. Condición para la suma directa]
> Sea $V$ un $\mathbb{K}$-espacio vectorial, $U$ y $W$ subespacios tal que $V = U \oplus W$. Entonces, para cada $v \in V$, $\exists ! u \in U, w \in W$ tal que $v = u+w$. 

**Demostración.** Como $V = U \oplus W$ en particular $v = u+w$ para cada $v \in V$. Entonces, veamos la unicidad. Supongamos que $v = u+w$, y $v= u'+w'$ entonces $u-u' = w-w'$ por consiguiente $u-u' \in U \cap W = \{0\}$ lo cual es un absurdo. $\blacksquare$ 

> [!Proposición 4. Bases de la suma directa]
> Sea $V$ un $\mathbb{K}$-espacio vectorial, $U$, $W$ subespacios y $B_U$, $B_W$ bases de $U$ y $W$ respectivamente, son equivalentes: 
> 1. $V = U \oplus W$
> 2. $B = B_U \cup B_W$ es una base de $V$.

**Demostración.** (1 $\Rightarrow$ 2) Como $B_U = v_1, \dots, v_n$ y $B_W = w_1, \dots, w_m$ generan a $U$ y $W$ respectivamente, entonces por la proposición 1 tenemos que $B$ genera a $U + W$. Nos faltaría ver que $B = B_U \cup B_W$ es LI,
$$\sum_{i=1}^n \alpha_i v_i + \sum_{j=1}^m \beta_j w_j = 0$$
como sabemos que cada uno de los conjuntos por separado son LI, y $0 + 0 = 0$ entonces $\sum \alpha_i v_i = \sum \beta_j w_j = 0$, por lo que $\alpha_i = 0$ y $\beta_j = 0, \forall i = 1, \dots, n; \; j = 1, \dots, m$. 
(1 $\Leftarrow$ 2) Como $B$ es una base de $V$, para cada $v  \in V$ existen $\alpha_i \in \mathbb{K}$, $i = 1, \dots, n$ y $\beta_j \in \mathbb{K}, j = 1, \dots, m$, tales que $v = \sum_{i=1}^n \alpha_i v_i + \sum_{j=1}^m \beta_j w_j$ tal que $v= u + w$ con $u = \sum_i \alpha_i v_i \in U$ y $w = \sum_j \beta_j w_j \in W$. Luego, $V = U + W$. 
Nos faltaría ver que la intersección es 0. Si $v \in U \cap W$, se tiene que $v = \sum_i \alpha_i v_i = \sum_j \beta_j w_j$, de donde nos queda que $\sum_i \alpha_i v_i + \sum_j (-\beta_j) w_j = 0$ y como $B$ es linealmente independiente tenemos que $\alpha_i = 0, \forall i = 1, \dots n$ y $\beta_j = 0, \forall j = 1, \dots, m$ por lo que se concluye $v=0$ y $U \cap W = \{0\}$ Y obtenemos que $V = U \oplus W$. $\blacksquare$ 

> [!Complemento de un subespacio]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial y sea $U \subseteq V$ un subespacio de $V$. Diremos que $W$ es un _complemento de $U$_ si $U \oplus W = V$. 
