# Notas de Álgebra II
**(NEF)** No Entra en Final.

# Espacios Vectoriales

> [!Operación.]
> #Definición Sea $A$ un conjunto no vacío. Una _operación_ de $A$ es una función $*: A \times A \rightarrow A$.

> [!ACCIÓN.]
> #Definición Sea $A$  y $B$ dos conjuntos no vacíos. Una _acción_ de $A$ en $B$ es una función $\cdot: A \times B \rightarrow A$.

El conjunto $\mathbb{K}$ es un #Cuerpo (cualquiera) y a cuyos elementos llamamos **escalares** y tenemos otr
o conjunto $V$ a cuyos elementos llamamos **vectores**, podemos definir un **espacio vectorial** $V$ sobre $\mathbb{K}$.   

> [!Espacio Vectorial]
> #Definición Sea $(\mathbb{K}, + , \cdot)$ un **cuerpo**. Sea $V$ un conjunto no vacío, sea $+$ una operación en $V$ y sea $\cdot$ una acción de $K$ en $V$. Se dice que $(V, +, \cdot)$ es un **$K$-espacio vectorial** si cumplen las siguientes condiciones:
>  1. $(V,+)$ es un **grupo abeliano**. Es decir, $+$ es asociativa, conmutativa, tiene neutro y opuesto.
>  2. La acción $\cdot : K \times V \rightarrow V$ satisface: 
> 	 i. $a \cdot (v+w) = a \cdot v + a \cdot w, \quad \forall \; a \in \mathbb{K}, \; \forall v, w \in V$ 
> 	 ii. $(a+b) \cdot v = a \cdot v + b \cdot v, \quad \forall a,b \in K; \; \forall v \in V$ 
> 	 iii. $1 \cdot v = v, \forall v \in V$ 
> 	 iv. $(a \cdot b) \cdot v = a \cdot (b \cdot v), \forall a,b \in K; \; v \in V$ 

Un ejemplo trivial de un conjunto que es un espacio vectorial es $V = \{0\}$  basado en $\mathbb{K}$  pues cumple:
(i) Sean $a \in \mathbb{K}$ y $v, w \in V$ tenemos que $v = w = 0$ por lo tanto, $a(0+0) = 0 \in V$.
(ii) Sean $a, b \in \mathbb{K}$ y $v \in V$ tenemos que $v = 0$ por lo tanto, $(a+b)0 =0 \in V$
(iii) Sea $v \in V$ entonces $v=0$ por lo tanto, $1 \cdot 0 = 0 \in V$.
(iv) Sea $a,b \in \mathbb{K}$ y $v \in V$ entonces $v=0$ y se cumple $(a \cdot b) 0 = a (b \cdot 0) = 0 \in V$. 
También, otro ejemplo trivial es eligiendo $V = \mathbb{K}$ basado en $\mathbb{K}$ es un espacio vectorial. Lo que no es tan obvio es si podemos encontrar un subconjunto de $\{0\} \subset W \subset \mathbb{K}$ tal que este sea un espacio vectorial. Adelantándonos, la respuesta es no.  

> [!Proposición 1.1]
> No existe un subconjunto $W$ ($\{0\} \subset W \subseteq \mathbb{K}$) tal que este sea un espacio vectorial sobre $\mathbb{K}$. 

**Demostración.** Supongamos que $W$ es un espacio vectorial. Sabemos que si $w \in W \subseteq \mathbb{K}$  y $\mathbb{K}$ es cuerpo entonces existe su inverso $\underset{\in \mathbb{K}}{\underbrace{w^{-1}}} \cdot w = 1 \in W$ y por la (iv) propiedad que se tiene que cumplir del espacio vectorial, si tomamos $a \in \mathbb{K}$ y $b = w^{-1} \in \mathbb{K}$ tenemos que $(a \cdot w^{-1}) \cdot w = a \cdot (w \cdot w^{-1}) = a \in W$ y como esto se cumple $\forall a \in \mathbb{K}$ entonces $\mathbb{K} \subseteq W$ pero luego por hipótesis sabemos que $W \subseteq \mathbb{K}$ por lo tanto $W = \mathbb{K}$.  $\blacksquare$ 

## Otros espacios vectoriales 
Podemos probar que $\mathbb{K}^n$ es un espacio vectorial probando las propiedades de la definición también, es más nuestra definición de $\mathbb{K}^n$ motivo la definición de espacio vectorial. 

**Ejemplo 1.**
Un conjunto muy interesante que nos interesaría estudiar podría ser $\mathbb{K}^{\infty} = \{(x_1,x_2, \dots) : x_i \in \mathbb{K}, \; \forall \; i \in I\}$ siendo $I$ un conjunto de índices (tiene infinitos elementos). La operación $+$ y la acción $\cdot$ están bien definidas:
$$(x_1, x_2, \dots) + (y_1, y_2, \dots) = (x_1+y_1, x_2 + y_2, \dots) \in \mathbb{K}^{\infty} \quad \lambda\in \mathbb{K}, \; \lambda(x_1,x_2, \dots) = \underset{\in \mathbb{K}^\infty}{\underbrace{(\lambda x_1, \lambda x_2,\dots)}}$$
Y luego se cumplen las 4 propiedades por lo tanto es un espacio vectorial. 

> [!Espacio Vectorial de Funciones.]
> #Definición Sea $S$ un conjunto. Se define a $\mathbb{K}^S = \{f : S \rightarrow \mathbb{K} / \; f \text{ es una función }\}$  como el conjunto de todas las funciones que van de $S$ a $\mathbb{K}$. 
> - Sea $f,g \in \mathbb{K}^S$, la suma $f+g \in \mathbb{K}^S$ es la función definida por $(f+g)(x) = f(x) + g(x)$ para todo $x \in S$.
> - Sea $f \in \mathbb{K}^S$, el producto $\lambda f \in \mathbb{K}^S$ es la función  $(\lambda f)(x) = \lambda f(x)$ para todo $x \in S$. 

**Ejemplo 2.**
Se puede probar usando las 4 propiedades de un espacio vectorial que si $S$ es no vacío, entonces $\mathbb{K}^S$ es un espacio vectorial. La identidad aditiva de $\mathbb{K}^S$ es la función $0: S \rightarrow \mathbb{K}$ definida por $0(x) = 0$.
Notemos que $\mathbb{K}^S$ es la generalización de los ejemplos anteriores $\mathbb{K}^n$ y $\mathbb{K}^{\infty}$. Pues una lista de largo $n$ de números en $\mathbb{K}$ puede ser pensada como una función de $\{1,2,\dots, n\} \rightarrow \mathbb{K}$ por lo tanto si juntamos todas las funciones posibles tenemos $\mathbb{K}^n$ y una sucesión de números en $\mathbb{K}$ puede ser pensada como una función desde los números naturales a $\mathbb{K}$ y si tomamos todas las sucesiones posibles tenemos $\mathbb{K}^{\infty}$. En otras palabras, podemos pensar en $\mathbb{K}^n$ como $\mathbb{K}^{\{1,2,\dots,n\}}$ y $\mathbb{K}^{\infty}$ como $\mathbb{K}^\mathbb{N}$.

# Subespacios 
Dentro de un $\mathbb{K}$-espacio vectorial ([[Espacios Vectoriales]]) $V$, hay subconjuntos del mismo que heredan la estructura de $V$, es decir, que también son espacios vectoriales con la misma operación, el mismo elemento neutro y la misma acción en $V$. Por ejemplo, tomando $V = \mathbb{R}^2$ tenemos que este es un plano, veamos que el subconjunto $W = \{(2x, -x): x \in \mathbb{R}\}$ es también un espacio vectorial, y es más forma una recta que pasa por el $(0,0)$ (notemos que si no lo hiciera no podría ser un espacio vectorial pues sí o sí tiene que tener un elemento neutro):
![[Pasted image 20230103092259.png | 400]]
Veamos que podemos reescribir el conjunto como $W = \{x(2,-1): x \in \mathbb{R}\}$ tal que todos los puntos de la recta son "generados" por multiplicar por un escalar al vector $(-2,1)$. Entonces, a estos espacios vectoriales que están dentro de otros los llamamos **subespacios vectoriales**.

> [!Subespacios Vectoriales]
> #Definición Sea $V$ un $\mathbb{K}$- espacio vectorial. Un subconjunto $S \subseteq V$ no vacío se dice _subespacio de $V$_ si la suma y el producto por escalares  son una operación y una acción en $S$ que lo convierten en un $\mathbb{K}$-espacio vectorial. 

Un ejemplo obvio de un subespacio vectorial de $\mathbb{R}^2$ por ejemplo es $S = \{(0,0)\}$ (lo puede comprobar por usted mismo probando las propiedades de espacio vectorial que tienen que cumplir la operación y la acción, note que es muy parecido a probar que $\{0\}$ es un espacio vectorial). Y también, por lo que vimos en nuestro ejemplo inicial, si $S$ tiene un elemento $v$ no nulo tal que para todo $\lambda \in \mathbb{R}, \;\lambda \cdot v \in S$ y estos son todos los elementos de $S$ entonces $S$ es un subespacio (que gráficamente es una recta que pasa por el origen).

> [!Proposición 1.2]
> Sea $V$ un $\mathbb{K}$ espacio vectorial y sea $S \subseteq V$. Entonces $S$ es un subespacio de $V$ si y sólo si valen las siguiente condiciones:
> 1. $0 \in S$ 
> 2. $v,w \in S \implies v+w \in S$ 
> 3. $\lambda \in \mathbb{K}, \; v \in S \implies \lambda \cdot v \in S$

**Demostración.** 
- ($\Rightarrow$) Si $S$ es un subespacio es obvio que se tiene que cumplir (1), (2) y (3). 
- ($\Leftarrow$ ) La condición (1) nos asegura que $S$ es no vacío, por las condiciones (2) y (3) tenemos que la suma $+$ y la multiplicación escalar $\cdot$ están bien definidas en $S$. Veamos que un espacio vectorial:
	- Probemos primero las propiedades que tiene que cumplir la suma, como $v+w \in S \subseteq V$ entonces la conmutatividad y la asociatividad en $S$ son validas gracias a que ocurren dentro de $V$ y por la condición (1) $0 \in S$ tiene neutro, por último existen los inversos aditivos gracias a que $-1 \in \mathbb{K}$ y por la condición (3) tenemos que si $v \in S, \; (-1)v \in S \implies -v \in S$.
	- Las 4 propiedades que tiene que cumplir la acción $\cdot$ salen también gracias a que valen en $V$, por ejemplo la 1era es verdad pues $v+w \in S$ por (2) y luego por (3) tenemos que $a(v+w) \in S$, siguiendo sabemos que $av \in S$ y $aw \in S$ por (3) por lo tanto por (2) tenemos que $av+aw \in S$ entonces se cumple $a(v+w) = av+aw$. $\blacksquare$  

Algunos ejemplos de subespacio vectorial:
1. $\{0\}$ es un subespacio de $V$.
2. $V$ es un subespacio de $V$.
3. Si $v \in V$, $S = \{\lambda v / \lambda \in \mathbb{K}\}$ es un subespacio de $V$ pues por la Prop.(1):
	1. $0 = 0 \cdot v \in S$ 
	2. Si $\lambda v \in S, \; \mu v \in S$ entonces $\lambda v + \mu v = (\lambda + \mu)v \in S$. 
	3. Si $\lambda v \in S$ y $\alpha \in \mathbb{K}$ entonces $\alpha (\lambda v) = (\alpha \lambda) \cdot v \in S$. 
Este ejemplo es muy interesante pues nos hace preguntarnos _¿Podemos combinar una cierta cantidad de vectores cualquiera que pertenezcan a $V$ y formar un subespacio con ellos multiplicándolos por escalares y sumándolos?_ La respuesta es sí y lo probaremos en el siguiente ejemplo:
4. Si $v_1, \dots, v_n \in V$ entonces $S = \{\alpha_1 v_1 + \alpha_2 v_2 + \cdots + \alpha_n v_n : \alpha_i \in \mathbb{K}, \; 1 \leq i \leq n\}$ es un subespacio, pues 
	1. Eligiendo $\alpha_i = 0$ para todo $1 \leq i \leq n$ entonces $0v_1 + \cdots + 0v_n = 0 \in S$. 
	2. Si $\alpha_1 v_1 + \alpha_2 v_2 + \cdots + \alpha_n v_n \in S$ y $\beta_1 v_1 + \beta_2 v_2 + \cdots + \beta_n v_n \in S$ entonces $\alpha_1 v_1 + \alpha_2 v_2 + \cdots + \alpha_n v_n + \beta_1 v_1 + \beta_2 v_2 + \cdots + \beta_n v_n$ $= (\alpha_1 + \beta_1)v_1 + (\alpha_2 + \beta_2)v_2 + \cdots + (\alpha_n + \beta_n)v_n \in S$
	3. Si $\alpha_1 v_1 + \alpha_2 v_2 + \cdots + \alpha_n v_n \in S$ y $\lambda \in \mathbb{K}$ entonces $\lambda(\alpha_1 v_1 + \alpha_2 v_2 + \cdots + \alpha_n v_n) = (\lambda\alpha_1) v_1 + (\lambda\alpha_2) v_2 + \cdots + (\lambda \alpha_n) v_n \in S$. 
	En este caso se dice que los vectores $v_1, v_2, \dots, v_n$ _generan el subespacio S_ y se denota $S = <v_1, \cdots, v_n>$. 
5. Sean $a_1, \dots, a_n \in \mathbb{K}$ fijos. Sea $S = \{(x_1, \dots, x_n) \in \mathbb{K}^n : a_1 x_1 + \dots + a_n x_n = 0\}$ es fácil ver que es un subespacio de $\mathbb{K}^n$ 

Pasaremos a responder la siguiente pregunta _¿Es la intersección de subespacios un subespacio también? ¿Y la unión?_ 

> [!Proposición 2.3]
> Sea $V$ un $\mathbb{K}$-espacio vectorial y sean $W_1$ y $W_2$ dos subespacios tenemos que $W_1 \cap W_2$ es un subespacio de $V$.

**Demostración.** Usemos la proposición (1): 
1. $0 \in W_1 \cap W_2$ pues $0 \in W_1$ y $0 \in W_2$ 
2. Si $v,w \in W_1 \cap W_2$ entonces $v,w \in W_1$ y $v, w \in W_2$ luego como $W_1$ es un subespacio entonces $v+w \in W_1$ lo mismo para $v+w \in W_2$ luego $v+w \in W_1 \cap W_2$.
3. Si $v \in W_1 \cap W_2$ y $\lambda \in \mathbb{K}$ entonces $v \in W_1$ y $v \in W_2$ luego como ambos son subespacios tenemos que $\lambda v \in W_1$ y $\lambda v \in W_2$, por lo tanto $\lambda v \in W_1 \cap W_2$. $\blacksquare$ 

**Contraejemplo de la únion.** Entonces, acabamos de probar que la intersección de subespacios de $V$ nos da otro subespacio. Sin embargo, __la unión de subespacios no necesariamente es subespacio__. Por ejemplo, supongamos que tenemos el espacio vectorial $\mathbb{R}^2$ y los subespacios $S = <(0,1)>$ y $T = < (1,0) >$ [^1], tenemos que $S \cup T$ no es un subespacio pues por la condición (2) en la proposición 1 debería cumplirse que si $v,w \in S \cup T \implies v+w \in S \cup T$, luego $(0,1) \in S$ y $(1,0) \in T$ pero $(1,0) + (0,1) = (1,1) \notin S \cup T$ se puede observar claramente porque este vector no está en el conjunto graficando en un plano $S$ y $T$.  

Otros ejemplos interesantes de subespacios salen de analizar el espacio vectorial de funciones (visto en [[Espacios Vectoriales]]) $\mathbb{K}^S$. Notemos que en $\mathbb{R}^{[0,1]}$ podemos decir que el conjunto de todas las funciones continuas ([[Continuidad]]) $W = \{f : [0,1] \rightarrow \mathbb{R} / f \text{ continua }\}$ son un subconjunto del mismo, pero ¿Es un subespacio? 
- Veamos que $0(x) = 0$ es el elemento neutro del espacio vectorial y es una función continua por lo tanto $0 \in W$. 
- Si $f \in W$ y $g \in W$ tenemos que $(f+g)(x) = f(x) + g(x)$ por un teorema visto en continuidad la suma de funciones continuas nos da otra función continua, entonces $f+g \in W$. 
- Por último, si $f \in W$ y $\lambda \in \mathbb{R}$ entonces $(\lambda f)(x) = \lambda f(x)$ y sabemos que esta función es continua también, por lo tanto $\lambda f \in W$. 

Tenemos entonces que $W$ si es un subespacio de $\mathbb{R}^{[0,1]}$. 
Podemos comprobar que $\{f: [0,1] \rightarrow \mathbb{R} / f'(x) \text{ exista }\}$ y $\{f:[0,1] \rightarrow \mathbb{R} / \int_0^1 f(x)dx \text{ exista }\}$ son subespacios vectoriales de $\mathbb{R}^{[0,1]}$ también. 


[^1]: Recordemos que esta notación quiere significar que son los subespacios generados por esos vectores entre los símbolos $<>$, es decir son todos los vectores que resultan de multiplicar a estos por cualquier escalar. 


# Sistemas de Generadores
A partir de la definición de [[Espacios Vectoriales]]  y por lo concluido en el ejemplo 4 de [[Subespacios]], podemos obtener nuevos elementos de un $\mathbb{K}$-espacio vectorial $V$ a partir de elementos sabidos de un subconjunto $G \subseteq V$ considerando sumas finitas de múltiplos por escalares de los elementos de $G$. Sigue entonces la noción de **combinación lineal**:

> [!COMBINACIÓN LINEAL]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial, y sea $G = \{v_1, \dots, v_r\} \subseteq V$. Una **combinación lineal de** $G$ es un elemento de $v \in V$ tal que $v = \sum_{i=1}^r \alpha_i v_i$ con $\alpha_i \in \mathbb{K}$ para cada $1 \leq i \leq r$. 

Un ejemplo de esta definición es por ejemplo que si tomamos $V = \mathbb{R}^3$ entonces el vector $(17,-4,2)$ es una combinación lineal de $(2,1,-3),(1,-2,4)$ porque 
$$(17,-4,2) = 6(2,1,-3) + 5(1,-2,4)$$
pero $(17,-4,5)$ no es una combinación lineal de los 2 vectores anteriores, porque no existen $a_1, a_2 \in \mathbb{R}$ tal que 
$$(17,-4,5) = a_1(2,1,-3) + a_2(1,-2,4)$$
¿Cómo sabemos esto? Porque si distribuimos los escalares en los vectores y los sumamos nos queda que 
$$(17,-4,5) = (2a_1 + a_2, a_1-2a_2, -3a_1+4a_2) \quad \rightarrow \quad \begin{cases} 2a_1+a_2 = 17 \\ a_1-2a_2 = -4 \\ -3a_1 + 4a_2 = 5 \end{cases}$$
Entonces, si podemos encontrar que el sistema de ecuaciones de arriba no tiene solución (lo cual aprenderemos más adelante), listo!

La definición de combinación lineal se puede extender al caso de subconjuntos no necesariamente finitos considerando $I$ como el conjunto de índices tal que $G = \{v_i / i \in I\}$ y para cada elemento de $v \in V$ podemos escribir $\sum_{i\in I} \alpha_i v_i$ donde $\alpha_i = 0$ salvo para finitos $i \in I$.

> [!Sistema de Generadores]
> #Definición Sea $V$ un $\mathbb{K}$ espacio vectorial y sea $G \subseteq V$, Se dice que $G$ es un _sistema de generadores de_ $V$ (y se denota $<G> = V$) si todo elemento de $V$ es una combinación lineal de elementos de $G$. 

Esta definición es muy importante, porque implica que si puedo expresar un espacio vectorial con una cantidad finita de vectores, se vuelve mucho más fácil obtener que vector pertenece o no al espacio (nos basta con resolver un sistema de ecuaciones). También quiere significar que si yo quiero manipular al espacio vectorial (por ejemplo, en funciones) se vuelve mucho más fácil tratar únicamente con los vectores que generan el espacio. 

# Sistemas de Ecuaciones Lineales
El ejemplo 5 de [[Subespacios]] vimos que una ecuación de las coordenadas de un vector es un subespacio de $\mathbb{K}^n$. Entonces por la proposición 2 de [[Subespacios]] tenemos que 
$$S = \Bigg\{(x_1,\dots,x_n) \in \mathbb{K}^n : \begin{cases} a_{11}x_1 + \dots + a_{1n}x_n = 0 \\ \quad \quad \quad \quad \vdots \\ a_{m1}x_1 + \dots + a_{mn}x_n = 0 \end{cases} \Bigg\}$$
es un subespacio de $\mathbb{K}^n$, pues $S = \bigcap_{i=1}^m S_i$ donde $S_i = \{(x_1,\dots, x_n) \in \mathbb{K}^n : a_{i1} x_1 + \dots + a_{in} x_n = 0\}$ y cada $S_i$ es un subespacio por lo tanto la intersección es un subespacio de $\mathbb{K}^n$. 
Los sistemas de ecuaciones aparecerán constantemente en Álgebra 2, por esto es muy importante saber como resolverlos. Queríamos describir el conjunto $S$ usando un _sistema de generadores de este subespacio_, para de esta manera obtener las soluciones del sistema de forma mucho más sencilla.

## Sistemas lineales homogéneos
> [!Sistemas Lineales Homogéneos]
> #Definición Un **sistema lineal homogéneo** de $n$ ecuaciones y $m$ incógnitas a coeficientes en un cuerpo $\mathbb{K}$ es un sistema del tipo 
>  $$\begin{cases} a_{11}x_1 + a_{12}x_2 + \dots + a_{1m}x_m = 0 \\ \quad \quad \quad \quad \vdots \\ a_{n1}x_1 + a_{n2}x_2 + \dots + a_{nm}x_m = 0 \end{cases}$$ donde $a_{ij} \in \mathbb{K}$ para cada $1 \leq i \leq n$, $1 \leq j \leq m$. 

Este sistema de ecuaciones **siempre tiene solución** pues siempre existe la opción de elegir $(x_1,x_2, \dots, x_m) = (0,0, \dots, 0)$ la cual se llama **solución trivial**. Podemos probar que las __soluciones de un sistema homogéneo es un subespacio__, pues por la Prop. 1 de [[Subespacios]], sea $S$ el conjunto de soluciones de un sistema homogéneo de $n$ ecuaciones y $m$ incógnitas: 
- $(0,0,\dots,0) \in S$ (porque la solución trivial siempre existe).
- Si $v,w \in S$ tal que $v = (x_1, \dots, x_m)$ y $w = (y_1, \dots, y_m)$, tenemos que $S$ se puede expresar como $S = \bigcap_{i=1}^m E_i$ siendo $E_i$ el conjunto de soluciones de la ecuación $i$. Tenemos que $v$ y $w$ cumplen la ecuación $i$ por hipótesis tal que $a_{i1}x_1 + \dots + a_{im}x_m = 0$ y $a_{i1}y_1 \dots + a_{im}y_m = 0$ sumando ambas tenemos que $a_{i1}(x_1 + y_1) + \dots + a_{im}(x_m + y_m) = 0$ por lo tanto $v+w \in E_i$. Como esto se cumple para todas las ecuaciones tenemos que $v+w \in S$.
- Si $v \in S$ y $\lambda \in \mathbb{K}$ tenemos que $v = (x_1, \dots, x_m)$ y para la ecuación $i$ se cumple que esta es una solución por lo tanto $v \in E_i$ tal que $a_{i1}x_1 + \dots + a_{im}x_m = 0$, luego multiplicándola por $\lambda$ tenemos que $a_{i1}(\lambda x_1) + \dots + a_{im}(\lambda x_m) = 0$. En conclusión, $\lambda v \in E_i$ y como esto se cumple para toda ecuación tenemos que $\lambda v \in S$. 
Queda comprobado que el conjunto de soluciones de un sistema homogéneo es un subespacio. 

> [!Sistemas Equivalentes]
> #Definición Dos sistemas de ecuaciones homogéneos (SEH) se dicen _equivalentes_ si sus conjuntos de soluciones son iguales.

Notemos que dos sistemas equivalentes no necesariamente tienen la misma cantidad de ecuaciones, por ejemplo 
$$\begin{cases} x+y= 1 \\ 2x+2y = 2\end{cases} \iff \{x+y = 1$$
tienen las mismas soluciones, esto es porque la segunda ecuación en el sistema de la izquierda es un múltiplo de la primera, por lo tanto no produce ningún cambio en el conjunto de soluciones por lo que podemos simplemente eliminarla.
Sería útil tener un método que _me permita obtener las soluciones de un sistema de ecuaciones lineales obteniendo sistemas equivalentes cada vez más sencillos_. De esta manera, nace el método de triangulación o de eliminación de Gauss. 

> [!Proposición 1.4. (Método de Gauss 1)]
> Dado un SEH, los siguientes cambios en las ecuaciones dan lugar a sistemas equivalentes:
> 1. Intercambiar dos ecuaciones de lugar. ($e^{(ij)}$)
> 2. Multiplicar una ecuación por una constante no nula. ($e_c^{(i)}$)
> 3. Al tener una ecuación con todos sus coeficientes nulos, podemos sacarla del sistema. 
> 4. Reemplazar una ecuación por ella misma más un múltiplo de otra. ($e_c^{(ij)}$)

Entre paréntesis se encuentran las notaciones de cada operación, cada una de estos cambios en las ecuaciones se llaman **operaciones elementales por fila**. 
Notemos que para ver que dos sistemas son equivalentes:
$$ S_1\begin{cases} 
a_{11}x_1 + a_{12}x_2 + \dots + a_{1m}x_m = b_1 \\ 
\quad \quad \quad \quad \vdots \\ 
a_{n1}x_1 + a_{n2}x_2 + \dots + a_{nm}x_m = b_n 
\end{cases} \quad \quad \quad S_2 \begin{cases} 
c_{11}x_1 + c_{12}x_2 + \dots + c_{1m}x_m = b_1 \\ 
\quad \quad \quad \quad \vdots \\ 
c_{r1}x_1 + c_{r2}x_2 + \dots + c_{rm}x_m = b_r
\end{cases}$$
Si $A_1 = \{v \in \mathbb{K}^m : v \text{ cumple } S_1\}$ y si $A_2 = \{v \in \mathbb{K}^m : v \text{ cumple } S_2\}$ queremos ver que $A_1 = A_2$ (recordemos que esto significa que $A_1 \subseteq A_2$ y $A_1 \supseteq A_2$). 

**Demostración.** Sea $S_1$ el conjunto de soluciones del SEH de $m$ ecuaciones y $n$ incógnitas antes del cambio y $S_2$ el conjunto de soluciones después del cambio, queremos ver en todos los casos que $S_1 = S_2$:
1. Si vemos al conjunto de soluciones del sistema como la intersección de los conjuntos de soluciones de cada una de las ecuaciones que lo integran $S = \bigcap_{i=1}^m E_i$ entonces cambiar de orden las ecuaciones, corresponde a intercambiar dos conjuntos en la intersección. Como la intersección es conmutativa, el conjunto que resulta es el mismo. Por ejemplo, si intercambio la ecuación $i$ con la $j$ : $$\begin{align} S_1 = E_1 \cap E_2 \cap \dots \cap E_i \cap \dots \cap E_j \cap \dots \cap E_m \\  S_2 = E_1 \cap E_2 \cap \dots \cap E_j \cap \dots \cap E_i \cap \dots \cap E_m\end{align}$$
	Notemos que $S_1 = S_2$.
2. Sea $x = (x_1, \dots, x_n) \in \mathbb{K}^n$ una solución de $$\begin{cases}  a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n & = 0 \\ \quad \quad \quad \quad \quad \vdots \\ a_{i1}x_1 + a_{i2}x_2 + \dots + a_{1n}x_n & = 0 \\ \quad \quad \quad \quad \quad \vdots \\ a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n & = 0 \end{cases}$$ Al multiplicar la $i$-ésima ecuación por $\lambda \in \mathbb{K}, \; \lambda \neq 0$, resulta el sistema $$\begin{cases}  a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n & = 0 \\ \quad \quad \quad \quad \quad \vdots \\ \lambda a_{i1}x_1 + \lambda a_{i2}x_2 + \dots + \lambda a_{1n}x_n & = 0 \\ \quad \quad \quad \quad \quad \vdots \\ a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n & = 0 \end{cases}$$ Tenemos que en este sistema el conjunto de soluciones de la ecuación multiplicada por un escalar es $\tilde{E}_i = \{v \in \mathbb{K}^n : \lambda a_{i1}x_1 + \lambda a_{i2}x_2 + \dots + \lambda a_{1n}x_n  = 0 \}$  nos basta ver que $\tilde{E}_i = E_i$ para que $S_1 = S_2$. Veamos $E_i \subseteq \tilde{E}_i$, si $x \in E_i$ es una solución de la ecuación tenemos que $$a_{i1}x_1 + a_{i2}x_2 + \dots + a_{1n}x_n  = 0 \underset{\lambda \in \mathbb{K}}{\implies} \lambda(a_{i1}x_1 + a_{i2}x_2 + \dots + a_{1n}x_n) = 0$$ Luego, $x \in \tilde{E}_i$ por lo que se cumple la contención. Para ver $E_i \supseteq \tilde{E}_i$ si $x \in \tilde{E}_i$ multiplicando de ambos lados por $\lambda^{-1} \in \mathbb{K}$ tenemos que $x \in E_i$. Por lo tanto, $\tilde{E}_i = E_i \implies S_1 = S_2$.
3. Si tengo una ecuación $i$ nula tenemos que $E_i = \{(x_1,\dots, x_n) \in \mathbb{K}^n : 0 x_1 + \dots + 0 x_n = 0\}$ y notemos que toda $x \in \mathbb{K}^n$ resuelve esta ecuación $E_i = \mathbb{K}^n$ pero luego $$\begin{align} S_1 & = E_1 \cap \dots \cap E_{i-1} \cap E_i \cap E_{i+1} \cap \dots \cap E_m = E_1 \cap \dots \cap E_{i-1} \cap \mathbb{K}^n \cap E_{i+1} \cap \dots \cap E_m \\ &= E_1 \cap \dots \cap E_{i-1} \cap E_{i+1} \cap \dots \cap E_n = S_2\end{align} $$
4. Como ya demostramos la operación 1, tenemos que no importa el orden en el que estén las ecuaciones, si puedo probar para dos cualquiera esta operación entonces queda probada para todas. Elijamos por ejemplo la primera y segunda ecuación sus conjunto solución son $E_1 = \{(x_1, \dots, x_n) \in \mathbb{K}^n : a_{11}x_1 + \dots + a_{1n}x_n = 0\}$ y $E_2 = \{(x_1, \dots, x_n) \in \mathbb{K}^n : a_{21}x_1 + \dots + a_{2n}x_n = 0\}$ entonces si multiplicamos a la segunda ecuación por una constante $c \in \mathbb{K}$ y las sumamos para luego reemplazarla en $E_1$ tenemos que $\tilde{E}_1 = \{(x_1, \dots, x_n) \in \mathbb{K} : (a_{11} + ca_{21})x_1 + \dots + (a_{1n}+ca_{2n})x_n = 0\}$. Veamos que si $E_1 \cap \tilde{E}_2 = E_1 \cap E_2$ entonces $S_1 = S_2$. 
	Veamos primero que $E_1 \cap E_2 \subseteq E_1 \cap \tilde{E}_2$, si $(y_1, \dots, y_n) \in E_1 \cap E_2$ es una solución de ambos por lo tanto se cumple $a_{11}y_1 + \dots + a_{1n}y_n = 0$ y $a_{21}y_1 + \dots + a_{1n}y_n = 0$. Multiplicando a la segunda ecuación por $c$ y sumándola a la otra tenemos que $(a_{11} + ca_{21})y_1 + \dots + (a_{1n}+ca_{2n})y_n = 0$ entonces $(y_1, \dots, y_n) \in \tilde{E}_2 \cap E_1$ y se cumple la contención. Se prueba $E_1 \cap E_2 \supseteq E_1 \cap \tilde{E}_2$ de manera inversa o lo anterior sabiendo que la ecuación 1 se cumple si la multiplicamos por $c$ y la restamos a nuestra ecuación 2 modificada obtenemos la ecuación 2 anterior. $\blacksquare$ 

Podemos generalizar la proposición anterior para un sistema de ecuaciones no homogéneo demostrándolo de forma prácticamente idéntica. Usando este método podemos resolver cualquier sistema de ecuaciones con muchas variables.

Notemos que al usar este método (en un sistema no homogéneo), si obtenemos un absurdo como por ejemplo $0x_1 + \cdots + 0x_n = 4$ esto quiere significar que nuestro sistema **no posee soluciones**. 


# Matrices
Al aplicar las operaciones por fila vistas en [[Sistemas de Ecuaciones Lineales]], notemos que las mismas cambian únicamente los coeficientes de las ecuaciones, el número de incógnitas no cambia. Sería entonces mucho más simple simplificar la información de una manera más conveniente para que sea más limpio aplicar las operaciones elementales, como solución a esto aparecen las matrices. 

> [!Matrices]
> #Definición Una _matriz_ de $m$ filas y $n$ columnas (o de $m \times n$) consiste de elementos del cuerpo $\mathbb{K}$ ordenados en $m$ filas, cada una con $n$ elementos. $$\begin{pmatrix} a_{11} & \cdots & a_{1n} \\
> \vdots & \ddots & \vdots \\
> a_{m1} & \cdots & a_{mn} 
> \end{pmatrix}$$ El conjunto de todas las matrices del cuerpo $\mathbb{K}$ es denotado $M_{m \times n}(\mathbb{K})$ o $\mathbb{K}^{m \times n}$. Un elemento en la columna $j$ y fila $i$ se denota $A_{ij} = a_{ij}$.

Usando esta definición podemos **asociar** un sistema de ecuaciones homogéneo $m$ ecuaciones y $n$ incógnitas a una matriz en $M_{m \times n}(\mathbb{K})$: 
$$\begin{cases} 
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n = 0 \\ 
\quad \quad \quad \quad \vdots \\ 
a_{m1}x_1 + a_{n2}x_2 + \dots + a_{mn}x_n = 0
\end{cases}  
\quad \quad \rightarrow  \quad \quad 
\left( \begin{matrix} 
a_{11} & a_{12} &\cdots & a_{1n} \\ 
\vdots & \vdots & \ddots & \vdots \\ 
a_{m1} & a_{m2} & \cdots & a_{mn}  
\end{matrix} \right) $$
A esta la llamamos **matriz asociada** y podemos aplicarle a esta las mismas operaciones que al SEH. A un sistema no homogéneo, es necesario incluir una columna con los términos independientes del lado derecho de las ecuaciones, tal que es una matriz de $m \times (n+1)$:
$$\begin{cases} 
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n = b_1 \\ 
\quad \quad \quad \quad \vdots \\ 
a_{m1}x_1 + a_{n2}x_2 + \dots + a_{mn}x_n = b_m
\end{cases}  
\quad \quad \rightarrow  \quad \quad 
\left( \begin{matrix} 
a_{11} & a_{12} &\cdots & a_{1n} \\ 
\vdots & \vdots & \ddots & \vdots \\ 
a_{m1} & a_{m2} & \cdots & a_{mn}  
\end{matrix} \right|
\left| \begin{matrix} 
b_1 \\ \vdots \\ b_m
\end{matrix} \right)$$
Las matrices tienen un significado mucho más profundo que simplemente una **simplificación de la información** de los sistemas de ecuaciones, lo exploraremos más en [[Matrices de Transformaciones Lineales]]. 

## Matrices equivalentes por fila
En [[Sistemas de Ecuaciones Lineales]] (SEL) vimos que podemos manipular un SEL para obtener sistemas equivalentes tal que al final del proceso, podemos resolverlo de forma obvia. Sin embargo, observemos que no queda muy claro como tener que aplicar las operaciones, podríamos elegir aplicarlas de manera aleatoria y nunca llegar a nada. Necesitamos mejorar el método de Gauss para que quede más claro a donde queremos llegar. 

> [!Matriz Triangular Superior]
> #Definición Decimos que una matriz $A$ es _triangular superior_ cuando $A_{ij} = 0$ si $i > j$.  $$A = \left( \begin{matrix} 
a_{11} & a_{12} &\cdots & a_{1(n-1)} & a_{1n} \\ 
0 & a_{22} & \cdots & a_{2(n-1)} & a_{2n}\\
\vdots & \vdots & \ddots & \vdots & \vdots\\ 
0 & 0 & \cdots & 0 & a_{mn}  
\end{matrix} \right)$$

Si pasamos un SEL a su matriz asociada y luego aplicando las operaciones elementales llegamos a la matriz triangular superior, para luego volver a pasar al SEL de esta matriz tal que se puede resolver de forma simple y directa. Nos faltaría ahora la certeza de que siempre puedo llegar a una matriz triangular superior usando el método de Gauss. 

> [!Teorema de Gauss 1.5.]
> Sea $H$ un **sistema lineal homogéneo** de $n$ ecuaciones con $m$ incógnitas. Entonces, aplicando los cambios descriptos en la Prop. 1 de [[Sistemas de Ecuaciones Lineales]], puede obtenerse un sistema lineal homogéneo $H'$ cuya matriz asociada $B$ es triangular superior.

**Demostración.** Procedemos por el [[Principio de la inducción]] en $n$, la cantidad de ecuaciones del sistema. 
- **(Caso Base)** Si $n = 1$ es trivial pues una matriz de una fila es en sí mismo una matriz triangular superior.
- **(HI)** Supongamos que vale para $n$ y consideremos un sistema lineal de $n+1$ ecuaciones
$$\begin{cases} 
a_{11}x_1 & + a_{12}x_2 & + \quad \dots &  +\; a_{1m}x_m &= 0 \\ 
\quad &\quad &\vdots &\quad & \quad \\ 
a_{n1}x_1 &+ a_{n2}x_2& + \quad \dots &+ \; a_{nm}x_m &= 0 \\
a_{(n+1)1}x_1 &+ a_{(n+1) 2}x_2 &+ \quad \cdots &+ \; a_{(n+1)m}x_m &= 0
\end{cases}$$
  Tenemos que considerar que ocurre cuando $m=1$, tenemos que:
 $$\begin{cases} a_{11}x_1 = 0 \\ a_{21}x_2 = 0 \\ \quad \vdots \\ a_{(n+1)1}x_1 = 0\end{cases} \quad \rightarrow \quad \begin{pmatrix} a_{11} \\ a_{21} \\ \vdots \\ a_{(n+1)1}\end{pmatrix}$$
 Si $a_{i1} = 0$ para todo $1 \leq i \leq n+1$ entonces la única solución al sistema es la trivial.  Si $a_{i1} \neq 0$ para algún $i$, tenemos que puedo cambiar el $a_{i1}$ al multiplicar su fila por $a_{i1}^{-1}$ tal que al final obtengo 1 (3ra operación $a_{i1}^{-1} E_i$), una vez hecho esto puedo cambiar $e^{(12)}$. Obtengo entonces $\begin{pmatrix}  1 \\ a_{21} \\ \vdots \\ a_{(n+1)1}\end{pmatrix}$, si ahora a cada fila no nula, por ejemplo $a_{j1} \neq 0$, le realizo la operación 4 $e^{(j1)}_{a_{j1}}$  obtengo $\begin{pmatrix} 1 \\ 0 \\ \vdots \\ 0 \end{pmatrix}$ que es una matriz triangular superior. 
($m > 1$) **Primer Caso:** Si $a_{i1} = 0$ para cada $1 \leq i \leq n+1$. Entonces la matriz del sistema es de la forma: $$\begin{pmatrix} 0 & a_{12} & \cdots & a_{1m} \\
	\vdots  & \vdots & \ddots & \vdots \\
	0 & a_{n2} & \cdots & a_{nm} \end{pmatrix} \quad \longrightarrow \quad \begin{pmatrix} 0 & c \\ \vec{0} & M\end{pmatrix}$$
donde $\vec{0}$ denota una columna de ceros y $c \in M_{1 \times (m-1)}(\mathbb{K})$ y $M \in M_{n \times (m-1)}(\mathbb{K})$. 
**Segundo Caso:** Existe $j$ en $1 \leq j \leq n+1$, tal que $a_{1j} \neq 0$. Realizando el mismo proceso que hicimos cuando $m=1$ (primero $e^{(j)}_{a_{j1}^{-1}}$, luego $e^{(j1)}$ y aplico las veces necesarias $e_{-a_{i1}}^{(i1)}$) de tal manera que obtengo $$\begin{pmatrix} 1 & \tilde{c} \\ \vec{0} & \tilde{M} \end{pmatrix}$$ con $\tilde{c} \in \in M_{1 \times (m-1)}(\mathbb{K})$ y $\tilde{M} \in M_{n \times (m-1)}(\mathbb{K})$. 
Por lo tanto, para cualquier caso, aplicando las operaciones me queda que
$$A = \begin{pmatrix} a & c \\ \vec{0} & \tilde{M} \end{pmatrix} \quad \text{ con } \tilde{M} \in M_{n \times (m-1)}(\mathbb{K}) \text{ y } a=1 \text{ ó } a= 0$$
Luego, la matriz $\tilde{M}$ tiene $n$ filas y $m-1$ columnas, por hipótesis inductiva puedo obtener una matriz triangular superior de esta que es $\tilde{\tilde{M}}$. Entonces encontramos nuestra matriz triangular superior del sistema homogéneo, que es  $$B = \begin{pmatrix} a & c \\ \vec{0} & \tilde{\tilde{M}}\end{pmatrix} \quad \text{ con } \; a=1 \text{ ó } a= 0. \quad \blacksquare$$
De esta manera, el método de Gauss consiste en:
![[Pasted image 20230106103102.png]]
Al igual que probamos que dado un sistema $H$ y su matriz asociada $A$, un sistema equivalente puede obtenerse usando las **cuatro operaciones elementales por fila**, podemos decir que la matriz asociada de este sistema equivalente es una **matriz equivalente por filas** a la matriz $A$. 





# Cantidad de Soluciones de un Sistema Homogéneo
Como una consecuencia del **Teorema de Gauss** visto en [[Matrices]], vemos que para un sistema homogéneo ([[Sistemas de Ecuaciones Lineales]]) de $n$ ecuaciones y $m$ incógnitas con más ecuaciones que incógnitas ($n > m$) tenemos que en el proceso de aplicar el método de Gauss nos quedarán filas nulas. Por lo tanto, existe un sistema $H'$ de $n$ ecuaciones con $n$ incógnitas cuyo conjunto de soluciones coincide con el de $H$. 
En el caso contrario, de tener más incógnitas que ecuaciones ($n < m$) entonces será obvio que $n$ incógnitas van a depender de $m-n$ de ellas. Por lo tanto, es obvio que existen otras soluciones del sistema a parte de la trivial, y eventualmente probaremos esto. 
Para entender que ocurre cuando $n < m$ veamos un ejemplo:
$$\begin{cases} 2x_2 - x_3 + x_4 =0 \\ 
3x_1 + x_2 + 10x_3 + 5x_4 = 0 \\
x_1 + 3x_3 + x_4 = 0\end{cases}$$
Tenemos un sistema con más incógnitas que ecuaciones, entonces luego de aplicar el método de Gauss, nos queda:
$$\begin{cases} x_1 + 3x_3 + x_4 = 0 \\ 
x_2 + x_3 + 2x_4 = 0 \\
-3x_3 - 3x_4 = 0\end{cases}$$
Entonces, despejando $x_4$ de la tercera ecuación tenemos que $x_3 = -x_4$. Reemplazando en la segunda ecuación y despejando $x_2$ se obtiene que $x_2 = -x_4$. Por último, de la primera ecuación (reemplazando lo obtenido de la ecuación 2 y 3) tenemos que $x_1 = 2x_4$. Notemos que $n=3$ variables dependen de $m-n = 4 - 3= 1$ incógnita tal como habíamos predicho.   
El conjunto de soluciones del sistema nos queda $\{(2x_4, -x_4, -x_4,x_4): x_4 \in \mathbb{R}\}$ $= \{x_4(2, -1,-1,1) : x_4 \in \mathbb{R}\} = <(2,-1,-1,1)>$. 

Entonces, podemos probar que siempre que $n <m$ existen soluciones que no son las triviales:

> [!Teorema 1.6.]
> Sea $H$ un **sistema homogéneo** de $n$ ecuaciones con $m$ incógnitas. Supongamos $n < m$. Entonces existe $x \in \mathbb{K}^m, \; x \neq 0$, que es solución del sistema $H$.

**Demostración.** Por inducción en la cantidad de ecuaciones $n$ de $H$.
- **(Caso Base)** Si $n=1, m \geq 2$: entonces $H : a_{11}x_1 + a_{12}x_2 + \dots + a_{1m}x_m = 0$. Si $a_{11} = 0$, entonces $(1,0,\dots, 0)$ es una solución del sistema y si $a_{11} \neq 0$ entonces veamos que si elegimos $x_1 = \frac{-a_{12}}{a_{11}}$ y $x_2 = 1$ se cancelan $a_{11}(\frac{-a_{12}}{a_{11}}) + a_{12} = 0$, por lo tanto una solución es $(\frac{-a_{12}}{a_{11}}, 1, 0, \dots, 0)$. 
- **(Paso Inductivo)** Supongamos que el resultado vale para sistemas de $n$ ecuaciones y sea $H$ un sistema de $n+1$ ecuaciones con $n$ incógnitas $n+1 < m$. 

 Gracias al Teorema de Gauss sabemos que podemos triangular el sistema para que su matriz asociada quede de la forma 
$$\begin{pmatrix} 
a_{11} & a_{12} & \dots & a_{1m} \\
\vec{0} & \quad & B & \quad \\
\end{pmatrix}$$
 donde $B \in M_{n \times (m-1)}(\mathbb{K})$ y $m-1 > n$. 
 Por lo tanto, el sistema cuya matriz asociada es $B$ está en condiciones de la hipótesis inductiva. Luego, existe $(x_1, \dots, x_{m-1}) \neq (0, 0, \dots,0)$ que es solución del sistema asociado a $B$. 
  - Si $a_{11} = 0$, entonces $(1,0,\dots, 0)$ es una solución del sistema original. 
  - Si $a_{11} \neq 0$, entonces $\Big(\frac{-1}{a_{11}} \cdot (\sum_{i=2}^m a_{1i}x_{i-1}), x_1, \dots, x_{m-1}\Big)$ es una solución no nula del sistema. $\blacksquare$

Nos podemos preguntar _¿Qué ocurre cuando $n=m$?_ _¿Podemos crear una condición para cuando existe una solución del mismo además de la trivial?_ 
Notemos que si al llegar a la matriz triangular superior, no se generó ninguna fila nula tenemos que la ecuación $n$ nos quedaría $a_{nn}x_n = 0 \rightarrow x_n = 0$, reemplazando a esta en la ecuación $n-1$ tenemos que $a_{(n-1)(n-1)}x_{n-1} + a_{(n-1)n}x_n = 0 \rightarrow a_{(n-1)(n-1)}x_{n-1} = 0 \rightarrow x_{n-1} = 0$ y así sucesivamente hasta que nos queda $(x_1, \dots, x_n) = (0, \dots, 0)$. De otra manera, si nos quedaran filas nulas esto significaría que tenemos más incógnitas que ecuaciones para despejar y existirían soluciones no nulas (como nos dice el Teorema 1). A partir de esto deducimos:

> [!Teorema 2.7.] 
> Sea $H$ un sistema lineal homogéneo de $n$ ecuaciones y $n$ incógnitas. Sea $H'$ un sistema equivalente a $H$ cuya matriz $B$ es triangular superior. Entonces $H$ tiene solución única si y sólo si $B_{ii} \neq 0, \; \forall  i : 1 \leq i \leq n$.

**Demostración.** ($\Leftarrow$) Supongamos que $$B = \begin{pmatrix} 
B_{11} & \cdots & B_{1n} \\
0 & \ddots & \vdots \\
\cdots & 0 & B_{nn} 
\end{pmatrix}$$
con $B_{ii} \neq 0$. Como deducimos anteriormente, la última ecuación de $H'$ sería $B_{nn}x_n = 0$ por lo que $x_n = 0$ y el resto de las otras variables también terminan dando cero por lo tanto $(x_1, \dots, x_n) = (0, \dots, 0)$.
($\Rightarrow$) Supongamos que $B_{11} \neq 0, \dots, B_{ii} \neq 0$ y $B_{(i+1)(i+1)} = 0$, encontremos que existe otra solución no nula que resuelve el sistema cuya matriz asociada sería:
$$\begin{pmatrix} 
B_{11} & \quad & \quad & \cdots & \quad & B_{1n} \\
0 & \ddots & \quad & \quad & \quad &  \vdots \\
\vdots& \ddots & B_{ii} & B_{i(i+1)} & \cdots & B_{in} \\
0 & \quad & 0 & 0 & \quad & \quad \\
\vdots & \quad & \vdots & \vdots & M & \quad \\
0 & \cdots & 0 & 0 & \quad \quad 
\end{pmatrix}$$
Es claro que (como vimos en la demostración anterior) una solución al sistema que tiene la matriz asociada $( \; \vec{0} \quad M \;)$ es $(1,0,\dots, 0)$ ó $x_{i+1} = 1, x_{i+2} = 0, \dots, x_n = 0$. 
La $i$-ésima ecuación nos quedaría $0x_1 + \dots + B_{ii}x_i + B_{i(i+1)}(1) + \cdots + B_{in}(0)$ tal que despejando nos quedaría $x_i = -\frac{B_{i(i+1)}}{B_{ii}}$. Se sigue de esta manera para calcular los valores de todas las variables y se obtiene una solución de $H'$ de la forma $(x_1, \dots, x_i, 1, 0, \dots, 0)$ que es no nula. $\blacksquare$ 

# Cantidad de Soluciones de un Sistema No Homogéneo

Ahora que entendemos el comportamiento de los sistemas homogéneos, el estudio de cuando un sistema no homogéneo tiene solución se vuelve mucho más sencillo.

> [!Sistema Homogéneo Asociado]
> Un sistema de ecuaciones lineales $$H: \begin{cases} 
> a_{11}x_1 + a_{12}x_2 + \dots + a_{1m}x_m & = b_1 \\
> \quad \quad \quad \quad \vdots \\
> a_{n1}x_1 + a_{n2}x_2 + \cdots + a_{nm}x_m & = b_n 
> \end{cases}$$
> se dice _no homogéneo_ si existe $i$, $1 \leq i \leq n$, con $b_i \neq 0$. La matriz $A = (a_{ij})$ se dice la _matriz asociada del sistema_. Llamaremos al _sistema homogéneo asociado a $H$_ a 
> $$H: \begin{cases} 
> a_{11}x_1 + a_{12}x_2 + \dots + a_{1m}x_m & = 0 \\
> \quad \quad \quad \quad \vdots \\
> a_{n1}x_1 + a_{n2}x_2 + \cdots + a_{nm}x_m & = 0 
> \end{cases}$$

Ya sabemos que las soluciones de un sistema homogéneo es un subespacio ([[Subespacios]]), lo vimos en [[Sistemas de Ecuaciones Lineales]], sin embargo el conjunto de soluciones de un sistema no homogéneo no es un subespacio, pues el $(0,0,\dots, 0)$ ya no es una solución. No obstante, el conjunto de soluciones del sistema homogéneo asociado y el del no homogéneo están íntimamente relacionados. 

> [!Proposición 3.8.]
> Sea $H$ un sistema lineal no homogéneo con soluciones. Sea $S$ el conjunto de soluciones del sistema homogéneo asociado a $H$ y $p$ una solución particular de $H$. Entonces, el conjunto $M$ de soluciones de $H$ es $M = S + p = \{s+p : s \in S\}$. 

**Demostración.** Sea $H$ el sistema 
$$H: \begin{cases} 
 a_{11}x_1 + a_{12}x_2 + \dots + a_{1m}x_m & = b_1 \\
 \quad \quad \quad \quad \vdots \\
 a_{n1}x_1 + a_{n2}x_2 + \cdots + a_{nm}x_m & = b_n 
 \end{cases}$$
 ($\subseteq$) Sea $z \in M$. Se tiene que $z = (z-p)+p$. Luego, para probar que $z \in S+p$, basta ver que $z-p = (z_1-p_1, \dots, z_m - p_m) \in S$, es decir, que es solución del sistema homogéneo asociado a $H$. 
 Sea $i$, $1 \leq i \leq n$. Entonces,  $$ \begin{align}
 a_{i1}(z_1 - p_1) + \dots + a_{im}(z_m - p_m) &= (a_{i1}z_1 + \dots + a_{im}z_m)- (a_{i1}p_1 + \dots + a_{im}p_m) \\
 & = b_i - b_i = 0
 \end{align}$$
 puesto que $z$ y $p$ son ambas soluciones de $H$. Luego, $z-p \in S$.

 ($\supseteq$) Sea $y \in S+p$. Entonces $y=s+p$ con $s \in S$.
 Para cada $1 \leq i \leq n$,$$\begin{align}
 a_{i1}y_1 + \dots + a_{im}y_m &= a_{i1}(s_1 + p_1) + \dots + a_{im}(s_m + p_m) = \\
 & = (a_{i1}s_1 + \dots + a_{im}s_m) + (a_{i1}p_1 + \dots + a_{im}p_m) = 0 + b_i = b_i
 \end{align}$$
 puesto que $p$ es una solución de $H$ y $s$ es una solución del sistema homogéneo asociado a $H$. 
 En consecuencia, $y$ es solución de $H$, es decir $y \in M$. $\blacksquare$ 

Sin embargo, es complicado encontrar que un sistema tiene soluciones a simple vista y es más difícil aún encontrar una solución particular, entonces esta proposición no es tan útil más que para mostrarnos como se estructura el conjunto de soluciones de un sistema no homogéneo. 
Observemos que si la única solución del sistema homogéneo asociado es la trivial, tenemos que siendo $p$ una solución particular el conjunto de soluciones es $\{(0,0, \dots, 0) + (p_1, p_2, \dots, p_n)\} = \{(p_1,p_2, \dots, p_n)\}$ es decir el sistema de ecuaciones no homogéneo tiene una **solución única**. 

Para poder encontrar el conjunto de soluciones de un sistema no homogéneo, lo más normal es usar también el método de Gauss (visto en [[Sistemas de Ecuaciones Lineales]] y [[Matrices]]) sobre la _matriz ampliada_.

> [!Matriz Ampliada]
> Dado un sistema de ecuaciones no homogéneo
> $$H: \begin{cases} 
 a_{11}x_1 + a_{12}x_2 + \dots + a_{1m}x_m & = b_1 \\
 \quad \quad \quad \quad \vdots \\
 a_{n1}x_1 + a_{n2}x_2 + \cdots + a_{nm}x_m & = b_n 
 \end{cases}$$ 
 > se llama _matriz ampliada asociada al sistema_ $H$ a la matriz 
 > $$ \left( \begin{matrix} 
a_{11} & a_{12} &\cdots & a_{1n} \\ 
\vdots & \vdots & \ddots & \vdots \\ 
a_{m1} & a_{m2} & \cdots & a_{mn}  
\end{matrix} \right|
 \left| \begin{matrix} 
b_1 \\ \vdots \\ b_m
\end{matrix} \right)$$ 
 

# Operaciones con Matrices
Las matrices tienen una importancia muy grande en el Algebra Lineal, su utilidad va más allá de ser una **simplificación de la información** de los [[Sistemas de Ecuaciones Lineales]] (como vimos en [[Matrices]]). Las Matrices son muy utilizadas en computación, por ejemplo para guardar información. Entonces, es muy útil entender el conjunto de todas las matrices $M_{n\times m}(\mathbb{K})$. 

> [!Igualdad de Matrices]
> #Definición Sean $A,B \in M_{n\times m}(\mathbb{K})$. Entonces $A = B$ si y solo si $A_{ij} = B_{ij}$ para cada $1 \leq i \leq n$, $1 \leq j \leq m$. 

Podemos definir la operación suma de matrices y la acción de $\mathbb{K}$ que transforman a $M_{n\times m}(\mathbb{K})$ en un $\mathbb{K}$-espacio vectorial:

> [!Operaciones Básicas de Matrices]
> #Definición Se definen la _suma de matrices_ y el _producto por escalares_ como
> $+ : M_{n\times m}(\mathbb{K}) \times M_{n\times m}(\mathbb{K}) \rightarrow M_{n\times m}(\mathbb{K}), \; (A+B)_{ij} = A_{ij} + B_{ij} \quad \quad (1 \leq i \leq n, \; 1 \leq j \leq m)$ $\cdot : \mathbb{K} \times M_{n\times m}(\mathbb{K}) \rightarrow M_{n\times m}(\mathbb{K}), \; (\lambda \cdot A)_{ij} = \lambda \cdot A_{ij}  \quad  \quad (1 \leq i \leq n, \; 1 \leq j \leq m)$

Es fácil verificar que $(M_{n\times m}(\mathbb{K}), +, \cdot)$ es un espacio vectorial ([[Espacios Vectoriales]]). Como sumar dos matrices es sumar sus respectivos elementos $(A+B)_{ij} = A_{ij} + B_{ij}$ como $A_{ij}$ y $B_{ij}$ son perteneces al cuerpo $\mathbb{K}$ entonces claramente son conmutativos, asociativos, tienen neutro (que sería la _matriz nula_ $\left(\begin{matrix} 0 & \dots & 0 \\ \vdots & \ddots & \vdots \\ 0 & \cdots & 0 \end{matrix}\right)$) y tienen opuesto (que sería $(-A)_{ij} = \{-a_{ij} : 1 \leq i \leq n, \; 1 \leq j \leq m\}$). Luego, la acción sobre $\mathbb{K}$ cumple las cuatro propiedades pues las cumple en el cuerpo $\mathbb{K}$, por ejemplo si $\lambda \in \mathbb{K}$ y $A, B \in M_{n\times m}(\mathbb{K})$ entonces $\lambda(A+B)_{ij} = \lambda( A_{ij} + B_{ij}) = \lambda A_{ij} + \lambda B_{ij} = (\lambda A)_{ij} + (\lambda B)_{ij}$ (el último paso es posible gracias a la definición del producto por escalares) y así se pueden probar las otras 3. 

Notemos que para poder sumar dos matrices tienen que pertenecer al mismo espacio vectorial, de otra manera si $A \in M_{n\times m}(\mathbb{K})$ y $B \in M_{n\times k}(\mathbb{K})$ ($k \neq m$) tenemos que no existe $A+B$. Es decir, para poder sumar dos matrices **tienen que tener el mismo número de filas y columnas**. 

La siguiente definición se refiere al producto de dos matrices $A \in M_{n\times m}(\mathbb{K})$ y $B \in M_{m\times r}(\mathbb{K})$, la necesidad del producto de matrices nace de las [[Transformaciones Lineales]], así que no entenderemos profundamente porque esta definido de esta manera hasta no mucho más adelante. 

> [!Producto de Matrices]
> #Definición Sean $A \in M_{n\times m}(\mathbb{K})$ y $B \in M_{m\times r}(\mathbb{K})$. Se define el _producto de $A$ por $B$_ como la matriz $C \in M_{n\times r}(\mathbb{K})$ tal que $$C_{ij} = \sum_{k=1}^m A_{ik}B_{kj} \quad 1 \leq i \leq n, 1 \leq j \leq r,$$

A partir de la definición podemos concluir que para multiplicar dos matrices **es necesario que el número de columnas de $A$ sea el mismo que el número de filas de $B$** de otra manera no puede existir el producto. 

Analicemos ahora algunas propiedades del producto de matrices: 

> [!Proposición 1.9.]
> Propiedades del producto de matrices:
> 1. _Propiedad asociativa_: dadas $A \in M_{n\times m}(\mathbb{K})$, $B \in M_{m\times r}(\mathbb{K})$ y $C \in M_{r\times s}(\mathbb{K})$ se tiene que $(A \cdot B) \cdot C = A \cdot (A \cdot B)$ 
> 2. Para cada $n \in \mathbb{N}$, sea $I_n \in M_{n\times m}(\mathbb{K})$ (_matriz identidad_ de $M_{n\times n}(\mathbb{K})$) definida por $(I_n)_{ij} = \begin{cases} 1 & si \; i = j \\ 0 & si i \neq j \end{cases}$. Entonces si $A \in M_{n\times m}(\mathbb{K})$, se verifica $I_n \cdot A = A \cdot I_m = A$.
> 3. Propiedades distributivas:
> 	1. Si $A \in M_{n\times m}(\mathbb{K})$ y $B, C \in M_{m\times r}(\mathbb{K})$, entonces $A(B+C) = AB + AC$
> 	2. Si $A,B \in M_{n\times m}(\mathbb{K})$ y $C \in M_{m\times r}(\mathbb{K})$, entonces $(A+B) \cdot C = AC + BC$. 

**Demostración.** 
1. Observemos que en primer lugar que si $A  \in M_{n\times m}(\mathbb{K})$, $B \in M_{m\times r}(\mathbb{K})$ y $C \in M_{r\times s}(\mathbb{K})$, entonces $(A \cdot B) \cdot C \in M_{n\times s}(\mathbb{K})$ y $A \cdot (B \cdot C) \in M_{n\times s}(\mathbb{K})$. Para cada $1 \leq i \leq n, 1 \leq j \leq s$, se tiene:
$$
\begin{align}
\left((A . B) \cdot C \right)_{i j}=\sum_{\alpha = 1}^r(A . B)_{i \alpha} C_{\alpha j}=\sum_{a=1}^r\left(\sum_{\beta=1}^m A_{i \beta} B_{\beta \alpha}\right) C_{\alpha j}=\sum_{\alpha=1}^r\left(\sum_{\beta=1}^m A_{i \beta} B_{\beta \alpha} C_{\alpha j}\right)= \\
\sum_{\beta=1}^m\left(\sum_{\alpha=1}^r A_{i \alpha} B_{\beta  i} C_{\alpha j}\right)=\sum_{\beta=1}^m A_{i \alpha}\left(\sum_{\alpha=1}^r B_{\beta i} C_{\alpha j}\right)=\sum_{\beta=1}^m A_{i \beta}(B \cdot C)_{\beta j}=(A \cdot (B \cdot C ))_{i j} \\
\end{align}
$$
2. Sean $1 \leq i \leq n, 1 \leq j \leq m$. Se tiene que
$$
\left(I_n . A\right)_{i j}=\sum_{k=1}^n\left(I_n\right)_{ik} . A_{k j}=1 \cdot A_{i j}=A_{i j}
$$

 De la misma manera, $(A \cdot I_m)_{ij} = A_{i j}$ para cada $1 \leq i \leq n, 1 \leq j \leq m$.
3. Se puede deducir de manera parecida a (1) considerando la definición de suma de matrices. $\blacksquare$

De las propiedades anteriores podemos deducir que como se cumple la asociatividad, distributivas y la existencia de la identidad, entonces $(M_{n\times m}(\mathbb{K}), +, \cdot)$ es un **anillo**.  Observemos que el producto de matrices **no es conmutativo**, pues por ejemplo si $A = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}$ y $B = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$ tenemos que $A \cdot B = \begin{pmatrix}  0 & 0 \\ 0 & 0\end{pmatrix}$ y $B \cdot A = \begin{pmatrix} 0 & 1 \\ 0 & 0\end{pmatrix}$ por lo tanto $A \cdot B \neq B \cdot A$. El ejemplo anterior sirve para ver también de que a pesar de que $A \cdot B = 0$ esto no implica que $A = 0$ y $B = 0$ por lo tanto se dice que existen **divisores de cero** en el conjunto de matrices.

Resulta que juntando la acción sobre $\mathbb{K}$, la operación suma y el producto de matrices $(M_{n\times m}(\mathbb{K}), +, \cdot_K, \cdot)$, tenemos que se cumple que la nueva estructura creada se llama una **$\mathbb{K}$-álgebra**. Las álgebras son estructuras muy interesantes con muchas aplicaciones. 

Notemos algo importante, que  $\mathbb{K}^n$ y $M_{1\times n}(\mathbb{K})$ que es una matriz de 1 fila y $n$ columnas (también $M_{n\times 1}(\mathbb{K})$) tiene una estructura muy parecida, hasta podríamos decir idéntica. Por cuestiones que veremos más adelante diremos que es lo mismo que un vector $v \in \mathbb{K}^n$ que esté en $v \in M_{1\times n}(\mathbb{K})$ (ó $M_{n\times 1}(\mathbb{K})$). 

Una forma de ver para que es útil definir el producto de matrices es que nos permite escribir un [[Sistemas de Ecuaciones Lineales]] de $n$ ecuaciones $m$ incógnitas 
$$\begin{cases} 
a_{11}x_1 + a_{12}x_2 + \dots + a_{1m}x_m = b_1 \\ 
\quad \quad \quad \quad \vdots \\ 
a_{n1}x_1 + a_{n2}x_2 + \dots + a_{nm}x_m = b_n
\end{cases}  $$
de la forma 
$$A \cdot \vec{x} = \vec{b}$$
donde $A \in M_{n\times m}(\mathbb{K})$ es la matriz asociada del sistema, $\vec{x} \in \mathbb{K}^m$ (en realidad sería una matriz de una columna pero ya vimos que es lo mismo) es el vector de incógnitas y $\vec{b} \in \mathbb{K}^n$ es el vector de términos independientes y $\cdot$ es el producto de matrices definido anteriormente. Usando esto, se nos abre un mundo de posibilidades para entender mejor los sistemas de ecuaciones, una ecuación $ax = b$ en $\mathbb{K}$ se resuelve despejando $x$ usando el inverso de $a$, tal que $a^{-1}a \cdot x = b \cdot a^{-1} \rightarrow x = b \cdot a^{-1}$, lo cual nos lleva a pensar de que si existiera una matriz que sea la **inversa** de $A$ tal que $A \cdot A^{-1} = I_n$ podríamos resolver la ecuación $Ax = b$ simplemente despejando. Exploraremos más esto último en [[Matrices Invertibles]]. 

# Matrices Invertibles
De lo que vimos en [[Operaciones con Matrices]], queremos definir la matriz ([[Matrices]]) inversa sobre $M_{n\times n}(\mathbb{K})$ es el conjunto de matrices **cuadradas** (es decir matrices con el mismo número de filas que de columnas): 

> [!Matrices Invertibles]
> #Definición Una matriz $A \in M_{n\times n}(\mathbb{K})$ se dice _invertible_ si existe una matriz $B \in M_{n\times n}(\mathbb{K})$ tal que $A \cdot B = B \cdot A = I_n$.

Podemos probar que la inversa de una matriz es **única**. 

> [!Proposición 1.10.]
> Sea $A, B \in M_{n\times n}(\mathbb{K})$ y $B$ es la inversa de $A$ es única.

**Demostración.** Supongamos por el absurdo que existe $C \in M_{n\times n}(\mathbb{K})$ tal que sea el inverso de $A$ también, es decir $AC = CA = I_n$ y $AB = BA = I_n$. Entonces
$$B = I_n B = (CA)B = C(AB) = CI_n = C \quad \blacksquare$$
Entonces, como sabemos que las inversas de _algunas_ matrices en $M_{n\times n}(\mathbb{K})$ existen, por ejemplo si $A = \begin{pmatrix} 0 & 1 \\ 2 & 0 \end{pmatrix}$ tiene inversa $B = \begin{pmatrix} 0 & 1/2 \\ 1 & 0 \end{pmatrix}$ pues 
$$AB = \begin{pmatrix} 0 & 1 \\ 2 & 0 \end{pmatrix} \cdot \begin{pmatrix} 0 & 1/2 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 0\cdot 0 + 1 \cdot 1 & 0 \cdot 1/2 + 1 \cdot 0 \\ 2 \cdot 0 + 0 \cdot 1 & 2 \cdot 1/2 + 0 \cdot 0\end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1\end{pmatrix}$$
Podemos definir entonces
> [!Grupo lineal general]
> #Definición Sea $M_{n \times n}(\mathbb{K})$ el conjunto de todas las matrices cuadradas, podemos definir $GL(n,\mathbb{K}) = \{A \in M_{n\times n}(\mathbb{K}) / A \text{ es inversible }\}$. 


Se pueden probar de este las siguientes propiedades: 

> [!Proposición 2.]
> Para cada $n \in N$, se verifican las siguientes propiedades
> 1. Si $A, B \in G L(n, K)$, entonces $A \cdot B \in G L(n, K)$. Más aún, $(A \cdot B)^{-1}=B^{-1} A^{-1}$. En particular, el producto de matrices $\cdot$ es una operación cerrada en $G L(n, K)$.
> 2. $I_n \in G L(n, K)$.
> 3. Si $A \in G L(n, K)$, entonces $A^{-1} \in G L(n, K)$.

**Demostración.**
1. Sean $A, B \in GL(n, K)$. Entonces existen $A^{-1}$ y $B^{-1}$. Se tiene que$$
(A \cdot B) \cdot\left(B^{-1} \cdot A^{-1}\right)=I_n \quad \text { y } \quad\left(B^{-1} \cdot A^{-1}\right) \cdot(A \cdot B)=I_n
$$Entonces $A \cdot B=B^{-1} \cdot A^{-1}$.
2. Es consecuencia de que $I_n \cdot I_n = I_n$.
3. De la definición de inversa se deduce inmediatamente que si $A \in G L(n, K)$, entonces $\left(A^{-1}\right)^{-1}=A$ y por lo tanto $A^{-1} \in G L(n, K)$. $\blacksquare$ 

Observemos que las 3 propiedades anteriores más la asociatividad en el producto de matrices, nos dice que $(GL(n, \mathbb{K}), \cdot)$ es una estructura algebraica nueva que llamamos **grupo**, que se llama **grupo lineal general**. 
En general, para que una estructura sea un grupo es necesario de un conjunto y una operación que cumpla 4 propiedades: cerradura (es decir que si yo opero dos elementos del conjunto me da otro elemento del conjunto), existencia del neutro, existencia del opuesto y asociatividad. 

## ¿Cómo obtenemos una inversa?
Ahora que entendimos bien el comportamiento de un grupo, podemos entender mejor a $(GL(n, \mathbb{K}), \cdot)$. El hecho de que esta estructura sea un grupo es fundamental y un hecho muy utilizado en álgebra lineal al que volveremos continuamente.  

> [!Proposición 3.11.]
> Sea $e$ una una operación elemental por fila y sea $E \in M_{n \times n}(\mathbb{K})$ sea una _matriz elemental_ $E= e(Id)$ (aplicarle la operación por fila a la identidad). Entonces, para cada $n \times m$ matriz $A$ tenemos que $e(A) = EA$. 

**Demostración.** El punto de esta prueba es que la entrada de la fila $i$ y la comuna $j$ del producto de matrices (visto en [[Operaciones con Matrices]]) es obtenida por la fila $i$ de $E$ y la columna $j$ de $A$. Probemos que $e(A) = EA$ para la operación $e_4: F_i + cF_j$ y los otros dos casos son aún más fáciles que este. Supongamos que $r \neq s$, tanto que $1 \leq r \leq n$ y $1 \leq s \leq n$, y $e_4$ es la operación de reemplazar la fila $F_r$ por la fila $F_r$ más un $c \in \mathbb{K}$  multiplicado por la fila $F_s$. Entonces, 
$$E_{ik} = \begin{cases} \delta_{ik}, & i \neq r \\ \delta_{rk}+ c\delta_{sk}, & i = r \end{cases}$$
donde $\delta_{ik} = 0$ ó $\delta_{ik} =1$ son los valores de la matriz identidad $Id_{ik} = \begin{cases} 0, & i \neq k \\ 1, & i = k \end{cases}$ . Luego,
$$(EA)_{ij} = \sum_{k=1}^n E_{ik}A_{kj} = \begin{cases} A_{ik}, & i \neq r \\ A_{rj} + cA_{sj}, & i = r\end{cases}$$
En otras palabras, $EA = e_4(A)$ . $\blacksquare$

Entonces, observemos que las matrices elementales pueden ser nuestro "bloques de construcción" para la inversa. Pues al multiplicarla por la matriz para obtener una matriz triangular obtenemos que estamos acercando cada vez más la matriz a la identidad, pero luego si una vez que llegamos a la matriz triangular superior las seguimos aplicando para generar también una _matriz triangular inferior_ ($A_{ij} = 0$ cuando $i < j$) llegamos a la matriz identidad. Por lo tanto una matriz $A$ se puede escribir como $A = E_1 \cdot E_2 \cdots E_l \cdot I_n$ siendo $l$ un número finito de operaciones elementales por fila realizadas, luego por la proposición 2(2) tenemos que $A^{-1} = E_l^{-1} \cdots E_{2}^{-1} \cdot E_{1}^{-1} \cdot I_n$. Pero para esto tendríamos que probar dos proposiciones antes: (1) Que las matrices elementales son invertibles y (2) que toda matriz $A$ que es un producto de matrices elementales es invertible.

> [!Proposición 4.12.]
> Una matriz elemental $E \in M_{n \times n}(\mathbb{K})$ es invertible, o también $E \in GL(n,\mathbb{K})$. 

**Demostración.** 
- (Operación 1) Sea $e^{(ij)}$ la operación para cambiar la fila $i$ por la fila $j$ y $E^{(ij)}$ su respectiva matriz elemental. Tenemos que si volvemos a aplicar la operación otra vez  $E^{(ij)}$ obtenemos la matriz identidad , es decir $e^{(ij)}(e^{(ij)}(Id_n)) = Id_n$ por lo tanto $E^{(ij)} \cdot E^{(ij)} = Id_n$. Luego, por definición $E^{(ij)}$ es inversa de sí misma. 
- (Operación 2) Sea $e^{(i)}_c$ la operación que multiplica la fila $i$ por una constante $c \in \mathbb{K}$ y $E_c^{(i)} = e_{c}^{(i)}(Id_n)$ su respectiva matriz elemental. Tenemos que al aplicar $e_{c^{-1}}^{(i)}$ sobre la matriz elemental $E_c^{(i)}$ tenemos de vuelta a la matriz identidad $e^{(i)}_{c^{-1}}(e^{(i)}_c(Id_n))$ por lo tanto $E_{c^{-1}}^{(i)} \cdot E_{c}^{(i)} = Id_n$. Luego, por definición $E^{(i)}_{c^{-1}}$ es la inversa. 
- (Operación 3) Es trivial.
- (Operación 4) Sea $e_c^{(ij)}$ la operación para cambiar fila $i$ por la fila $i$ más una constante $c$ por la fila $j$  y $E^{(ij)}_{c} = e_{c}^{(ij)}(Id_n)$ su respectiva matriz elemental. Tenemos que si aplicamos la operación $e_{-c}^{(ij)}$ sobre la matriz elemental $E_{c}^{(ij)}$ obtenemos la matriz identidad, es decir $e_{-c}^{(ij)}(e_{c}^{(ij)}(Id_n)) = Id_n$ por lo tanto $E_{-c}^{(ij)} \cdot E_{c}^{(ij)} = Id_n$. Luego, por definición $E_{-c}^{(ij)}$ es la inversa. $\blacksquare$ 

> [!Teorema 5.13. (Inversibilidad / Operaciones por fila)]
> Si $A \in M_{n \times n}(\mathbb{K})$ una matriz, las siguientes son equivalentes: 
> 1. $A$ es invertible.
> 2. $A$ es equivalente por filas a la matriz identidad $Id_n$.
> 3. $A$ es un producto de matrices elementales. 

**Demostración.** 
- (1 $\Rightarrow$ 2) Por el teorema de Gauss, visto en [[Matrices]], $\exists E_1, \dots, E_n$ matrices elementales tal que $R = E_1 \cdots E_r A$ (por la proposición 3) y $R$ es una matriz triangular superior. Como el producto de matrices invertibles son invertibles, tenemos que $A$ es invertible entonces $R$ es invertible.  Tenemos que $R$ es invertible si y sólo si cada fila de $R$ contiene una entrada no nula, pues de otra manera tendríamos $R = \begin{pmatrix} 1  & \cdots & \cdot \\ \vdots & \ddots & 1 \\ 0 & \cdots & 0 \end{pmatrix}$ y por lo tanto al multiplicarla por cualquier otra matriz que "podría" ser la inversa tendríamos que por definición de la multiplicación existe una fila nula en el producto, que tendría que ser la identidad por lo tanto llegamos a un absurdo. Entonces, una vez que sabemos que existen valores no nulos en casa fila, puedo usarlos de _pivot_[^1] para hacer $0$ a las entradas por arriba de la diagonal. De esta manera, existen $k$ matrices elementales tal que $(\tilde{E}_k \cdots \tilde{E}_2 \cdot \tilde{E}_1) \cdot (E_n \cdots E_2 \cdot E_1) \cdot A = Id_n$. Para ver la vuelta (1 $\Leftarrow$ 2) empezamos sabiendo que que podemos aplicar una serie de operaciones a $A$ para obtener $Id_n$ pero luego es obvio que como las operaciones por filas es lo mismo que multiplicar por su respectiva matriz elemental tenemos que $(\tilde{E}_k \cdots \tilde{E}_2 \cdot \tilde{E}_1) \cdot (E_n \cdots E_2 \cdot E_1) \cdot A = Id_n$ y por definición de la inversa tenemos que $A^{-1} = (\tilde{E}_k \cdots \tilde{E}_2 \cdot \tilde{E}_1) \cdot (E_n \cdots E_2 \cdot E_1)$. 
- (2 $\Rightarrow$ 3) Como las matrices elementales son invertibles tenemos que $(A^{-1})^{-1}=(\tilde{E}_k \cdots \tilde{E}_2 \cdot \tilde{E}_1 \cdot E_n \cdots E_2 \cdot E_1)^{-1} = \tilde{E}_1^{-1} \cdots \tilde{E}_{k-1}^{-1} \cdot \tilde{E}_k^{-1} \cdot E_1^{-1} \cdots E_{n-1}^{-1} \cdot E_n^{-1}$ por la proposición 2 tenemos que $(A^{-1})^{-1} = A$ y las inversas de matrices elementales son elementales que realizan el proceso inverso. (2 $\Leftarrow$ 3) es trivial.
- (1 $\Rightarrow$ 3) Si $A$ es un producto de matrices elementales, y las elementales son invertibles, como el producto de invertibles es invertible, entonces $A$ es invertible. (1 $\Leftarrow$ 3) es trivial. $\blacksquare$ 

Este teorema se puede utilizar para obtener la matriz inversa, si yo se que $A^{-1} = (\tilde{E}_k \cdots \tilde{E}_2 \cdot \tilde{E}_1) \cdot (E_n \cdots E_2 \cdot E_1)$ ó también $A^{-1} = \tilde{e}_k (\cdots \tilde{e}_2(\tilde{e}_1(e_n(\cdots e_2(e_1(Id_n)))))$ es decir, si yo le aplico a la identidad las mismas operaciones elementales que le aplico a $A$ para que llegue a la identidad entonces obtengo la inversa. 

Observemos que en un sistema de ecuaciones lineales __que tiene solución única__ se puede expresar $A\vec{x} = \vec{b}$ donde $A$ es la matriz $n \times n$ de coeficientes, ahora si aplicamos de ambos lados la multiplicación por
matrices elementales (que reducen la matriz) tenemos que 
$$\underset{A^{-1}}{\underbrace{(\tilde{E}_k \cdots \tilde{E}_2 \cdot \tilde{E}_1 \cdot E_n \cdots E_2 \cdot E_1)}} \cdot A \vec{x} = \underset{A^{-1}}{\underbrace{(\tilde{E}_k \cdots \tilde{E}_2 \cdot \tilde{E}_1 \cdot E_n \cdots E_2 \cdot E_1)}} \vec{b}$$
entonces encontramos de esta manera la solución del sistema $\vec{x} = A^{-1}\vec{b}$ (recordemos que $\vec{x}$ y $\vec{b}$ son en realidad matrices de una columna y $n$ filas). 

[^1]: Un "pivot" o pivote es el nombre que se le da un valor no nulo en una fila de una matriz, tal que al aplicar el método de Gauss puedo usarlo para hacer los elementos debajo de este 0, aplicando la operación 4 de la proposición vista en [[Sistemas de Ecuaciones Lineales]].  

# Espacios Vectoriales Finitos
Ya vimos en [[Sistemas de Ecuaciones Lineales]] el concepto de **sistemas de generadores** de un espacio vectorial. Que ya vimos que en $\mathbb{R}^2$ tenemos que el subespacio generado por un vector $v$, nos da una recta que pasa por el origen, luego en $\mathbb{R}^3$ si tomamos el subespacio ([[Subespacios]]) generado por dos vectores, tenemos que _muchas veces nos da_ un plano que pasa por el origen y contiene a los dos vectores. Observemos también que el subespacio de soluciones de un sistema de ecuaciones homogéneo (visto en [[Cantidad de soluciones de un SEL]]) de 1 ecuación y 3 incógnitas es también un plano que pasa por el origen, pues está generado por dos vectores.

Resaltemos el hecho de que en el párrafo anterior nos dicen que "muchas veces", es decir no siempre, se puede formar un plano con dos vectores _¿Cuándo esto no ocurre?_ Tomemos por ejemplo los vectores $(1,-1,4), \; (1/2, -1/2, 2)$ no generan un plano, sino una recta en el espacio. Esto ocurre porque el segundo vector $(1/2, -1/2,2)$ al multiplicarlo por 2 obtenemos el primero $(1,-1,4)$ lo cual hace que al escribirlos como combinación lineal $a(1,-1,4) + b(1/2,-1/2,2)$ podemos reescribir a el secundo vector como $1/2(1,-1,4)$ tal que $(a+b/2)(1,-1,4)$ y al final todo depende de un solo vector, de ahí obtenemos la recta. 

Entonces, observemos que es muy importante entender que cuando un conjunto de vectores genera un subespacio, en el pueden existir vectores "de más" que no son necesarios incluirlos en el conjunto de generadores. Desarrollaremos un método para deshacernos de estos vectores. 

> [!Proposición 1.14. El sist. de generadores es el subespacio más chico.]
> **(NEF)** Sea $V$ un $\mathbb{K}$-espacio vectorial. El subespacio generado por una lista de vectores $v_1, \dots, v_m$ en $V$ es el subespacio más chico de $V$ que contiene a todos los vectores de la lista.

**Demostración. (NEF)**[^1]  Supongamos $\{v_1, \dots, v_m\}$ es una lista de vectores en $V$. Sabemos que $<v_1, \dots, v_m>$ es un subespacio de $V$. Para cada $v_j \in \{v_1, \dots, v_m\}$, pertenece a $<v_1, \dots, v_m>$ pues en la combinación lineal $a_1v_1 + a_2v_2 + \cdots + a_mv_m$ eligiendo $a_j = 1$ y el resto igual a 0 se genera $v_j$. 
Luego, como todos los subespacios están cerrados en multiplicaciones por escales y sumas (por la proposición 1 en [[Subespacios]]), cada subespacio de $V$ que contiene a todos los $v_j$ a su vez contiene a $<v_1, \dots, v_m>$. Para entender mejor esto supongamos $S$ un subespacio de $V$ tal que $v_1, \dots, v_m \in S$, entonces $\sum_{i=1}^n \alpha_i v_i \in S, \; \forall \alpha_i \in \mathbb{K}$. Luego, $<v_1, \dots, v_n> \subseteq S$. 
En conclusión, $<v_1, \dots, v_m>$ es el subespacio más chico de $V$ que contiene todos los vectores de $v_1, \dots, v_m$. $\blacksquare$ 

> [!Corolario. 1.1.14]
> Sea $v_1, \dots, v_n, v_{n+1}$ una lista de vectores en $V$. Entonces $<v_1, \dots, v_n, v_{n+1}> = <v_1, \dots, v_n> \iff v_{n+1} \in <v_1, \dots,v_n>$.
   
Notemos como en la proposición anterior usamos el concepto de "lista" en vez de conjunto[^2], esto lo haremos muchas veces, por razones que exploraremos más en [[Bases Vectoriales]]. 
Lo primero que tenemos que notar es que existen [[Espacios Vectoriales]] que pueden ser **generados por vectores finitos**. Por ejemplo, se puede probar fácilmente que $\mathbb{K}^n$ es generado por $<(1,0, \dots, 0), (0,1,\dots, 0) \cdots, (0,0,\dots, 1)>$ que son $n$ vectores. Supongamos $(x_1, \dots, x_n) \in \mathbb{K}^n$. Luego, 
$$(x_1, \dots, x_n) = x_1(1,0,\dots, 0) + x_2(0,1,\dots, 0) + \cdots + x_n(0,\dots, 0,1)$$
Por lo tanto, $(x_1, \dots, x_n) \in <(1,0, \dots, 0), \cdots, (0, \dots, 0,1)>$ como se buscaba. 
Notemos que por la proposición 1 tenemos que entonces, $\mathbb{K}^n$ es el espacio vectorial más chico que contiene a todos esos vectores, lo cual quiere significar que si yo saco cualquiera de estos vectores, obtengo un subespacio menor. A partir de esto podemos definir

> [!Espacios Vectoriales de dimensión finita]
> #Definición Un espacio vectorial $(V, +, \cdot)$ se dice de **dimensión finita** si existe una lista de vectores que genere al espacio.

Tal que $\mathbb{K}^n$ sería un subespacio de _dimensión finita_. 
Notemos que si $\mathbb{K}_{\leq m}[x]$ es el conjunto de polinomios en $\mathbb{K}$ con grado menor o igual a $m$, este es un espacio de dimensión finita generado por $\{1, x, \dots, x^m\}$ que tiene $m$ vectores, lo cual resulta obvio pues un polinomio de grado menor o igual que $m$ se puede escribir como $a_0 + a_1x + \cdots + a_mx^m$.

Algo más interesante ocurre cuando analizamos directamente $\mathbb{K}[x]$ (es decir el conjunto de todos los polinomios). Resulta que no existe una lista de vectores finitos que generen a todo este espacio, y para probarlo supongamos por un momento que si existiera y $k$ sea el grado del polinomio más alto en la lista. Luego, todo polinomio en el conjunto tiene un grado menor o igual a $k$ por lo que está generado por $\{1, x, \dots, x^k\}$. Pero  $x^{k+1} \in \mathbb{K}[x]$ y no puede ser generado   por los vectores en la lista, entonces la lista no genera a $\mathbb{K}[x]$ llegamos a un absurdo. Por lo tanto, $\mathbb{K}[x]$ no tiene dimensión finita.

> [!Espacios vectoriales de dimensión infinita]
> #Definición Un espacio vectorial $(V, +, \cdot)$ es llamado de **dimensión infinita** si no es de dimensión finita.

Entonces, $\mathbb{K}[x]$ es de dimensión infinita.

## Independencia Lineal
Supongamos $v_1, \dots, v_m \in V$ y $v \in <v_1, \dots, v_m>$. Por la definición de sistema de generadores existen $\alpha_1, \alpha_2, \dots, \alpha_m \in \mathbb{K}$ tal que $v = \alpha_1v_1 + \cdots + \alpha_m v_m$ pero notemos que nada en la definición me asegura que los coeficientes sean únicos, es decir podrían existir otros $\beta_1, \beta_2, \dots, \beta_m \in \mathbb{K}$ tal que $v = \beta_1 v_1 + \cdots + \beta_m v_m$. 
Restando las dos ecuaciones planteadas tenemos que $v-v = 0 = (\alpha_1 - \beta_1)v_1 + \cdots + (\alpha_m - \beta_m)v_m$, entonces tenemos que $0$ es una combinación lineal de $v_1, \dots, v_m$. Si la única forma de hacer esto es de la forma obvio (igualando todos los coeficientes a 0) tenemos que cada $\alpha_j - \beta_j = 0 \rightarrow \alpha_j = \beta_j$, es decir los vectores de la lista escriben a cada vector en su subespacio con unos coeficientes **únicos**. Esta situación es tan importante que se le dio un nombre especial: independencia lineal. 

> [!Independencia Lineal]
> #Definición Un conjunto $\{v_1, \dots, v_n\} \subseteq V$. Se dice linealmente independiente (LI) si la única elección $a_1, \dots, a_m \in \mathbb{K}$ que hace $a_1v_1 + \cdots + a_mv_m$ igual a 0 es $a_1 = \cdots = a_m = 0$. 
> El conjunto vacío $\{\}$ es también considerado un conjunto linealmente independiente. 

Por otro lado podemos definir:

> [!Dependencia Lineal]
> #Definición Un conjunto $\{v_1, \dots, v_n\} \subseteq V$ se dice linealmente dependiente (LD) si existen $a_1, \dots, a_m \in \mathbb{K}$, no todos cero, tal que $a_1v_1 + \cdots + a_mv_m = 0$. 

Sería útil desarrollar un método para encontrar si una cierta cantidad de vectores es LI o LD. En $V = \mathbb{K}^n$ notemos que si tenemos una lista de $k$ vectores $v_1 = (a_{11}, a_{12}, \dots, a_{1n})$, $v_2 = (a_{21}, a_{22}, \dots, a_{2n})$, ... , $v_k = (a_{k1}, a_{k2}, \dots, a_{kn})$, como ya vimos en [[Operaciones con Matrices]] tenemos que los vectores en $\mathbb{K}^n$ se pueden expresar como una matriz de una columna en $M_{n \times 1}(\mathbb{K})$. Entonces queremos encontrar los valores de $\alpha_1, \alpha_2, \dots, \alpha_k \in \mathbb{K}$ tal que
$$\alpha_1 \cdot \begin{pmatrix} a_{11} \\ a_{12} \\ \vdots \\ a_{1n} \end{pmatrix} + \alpha_2 \cdot \begin{pmatrix} a_{21} \\ a_{22} \\ \vdots \\ a_{2n} \end{pmatrix} + \cdots + \alpha_k \cdot \begin{pmatrix} a_{k1} \\ a_{k2} \\ \vdots \\ a_{kn} \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ \vdots \\ 0 \end{pmatrix}$$
Notemos que por la definición de la multiplicación de matrices, es lo mismo expresar $A \cdot \vec{\alpha} = \vec{0}$ siendo $A = \begin{pmatrix} a_{11} & \cdots & a_{k1} \\ \vdots & \ddots & \vdots \\ a_{1n} & \cdots & a_{kn} \end{pmatrix}$ la matriz con los vectores como columnas y $\vec{\alpha} = (\alpha_1, \dots, \alpha_k)$  el vector de coeficientes que son nuestras incógnitas. Nos queda entonces que tenemos un sistema homogéneo, que puede tener una solución (mientras $A$ sea cuadrada) $(0,0, \dots, 0)$ la trivial y entonces es LI ó puede tener muchas soluciones y entonces el LD.

Finalmente, veamos que si tenemos un conjunto LD podemos llegar a un conjunto LI considerando que existen vectores que dependen linealmente de otros dentro del conjunto.

> [!Lema 2.15.]
> Supongamos $v_1, \dots, v_m$ es una lista linealmente dependiente de $V$ si y sólo si existe un $j \in \{1,2, \dots, m\}$ tal que los siguientes se cumplen:
> 1. $v_j \in <v_1, \dots, v_{j-1}>$
> 2. Si el elemento $j$-ésimo es removido de $v_1, \dots, v_m$ el subespacio generado por los vectores que quedan es igual a $<v_1, \dots, v_m>$. 

**Demostración.** ($\Rightarrow$) Como la lista es LD, existen $\alpha_1, \dots, \alpha_m \in \mathbb{K}$ tal, no todos cero, tal que $\alpha_1v_1 + \dots+ \alpha_mv_m$. Sea $j \in \{1, \dots, m\}$  tal que $a_j \neq 0$. Entonces, 
$$v_j = -\frac{a_1}{a_j}v_1 - \dots - \frac{a_{j-1}}{a_j}v_{j-1}$$
Luego, $v_j \in <v_1,\dots, v_{j-1}>$ probando (1).  Para probar (2), supongamos $u \in <v_1, \dots, v_m>$. Entonces, existen $\beta_1, \dots, \beta_m \in \mathbb{K}$ tal que $u = \beta_1 v_1 + \cdots + \beta_m v_m$.  En esta última ecuación podemos reemplazar $v_j$ por lo que obtuvimos en (1), lo cual nos muestra que $u$ esta en el subespacio generado por remover el $j$-ésimo término de $v_1,\dots, v_m$. 
($\Leftarrow$) Supongamos que $v_j \in <v_1, \dots, v_{j-1}>$ y el subespacio $<v_1, \dots, v_{j-1}, v_{j+1}, \dots, v_{m}> = <v_1, \dots, v_m>$ . Luego, tenemos que  $v_j \in <v_1, \dots, v_{j-1}, v_{j+1}, \dots, v_m>$ por lo tanto existen $\alpha_1, \dots, \alpha_{j-1}, \alpha_{j+1}, \dots, \alpha_m$ tal que 
$$\begin{align} v_j &= \alpha_1v_1 + \cdots \alpha_{j-1}v_{j-1} + \alpha_{j+1}v_{j+1} + \cdots + \alpha_mv_m \\
0 & = \alpha_1v_1 + \cdots \alpha_{j-1}v_{j-1} - v_j +\alpha_{j+1}v_{j+1} + \cdots + \alpha_mv_m\end{align} $$
Por lo que tengo una forma de escribir el vector $0$ usando escalares no nulos, entonces $v_1, \dots, v_m$ es LD. $\blacksquare$ 
  

[^1]: NEF: No Entra en el examen Final.
[^2]: Recordemos que una lista es un **conjunto ordenado**, es decir un conjunto en el que importa el orden de los elementos. 

# Bases Vectoriales
Ya exploramos los conceptos de [[Independencia Lineal]] y Sistemas de Generadores (visto en [[Sistemas de Ecuaciones Lineales]]). Ahora, juntemos estos dos conceptos.

> [!Bases Vectoriales]
> Una _base_ de un $\mathbb{K}$-espacio vectorial $V$ es un conjunto de vectores en $V$ que es linealmente independiente y genera a $V$. 

Sabemos que la lista $E = \{(1,0,\dots, 0), (0,1,\dots, 0), \dots, (0,0,\dots, 1)\}$ es un sistema de generadores de $\mathbb{K}^n$ y sabemos que es linealmente independiente pues al aplicar el método visto en [[Independencia Lineal]] de formar una matriz con los vectores como columnas, tenemos que las soluciones del sistema son $x_1 = 0, \dots, x_n = 0$. Luego, $E$ es una _base de_ $V$ y se llama la **base canónica estándar**.  
El siguiente teorema nos ayuda de forma rápida a descartar algunos casos de listas de vectores que no pueden ser bases pues no so LI:

> [!Proposición 1.16. Largo de una lista LI < Largo del conj de generadores]
> Sea $V$ un $\mathbb{K}$-espacio vectorial con dimensión finita, supongamos que $<v_1, \dots, v_r> = V$ y que $w_1, \dots, w_s \in V$ es una lista de vectores linealmente independientes. Entonces, $s \leq r$. 

Esta proposición nos dice que el largo de una lista de vectores LI es siempre menor o igual al largo de la lista de vectores que general el espacio. Si nos fijamos esto tiene sentido pues en la lista de vectores que generan al espacio puede ser LD y usando el Lema 2 (visto en [[Independencia Lineal]]) tenemos que  podemos ir quitando vectores, hasta tener un conjunto LI.

**Demostración.** Supongamos por el absurdo que $s > r$. Como $V = <v_1, \dots, v_r>$, para cada $1 \leq i \leq s$, y como la lista de vectores  $\{w_1, \cdots, w_s\} \subseteq V$ existen $\alpha_{ij} \in \mathbb{K}$ ($1 \leq j \leq r$) tales que $w_i = \alpha_{i1}v_1 + \dots + \alpha_{ir}v_r$. Entonces al escribir $\beta_1 w_1 + \dots + \beta_s w_s = 0$ para cualquier $\beta_1, \dots, \beta_m$ tenemos que $$\begin{align} \beta_1w_1 + \dots + \beta_m w_m & = \sum_{k=1}^s \beta_{k}w_{k}  \\ &= \sum_{k=1}^s \beta_{k}\Bigg( \sum_{i=1}^r \alpha_{ki} v_{i}\Bigg) \\ & = \sum_{k=1}^s \sum_{i=1}^r(\beta_k\alpha_{ki})v_i \\ & = \sum_{i=1}^r \Big(\sum_{k=1}^s \beta_{k}\alpha_{ki}\Big) v_i = 0\end{align} $$
Veamos ahora que si $\sum_{k=1}^s \beta_{k}\alpha_{ki} = 0$ entonces todo da 0. Pero notemos que hacer esta sumatoria es lo mismo que multiplicar las matrices 
$$\underset{\begin{matrix} w_1 & & w_2 & \quad \cdots \quad  & w_s  \end{matrix}}{\begin{pmatrix}\alpha_{11} & \alpha_{21} & \cdots & \alpha_{s1} \\
\alpha_{12} & \alpha_{22} & \cdots & \alpha_{s2} \\ \vdots & \vdots & \ddots & \vdots \\ \alpha_{1r} & \alpha_{2r} & \cdots & \alpha_{sr}\end{pmatrix}} \cdot \begin{pmatrix} \beta_{1} \\ \beta_2 \\ \vdots \\ \beta_s  \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ \vdots \\ 0\end{pmatrix}$$
y a su vez $\beta_1, \dots, \beta_m$ son nuestras "incógnitas" que queremos que sean 0, para que así el conjunto sea LI. Notemos que inicialmente suponemos que $s > r$ lo cual implicaría que hay más columnas que filas o (pasándolo a ecuaciones) más incógnitas que ecuaciones. Debido al Teorema 1 visto en [[Cantidad de soluciones de un SEL]] tenemos que existe una solución para las incógnitas $(\beta_1, \beta_2, \dots, \beta_s) \neq (0,0, \dots, 0)$ por lo tanto tenemos que la lista $w_1, \dots, w_s$ es LD lo cual es un absurdo. El absurdo vino de suponer que $s > r$. $\blacksquare$ 

Otra forma de demostrar esta proposición es considerando que si agregamos al conjunto de vectores que generan $V$ un vector del conjunto LI tenemos que $w_1, v_1, \dots, v_r$ es LD (porque $w_1$ pertenece a $V$ y se puede escribir como combinación lineal del resto). Como ahora esta lista es LD, por el Lema 2, podemos remover uno de los $v$'s tal que la nueva lista $B$ (de largo $r$), que consiste en $w_1$ y los restantes $v$'s, genera a $V$. Podemos repetir este proceso hasta que hayamos agregado todos los $w$'s y el proceso para. En cada paso en el que agregamos $v_i$ a $B$, el Lema 2 implica que hay algún $v$ que remover. Hay al menos tantos $v$'s como $w$'s.

De esta manera podemos probar que por ejemplo la lista $(1,2,3), (4,5,8), (9,6,7), (-3,2,8)$ no es linealmente independiente en $\mathbb{R}^3$ pues $(1,0,0), (0,1,0), (0,0,1)$ genera a $\mathbb{R}^3$ y tiene 3 vectores. Entonces, como la lista tiene 4 vectores por la proposición anterior debería tener menos de 3 para ser LI. 

> [!Corolario. (Prop. 1)]
> Sea $V$ un $\mathbb{K}$-espacio vectorial, y sean $B_1$ y $B_2$ dos bases de $V$. Si $B_1 = \{w_1, \dots, w_n\}$ y $B_2 = \{v_1, \dots, v_m\}$, entonces $n=m$. 

**Demostración.** Por el teorema anterior
- $B_1$ es un sistema de generadores de $V$ y $B_2$ es un conjunto LI $\implies n \geq m$.
- $B_2$ es un sistema de generadores de $V$ y $B_1$ es un conjunto LI $\implies m \geq n$.
Luego, $n =m$. $\blacksquare$

Las bases son muy útiles porque nos permiten escribir como un vector usando coeficientes **únicos**, esto es útil pues podemos expresar a los vectores de un espacio vectorial usando la menor cantidad de vectores posibles y de forma única.

Gracias a las bases ahora podemos definir mejor el concepto de dimensión:
> [!Dimensión]
> #Definición Si $V$ es un $\mathbb{K}$-espacio vectorial, $V \neq 0$. Y $B$ es una base de $V$ llamamos dimensión de $V$ a $|B|$. Y la denotamos $\dim V$.

Sabemos que por el corolario anterior, las bases siempre tienen el mismo número de elementos dentro de $V$, es por esto que la dimensión de $V$ está bien definida y es única para cada espacio vectorial.

El siguiente criterio prueba de que las bases son los únicas listas de vectores que me permiten describir a todo vector de un espacio vectorial $V$ como una combinación lineal con coeficientes únicos. 

> [!Proposición 2.17. (Criterio para la base)]
> Una lista de vectores en $V$ es una base de $V$ si y solo si cada $v \in V$ puede ser escrito de forma única en $v = a_1v_1 + \cdots + a_n v_n$ donde $a_1, \dots, a_n \in \mathbb{K}$.

**Demostración.** ($\Rightarrow$) Primero supongamos que $v_1,\dots, v_n$ es una base de $V$. Sea $v \in V$. Debido a que $v_1, \dots, v_n$ genera a $V$, existen $a_1, \dots, a_n \in \mathbb{K}$ tal que escriben como una combinación lineal a $v$. Para mostrar que son únicos, supongamos que $c_1, \dots, c_n$ son otros escalares tal que $v = c_1v_1 + \dots + c_n v_n$. Restando las dos ecuaciones tenemos que $0 = (a_1 - c_1)v_1 + \dots + (a_n - c_n)v_n$, esto implica que como los vectores de la lista son LI entonces $a_1 = c_1, \dots, a_n = c_n$.
($\Leftarrow$) Supongamos que $v \in V$ puede ser escrito de manera única como combinación lineal tal que $v = a_1v_1 + \dots + a_nv_n$. Claramente, esto implica que $<v_1, \dots, v_n> = V$. Para mostrar que la lista de vectores es LI, supongamos que $a_1, \dots, a_n \in \mathbb{K}$ tal que $0 = a_1v_1 + \dots + a_nv_n$, por hipótesis sabemos que los coeficientes son únicos por lo tanto $a_1 = \dots = a_n = 0$. Entonces, $v_1, \dots, v_n$ es linealmente independiente y es una base de $V$. $\blacksquare$ 

De esta manera, una forma clara obtener si una lista de vectores es una base, es igualando $a_1 v_1 + \dots + a_nv_n = 0$ ó expresándolo como $A\vec{x} = \vec{0}$ ($A$ es la matriz con los vectores como columnas y $\vec{x} = (a_1, \dots, a_n)$) y la solución de este sistema es única y  es la trivial, tenemos que las columnas son LI. Ya vimos que cuando el sistema tiene solución única en $A\vec{x} = \vec{b}$ entonces $A$ es invertible (como vimos en [[Matrices Invertibles]]) y la solución única es $\vec{x} = A^{-1}\vec{b}$ . Entonces, podemos probar fácilmente el siguiente corolario:

> [!Corolario. (prop 2.)]
> Si $A \in M_{n \times n}(\mathbb{K})$ invertible, entonces las columnas de $A$ son LI y forman una base de $\mathbb{K}^n$ 

Un sistema de generadores de un espacio vectorial puede no ser una base porque no es LI. La siguiente proposición dice que _cualquier sistema de generadores, puede ser reducida a un conjunto de vectores LI y que sigua generando a todo el espacio vectorial._

> [!Proposición 3.18. Sist. de generadores contiene una base]
> Sea $v_1, \dots, v_n$ un sistema de generadores de $V$. Entonces, existe un subconjunto $G \subseteq \{v_1, \dots, v_n\}$ que es una base de $V$. 

**Demostración.** Supongamos $v_1, \dots, v_n$ es un sistema de generadores de $V$. Si la lista es LI, entonces listo. Si es LD, queremos remover algunos de los vectores de $v_1, \dots, v_n$ tal que los que queden sean una base de $V$. Haremos esto usando un proceso descrito abajo.
Si $B$ es igual a la lista $v_1, \dots, v_n$.
- _Paso 1:_ Si $v_1 = 0$, eliminemos $v_1$ de $B$. Si $v_1 \neq 0$, deja a $B$ sin cambiar.
- _Paso $j$:_ Si $v_j$ esta en el subespacio $<v_1, \dots, v_{j-1}>$ (por el Lema 2 de [[Independencia Lineal]]), eliminemos $v_j$ de $B$ y nos queda $B_j$. Si $v_j$ no esta en $<v_1, \dots, v_{j-1}>$, deja $B$ sin cambiar. 
Paramos el proceso después del paso $n$, obteniendo la lista $B_n$. El proceso termina cuando ningún vector en $B_n$ es el conjunto de generadores de los previos. Entonces, $B_n$ es LI, por el Lema 2. Entonces $B$ es una base de $V$. $\blacksquare$ 

> [!Proposición 4.19. Una lista LI se puede expandir a una base]
> Sea $V$ un $\mathbb{K}$-espacio vectorial de dimensión finita y sea $w_1, \dots, w_r$ una lista linealmente independiente de $V$. Entonces existen elementos $w_{r+1}, \dots, w_{n} \in V$ tales que $w_1, \dots, w_r, w_{r+1}, \dots, w_n$ es una base de $V$. 

**Demostración.** Sea $B= z_1, \dots z_n$ una base de $V$. 
Consideremos $G_0 = <w_1, \dots, w_r>$ un subespacio de $V$. Veamos que podemos definir a un conjunto $G_1 = w_1, \dots, w_r, z_1$ como linealmente independiente si $z_1 \notin G_0$ ó de otra manera si $z_1 \in G_0$ entonces $G_1 = w_1, \dots, w_r$. Podemos repetir este proceso, creando $G_i = G_{i-1} \cup \{z_i\}$ si $z_i \notin G_{i-1}$ ó $G_i = G_{i-1}$ si $z_i \in G_{i-1}$ con cada $G_i, 1 \leq i \leq n$ linealmente independiente, hasta que lleguemos a $G_n$ que nos dice que $V = <z_1, \dots, z_n> \subseteq <G_n>$ y $G_n$ es linealmente independiente. Luego, $G_n$ es una base de $V$. $\blacksquare$ 

Notemos que en toda la nota usamos el concepto de lista en vez de conjuntos, aunque podríamos haberlo hecho, las proposiciones vistas funcionan de igual manera aunque conjuntos en vez de listas. 

Una de las propiedades más útiles de las bases en un espacio vectorial finito $V$ es que nos permiten introducir coordenadas en $V$ análogas a las "coordenadas naturales" de un vector $v = (x_1, x_2, \dots, x_n)$ en un espacio $\mathbb{K}^n$. Si $B = \{v_1, \dots, v_n\}$ es una base de $\mathbb{K}^n$ tenemos que existen únicos coeficientes $a_1, \dots, a_n$ tal que para todo $v  \in V, \; y = a_1v_1 + \dots + a_nv_n$, entonces podemos definir a los coeficientes como "las coordenadas del vector $v$ en la base $B$". Tal que $v = (x_1, x_2, \dots, x_n)$ es un vector en las coordenadas de la **base estándar o canónica**. Notemos que en estos casos, el orden en el que estén los vectores sí importa, pues por ejemplo si cambiamos de orden en la combinación lineal a $v_j$ por $v_j$ entonces tenemos el nuevo vector de coordenadas $(a_1, \dots, a_j, \dots, a_i, \dots, a_n) \neq (a_1, \dots, a_i, \dots, a_j, \dots, a_n)$. Es por esto que usamos listas en vez de conjuntos, pues al hablar de las coordenadas generadas por las bases el orden importa. 

Aquellas bases que se escriben como listas de vectores se las suele llamar **bases ordenadas**. 

# Dimensión de un espacio vectorial

La siguiente proposición trata sobre la dimensión, ya definida en [[Bases Vectoriales]], como el módulo del conjunto de vectores den la base del espacio vectorial, tenemos ahora una proposición que habla sobre la dimensión de los [[Subespacios]] de $V$.

> [!Proposición 1.20.] 
> Sean $S$ y $T$ subespacios de un $\mathbb{K}$-espacio vectorial ([[Espacios Vectoriales]]) $V$ de dimensión finita. Entonces: 
> 1. $S \subseteq T \implies \dim S \leq \dim T$
> 2. $S \subseteq T$ y $\dim S = \dim T \implies S = T$.

**Demostración.** 
1. Sea $\{s_1, \dots, s_r\}$ una base de $S$ , $\dim T = n$ y $\dim S = r$. Como $S \subseteq T$, tengo entonces que $\{s_1, \dots, s_r\} \subseteq T$, y es un conjunto LI. Luego, por la proposición 4 en [[Bases Vectoriales]], tenemos que la base de $S$ puede ser extendida a una base de $T$, y en consecuencia, $r \leq n$. 
2. Siguiendo el razonamiento de (1), al extender la base de $\{s_1,\dots, s_r\}$ como $n = r$ entonces no se agrega ningún vector y $S = <s_1, \dots, s_r> = T$. $\blacksquare$ 

El ítem (2) de la proposición anterior es muy útil para facilitar la verificación de la igual de dos subespacios. 
Por ejemplo, sean $S$ y $T$ dos subespacios de $\mathbb{R}^3$ definidos como $S = <(1,-k^2+1,2), (k+1, 1-k,-2)>$ y $T = \{x \in \mathbb{R}^3 : x_1+x_2+x_3\}$. Nos piden hallar los valores de $k$ para los cuales $S=T$. Probemos inicialmente que $S \subseteq T$ usando la proposición 1 de [[Independencia Lineal]], que nos dice que $S$ es el subespacio más chico que contiene a $(1,-k^2+1,2)$ y $(k+1,1-k,-2)$ entonces si $(1,-k^2+1,2) \in T$ y $(k+1,1-k,2) \in T$ se cumple $S \subset T$, notemos que esto ocurre cuento $k = \pm 2$. Luego, usando la proposición anterior para probar $S=T$ solo basta con ver $\dim S = \dim T$ lo cual se puede hacer simplemente reemplazando los posibles valores de $k$ obtenidos. Si $k = -2$ entonces $S = <(1,-3,2)>$, $\dim S =1$, y si $k = 2$ tenemos que $S = <(1,-3,2),(-1,3,-2)>$, $\dim S = 2$. Concluimos entonces que $S=T$ si y solo si $k=2$. 

Para probar que una lista de vectores en $V$ es una base en $V$, debe satisfacer ser LI y debe ser un sistema de generadores de $V$. La siguiente proposición demuestra que si la lista en cuestión tiene el largo correcto, entonces solo necesitamos chequear una de las 2 propiedades requeridas.

> [!Proposición 2.21.]
> Supongamos que $V$ es un $\mathbb{K}$-espacio vectorial de dimensión finita.
> 1. Toda lista de vectores LI en $V$ con un módulo $\dim V$ es una base de $V$.
> 2. Toda lista de vectores que es un sistema de generadores de $V$ con módulo $\dim V$ es una base de $V$. 

**Demostración.** (1) Supongamos $\dim V = n$ y $v_1,\dots, v_n$ es linealmente independiente en $V$. La lista $v_1, \dots, v_n$ puede ser extendida a una base de $V$ por la proposición 3 de [[Bases Vectoriales]]. Pero, cada base de $V$ tiene largo $n$, por lo tanto la extensión en este caso es la trivial, es decir no se agregan elementos a $v_1, \dots, v_n$. En otras palabras, $v_1, \dots, v_n$ es una base. 
(2) La lista de vectores $v_1, \dots, v_n$ que genera a $V$ puede ser reducida a una base por la proposición 4 de [[Bases Vectoriales]]. Pero por la misma razón que (1), no es necesario reducirla, por lo tanto $v_1, \dots, v_n$ es una base. $\blacksquare$ 

Un gran error que se suele cometer, es que como $\mathbb{R}^2$ tiene dimensión 2, se puede llegar a que $\mathbb{C}$ también tiene dimensión 2. Esto sería un error, que viene de que como conjuntos $\mathbb{R}^2$ puede ser identificado con $\mathbb{C}$. Sin embargo, _la dimensión de $\mathbb{C}$ es 1_. Por lo tanto, cuando hablamos de la dimensión de un espacio vectorial, la elección del cuerpo $\mathbb{K}$ no afecta a la dimensión. 

### Ejemplo. Bases de funciones polinómicas
Un ejemplo claro de una aplicación de la proposición 2 es probar que $1, (x-5)^2, (x-5)^3$ es una base del subespacio $U = \{p \in \mathbb{R}_3[x]: p'(5) = 0\}$ de $\mathbb{R}_3[x]$. Claramente cada uno de los polinomios $1 \in U$, $(x-5)^2 \in U$ y $(x-5)^3 \in U$, por lo que por la proposición 1 en [[Independencia Lineal]], tenemos que $<1, (x-5)^2, (x-5)^3> \subseteq U$. 
Luego, $a + b(x-5)^2 + c(x-5)^3 = 0$ para todo $x \in \mathbb{R}$. Es claro que sin necesidad de expandir el lado izquierdo de la ecuación que $a = b = c = 0$, entonces la lista de vectores es LI. 
Notemos que $\dim U \geq 3$  por la proposición (1.1). Como $U$ es un subespacio de $\mathbb{R}_3[x]$, tenemos que $\dim U \leq \dim \mathbb{R}_3[x] = 4$. No obstante no puede ocurrir que $\dim U = 4$ pues sino $U = \mathbb{R}_3[x]$ lo cual no es verdad pues por ejemplo $(x-5) \notin U$. Entonces $\dim U =3$ y esto implica que la lista LI $1, (x-5)^2, (x-5)^3$ es una base de $U$. 

## Aplicaciones de las bases y el concepto de dimensión
Se puede generalizar la dimensión del subespacio de soluciones de un sistema homogéneo, del trabajo que hicimos en [[Cantidad de soluciones de un SEL]]. 
> [!Teorema 3.22.]
> Dado un sistema de ecuaciones $A\vec{x} = \vec{0}$, $A \in M_{n \times n}(\mathbb{K})$ ([[Matrices]]) el subespacio $S \subseteq \mathbb{K}^n$ de soluciones tiene dimensión $n-r$ donde $r$ es la cantidad de pivotes de la matriz reducida.

**Demostración.** Se sigue de pensar que la matriz $A$ al reducirla por filas tenemos que puede tener filas nulas, lo cual nos daría un sistema equivalente con más incógnitas que ecuaciones y por el Teorema 1 visto en [[Cantidad de soluciones de un SEL]] existen soluciones no nulas. 
Ahora, las variables que tienen un pivote $1$ son las variables dependientes de otras, entonces si $r$ es la cantidad de pivotes que hay (hay $r$ variables dependientes) y hay $n$ incógnitas en total, tenemos entonces que hay $n-r$ variables independientes. Las variables independientes (o libres) al reordenarlas en vectores nos quedan $x_i(\times, \times,  \cdots, \times) + \cdots + x_j(\times, \times, \cdots, \times)$ tal que el conjunto de soluciones es generado por $n-r$ vectores. Luego, $\dim(S) = n-r$. $\blacksquare$

### Ejemplo. Bases Infinitas.
Resulta que nuestra definición de Base (vista en [[Bases Vectoriales]]) no especifica nada acerca de que solos los espacios vectoriales de dimensión finita pueden tener bases. 

Demos ahora un ejemplo de una base infinita. Sea $\mathbb{K}$ un subcuerpo de los número complejos [[C]], y sea $\mathbb{K}[x]$ el espacio de funciones polinomiales de $\mathbb{K}$ a $\mathbb{K}$. Ahora es obvio que si consideramos $f_k(x) = x^k, \; k = 0, 1, 2, \dots$ entonces veamos que el conjunto infinito $\{f_0, f_1, f_2, \dots\}$ es una base para $\mathbb{K}[x]$. Claramente el conjunto es un sistema de generadores de $V$. Para ver que el conjunto es LI lo más normal en estos casos es _probar que cada subconjunto finito es LI_. Es suficiente con probar que, para cada $n$, el conjunto $\{f_0, \dots, f_n\}$ es LI. Supongamos que 
$$c_0f_0 + \cdots + c_nf_n = 0$$
es lo mismo que $$c_0 + c_1x + \cdots + c_nx^n = 0$$
para todo $x \in \mathbb{K}$, en otras palabras, cada $x \in \mathbb{K}$ es una raíz del polinomio $f(x) = c_0 + c_1x + \dots + c_nx^n$. Por el [[Teorema Fundamental del Álgebra]] sabemos que un polinomio con grado $n$ (en los complejos) no puede tener más de $n$ raíces. Entonces, se sigue que $c_0 = c_1 = \dots = c_n = 0$. 


# Suma de subespacios
Ya probamos en [[Subespacios]], que la unión de subespacios no es un subespacio necesariamente. Sin embargo, sería muy útil tener una herramienta parecida a la unión que me permita combinar dos subespacios en uno. De esta manera podemos definir la suma de subespacios.

> [!Suma de subespacios]
> #Definición Supongamos $U_1, \dots, U_m$ son subespacios de $V$. La _suma_ de $U_1 + \cdots + U_m$, es el conjunto de todas las posibles sumas de elementos de $U_1, \dots, U_m$. Más precisamente, 
> $$U_1+ \cdots + U_m = \{u_1 + \cdots + u_m : u_1 \in U_1, \dots, u_m \in U_m\}$$ 

Un ejemplo de porque la suma de subespacios es útil, es por ejemplo si tenemos $V = \mathbb{K}^2$ y $U = \{(x,0) \in \mathbb{K}^2 : x \in \mathbb{K}\}$ que es el eje "x" en el sistema cartesiano y $W = \{(0,y) \in \mathbb{K}^2: y \in \mathbb{K}\}$ que es el eje "y". Entonces tenemos que $U + W = \{(x,0) + (y, 0) : x,y \in \mathbb{K}\} = \{(x,y): x,y \in \mathbb{K}\} = \mathbb{K}^2$. Podrá notar entonces, que si entendemos cada uno de los subespacios por separado, entonces podemos entender es espacio vectorial ([[Espacios Vectoriales]]) en su conjunto. 

> [!Lema 1.23. Suma de subespacios es el subespacio más chico conteniendo los subespacios]
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

> [!Teorema 2.24. Dimensión de la suma]
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

> [!Proposición 3.25. Condición para la suma directa]
> Sea $V$ un $\mathbb{K}$-espacio vectorial, $U$ y $W$ subespacios tal que $V = U \oplus W$. Entonces, para cada $v \in V$, $\exists ! u \in U, w \in W$ tal que $v = u+w$. 

**Demostración.** Como $V = U \oplus W$ en particular $v = u+w$ para cada $v \in V$. Entonces, veamos la unicidad. Supongamos que $v = u+w$, y $v= u'+w'$ entonces $u-u' = w-w'$ por consiguiente $u-u' \in U \cap W = \{0\}$ lo cual es un absurdo. $\blacksquare$ 

> [!Proposición 4.26. Bases de la suma directa]
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


# Transformaciones Lineales
Pasaremos a comprender el objeto de estudio más importante del **algebra lineal** que son las llamadas transformaciones lineales. Que consisten en simplemente, crear una función con [[Espacios Vectoriales]]. 

> [!Transformaciones Lineales]
> #Definición  Sean $(V, +_V, \cdot_V)$ y $(W, +_W, \cdot_W)$ dos $\mathbb{K}$-[[Espacios Vectoriales]]. Una función $f:V \rightarrow W$ se le llama transformación lineal (u homomorfismo o simplemente morfismo) de V en W si cumple:
> 1. $f(v +_V v') = f(v) + _W f(v')$ 
> 2. $f(\lambda \cdot_V v) = \lambda \cdot_W f(v), \;  \forall \lambda \in K, \forall v \in V$.

Notemos que el ejemplo más simple de transformación lineal es $0: V \rightarrow W$ o también llamada la transformación trivial, que consiste en tomar cualquier vector $v$ del espacio vectorial $V$ y multiplicarlo escalarmente por $0 \in \mathbb{K}$ lo cual nos da el $0_W$ (el cero del espacio vectorial $W$), $0(v) = 0_W$. Sabemos que esta es una transformación lineal porque cumple las dos propiedades: 
- $0(v +_V v') = 0_{\mathbb{K}} \cdot (v +_V v') = 0_{\mathbb{K}} \cdot v +   0_{\mathbb{K}} \cdot v' = 0(v) +_W 0(v')$
- $0(\lambda v) = 0_\mathbb{K} \cdot \lambda \cdot_V v = \lambda \cdot_V 0_\mathbb{K} \cdot v = \lambda \cdot_W 0(v)$  
Luego, está la transformación identidad $I: V \rightarrow V$ que es no hacerle ningún afecto al vector. Es decir $I(v) = v$. 

Si $T: \mathbb{R}^2 \rightarrow \mathbb{R}^2$ y la definimos como $T(x,y) = (1+x,y)$ no es una transformación lineal pues $T((x_1,y_1) + (x_2, y_2)) = T((x_1+x_2, y_1+y_2)) = (x_1+x_2+1, y_1+y_2)$ y que no es igual a $T(x_1, y_1) + T(x_2,y_2) = (x_1+1, y_1) + (x_2+1, y_2) = (x_1+x_2+2, y_1+y_2)$. En general, cuando estamos operando con espacios vectoriales $\mathbb{K}^n$, sumar constantes a las coordenadas ya evita que pueda ser una transformación lineal, al igual que multiplicar las coordenadas entre si como $T(x,y)=xy$ tampoco es una transformación lineal (TL). _Una forma fácil de comprobar que una función no es una transformación lineal es usando $T(0_V) = 0_W$_, en el ejemplo anterior $T(x, y) = (1+x, y)$ tenemos que $T(0,0) = (1,0) \neq (0,0)$.  

Otros ejemplos de transformaciones lineales pueden ser la diferenciación $D: \mathbb{K}[x] \rightarrow \mathbb{K}[x]$ siendo $\mathbb{K}$ un subcuerpo de los complejos, tal que $D(p) = p'$. Podemos probar que lo es pues $(f+g)' = f' + g'$ y $(\lambda f)' = \lambda f'$. También, la integración (con limites definidos), por ejemplo $T: \mathbb{K}[x] \rightarrow \mathbb{K}, \; T(p) = \int_0^1 p(x)dx$ es una transformación lineal pues $\int (f+g)(x) dx = \int f(x)dx + \int g(x)dx$ y $\int\lambda f(x)dx = \lambda \int f(x)dx$ por propiedades vistas en [[Una definición formal de Área]]. 

También, una transformación lineal muy importante es la de [[Matrices]]. Si $T: \mathbb{K}^n \rightarrow \mathbb{K}^m, T(v) = Av$ con $A \in M_{m \times n}(\mathbb{K})$ es una transformación lineal.  Y lo puede probar usted mismo, usando que la suma de matrices esta definida como $(A+B)_{ij} = (A)_{ij} + (B)_{ij}$, la multiplicación por escalar esta definida como $(\lambda   A)_{ij} = \lambda (A)_{ij}$. 

Las transformaciones lineales representan la **estructura de un espacio vectorial**. De hecho las tras propiedades que tienen que cumplir las TL son muy parecidas a las tres propiedades que tiene que cumplir un [[Subespacio Vectorial]]. De esta manera, podemos decir que estamos generando un subespacio en $W$ al agarrar todos los vectores de $V$ y "transformándolos". La siguiente proposición nos dice que podemos agarrar subespacios de un espacio $V$ y usar la transformación lineal para obtener subespacios de $W$ y viceversa.

> [!Proposición 1.26. las tl's mantienen los subespacios]
> Sea $f: V \rightarrow W$ una transformación lineal. Entonces,
> 1. Si $S$  es un subespacio de $V$, entonces $f(S)$ es un subespacio de $W$. 
> 2. Si $T$ es un subespacio de $W$, entonces $f^{-1}(W)$ es un subespacio de $V$.

**Demostración.** 
1. Sea $S \subseteq V$ un subespacio y consideremos $f(S) = \{w \in W / \exists s \in S, f(s) = w\}$. Probemos por la proposición 1 de [[Subespacios]] que es un subespacio de $W$.
		1. $0_W \in f(S)$, puesto que $f(0_V) = 0_W$ y $0_V \in S$. 
		2. Sean $w, w' \in f(S)$. Entonces existen $s, s' \in S$ tales que $f(s)= w$ y $f(s') = w'$ tal que $w+w' = f(s) + f(s') = f(s+s')$. Por lo tanto, $w+w' \in f(S)$.
		3. Sean $\lambda \in \mathbb{K}$ y $w \in f(S)$. Existe $s \in S$ tal que $w = f(s)$ luego $\lambda w = \lambda f(s) = f(\lambda s)$
2. Sea $T$ un subespacio de $W$ y consideremos $f^{-1}(T) = \{v \in V / f(v) \in T\}$. Probemos por la proposición 1 de [[Subespacios]] que es un subespacio de $V$. 
	1. $0_V \in f^{-1}(T)$ puesto que $f(0_V) = 0_W \in T$. 
	2. Sean $v,v' \in f^{-1}(T)$. Entonces $f(v)$, $f(v') \in T$ y, por lo tanto $f(v+v') = f(v) + f(v') \in T$. Luego $v+v' \in f^{-1}(T)$.
	3. Sean $\lambda \in \mathbb{K}$ y $v \in f^{-1}(T)$. Entonces $f(v) \in T$ por lo tanto $\lambda f(v) = f(\lambda v) \in T$. Luego $\lambda v \in f^{-1}(T)$. $\blacksquare$ 

Gracias a la definición de transformación lineal es obvio que estas son capaces de preservar combinaciones lineales de un espacio a otro. Es decir, teniendo una base de un subespacio $S \subset V$ que es $\beta = \{v_1, \dots, v_n\}$ nos permite escribir de manera **única** los vectores del subespacio como una comb. lineal por una proposición (Criterio de la Base) vista en [[Bases Vectoriales]], tal que si $v \in S$ entonces existen $a_i$'s únicos de manera que $v = \sum_{i=1}^n a_iv_i$. Luego, $f(v) = f\Big(\sum_{i=1}^n a_i v_i\Big) = \sum_{i=1}^n a_if(v_i)$  por la definición de TL. Por la proposición 1 tenemos que los $\{f(v_1), \dots, f(v_n)\}$ generan un subespacio en $W$. 
Esto es útil si nos dan una base de un espacio vectorial de salida $V$ y a donde se dirigen en la imagen de la función, se puede obtener una **transformación única** que cumpla esto. Las siguientes dos proposiciones demuestran lo dicho.

> [!Proposición 2.27. TL's y bases del dominio]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales, V de dimensión ﬁnita. Sea $B = v_1 , . . . , v_n$ una base ordenada de V y sean $w_1 , . . . , w_n \in W$ vectores arbitrarios. Entonces existe una única transformación lineal $T: V → W$ tal que $T (v_i) = w_i$ para cada $1 ≤ i ≤ n$.

**Demostración.** Primero probemos la existencia de la TL con la propiedad deseada. Definamos $T: V \rightarrow W$ por $T(c_1 v_1 + \cdots + c_nv_n) = c_1w_1 + \cdots + c_n w_n$ donde $c_1, \dots, c_n$ son elementos arbitrarios de $\mathbb{K}$. Como $\{v_1, \dots, v_n\}$ es una base de $V$, y cada elemento de $v \in V$ se puede escribir como una combinación lineal de estos, y $w_1, \dots, w_n \in W$ entonces la función esta bien definida. Veamos ahora que es una transformación lineal. Si $u,v \in V$ con $u = a_1v_1 + \dots + a_nv_n$ y $v= c_1v_1 + \dots +c_nv_n$. Entonces 
$$\begin{align} T(u+v) &= T((a_1+c_1)v_1 + \dots + (a_n+c_n)v_n) \\
&= (a_1+c_1)w_1 + \dots +(a_n+c_n)w_n \\
& = (a_1w_1 + \dots + a_n w_n) + (c_1v_1 + \dots +c_n v_n) \\
&= T(u) + T(v)
\end{align}$$
Probar que para un $\lambda \in \mathbb{K}$ y $v \in V$, $T(\lambda v) = \lambda T(v)$ es aún más sencillo.
Luego, la transformación lineal es **única** pues si $T(v_j) = w_j$ para todo $1 \leq j \leq n$. Sean $c_1, \dots, c_n \in \mathbb{K}$ fijos. La 2da propiedad de $T$ implica que $T(c_jv_j) = c_jw_j$ para todo $1 \leq j \leq n$. La 1era propiedad de $T$ implica $T(c_1 v_1 + \dots + c_n v_n) = c_1 w_1 + \dots + c_nw_n$. Como $\{v_1, \dots, v_n\}$ es una base en $V$ esto implica que existen coeficientes **únicos** $c_1, \dots, c_n \in \mathbb{K}$ para cada $v \in V$, esto significa que $T$ está únicamente determinada en $V$. $\blacksquare$ 

Se puede generalizar esta proposición para infinitos vectores que sean bases de un espacio vectorial $V$. Algo importante que nos dice esta proposición es que *nos basta con saber a donde van los elementos de una base de $V$ para definir una transformación lineal*.

## El conjunto de todas las TL
Fijados dos $\mathbb{K}$-espacios vectoriales $V$ y $W$, tiene sentido considerar el conjunto de todas las transformaciones lineales de $V$ en $W$. 

> [!Espacios vectoriales de Transformaciones Lineales]
> #Definición Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales. Definimos $$\text{Hom}_{\mathbb{K}}(V,W) = \{f: V \rightarrow W / f \text{ es una transformación lineal } \}$$
> Otra forma de escribirlo es $\mathcal{L}(V,W)$.

>[!Adición y multiplicación escalar en el conjunto de todas las TL]
>Dadas $f,g \in \mathrm{Hom}(V,W)$ se define $f+g$ como $(f+g)(x) = f(x) + g(x)$ , $\forall x \in V$. Y el producto $\lambda f$ como $(\lambda f)(x) = \lambda f(x)$. 

Se puede probar que $f+g$ y $\lambda f$ son efectivamente transformaciones lineales y pertenecen a $\mathrm{Hom}(V,W)$. Luego, **se puede probar que $\mathrm{Hom}(V,W)$ es un espacio vectorial.**



# La Imagen y el Núcleo de una TL
Como las transformaciones lineales son operaciones entre conjuntos tiene sentido estudiar la validez de las propiedades usuales: inyectividad, suryectividad y biyectividad. 

> [!Tipos de Transformaciones Lineales]
> #Definición Sean $V$ y $W$ dos $\mathbb{K}$ [[Espacios Vectoriales]] y sea $T:V \rightarrow W$ una TL. Se dice que:
> 1. $T$ es un **monomorfismo** si $T$ es inyectiva.
> 2. $T$ es un **epimorfismo** si $T$ es suryectiva.
> 3. $T$ es un **isomorfismo** si $T$ es biyectiva.}
> 
>  #Definición Sea $V$ un $\mathbb{K}$ espacio vectorial y sea $T:V \rightarrow V$ una TL, se llama **endomorfismo** y si además es un isomorfismo se le dice **automorfismo**.

Una observación que podemos observar de la proposición 1 de [[Transformaciones Lineales]] es que como $\{0\} \subset W$ y es subespacio vectorial de este, entonces $f^{-1}({0})$ también debe ser un subespacio a este lo llamamos núcleo.

> [!Núcleo de una transformación lineal]
> #Definición Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales, y sea $T: V \rightarrow W$ una TL. Se llama núcleo de $T$ al conjunto $\mathrm{Nu}(T)= \{v \in V : T(v)=0\} = f^{-1}({0_W})$  

El núcleo se puede usar para determinar si tenemos un **monomorfismo** o no pues si existen otros valores que nos den $0_W$ además de $f(0_V) = 0_W$ entonces no va ser un monomorfismo. 

> [!Proposición 1.28. inyectividad (mono) es equivalente al núcleo igual a 0]
> Sea $T: V \rightarrow W$ una TL. Entonces, $T$ es un **monoformismo** si y solo si $\mathrm{Nu}(T) = \{0\}$. 

**Demostración.** ($\Rightarrow$) Primero supongamos que $T$ es un monomorfismo.  Queremos probar que $\mathrm{Nu}(T) = \{0\}$. Ya sabemos que $\{0\} \subseteq \mathrm{Nu}(T)$. Para ver la inclusión en la otra dirección, supongamos $v \in \mathrm{Nu}(T)$. Entonces, $T(v) = 0 = T(0)$ pues $T$ es inyectiva ( o monomorfismo). 
($\Leftarrow$) Supongamos que $\mathrm{Nu}(T) = \{0\}$ entonces para probar que es inyectiva veamos que dados $v,w \in V$ entonces $T(v) = T(w) \rightarrow T(v) - T(w) = 0$ lo que nos dice que $v-w \in \mathrm{Nu}(T)$, usando la definición de las TL tenemos $T(v-w) = T(0) \rightarrow v-w = 0 \rightarrow v=w$. $\blacksquare$ 

Otro conjunto importante que es interesante analizar es la **imagen de $f$** que se define como 
> [!Imagen de una TL.]
> Sea $f:V \rightarrow W$ una transformación lineal. Entoncesn definimos $\mathrm{Im}(f) = \{ w \in W : \exists v \in V, f(v) = w\}$ como la _Imagen de $f$_.

que de la proposición 1  vista en [[Transformaciones Lineales]] sabemos que también es un subespacio. 
Como podemos definir una transformación única teniendo elementos de una base de $V$ (por lo que vimos en la proposición 2 de [[Transformaciones Lineales]]). Resulta que no es difícil de deducir que los vectores a los que se dirigen los elementos de la base ordenada $T(a_1v_1 + \dots + a_nv_n) = a_1w_1 + \dots + a_n w_n$ forman una lista de vectores que generan la imagen de $T$. La siguiente proposición demuestra que las TL's mantienen las combinaciones lineales:

> [!Proposición 2.29.]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales y sea $T: V \rightarrow W$ una transformación lineal. Entonces, si $v_1, \dots, v_n$ es un sistema de generadores de $V$, $T(v_1), \dots, T(v_n)$ es un sistema de generadores de $Im(T)$.

**Demostración.** Por definición, $\mathrm{Im}(T) = \{T(v): v \in V\}$. Si $v_1, \dots, v_n$ una lista de vectores que son un sistema de generadores de $V$, existen $a_1, \dots, a_n \in \mathbb{K}$ tales que $v = a_1v_1 + \dots + a_nv_n$. Luego $T(v) = a_1T(v_1) + \dots + a_nT(v_n)$ por lo tanto $T(v) \in <T(v_1), \dots, T(v_n)>$. Esto prueba $\mathrm{Im}(T) \subseteq <f(v_1), \dots, f(v_n)>$, es claro que la vuelta vale también pues  $T(v_i) \in \mathrm{Im}(T)$. Entonces, $\mathrm{Im}(T) = <f(v_1), \dots, f(v_n)>$. $\blacksquare$ 

Supongamos que tenemos la TL; $f: \mathbb{R}^3 \rightarrow \mathbb{R}^3$ tal que $(x,y,z) \mapsto (x-y, -x+y, 2x-2y+z)$. Podemos encontrar un sistema de generadores de la imagen (por la proposición anterior), reemplazando por un sistema de generadores de $V$ (usemos la base canónica): $f(1,0,0) = (1,-1,2)$, $f(0,1,0)= (-1,1,2)$ y $f(0,0,1) = (0,0,1)$. Si usted comprueba usando los métodos vistos en [[Bases Vectoriales]], verá que los vectores son LD, si luego quitamos uno nos queda una base de la imagen $\mathrm{Im}(f) = < (1,-1,2), (0,0,1) >$ . Observemos que a pasar de que agarramos a una base, esta nos llevó a un sistema de generadores que era linealmente dependiente ([[Independencia Lineal]]).

Como consecuencia de esta proposición tenemos que si tenemos una base de $V$ y la mandamos a la función vamos a tener un sistema de generadores de vectores que pueden (o no) ser **linealmente Dependientes**, las transformaciones lineales no mantienen la independencia lineal. De esta manera, como existe la posibilidad de que sean LD, entonces una base de la imagen puede tener la misma dimensión o menor a la del conjunto de salida $V$.

> [!Corolario 2.1.29.]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales y sea $T: V \rightarrow W$ una transformación lineal. Si $V$ es de dimensión finita, entonces $Im(T)$ también lo es y se tiene que $\mathrm{dim(Im}(T)) \leq \dim(V)$.

También se puede deducir que 

> [!Corolario 2.2.29.]
> Si $T:V \rightarrow W$ es un epimorfismo, y $v_1, \dots, v_n$ es un sistema de generadores de $V$, entonces $T(v_1), \dots, T(v_n)$ es un sistema de generadores de $W$.

El ejemplo anterior muestra claramente un ejemplo de estos corolarios, $T$ no mantiene independencia lineal porque $\mathrm{dim(Im}(f)) = 2 \leq \mathrm{dim}(V) = 3$, es decir muestra que **una base de $V$ no nos lleva a una base de $\mathrm{Im}(f)$ sino a un sistema de generadores que puede o no ser LI**. 
Resulta, que para que se mantenga la independencia lineal es necesario que $T$ sea un **monomorfismo** (inyectiva), lo cual tiene sentido porque si no lo fuera $\{v\} \subset V$ es un conjunto LI y $\{f(v)\} = \{0\} \subset W$ no lo es (el vector nulo siempre es linealmente dependiente). 

> [!Proposición 3.30.]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales y sea $T: V \rightarrow W$ un monomorfismo. Entonces, si $v_1, \dots, v_n$ es una lista de vectores LI de $V$, $T(v_1), \dots, T(v_n)$ también es LI.

**Demostración.** Queremos ver que dado $v_1, \dots, v_n$ es LI, entonces para la combinación lineal $a_1T(v_1) + \dots + a_nT(v_n) = 0$ es solo posible si $a_1= \dots = a_n = 0$. Notemos que $T(a_1v_1) + \dots + T(a_nv_n) = 0 \rightarrow T(a_1v_1 + \dots + a_nv_n) = 0$ por definición de las TL. Luego, como sabemos por hipótesis $T$ es un monomorfismo, por la proposición 1 tenemos que $a_1v_1 + \dots + a_nv_n = 0$ y entonces $a_1 = \dots = a_n = 0$. $\blacksquare$ 

Como consecuencia

> [!Corolario 3.1.30.]
> Sea $T: V \rightarrow W$ un monomorfismo y $B = v_1, \dots, v_n$ una base ordenada de $V$, entonces $B_T = T(v_1), \dots, T(v_n)$ es una base ordenada de $\mathrm{Im}(T)$. En particular, $\dim(\mathrm{Im}(T)) = \dim V$.

Como un isomorfismo es a la vez un monomorfismo y un epimorfismo (que significa que $\dim W = \dim (\mathrm{Im}(T))$) entonces se deduce:

> [!Corolario 3.2.30.]
> Sea $T: V \rightarrow W$ un isomorfismo. Entonces, para toda base $B$ de $V$, $f(B)$ es una base de $W$. En particular, $\dim V = \dim W$.

Las proposiciones 1, 2 y 3 se pueden generalizar para espacios vectoriales de dimensión infinita considerando al sistema de generadores como $\{v_i: i \in I\}$, siendo $I$ el conjunto de índices. 

## Composición de Transformaciones Lineales
Se puede demostrar que la composición de transformaciones lineales es una transformación lineal:
> [!Proposición 4.31. Composición de Tl's]
> Sean $V, W$ y $Z K$-espacios vectoriales. Sean $f: V \rightarrow W y g: W \rightarrow Z$ trungformtaciones lineales. Fintonces $g \circ f: V \rightarrow Z$ es una transformación linat.

**Demostración.** Sean $v, v^{\prime} \in V$. Entonces
$$
\begin{align} g \circ f\left(v+v^{\prime}\right)=g\left(f\left(v+v^{\prime}\right)\right)=g\left(f(v)+f\left(v^{\prime}\right)\right)& =g(f(v))+g\left(f\left(v^{\prime}\right)\right) \\ &=g \circ f(v)+g \circ f\left(v^{\prime}\right) \end{align}
$$
Análogamente, si $\lambda \in K$ y $v \in V$, se tiene que
$$
g \circ f(\lambda \cdot v)=g(f(\lambda \cdot v))=g(\lambda \cdot f(v))=\lambda \cdot g(f(v))=\lambda \cdot(g \circ f(v)) . \quad \blacksquare
$$
Finalmente, analizamos las propiedades de la función inversa de una transformación lineal biyectiva (es decir, un isomorfismo).

> [!Proposición 5.32. La tl inversa]
>  Sean $V$ y W dos $\mathbb{K}$-espacios vectoriales y sea $f: V \rightarrow W$ una transformación lineal. Si $f$ es un isomorfismo, entonces $f^{-1}: W \rightarrow V$ es una transformación lineal (que resulta ser un isomorfismo).

**Demostración.** Sean $w, w^{\prime} \in W$. Como $f$ es un isomorfismo, existen únicos $v ; v^{\prime} \in V$ tales que $w=f(v)$  y $w^{\prime}=f\left(v'\right)$. Entonces:
$$
f^{-1}\left(w+w^{\prime}\right)=f^{-1}\left(f(v)+f\left(v^{\prime}\right)\right)=f^{-1}\left(f\left(v+v^{\prime}\right)\right)=v+v^{\prime}=f^{-1}(w)+f^{-1}\left(w^{\prime}\right) .
$$
Dadas $w \in W$ y  $\lambda \in \mathbb{K}$, existe un único $v \in V$ tal que $w=f(v)$. Entonces
$$
f^{-1}(\lambda \cdot w)=f^{-1}(\lambda \cdot f(v))=f^{-1}(f(\lambda \cdot v))=\lambda \cdot v=\lambda \cdot\left(f^{-1}(w)\right) .
$$
Luego. $f^{-1}$ es una transformación lineal. Es claro que es biyectiva. $\blacksquare$ 

# Teorema de la dimensión
Ya entendimos bastante respecto a las [[Transformaciones Lineales]] en relación con dos subespacios muy importantes que son [[La Imagen y el Núcleo de una TL]]. Aprendimos que cuando $\mathrm{Nu}(T) = \{0\}$ la transformación es un monomorfismo (es decir, inyectiva). 

Notemos que realizando un análisis de la dimensión de los subespacios núcleo, imagen y el espacio de salida $V$, podemos entender bastante sobre la transformación. En el corolario 2.1 de [[La Imagen y el Núcleo de una TL]] concluimos que $\dim V \geq \dim (\mathrm{Im}(T))$, pero luego en el corolario 3.1 concluimos que cuando $T$ es un monomorfismo tenemos que $\dim V = \dim (\mathrm{Im}(T))$. Por lo tanto, tenemos que la dimensión de la imagen y el espacio de salida son iguales cuando $\mathrm{Nu}(T) = \{0\}$ pero a su vez esto quiere significar que la dimensión del núcleo es 0. Mientras que generalmente cuando la dimensión del núcleo puede ser más grande tenemos que $\dim V \geq \dim (\mathrm{Im}(T))$. Puede usted mismo notar que la dimensión de estos tres espacios se encuentran relacionadas entre sí, y encontrar esa relación nos puede llevar a obtener resultados muy interesantes. 

Ahora estamos listos para demostrar el teorema de la dimensión.

> [!Teorema de la dimensión. 1.33.]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales, $V$ de dimensión finita, y sea $T: V \rightarrow W$ una transformación lineal. Entonces,
> $$\dim V = \dim(\mathrm{Nu}(T)) + \dim(\mathrm{Im}(T))$$

**Demostración.** Sean $n = \dim V$ y $r = \dim (\mathrm{Nu}(T))$. Si $r=n$, entonces $T \equiv 0$ pues $\dim(\mathrm{Im}(T)) = 0$. Si $r=0$, entonces $T$ es un monomofismo y ya probamos que en este caso $\dim(Im(T)) = n = \dim V$ y el teorema vale. 
Supongamos ahora que $0 < r < n$. Sea $\{v_1, \dots, v_n\}$ una base de $\mathrm{Nu}(T)$, como el núcleo es un subespacio de $V$, entonces $\{v_1, \dots, v_n\}$ es LI en $V$ y se puede extender a una base por la proposición 4 en [[Bases Vectoriales]]. Sean $v_{r+1}, \dots, v_n$ en $V$ tales que $\{v_1, \dots, v_r, v_{r+1}, \dots, v_n\}$ es una base de $V$, se tiene que por la proposición 2 en [[La Imagen y el Núcleo de una TL]]: 
$$\mathrm{Im}(T) = < T(v_1), \dots, T(v_r), T(v_{r+1}), \dots, T(v_{n})>$$
y como $T(v_i) = 0, \; 1 \leq i \leq r$ tenemos que $\mathrm{Im}(T) = <T(v_{r+1}), \dots, T(v_n)>$. Nos faltaría ver que el sistema de generadores de la imagen planteado, es linealmente independiente. 
Sean $\alpha_{r+1}, \dots, \alpha_n \in \mathbb{K}$ tales que $\sum_{i=r+1}^n \alpha_i T(v_i)= 0$. Entonces, $T\Big(\sum_{i={r+1}}^n \alpha_iv_i\Big) = 0$ por la 2da propiedad de las [[Transformaciones Lineales]]. Luego, $\sum_{i=r+1}^n \alpha_iv_i \in \mathrm{Nu}(T)$. Y como $\{v_1, \dots, v_r\}$ es una base del núcleo tenemos que 
$$\sum_{i= r+1}^n \alpha_i v_i = \sum_{i=1}^r \alpha_i v_i \iff \sum_{i= r+1}^n (-\alpha_i) v_i + \sum_{i=1}^r \alpha_i v_i = 0$$
Como $\{v_{r+1}, \dots, v_n\}$ es un conjunto LI en $V$ y $\{v_1, \dots, v_r\}$ también lo es tenemos que $\{v_1, \dots, v_n\}$ es LI, por lo tanto $\alpha_i = 0$ para cada $1 \leq i \leq n$. Luego, $\{T(v_{r+1}), \dots, T(v_n)\}$ es LI. Entonces, tenemos que $\mathrm{Im}(T) =n - r = \dim V - \dim (\mathrm{Nu}(T))$. $\blacksquare$ 

Usando este teorema se puede concluir que cuando una transformación lineal es un monomorfismo es un epimormismo y a su vez es un isomorfismo.

> [!Corolario 1.1.33.]
> Sean $V$ y $W$ dos $\mathbb{K}$ espacios vectoriales de dimensión $n$, y $T: V \rightarrow W$ una transformación lineal. Son equivalentes:
> 1. $T$ es un monomorfismo.
> 2. $T$ es un epimorfismo.
> 3. $T$ es un isomorfismo.

Notemos que el teorema solo vale para transformaciones lineales de dimensión finita. No funciona para espacios vectoriales infinitos. Por ejemplo $T: \mathbb{K}[x] \rightarrow \mathbb{K}[x], \; T(P) = P'$ es un epimorfismo pues si $Q = \sum_{i=0}^n a_ix^i \in \mathbb{K}[x]$ entonces $T\Big(\sum_{i=1}^{n+1} \frac{a_i}{i} x^i\Big) = Q$, pero no es un monomorfismo pues los vectores contantes se dirigen todos al $0$ por lo tanto la dimensión del núcleo es 1.

A partir del Teorema de la dimensión se puede demostrar:

> [!Proposición 2.34.]
> **(NEF)** Sean $V$ y $W$ son dos $\mathbb{K}$-espacios vectoriales finitos, tenemos que:
> 1. Si $\dim V > \dim W$ no existe transformación lineal tal que vaya de $V$ a $W$ que sea un monomorfismo.
> 2. Si $\dim V < \dim W$ no existe una transformación lineal tal que vaya de $V$ a $W$ que sea un epimorfismo. 

**Demostración.** Sea $T : V \rightarrow W$ una transformación lineal.
1. Como, $\dim(\mathrm{Nu}(T)) = \dim V - \dim (\mathrm{Im}(T)) \geq \dim V - \dim W > 0$. Entonces no puede ser inyectiva (monomorfismo), a su vez esto quiere significar, que por el corolario 2.1, no puede existir un ismorfismo.
2.  Como, $\dim (\mathrm{Im}(T)) = \dim V - \dim (\mathrm{Nu}(T)) \leq \dim V < \dim W$. Entonces como $\dim (\mathrm{Im}(T)) < \dim W$ esto significa que no puede ser sobreyectiva (epimorfismo), a su vez esto quiere significar por el corolario 2.1 que no puede existir un isomorfismo. $\blacksquare$ 

Esta proposición nos da mucha información útil, con simplemente analizar la dimensión de los espacios vectoriales de salida y de llegada, ya podemos encontrar si _puede existir o no un isomorfismo_, sin embargo que $\dim V = \dim W$ **no me indica necesariamente que la transformación sea un isomorfismo**. Por ejemplo, $T(x,y,z) = (x,y,0)$ no es un isomorfismo a pesar de que la dimensión del conjunto de llegada sea el mismo que el de salida.  

Usando transformaciones lineales, se puede expresar de una nueva manera la demostración del teorema 1 en [[Cantidad de soluciones de un SEL]]. Supongamos que $a_{ij} \in \mathbb{K}$ para $i = 1, \dots, m$ y $j = 1, \dots, n$. Consideremos el siguiente sistema homogéneo de $m$ ecuaciones y $n$ incógnitas:
$$\sum_{i=1}^n a_{1i}x_i = 0 \quad \cdots \quad \sum_{i=1}^n a_{mi}x_i = 0$$ Podemos definir $T : \mathbb{K}^n \rightarrow \mathbb{K}^m, \; T(x_1, \dots, x_n) = \Big(\sum_{i=1}^n a_{1i}x_i, \dots, \sum_{i=1}^n a_{mi}x_i\Big)$ como una transformación lineal (se puede probar que lo es muy fácilmente). Queremos saber cuando el sistema tiene más de una solución que no sea la trivial, es decir todas las soluciones tales que $T(x_1, \dots, x_n) = (0,0, \dots, 0)$. O sea queremos encontrar el núcleo de la transformación cuando $\mathrm{Nu}(T) \neq \{0\}$, pero esto a su vez quiere significar que la función no es inyectiva. Por lo tanto, por la proposición 2 $n > m$ (hay más incógnitas que ecuaciones). De esta manera, demostrarmos el teorema 1 usando transformaciones lineales.
También podemos probar que para un sistema no homogéneo pueden no existir soluciones cuando tenemos más incógnitas que ecuaciones, pues esto significaría que podemos armar una transformación lineal $\mathbb{K}^n \rightarrow \mathbb{K}^m$ no es suryectiva (epimorfismo) cuando $n < m$. 

Muchos de los teoremas que vimos anteriormente se pueden demostrar usando transformaciones lineales. 

## Proyectores
Un tipo de transformaciones lineales muy interesantes son los **proyectores**, se utilizan en múltiples ocasiones. 

> [!Proyectores]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial. Una transformación lineal $\mathrm{P} : V \rightarrow V$ si $P \circ P = P$, es decir son aquellas TL's tales que si las aplico dos veces sobre sí misma dan el mismo resultado que si las hubiera aplicado una vez.

La definición de proyector formaliza y generaliza la idea de una _"proyección gráfica"_. Es decir, en ciertas ocasiones, es necesario obtener que tanto de un vector esta paralelo a una línea o un plano. Por ejemplo en física, para obtener que tanto de una velocidad esta "tangencial" a la trayectoria de una partícula. La siguiente imagen muestra una forma de aplicar una proyección sobre una línea:
![[Pasted image 20230116174446.png| 200]]
Es claro que está función es una transformación lineal y se entiende de donde viene la definición de proyección que dice que todo elemento en la imagen, al aplicar $P$ otra vez obtenemos el mismo vector, pues la proyección gráfica de un vector que esta sobre la línea es sí mismo. 

> [!Proposición 3.35.]
> Sea $V$ un $K$-espacio vectorial, y sea $P: V \rightarrow V$ una transformación lineal. Entonces $P$ es un proyector si y sólo si $P(v)=v$ para cada $v \in \operatorname{Im}(P)$.

**Demostración.** $(\Rightarrow)$ Supongamos que $P$ un proyector. Sea $x \in \operatorname{Im}(f)$. Entonces existe $v \in V$ tal que $x=P(v)$. Luego, $P(x)=P(P(v))=P \circ P(v)=P(x)=x$.
($\Leftarrow$) Sea $v \in V$. Entonces $P(v) \in \mathrm{Im} (f)$ y por hipótesis, $P(P(v))=P(v)$, es decir, $P \circ P(v)=$ $P(v)$. Como esto vale para cada $v \in V$, resulta que $P \circ P=P$. $\blacksquare$

Un ejemplo claro de un proyector es por ejemplo $P: \mathbb{R}^3 \rightarrow \mathbb{R}^3, \;P(x,y,z) = (x,y,0)$ que "aplasta" o "proyecta" todos los vectores del espacio de 3D en el plano $xy$. 
![[Pasted image 20230116181504.png| 250]]
Notemos que el núcleo de esta transformación es $\mathrm{Nu}(P) = <(0,0,1)>$, es decir el eje $z$, y la imagen de la transformación es $\mathrm{Im}(P) = <(1,0,0), (0,1,0)>$, que es todo el plano $xy$. Entonces, se puede probar que usando la suma directa vista en [[Suma de subespacios]]:  

> [!Proposición 4.36.]
> Sea $V$ un $K$-espacio vectorial y sea $P: V \rightarrow V$ un proyector. Entonces $\mathrm{Nu}(P) \oplus \operatorname{Im}(P)=V$.

**Demostración.** En primer lugar, veamos que $\operatorname{Nu}(P) \cap \operatorname{Im}(P)=\{0\}$. Sea $x \in \operatorname{Nu}(P) \cap \operatorname{Im}(P)$. Como $x \in \operatorname{Im}(P)$, por la proposición anterior, $P(x)=x$. Pero $x \in \mathrm{Nu}(P)$, de donde $P(x)=0$. Luego, $x=0$.
Veamos ahora que $\operatorname{Nu}(P) + \operatorname{Im}(P)=V$. Sea $x \in V$. Entonces $x = (x - P(x)) - P(x)$ y se tiene que $P(x-P(x))=P(x)- P\circ P(x)=P(x)-P(x)=0$, con lo que $x-P(x) \in \operatorname{Nu}(P)$ y $P(x) \in \operatorname{Im}(f)$. $\blacksquare$ 

Luego, se puede pensar de manera inversa. Si yo tengo dos subespacios $U$ y $W$ de $V$ tal que uno es complemento del otro, es decir $U \oplus W = V$, entonces yo puedo encontrar un proyector tal que $\mathrm{Nu}(P) = U$ y $\mathrm{Im}(P) = W$, y es más resulta que este proyector es **único**.

>[!Proposición 5.37.]
>Sea un $K$-espacio vectorial, y sean $U$ y $W$ subespacios de $V$ tales que. $U \oplus W=V$. Entonces exisle un único proyector $P: V \rightarrow V$ tal que $\operatorname{Nu}(f)=U, \operatorname{Im}(f)=W$.

**Demostración.** Como $V=U \oplus W$, para cada $v \in V$, existen únicos $u \in U$ y $w \in W$ tales que $v=u+w$ (por la proposición 3 en [[Suma de subespacios]]). Entonces, si $P: V \rightarrow V$ es un proyector tal que $\mathrm{Nu}(P)=U, \operatorname{Im}(P)=W$, se tiene que $P(v)=P(v+w)=P(u)+P(w)=0+w=w$, donde la penúltima igualdad es consecuencia de que $P$ es un proyector y $w \in \operatorname{Im}(P)$ (ver Proposición 5).
Consideremos entonces la función $P: V \rightarrow V$ definida por
$$
P(v)=w \quad \text { si } v=u+w \text { con } u \in U, w \in W
$$
Observamos que $P$ es una transformación lineal:
- Si $v, v^{\prime} \in V$ tales que $v=u+w, v^{\prime}=u^{\prime}+w^{\prime}$, con $u, u^{\prime} \in U$ y $w, w^{\prime} \in W$, entonces $v+v^{\prime}=\left(u+u^{\prime}\right)+\left(w+w^{\prime}\right)$ con $u+u^{\prime} \in U$ y $w+w^{\prime} \in W$ (puesto que $U$ y $W$ son subespacios de $V$) por lo tanto, $P\left(v+v^{\prime}\right)=w+w^{\prime}=P(v)+P\left(v^{\prime}\right)$
- Si $\lambda \in \mathbb{K}$ y $v \in V, v=u+w$ con $u \in U, w \in W$, entonces $\lambda v=(\lambda  u)+(\lambda w)$ con $\lambda . u \in U$, $\lambda . w \in W$. Luego, $P(\lambda, v)=\lambda v=\lambda . P(v)$.
Además, $P$ es un proyector: pues si $v \in V$ y $v = u+w$, entonces $P(P(v)) = P(P(u)+P(w)) = P(0 + w) = P(w) = w = P(v)$. Es claro que $\mathrm{Im}(P) = W$ pero comprobemos $\mathrm{Nu}(P) = U$, si $v = u+w$ con $u \in U$ entonces $P(v) = P(u) + P(w) = 0 + w$ tal que $P(u) = 0$ por lo tanto $u \in \mathrm{Nu}(P)$.  $\blacksquare$ 



# Matrices de Transformaciones Lineales
Primero, obtengamos un resultado muy importante que es una conclusión de lo visto en [[Bases Vectoriales]]. Resulta que teniendo una base ordenada de un espacio vectorial de dimensión $n$, puedo asociar todos sus vectores a un vector de coordenadas en $\mathbb{K}^n$. Esto nos permite de manera mucho más simple, trabajar con espacios vectoriales más complicados como los polinomios, las matrices, etc. 

> [!Proposición 1.38. Vectores coordenadas]
> Sea $V$ un $\mathbb{K}$-espacio vectorial de dimensión $n$. Entonces, existe un isomorfismo ([[La Imagen y el Núcleo de una TL]]) $C: V \rightarrow \mathbb{K}^n$.

**Demostración.** Sea $B = v_1, \dots, v_n$ una **base ordenada** de $V$. Dado $v \in V$ existen únicos $x_1, \dots, x_n \in \mathbb{K}$ tales que $v = \sum_{i=1}^n x_iv_i$. Definimos, $C: V \rightarrow \mathbb{K}^n$, $C(v) = (x_1, \dots, x_n)$. Es una TL pues: 
1. Sean $v, w \in V$. Si $v = \sum_{i=1}^n x_iv_i$ e $w = \sum_{i=1}^n y_iv_i$, entonces $v+w = \sum_{i=1}^n (x_i + y_i)v_i$. Luego, $C(v+w) = (x_1+y_1, \dots, x_n + y_n) = (x_1, \dots, x_n) + (y_1, \dots, y_n) = C(v)+ C(w)$. 
2. Se puede probar de forma análoga que $C(\lambda v) = \lambda C(v)$.
Luego, $C$ es un monomorfismo pues si $C(v) = (0,0, \dots, 0)$ y es un epimorfismo pues si $(x_1, \dots, x_n) \in \mathbb{K}^n$ existe un $v = \sum_{i=1}^n x_iv_i \in V$ tal que $f(x) = (x_1, \dots, x_n)$. Entonces es un isomorfismo $\blacksquare$

De esta manera, si tenemos por ejemplo $\mathbb{K}_3[x]$ que es el espacio de polinomios con grado menor o igual a 3. Entonces, como este tiene dimensión 4, podemos crear un isomorfismo $C: \mathbb{K}_3[x] \rightarrow \mathbb{K}^4$ tal que si $P \in \mathbb{K}_3[x], \; P(x) = a_0 + a_1x + a_2x^2 + a_3x^3$ tenemos que $C(P) = (a_0, a_1, a_2, a_3)$. Esto nos simplifica la capacidad de encontrar si un conjunto es linealmente independiente, pues como ya vimos cuando la TL es un monomorfismo mantiene los conjuntos LI del espacio de salida al de llegada. Es decir, 
- $w_1, \dots, w_s$ es LI en $V \iff C(w_1), \dots, C(w_s)$ es LI en $\mathbb{K}^n$. 
- $w_1, \dots, w_r$ es un sist. de generadores en $V \iff C(w_1), \dots, C(w_s)$ es un sist. de generadores en $\mathbb{K}^n$.
- $w_1, \dots, w_n$ es una base en $V \iff C(w_1),  \dots, C(w_n)$ es una base en $\mathbb{K}^n$.

Ya vimos en [[Transformaciones Lineales]] que $T: \mathbb{K}^n \rightarrow \mathbb{K}^m, T(v) = Av$ con $A \in M_{n \times m}(\mathbb{K})$ es una transformación lineal. Resulta que existe una manera de expresar a **toda transformación lineal como una matriz**. Ya vimos que es posible (por la proposición 2 en [[Transformaciones Lineales]]) que una transformación lineal $T: V \rightarrow W$ queda determinada usando una base ordenada de $V$, $B = v_1, \dots, v_n$, tal que $T(v_1), \dots, T(v_n)$ determinan los valores de $T$ para vectores arbitrarios en $V$. Como veremos, las matrices son usadas como un **método eficiente para guardar todos los valores de los $T(v_j)$'s en términos de una base de $W$**.

> [!Matriz de una Transformación lineal]
> #Definición Supongamos $T: V \rightarrow W$ y $B = v_1, \dots, v_n$ es una base ordenada de $V$ y $B' = w_1, \dots, w_m$ es una base ordenada de $W$. La _matriz de $T$_ con respecto a las bases $B$ y $B'$ es una matriz $m \times n$ denotada $[T]_{BB'}$ o $\mathcal{M}(T)$, cuyas entradas $A_{ij}$ están definidas por $$T(v_i) = A_{1i}w_1 + \dots + A_{mi}w_m$$

Para recordar como $[T]_{BB'}$ es construida de $T$, se puede escribir cada columna como $T(v_i)$ expresado en la base $B'$.
![[Pasted image 20230117112013.png]]
Notemos también, que al escribir una matriz de transformación lineal estamos aplicando la proposición 1 dos veces, la forma en la cual se construye a partir de esta se puede expresar en el siguiente diagrama:
![[Pasted image 20230117113402.png | 200]]
Tal que nos muestra que aplicar la transformación $T: V \rightarrow W$ es lo mismo que aplicar otra transformación usando la matriz de $T$ y multiplicándola por el vector coordenadas, $(T(v))_{B'} = [T]_{BB'}(v)_{B}$ donde $(v)_{B}$ es un vector coordenadas de $V$ escrito en la base $B$. Se puede probar este resultado de la siguiente manera:

> [!Proposición 2.39.]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales de dimensión finita, y sea $T: V \rightarrow W$ una transformación lineal. Si $B_1$ y $B_2$ son dos bases ordenadas de $V$ y $W$ respectivamente, entonces para cada $v \in V$, 
> $$[T]_{B_1 B_2} \cdot (v)_{B_1} = (T(v))_{B_2}$$
> 

**Demostración.** Supongamos la base ordenada $B_1 = \{v_1, \dots, v_n\}$. Sea $v \in V$ y sea $(v)_{B_1} = (x_1, \dots, x_n)$, es decir $v = \sum_{i=1}^n x_iv_i$. 
Para cada $1 \leq i \leq n$, sea $C_i$ la $i$-ésima columna de $[T]_{B_1B_2}$. Por definición de la matriz transformación lineal tenemos que $C_i = (T(v_i))_{B_2}$. Entonces, por la definición de multiplicación de matrices (vista en [[Operaciones con Matrices]]) tenemos que
$$\begin{align} [T]_{B_1B_2} \cdot (v)_{B_1} &= x_1 C_1 + \cdots + x_nC_n \\
&= x_1(T(v_1))_{B_2} + \cdots + x_n(T(v_n))_{B_2} \\
& = \Big(\sum_{i=1}^n x_i \cdot T(v_i)\Big)_{B_2} = (T(v))_{B_2}. \quad \blacksquare
\end{align} $$
Podemos preguntarnos los siguiente _¿Es la matriz que representa la suma de dos transformaciones igual a la suma de las dos matrices de cada una?_ es decir, sean dos transformaciones $T, S: V \rightarrow W$, y sean $B = v_1, \dots, v_n$ y $B' = w_1, \dots, w_m$ dos bases ordenadas de $V$ y $W$ respectivamente, entonces ¿Ocurre que $[T+ S]_{BB'} = [T]_{BB'} + [S]_{BB'}$?  Es claro que sí, pues para la columna $i$-ésima tenemos que $T(v_i) = \sum_{j=1}^m \alpha_{ij}w_j$ , $S(v_i) = \sum_{j=1}^m \beta_{ij}w_j$, y $(S+T)(v_i) = S(v_i) + T(v_i) = \sum_{j=1}^m (\alpha_{ij} + \beta_{ij})w_j$. Entonces, $([T]_{BB'})_{ij}  = \alpha_{ij}$,  $([S]_{BB'})_{ij} =  \beta_{ij}$ y $([T+S]_{BB'})_{ij} = \alpha_{ij} + \beta_{ij} = ([T]_{BB'})_{ij} + ([S]_{BB'})_{ij}$. 
Se puede de igual manera demostrar que $[\lambda T]_{BB'} = \lambda \cdot [T]_{BB'}$. 

## La multiplicación de matrices y la composición de transformaciones lineales
Supongamos que, al igual que antes, $B_1 = v_1, \dots, v_n$ es una base de $V$ y $B_2 = w_1, \dots, w_m$ es una base de $W$. También supongamos que hay otro espacio vectorial $U$ con una base ordenada $B_3 = u_1, \dots, u_p$. 

Consideremos las transformaciones lineales $T: U \rightarrow V$ y $S: V \rightarrow W$. Nos podemos preguntar, _¿La composición de las transformaciones $S \circ T$ cumple que $[S \circ T]_{B_1B_3} = [S]_{B_2B_3}[T]_{B_1B_2}$ ?_  Cuando definimos la multiplicación de matrices en [[Operaciones con Matrices]], dijimos que la razón por la cual definimos a la multiplicación de esta manera viene de las transformaciones lineales. Sin darnos cuenta definimos a la multiplicación de matrices para forzar que la pregunta anterior tenga una respuesta afirmativa.
Supongamos $[S]_{B_1B_2} = A$ y $[T]_{B_2B_3} = B$. Para $1 \leq i \leq p$, tenemos que
$$\begin{align} (S \circ T)(u_j) &= S\Big(\sum_{i=1}^nB_{ij}v_i\Big) = \sum_{i=1}^n B_{ij}S(v_i) = \sum_{i=1}^n B_{ij}\sum_{k=1}^m A_{ki}w_j = \sum_{k=1}^m\Big(\sum_{i=1}^nA_{ki}B_{ij}w_j\Big)
\end{align}$$
Entonces, tenemos que las entradas de la matriz $p \times n$  que representa la composición de las transformaciones lineales tiene la forma $([S \circ T]_{B_1B_3})_{ij} = \sum_{i=1}^n A_{ki}B_{ij}$. Que notemos es la definición que dimos del producto de las matrices $(AB)_{ij} = \sum_{i=1}^n A_{ki}B_{ij}$. 

> [!Proposición 3.40.]
> Sean $V$, $W$ y $U$, 3 $\mathbb{K}$-espacios vectoriales y sean $B_1$, $B_2$ y  $B_3$ bases ordenadas de $V,W$ y $U$ respectivamente. Sean $T: V \rightarrow W$ y $S:W \rightarrow U$ transformaciones lineales. Entonces
> $$[S \circ T]_{B_1B_3} = [S]_{B_2B_3}[T]_{B_1B_2}$$

**Demostración.** Sean $n = \dim V$, $m = \dim W$ y $p = \dim U$. Entonces, $[S]_{B_2 B_3} \in M_{p \times m}(\mathbb{K})$ y $[T]_{B_1B_2} \in M_{m \times n}(\mathbb{K})$ con lo que se puede multiplicar a las matrices y $[S]_{B_3B_2} \cdot [T]_{B_1B_2} \in M_{p \times n}(\mathbb{K})$. Para cada $v \in V$ se tiene 
$$[S]_{B_2B_3}[T]_{B_1B_2}(v)_{B_1} = [S]_{B_2B_3}(T(v))_{B_2} = (S(T(v)))_{B_3} = ((S \circ T)(v))_{B_3} = [S \circ T]_{B_1B_3}(v)_{B_1}$$
Usando repetidas veces la proposición 2. Luego, $[S \circ T]_{B_1B_3} = [S]_{B_2B_3}[T]_{B_1B_2}$. $\blacksquare$ 

Notemos que cuando la transformación lineal sea un isomorfismo, sabemos que es **invertible**. Y su matriz sería la inversa ([[Matrices Invertibles]]) de $[T]_{B_1B_2}$ por la proposición anterior. 

> [!Corolario 3.1.40.]
> Sean $B_1$ y $B_2$ dos bases de $V$ y $W$ respectivamente. Y sea $T: V \rightarrow W$ un isomorfismo. Entonces $[T^{-1}]_{B_2B_1} = ([T]_{B_1B_2})^{-1}$ 

Desde ahora en adelante, veremos las matrices directamente como una transformación lineal, realmente son equivalentes. **Toda matriz representa a una transformación lineal y toda transformación lineal representa una matriz**. 
Notemos la importancia de las transformaciones lineales, que hasta ahora nos han servido para explicar ciertos comportamientos de los espacios vectoriales, las matrices y las soluciones de los sistemas de ecuaciones (estos dos últimos también espacios vectoriales). 

## Isomorfismos
Notemos que el hecho de que una matriz sea invertible tiene un nuevo significado. Como cada matriz representa a una específica transformación lineal entonces, por el corolario anterior, **para que la matriz sea invertible es necesario que la transformación que representa sea un isomorfismo.** Sabemos que para que exista un isomorfismo $\dim V = \dim W$, lo cual en un matriz transformación quiere significar que tengamos la misma cantidad de filas que de columnas y que a su vez las filas y las columnas sean linealmente independientes entre sí. De esta manera, se introduce el concepto de **rango** de una matriz, que veremos mejor en [[Cambio de Base y Rango de una matriz]]. 

Por muchos motivos, a menudo se tratan [[Espacios Vectoriales]] **isomórficos** (es decir, que se puede crear un isomorfismo entre ambos) como "iguales" o "equivalentes", es más se los suele denotar $V \equiv W$, aunque las operaciones en los espacios sean muy diferentes parecen mantener la misma estructura o simetría. 
Una de las capacidades que tienen los isomorfismos es la de "preservar dimensiones". Por la proposición 3 de [[La Imagen y el Núcleo de una TL]] sabemos que si $T: V \rightarrow W$ es un isomorfismo entonces todo subespacio $S$ de $V$ es linealmente independiente si y solo si $T(S)$ es linealmente independiente en $W$. Entonces, cada subespacio finito en $V$ tiene la misma dimensión que su imagen bajo $T$.  
En [[Operaciones con Matrices]] sentimos la necesidad de decir que es "lo mismo" tener un elemento en $(x_1, \dots, x_n) \in \mathbb{K}^n$ que tenerlo en $\begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix} \in M_{n \times 1}(\mathbb{K})$, nuestra justificación ahora para hacerlo es que existe un claro isomorfismo entre $\mathbb{K}^n$ y $M_{n \times 1}(\mathbb{K})$ (nos lo verifica la proposición 1). Bajo este isomorfismo, la independencia lineal de vectores en $\mathbb{K}^n$ es "llevada" o "transportada" a $M_{n \times 1}(\mathbb{K})$ y lo mismo con sistemas de generadores que pasan de uno a otro. 

La siguiente proposición prueba lo dicho arriba, tal que nos dice que hablar de matrices y transformaciones lineales es "lo mismo" (pues existe un isomorfismo entre ellas).  

> [!Proposición 4. El espacio de tl's y el espacio de matrices son isomórficos]
> **(NEF)** Supongamos $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales,  $B_1 = \{v_1, \dots, v_n\}$ es una base de $V$ y $B_2 = \{w_1, \dots, w_n\}$ es una base de $W$. Entonces, $[*]_{B_1B_2}$ es un isomorfismo entre $\mathrm{Hom}(V,W) \rightarrow M_{m \times n}(\mathbb{K})$. 

**Demostración.** Ya demostramos que dados dos transformaciones lineales $T,S \in \mathrm{Hom}(V,W)$ entonces $[T]_{B_1B_2} + [S]_{B_1B_2} = [T+S]_{B_1B_2}$ y $\lambda [T]_{B_1B_2} = [\lambda T]_{B_1B_2}$ por lo tanto $[*]_{B_1B_2}$ (la función que crea la matriz transformación lineal) es una transformación lineal en sí misma. Nos quedaría probar que $[*]_{B_1B_2}$ es un monomorfismo y epimorfismo. Si $T \in \mathrm{Hom}(V,W)$ y $[T]_{B_1B_2} = 0$, entonces $T(v_i) = 0$ para todo $i = 1, \dots, n$. Como $v_1, \dots, v_n$ es una base de $V$, esto implica que $T \equiv 0$. Entonces, $[*]_{B_1B_2}$ es un monomorfismo, luego no es necesario probar que es un epimorfismo por el corolario 1.1 del [[Teorema de la dimensión]]. $\blacksquare$ 

Algo muy importante de notar, es que el conjunto de todas las transformaciones lineales isomórficas, tienen una amplia relación con el conjunto de todas las matrices invertibles $GL(n, \mathbb{K})$ (que ya vimos que es un grupo en [[Matrices Invertibles]]).  

# Cambios de Bases
En [[Matrices de Transformaciones Lineales]] aprendimos a formar matrices que representan a una transformación lineal. Esto va a ser muy útil para las siguientes notas. 
Un problema que todavía no hemos abordado es la capacidad de querer cambiar de una base vectorial a otra en el mismo espacio vectorial. Esto es útil en la física, por ejemplo cuando queremos cambiar de coordenadas.
Podemos pensar en el cambio de base muy fácilmente, pensado en que si a la transformación identidad $\mathrm{Id}: V \rightarrow V$ le asigno una matriz transformación usando dos bases $B$ y $B'$, lo que obtengo es la matriz capaz de cambiarnos las coordenadas de un vector expresada en una base $B$ a la base $B'$ sin provocarle ningún cambio al mismo. En símbolos, $[\mathrm{Id}]_{BB'}(v)_{B} = (v)_{B'}$.  

> [!Matriz cambio de base]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial de dimensión $n$, y sean $B_1 = v_1, \dots, v_n$ y $B_2 = w_1, \dots, w_n$ dos bases ordenadas de $V$. Para cada $1 \leq j \leq n$, sean $\alpha_{ij} \in \mathbb{K}$ tales que $v_j = \sum_{i=1}^n \alpha_{ij}w_i$. Se llama _matriz cambio de base de $B_1$ a $B_2$,_ y se nota $C(B_1, B_2) \in M_{n \times n}\mathbb{K}$ , a la matriz definida por $C(B_1, B_2) = \alpha_{ij}$, para cada $1 \leq i, j \leq n$. 

Dos afirmaciones que son importantes de notar son las siguientes: 
1. Si tenemos tres  bases de un espacio vectorial finito $V$, que son $B_1, \; B_2$ y $B_3$, entonces $C(B_1, B_3) = [\mathrm{Id}]_{B_1B_3} = [\mathrm{Id}]_{B_2B_3} \cdot [\mathrm{Id}]_{B_1B_2}$ (por la proposición 3 en [[Matrices de Transformaciones Lineales]])
2. Si tenemos dos bases de un espacio vectorial finito $V$, que son $B_1$ y $B_2$, entonces $C(B_2,B_1) = [\mathrm{Id}]_{B_2B_1} = [\mathrm{Id}]_{B_1B_2}^{-1} = (C(B_1,B_2))^{-1}$ (por el corolario 3.1)

Notemos que entonces la matriz cambio de base es siempre invertible, y si tengo la matriz de $C(B_1, B_2)$ puedo obtener $C(B_2, B_1)$ simplemente invirtiéndola, usando el proceso visto en [[Matrices Invertibles]]}. 
La siguiente proposición presenta un resultado muy interesante. 

> [!Proposición 1.41.]
> Sea $A \in GL(n, \mathbb{K})$. Existen bases $B_1, B_2$ de $\mathbb{K}^n$ tales que $A = C(B_1, B_2)$.

**Demostración.** Supongamos que $A_{ij} = a_{ij}$, $i=1, \dots, n$ y $j = 1, \dots, n$. 
$$A= \begin{align} \begin{pmatrix} 
a_{11} & a_{12} & \cdots & a_{1n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{pmatrix} \\
B_1= v_1 \quad v_2 \quad \cdots \quad v_n \; \quad 
\end{align}$$
Supongamos que $B_2 = E = e_1, e_2, \dots, e_n$ es la base canónica de $\mathbb{K}^n$, y sea $B_1 = v_1, \dots, v_n$ una base ordenada que queremos encontrar, eligiendo convenientemente $v_j = \sum_{i=1}^n a_{ij}e_i$ para todo $j$, el conjunto que nos queda es LI pues la matriz $A$ es invertible, entonces $B_1$ es una base. Luego, $C(B_1, B_2) = A$. $\blacksquare$ 

La siguiente proposición es útil para cuando queremos pasar una matriz de transformación lineal que esta en dos bases $B_1$ y $B_2$ a otras dos bases $B_1'$ y $B_2'$. 

> [!Proposición 2.42.]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales de dimensión finita. Sean $B_1$, $B_1'$ dos bases ordenadas de $V$ y $B_2$, $B_2'$ dos bases de $W$. Entonces,
> $$[T]_{B_1'B_2'} = C(B_2, B_2') \cdot [T]_{B_1B_2} \cdot C(B_1',B_1)$$

**Demostración.** Se tiene que $T = id_W \circ T \circ id_V$. Aplicando 2 veces el resultado dado por la proposición 3 en [[Matrices de Transformaciones Lineales]], tenemos que 
$$\begin{align} [T]_{B_1'B_2'} & = [id_W \circ T \circ id_V]_{B_1'B_2'} = [id_W \circ T]_{B_1B_2'}[id_V]_{B_1'B_1} = \\
& = [id_W]_{B_2B_2'}[T]_{B_1B_2}[id_V]_{B_1'B_1} = C(B_2,B_2')[T]_{B_1B_2}C(B_1',B_1)
\end{align}$$
que es lo que queríamos probar. $\blacksquare$ 


# Rango de una matriz
Algo que todavía no nos hemos cuestionado es _¿Por qué al escribir la matriz transformación lineal colocamos nuestros vectores (expresados en su base correspondiente) como columnas y no como filas?_ _¿Existe alguna diferencia de escribir a los vectores como filas en vez de columnas?_ Ya hemos visto de que existe un isomorfismo entre $\mathbb{K}^n$ y $M_{n \times 1}(\mathbb{K})$ (vectores columna), pero también existe uno entre $\mathbb{K}^n$ y $M_{1 \times n}(\mathbb{K})$ (vectores fila) así que estas preguntas preguntas son válidas. La siguiente sección llegará a la conclusión de que da igual como pongamos los vectores (con respecto a ponerlos como filas o columnas), el resultado de la dimensión de la imagen de la transformación y del núcleo no se ve modificado.

Consideremos la matriz de $T: V \rightarrow W$ en $B_1$ y $B_2$ que son las bases ordenadas de $V$ y $W$ respectivamente. 
$$[T]_{B_1B_2} = (C_1 \; | \cdots | \; C_m) \in M_{n \times m}(\mathbb{K})$$
Si $B_2 = \{v_1, \dots, v_m\}$ entonces (por la proposición 2 de [[Transformaciones Lineales]]) $\mathrm{Im}(T) = <T(v_1), \dots, T(v_m)>$. Tomando coordenadas de la base $B_2$ se obtiene un subespacio $U \subseteq \mathbb{K}^n$ dado por $U = <(T(v_1))_{B_2}, \dots, (T(v_n))_{B_2}>$. Como tomar coordenadas en una base es un isomorfismo, son iguales $\dim (\mathrm{Im}(T)) = \dim U$. Entonces, para encontrar la dimensión de la imagen de una transformación lineal, o incluso el núcleo, en ciertas ocasiones es más útil trabajar directamente con su matriz de transformación, ya que existe un isomorfismo entre $M_{n \times m}(\mathbb{K}) \equiv \mathrm{Hom}(V,W)$ puedo pasar libremente entre una y otra. 

> [!Rango colum. de una matriz]
> Sea $A \in M_{n \times m} (\mathbb{K})$. Se llama _rango columna de $A$_ a la dimensión del subespacio de $\mathbb{K}^m$ generado por las columnas de $A$, es decir, si $A = (C_1 | \cdots | C_m)$, entonces $\mathrm{rg}_C(A) = \dim < C_1, \dots, C_m >$. 

Se puede usar el rango de columnas para poder obtener el conjunto de soluciones de un sistema lineal homogéneo. Si $A \in M_{m \times n}(\mathbb{K})$ y sea $S = \{x \in \mathbb{K}^m / Ax = 0\}$, entonces $\dim S = m - \mathrm{rg}_C(A)$ gracias al [[Teorema de la dimensión]]. 

> [!Rango fila de una matriz]
> Sea $A \in M_{n \times m} (\mathbb{K})$. Se llama _rango fila de $A$_ a la dimensión del subespacio de $\mathbb{K}^n$ generado por las filas de $A$, es decir, si $A = \begin{pmatrix} F_1 \\ \vdots \\ F_n \end{pmatrix}$, entonces $\mathrm{rg}_F(A) = \dim < F_1, \dots, F_n >$.

Queríamos llegar a que es lo mismo hablar sobre el rango fila, que del rango columna, $\mathrm{rg}_{F}(A) = \mathrm{rg}_C(A)$. Una forma para comprobar esto, es pensarlo como si transpusiéramos a la matriz $A$[^1] y entonces las filas se vuelven columnas, por lo que podemos comparar el rango de las columnas de la matriz transpuesta $A^t$ y si es el mismo que el rango de columnas de la matriz $A$ demostramos lo que queríamos. 

Primero probemos un resultado que será más útil en proposiciones posteriores, que nos dice que multiplicar por matrices invertibles no modifica el rango. Esta conclusión sale de analizar las proposiciones 1 y 2. 

> [!Lema 3.43.]
> Sea $A \in K^{n \times m}$. Sean $G \in G L(n, K)$ y $D \in G L(m, K)$. Entonces$$ \mathrm{rg}_C(A)=\operatorname{rg}_C(C \cdot A \cdot D)$$

**Demostración.** Sea $f_A: K^m \rightarrow K^n$ la transformación lineal inducida por la multiplicación a izquierda por $A$. Si $E$ y $E^{\prime}$ son las bases canónicas de $K^m$ y $K^n$ respectivamente, se tiene que $\left|f_A\right|_{E E^{\prime}}=A$ y por lo $\operatorname{rg}(A)=\operatorname{dim}\left(\operatorname{Im}\left(f_A\right)\right)$.
Por la Proposición 1, puesto que $D \in G L(m, K)$, existe una base $B_1$ de $K^m$ tal que $D=C\left(B_1, E\right), y$ como $C \in G L(n, K)$, existe una base $B_2$ de $K^n$ tal que $C=C\left(E^{\prime}, B_2\right)$.
Entonces por la proposición 2,
$$
 { C \cdot A \cdot D }=C\left(E^{\prime}, B_2\right) \cdot\left|f_A\right|_{E E} \cdot C\left(B_1, E\right)=\left|f_A\right|_{B_1 B_2}
$$
la dimensión de la imagen no cambia por haber cambiado las bases, por lo tanto $\operatorname{rg}_C(C . A . D)=\operatorname{dim}\left(\operatorname{Im}\left(f_A\right)\right)=\operatorname{rg}_C(A)$. $\blacksquare$ 

El siguiente lema prueba de que multiplicando por las matrices invertibles apropiadas se puede llegar a una matriz más sencilla tal que el rango de la misma sea muy claro. 

> [!Lema 4.44.]
> Sea $A \in M_{n \times m}(\mathbb{K}) - \{0\}$. Entonces, existen $k \in \mathbb{N}, 1 \leq k \leq \mathrm{min}\{n,m\}$, y las matrices $C \in GL(n, \mathbb{K})$ y $D \in GL(m, \mathbb{K})$ tales que $$(C \cdot A \cdot D)_{ij} = \begin{cases} 0 & \text{ si } i \neq j \\ 1 & \text{ si } i = j \leq k \\ 0 & \text{ si } i = j > k \end{cases}$$

**Demostración.** Consideremos la transformación lineal $f_A: K^m \rightarrow K^n$ inducida por la multiplicación a izquierda por $A$. Sea $\left(v_1, \ldots, v_s\right\}$ una base de $\mathrm{Nu}\left(f_A\right)$ y sean $w_1, \ldots, w_{m-s} \in K^m$ tales que
$$
B_1=\left\{w_1, \ldots, w_{m-s}, v_2, \ldots, v_s\right\}
$$
es una base de $K^m$ (si $\mathrm{Nu}\left(f_A\right)=\{0\}, s=0$ y se toma una base $B_1$ cualquiera de $K^m$ ).
Entonces $\left\{f_A(w_1) \ldots, f_A\left(w_{m-s}\right)\right\}$ es una base de $\operatorname{Im}\left(f_A\right)$ y puede extenderse a una base de $K^n$. Usando la proposición 4 de [[Bases Vectoriales]], existen $z_1, \ldots, z_{n - m+s} \in K^n$ tales que
$$
B_2=\left\{f_A\left(w_1\right), \ldots . f_A\left(w_{m-s}\right), z_1, \ldots, z_{n-m+s}\right\}
$$
es una base de $K^n$.
Se tiene que
$$
\left(|f_A|_{B_1 B_2}\right)_{i j}=\left\{\begin{array}{ll}
0 & \text { si } i \neq j \\
1 & \text { si } i=j \leq m-s \\
0 & \text { si } i=j>m-s
\end{array}\right.
$$
Pues para columnas $j$ tales que $j > m-s$ van a ser nulas pues $f(v_i) = 0$ y por ejemplo en la primera columna $(f(w_1))_{B_2} = 1 f(w_1) + 0 f(w_2) + \dots + 0 f(w_{m-s}) + 0 f(z_1) + \dots + 0 f(z_{n-m+s})$ tal que tenemos una matriz parecida a la identidad para $j \leq m-s$. 
Observamos que por la proposición 2
$$
|f_A|_{B_1 B_2}= C\left(E^{\prime}, B_2\right) \cdot \left|f_A\right|_{E E'} \cdot C\left(B_1, E\right)=C . A . D,
$$
donde $C=C\left(E^{\prime}, B_2\right) \in G L(r, \kappa)$ y $D=C\left(B_2, E^{\prime}\right) \in C L\left(r_1, K\right)$. Y entonces llegamos a lo que queríamos. $\blacksquare$ 

> [!Proposición 5.45. El rango filas es igual al rango colum]
>  Sea $A \in M_{n \times m}(\mathbb{K})$. Entonces $\mathrm{rg}_C(A)=\operatorname{rg}_F(A)$.

**Demostración.** Es claro que el resultado vale si $A=0$. Dada $A \in M_{n \times m}(\mathbb{K})-\{0\}$, por el lema anterior, existen matrices $C \in G L(n, K), D \in C L(m, K)$ y $k \in \mathbb{N}$, tales que
$$
(C \cdot A \cdot D)_{i j}=\left\{\begin{array}{ll}
0 & \text { si } i \neq j \\
1 & \text { si } i=j \leq k \\
0 & \text { si } i=j>k
\end{array}\right.
$$

Es claro entonces que $\mathrm{rg}_C(A) = \mathrm{rg}_C(C \cdot A \cdot D) = k$. Por otro lado, transponiendo se tiene que 
$$(D^t \cdot A^t \cdot C^t)_{i j}=\left\{\begin{array}{ll}
0 & \text { si } i \neq j \\
1 & \text { si } i=j \leq k \\
0 & \text { si } i=j>k
\end{array}\right.$$
con $D^t \in GL(m, \mathbb{K})$ y $C^t \in GL(n, \mathbb{K})$, de donde $\mathrm{rg}_C(A^t) = \mathrm{rg}_C(D^t \cdot A^t \cdot C^t) = k$. Es claro que $\mathrm{rg}_C (A^t) = \mathrm{rg}_F(A)$ por lo que nos queda que $\mathrm{rg}_C(A) = \mathrm{rg}_F(A) = k$. $\blacksquare$  


[^1]: Matriz transpuesta: si $A \in M_{n \times n}$ entonces $(A^t)_{ij} = A_{ji}$. Visualmente, sería como rotar 90° a la matriz $A$. 


# Formas bilineales y Funciones Multilineales
Si bien las [[Transformaciones Lineales]] son un tipo de funciones muy interesante entre [[Espacios Vectoriales]], no son las únicas. Existen otros tipos de funciones muy interesantes que valen la pena estudiar que no son transformaciones lineales. Por ejemplo, $f: \mathbb{R}^2 \rightarrow \mathbb{R}, \; f(x,y) = xy$ no es una transformación lineal. Sin embargo, si fijamos una de sus variables, por ejemplo $x \in \mathbb{R}$ , tenemos que $f(y) = xy$ si es una transformación lineal. Podemos generalizar esto último y hablar de todas las funciones $f: V \rightarrow \mathbb{K}$ con $V$ un $\mathbb{K}$-espacio vectorial finito, y veamos que $f_{w}(\vec{v}) = \vec{v} \cdot \vec{w}$[^1] con $\vec{w} \in V$ fijo y donde $\cdot$ es un [[Producto Interno]]  en $V$[^2],  es una transformación lineal especial llamada **forma lineal** o **función lineal**. 

Entonces, se puede probar que una función es una **forma lineal** si el producto en $V$ esta definido de forma tal que se cumple  $\vec{v}, \vec{u} \in V, \; f_w(\vec{v} + \vec{u})$$= (\vec{v} + \vec{u}) \cdot \vec{w}$ $= \vec{v} \cdot \vec{w} + \vec{u} \cdot \vec{w} = f_w(\vec{v}) + f_w(\vec{u})$  y $\lambda \in \mathbb{K}, \vec{v} \in V, \; f_w(\lambda\vec{v}) = (\lambda\vec{v}) \cdot \vec{w} = \lambda(\vec{v} \cdot \vec{w})$ $= \lambda f_w(\vec{v})$ . Para acortar este proceso de demostrar que una función es una forma lineal, basta con demostrar $f(\lambda \vec{v} + \vec{w}) = \lambda f(\vec{v}) + f(\vec{w})$ pues eligiendo $\lambda = 1$ tenemos la primer propiedad y luego eligiendo $\vec{w} = 0$ tenemos la segunda. Ahora, notemos que la función $f_w(\vec{v}) = \vec{v} \cdot \vec{w}$ tiene a $\vec{w}$ fijo, pero si aparte podemos definir $f_{v}(\vec{w}) = \vec{v} \cdot \vec{w}$ con $\vec{v}$ fijo y esta también cumple ser una forma lineal. Entonces decimos que podemos simplemente definir $f(\vec{v}, \vec{w}) = \vec{v} \cdot \vec{w}$ que fijando un vector o el otro es una forma lineal, a esta la llamamos **forma bilineal**.  

> [!Forma Binomial]
> #Definición Sean $V$ y $W$ dos $\mathbb{K}$ espacios vectoriales. Una _forma bilineal_ de $V$ en $W$ es una función $F: V \times W \rightarrow \mathbb{K}$  si:
> 1. $F( v_1 + v_2, w) = F(v_1, w) + F(v_2, w)$ 
> 2. $F(v, w_1 + w_2) =  F(v, w_1) + F(v, w_2)$ 
> 3. $F(\lambda v, w) = \lambda F(v,w) = F(v, \lambda w)$
> Con $w, w_1, w_2 \in W, \; v, v_1, v_2 \in V$ y $\lambda \in \mathbb{K}$

Notemos como construimos el concepto de forma bilineal usando transformaciones lineales. Esto nos permite entender a las formas bilineales gracias a que ya entendemos a las TL's. El siguiente ejemplo muestra la intima relación entre ambos tipos de funciones.

**Ejemplo 1.** Sean $f, g : V \rightarrow \mathbb{K}$ dos transformaciones lineales, tenemos que $F(v,w) = f(v)g(w)$ es una forma binomial. Esto pues 
- $F(\lambda v_1 + v_2, w) = f(\lambda v_1 + v_2)g(w) = (\lambda f(v_1) + f(v_2)) g(w)$ $= \lambda f(v_1)g(w) + f(v_2)g(w) = \lambda F(v_1, w) + F(v_2, w)$. Donde en la segunda igualdad usamos que $f$ es una TL.
- $F(v, \lambda w_1 + w_2) = f(v)g(\lambda w_1 + w_2) = f(v)(\lambda g(w_1) + g(w_2) =$ $\lambda f(v)g(w_1) + f(v)g(w_2) = \lambda F(v,w_1) + F(v, w_2)$ . Donde en la segunda igualdad usamos que $g$ es una TL.

Empecemos con nuestro desarrollo de definir el determinante. El determinante es un escalar en un cuerpo $\mathbb{K}$ que se le asigna a una matriz, este va a resultar muy útil para darnos cierta información de la matriz y de la transformación lineal que representa. Entender las formas bilineales son un paso a definir el determinante. 

**Ejemplo 2.** Supongamos que tenemos la forma bilineal $F: \mathbb{R}^2 \times \mathbb{R}^2 \rightarrow \mathbb{R}$, notemos lo siguiente
$$\begin{align} F((a,b),(c,d)) & = F((a,0) + (0,b), (c,d)) = F((a, 0) + (0,b), (c,0) + (0,d)) \\ 
& = a \cdot F((1,0), (c,0)+ (0,d) + b \cdot F((0,1),(c,0)+(0,d)) \\ &= ac \cdot F((1,0),(1,0) + ad \cdot F((1,0),(0,1)) + bc \cdot F((0,1),(1,0)) \\ & \quad + bd \cdot F((0,1),(0,1)) \end{align}$$
Usando las propiedades de las formas bilineales. Notemos que entonces la función queda determinada por $F((1,0),(1,0)), \; F((0,1),(1,0)), \; F((1,0), (0,1))$ y $F((0,1),(0,1))$. 

## Matriz de una forma bilineal
Supongamos que dada la matriz $A = \begin{pmatrix} 1 & -3 & 2 \\ 0 & 4 & -1\end{pmatrix}$ queremos encontrar una forma bilineal $F: \mathbb{R}^2 \times \mathbb{R}^3 \rightarrow \mathbb{R}$, $F(v, w) = v^t \cdot A \cdot w$ tal que esté expresada solo en las coordenadas de $\mathbb{R}^2$ y $\mathbb{R}^3$, $v = (x_1, x_2)$ y $w = (y_1, y_2, y_3)$, o lo que es lo mismo $v = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$ y $w = \begin{pmatrix} y_1 \\ y_2 \\ y_3 \end{pmatrix}$ . Notemos que $F$ si es una forma bilineal y lo puede comprobar usando las propiedades de la definición. 
Veamos también que $v^t \cdot A \cdot w$ tiene sentido pues $v^t$ es una matriz $1 \times 2$, $A$ es una matriz $2 \times 3$ y $w$ es una matriz $3 \times 1$, entonces tenemos permitida la multiplicación de matrices (vista en [[Operaciones con Matrices]]). 
Luego,
$$\begin{pmatrix} x_1 & x_2\end{pmatrix} \cdot \begin{pmatrix} 1 & -3 & 2 \\ 0 & 4 & -1\end{pmatrix} \cdot \begin{pmatrix} y_1 \\ y_2 \\ y_3 \end{pmatrix} = x_1y_1 -3x_1y_2 + 2x_1y_3 +4x_2y_2 - x_2y_3$$
Y listo, tenemos definida $F((x_1,x_2), (y_1, y_2, y_3)) = x_1y_1 -3x_1y_2 + 2x_1y_3 +4x_2y_2 - x_2y_3$ como nuestra forma binomial. 

Una pregunta que nos podemos hacer es _¿Al igual que puedo obtener de cualquier matriz una forma binomial correspondiente, puedo obtener de una forma binomial una matriz?_ Resulta que si podemos, lo cual motiva la siguiente definición

> [!Matriz de una forma bilineal]
> #Definición Sea $F: V \times V \rightarrow \mathbb{K}$ una forma binomial, y sea $B = v_1, \dots, v_n$ una base de $V$. Definamos $([F]_{B})_{ij} = (F(v_i, v_j)) \in M_{n \times n}(\mathbb{K})$ es la _matriz de $F$ en la base $B$._

De esta manera, se puede comprobar en el ejemplo anterior que $A$ es la matriz de la forma binomial $F$ usando la base canónica. 

Podemos probar entonces lo siguiente
> [!Proposición 1.46.]
> Sea $V$ un $\mathbb{K}$-espacio vectorial de dimensión finita y sea $B = v_1, \dots, v_n$ es una base ordenada de $V$. Sea $F: V \times V \rightarrow \mathbb{K}$ una forma bilineal. Entonces, para cada $v,w \in V$, $$F(v,w) = (v)^t_B[F]_{B}(w)_{B}$$
> 

**Demostración.** Probemos que de ambos lados obtenemos lo mismo. Teniendo $v = \sum_{i=1}^n \alpha_iv_i$ y $w = \sum_{i=1}^n \beta_iv_i$ expresados en la base $B$.
$$F(v,w) = F\Big(\sum_{i=1}^n \alpha_i v_i, \sum_{j=1}^n \beta_jv_j\Big) = \sum_{i=1}^n \alpha_i F\Big(v_i, \sum_{j=1}^n\beta_j v_j\Big) = \sum_{i=1}^n \alpha_i \Big(\sum_{j=1}^n \beta_j F(v_i,v_j)\Big)$$
Luego,
$$\begin{align} (v)_{B}^t [F]_B (w)_B & = \begin{pmatrix} \alpha_1 & \alpha_2 & \cdots & \alpha_n \end{pmatrix} \cdot 
[F]_{B} \cdot 
\begin{pmatrix} \beta_1 \\ \beta_2 \\ \vdots \\ \beta_n\end{pmatrix} = \sum_{i=1}^n \alpha_i \left( [F]_B \cdot \begin{pmatrix} \beta_1 \\ \beta_2 \\ \vdots \\ \beta_n \end{pmatrix}\right)_{i1}  \\ & = \sum_{i=1}^n \alpha_i\Big( \sum_{j=1}^n \beta_j F(v_i, v_j)\Big) \quad \blacksquare \end{align} $$
Algo muy importante de notar al observar a las formas bilineales, es que la mayoría parecen **polinomios**. 

Volveremos a las formas bilineales para cuando queremos generalizar el [[Producto Interno]] de un espacio vectorial. 

## Funciones Multilineales
Nos vamos a concentrar de ahora en adelante en definir el **determinante**. Una de las aplicaciones más útiles del determinante, es la capacidad de decirnos si una matriz es invertible o no y a la vez nos dice si la transformación lineal que representa es un isomorfismo o no (por lo visto en [[Matrices de Transformaciones Lineales]]).  Entonces, buscamos definir una función que nos lleve de varios vectores (que se pueden ordenar en una matriz) a un escalar que nos diga si los vectores columna (o filas) son linealmente independientes, en ese caso el determinante es distinto de 0.

**Ejemplo 3.** Primero veamos como definir un determinante de $2 \times 2$. Para esto, ya vimos en el ejemplo 2 que en una forma bilineal $F: \mathbb{R}^2 \times \mathbb{R}^2 \rightarrow \mathbb{R}$ tenemos que está determinada por $F((1,0),(1,0)), \; F((0,1),(1,0)), \; F((1,0), (0,1))$ y $F((0,1),(0,1))$. 
Tenemos que claramente la primera lista de vectores y la cuarta son dos vectores linealmente dependientes, entonces queríamos que $F((0,1), (0,1)) = 0$ y $F((1,0), (1,0)) = 0$. Por lo tanto, podemos definir al determinante como "una forma bilineal  tal que al evaluarla en vectores iguales nos da 0". Sabiendo que $F$ es una función de este tipo veamos ahora que dado $v ,w \in \mathbb{R}^2$ tenemos que
$$\begin{align} 0 & = F(v+w, v+w) = \underset{=0}{\underbrace{F(v,v)}} + F(w,v) + F(v,w) + \underset{=0}{ \underbrace{F(w,w)}} \\ 
0 & = F(v,w) + F(w,v) \\
\boxed{F(v,w)} & = - F(w,v)
\end{align}$$
Luego, $F((1,0),(0,1)) = -F((0,1), (1,0))$ y tenemos entonces que nuestra función buscada es $F((a,b),(c,d)) = (ad - bc)F((1,0),(0,1))$. 

Sin embargo, el determinante puede calcularse para cualquier matriz cuadrada (para encontrar si estas son invertibles), entonces tenemos que definir el concepto de función multilineal. 
> [!Función multilineal]
> #Definición  Sea $V$ un $\mathbb{K}$-espacio vectorial, y una función $F: \prod_{i=1}^n V \rightarrow \mathbb{K}$  se dice _multilineal_ si cumple la propiedad de ser una _forma lineal_ en cada entrada. Es decir, fijando $n-1$ valores y dejando $v_i$ libre, si se cumplen $F(v_1 + v, \dots, cv_i +v_j, \dots, v_n) = cF(v_1, \dots, v_i, \dots, v_n) + F(v_1, \dots, v_j, \dots, v_n)$  para cada $i = 1, \dots, n$ con $v_j \in V$ y $c \in \mathbb{K}$. 

A una función multilineal "tal que al que al evaluarla en listas con dos vectores iguales nos da 0" la llamamos **función alternada**.
> [!Función Alternada]
> Una _función multilineal_ $F: \prod_{i=1}^n V \rightarrow \mathbb{K}$ se dice _alternada_ si se cumple que al evaluarla en una lista de $n$ vectores en los que 2 son iguales nos da 0. Es decir, para $v_1, \dots, v_i, \dots, v_j, \dots, v_n$, una lista de vectores con $v_i = v_j$, $F(v_1, \dots, v_n) = 0$.

Ya sabemos que podemos crear un isomorfismo entre $\mathbb{K}^n$ y $V$ (gracias a la proposición 1 en [[Matrices de Transformaciones Lineales]]) usando una base de finita $V$ y luego existe otro claro isomorfismo entre $\mathbb{K}^n \times \cdots \times \mathbb{K}^n$ y $M_{n \times n} (\mathbb{K})$. Por lo tanto, a cada función multilineal alternada $F: \prod_{i=1}^n V \rightarrow \mathbb{K}$ le asignamos (gracias a los isomorfismos) a una función $F: M_{n \times n}(\mathbb{K}) \rightarrow \mathbb{K}$, por lo tanto trabajemos simplemente con estas funciones.

Gracias a estas dos definiciones, estamos listos para definir el determinante de una matriz $2\times 2$ : 
> [!Determinante 2x2]
> #Definición La función bilineal alternada $\det_2: M_{2 \times 2}(\mathbb{K}) \rightarrow \mathbb{K}$ tal que $\det_2(Id_2) = 1$ se llama _determinante de orden 2_. 

Tal que
$$\det \begin{pmatrix} a & b \\ c & d\end{pmatrix} = (ad-cb) \cdot \underset{= 1}{\underbrace{\det \begin{pmatrix} 1 & 0 \\ 0 & 1\end{pmatrix}}}$$
 
> [!Proposición 1.47.]
> Una matriz $A \in M_{2 \times 2}(\mathbb{K})$ es invertible si y sólo si su determinante es distinto de 0. 

**Demostración.** ($\Rightarrow$) Supongamos que $A = \begin{pmatrix}a & b \\ c & d \end{pmatrix}$ es invertible si y solo si $T_A(x) = Ax$ entonces $\mathrm{Im}(T_A) = \mathbb{K}^2$ (es decir es un epimorfismo, visto en [[La Imagen y el Núcleo de una TL]]). Lo que a su vez quiere significar que el rango de la matriz $A$ es 2, es decir tanto las filas como las columnas forman una base en $\mathbb{K}^2$. Entonces, $(a,b), (c,d)$ queremos probar que es una lista de vectores LI. Luego $\exists \lambda_1, \lambda_2 \in \mathbb{K}$ tal que 
$$\lambda_1(a,b) + \lambda_2(c,d) = 0 \implies \begin{cases} \lambda_1a + \lambda_2c = 0 \\ \lambda_1b + \lambda_2 d = 0\end{cases}$$
Podemos dividir la solución del sistema en 2 casos: (1) si $a \neq 0$ y (2) si $a = 0$. 
1. Si $a \neq 0$, supongamos que $\lambda_2 \neq 0$ y que por lo tanto podemos despejar de la primera ecuación $\lambda_1 = - \frac{\lambda_2 c}{a}$ y reemplazarlo en la segunda tal que $- \frac{\lambda_2 c}{a}b + \lambda_2 d = 0 \rightarrow \lambda_2 \Big(\frac{-cb}{a} + d\Big) = 0 \rightarrow \frac{\lambda_2}{a} (ad - cb) = 0 \rightarrow ab-cd = 0$ . Lo cual es lo opuesto a lo que queríamos probar, por lo tanto cuando $\lambda_2 =0 = \lambda_1$ entonces $ab-cd \neq 0$. 
2. Si $a = 0$, veamos que nos queda $\lambda_2 c = 0$. Si $c = 0$, entonces el $\mathrm{rg}(A) \leq 1$ lo cual es un absurdo, así que este caso no puede pasar. Si $c \neq 0$, entonces $\lambda_2 = 0$ y nos queda únicamente $\lambda_1 b = 0$. Por último si $\lambda_1 \neq 0$ nos queda que $b= 0$ y $ab-bc = 0$. Lo cual es lo opuesto a lo que queríamos demostrar, por lo tanto cuando $\lambda_1 = \lambda_2 = 0$ entonces $ad-cb \neq 0$. 
($\Leftarrow$) Suponiendo que $\det(A) = ad-cb \neq 0$ entonces (por lo desarrollado anteriormente) tenemos que $(a,b), (c,d)$ son LI. Luego, tenemos que generan un base y que el rango de la matriz $A$ es 2, por lo tanto es invertible. $\blacksquare$




[^1]: Notemos que para algunos espacios vectoriales, específicamente para las matrices, es necesario definir $f({v}) = {v}^t \cdot {w}$ para poder hacer la multiplicación de matrices.  
[^2]:  No es necesario entender esto ahora mismo, solo piénselo como un producto ya definido que multiplica los elementos del espacio vectorial entre sí, por ejemplo la multiplicación de matrices en el espacio vectorial $M_{m \times n}(\mathbb{K})$ ó el conocido "producto escalar" definido para $\mathbb{R}^3$ y $\mathbb{R}^2$. 

# El determinante
Resulta que para matrices más grandes que $2 \times 2$ es más complicado encontrar la función determinante de la forma en la que lo hicimos en [[Formas bilineales y multilineales]]. Queremos llegar a que existe una **única función determinante** que se aplica para cada matriz $n \times n$. 
Agreguemos la siguiente notación, sea $D$ una función multilineal de matrices $n \times n$ y sea $A \in M_{n \times n}(\mathbb{K})$ ([[Matrices]]) y si $\alpha_1, \dots, \alpha_n$ son una lista de vectores filas de $A$, entonces podemos escribir $D(A) = D(\alpha_1, \dots, \alpha_n)$.  Pero, en ciertas ocasiones, solo estamos trabajando con una fila y las otras se quedan fijas, podemos abreviar por ejemplo para la fila $i$ se cumple $D(c\alpha_i + \alpha_i') = cD(\alpha_i) + D(\alpha_i')$ por abuso de notación. 

> [!Lema 1.]
> **(NEF)** Sea $D: M_{n \times n}(\mathbb{K}) \rightarrow \mathbb{K}$ una función multilineal alternada y sea $A, A' \in M_{n \times n}(\mathbb{K})$ con $A'$ una matriz obtenida al intercambiar las filas $\alpha_i$ con $\alpha_j$ de $A = \alpha_1, \dots, \alpha_i, \dots, \alpha_j, \dots, \alpha_n$, entonces $D(A) = -D(A')$.

**Demostración.** Primero supongamos que $A'$ es obtenida al intercambiar dos filas adyacentes de $A$. En ese caso, por lo que vimos en [[Formas bilineales y multilineales]] en el ejemplo 3 se cumple que $D(A) = -D(A')$, pues $D(\alpha_i, \alpha_j) = - D(\alpha_j, \alpha_i)$. 
Ahora dada la matriz $B$ que es obtenida al intercambiar las filas $i$ y $j$ de $A$, donde $i < j$. Podemos obtener $B$ de $A$ realizando una sucesión de intercambios de pares de filas adyacentes. Empecemos con el intercambio de la fila $i$ con la fila $i+1$ y continuamos hasta que las filas estén una al lado de la otra
$$\alpha_1, \dots, \alpha_{i-1}, \alpha_{i+1}, \dots, \alpha_j, \alpha_i, \alpha_{j+1}, \dots, \alpha_n$$
Esto nos llevó $k = j-i$ intercambios de filas adyacentes. Ahora, movemos a $\alpha_j$ a la $i$-ésima posición usando $k-1$ intercambios. Tal que ahora hemos obtenido a $B$ a partir de $A$ usando $k+(k-1) = 2k-1$ intercambios de filas adyacentes. Entonces,
$$D(B) = (-1)^{2k-1}D(A) = -D(A)$$
La segunda igualdad queda clara pues $2k-1$ es un número impar. $\blacksquare$

La siguiente proposición, nos ayudará a entender que tipos de operaciones sobre las filas de una matriz cambian o no el determinante. Tomemos por ejemplo las 4 operaciones por fila que vimos en [[Sistemas de Ecuaciones Lineales]], nos podemos preguntar _¿Cómo cambian estas a las funciones alternadas?_ como todavía no podemos asegurar que exista una función determinante para cada matriz $n \times n$ procedemos a usar funciones multilineales alternadas, que sabemos que si existen y son fáciles de encontrar.  Por consiguiente, si existe una función determinante y la encontramos, entonces este lema vale también para ella. 

> [!Lema 2. Operaciones por fila sobre funciones alternadas]
> **(NEF)** Sea $D: M_{n \times n} (\mathbb{K}) \rightarrow \mathbb{K}$ una función multilineal alternada. Entonces,
> 1. $D(\alpha_1, \dots, \underset{\text{fila } i}{\underbrace{\vec{0}}}, \dots, \alpha_n) = 0, \; \forall 1 \leq i \leq n$ 
> 2. $D(\alpha_1, \dots, \alpha_i, \dots, \alpha_j, \dots, \alpha_n) = - D(\alpha_1, \dots, \alpha_j, \dots, \alpha_i, \dots, \alpha_n)$
> 3. $D(\alpha_1, \dots, \alpha_i + c\alpha_j, \dots, \alpha_j \dots, \alpha_n) = D(\alpha_1, \dots, \alpha_i, \dots, \alpha_j, \dots, \alpha_n)$
> 4. Si $\alpha_i = \underset{j \neq i}{\sum_{j=1}^n} a_j \alpha_j$, entonces $D(\alpha_1, \dots, \alpha_i, \dots, \alpha_n) = 0$.

**Demostración.** (1) Nos dice que si existe una fila nula en la matriz toda función multilineal alternada nos da 0. Y esto es porque entonces yo puedo sacar a 0 como un escalar que multiplica a toda la fila y por las propiedades de la linealidad sacarlo a fuera. (2) Es un resultado directo del lema 1. (3) Resulta de $$\begin{align}D(\alpha_1, \dots, \alpha_i + c\alpha_j, \dots, \alpha_j, \dots, \alpha_n) & = D(\alpha_1, \dots, \alpha_i, \dots, \alpha_j, \dots, \alpha_n) + c D(\alpha_1, \dots, \alpha_j, \dots, \alpha_j, \dots, \alpha_n) \\ &= D(\alpha_1, \dots, \alpha_i, \dots, \alpha_j, \dots, \alpha_n) \end{align}$$
(4) Resulta de aplicar (3) sucesivamente. $\blacksquare$ 

Notemos que el apartado 4 de la proposición anterior nos dice que si existen filas linealmente dependientes, entonces el determinante vale 0. 

Usando las propiedades del Lema 2 tenemos que usando estas propiedades, podemos simplificar el problema de encontrar como se caracterizan funciones multilineales alternadas de más de $n \geq 2$. Pues usándolas, se puede llegar a que se dependen de funciones más simples, reduciendo la cantidad de filas y columnas sucesivamente. 
Por ejemplo, veamos $f: M_{3 \times 3} (\mathbb{K}) \rightarrow \mathbb{K}$ multilineal alternada tal que $f(Id_3) = 1$. 

El siguiente teorema redefine al determinante como una función **única**.

> [!Teorema 3.47. El determinante es único]
> Para cada $n \in \mathbb{N}$, existe una **única función multilineal alternanda** de $D: M_{n \times n}(\mathbb{K}) \rightarrow \mathbb{K}$ tal que $D(\mathrm{Id}_n) = 1$.

**Demostración. (No entra)** Dada $A \in M_{(n+1) \times (n+1)}(\mathbb{K})$ notemos que $A(i|j) \in M_{n \times n}(\mathbb{K})$ es la matriz que se obtiene _al suprimir la fila $i$ y la columna $j$ de $A$_. 
- **Existencia.** Usando el [[Principio de la inducción]] por $n$. 
	- **(Caso Base)** Para $n=1$, definimos $D: M_{1 \times 1} (\mathbb{K}) \rightarrow \mathbb{K}, D(v) = v$, que es una función multilineal alternada que cumple que $D(1) = 1$.
	- **(Paso Inductivo)** Supongamos que existe $D_n : M_{n\times n}(\mathbb{K}) \rightarrow \mathbb{K}$ multilineal alternada tal que $D_n(Id_n) = 1$. Definamos $D_{n +1}: M_{(n+1) \times (n+1)}\mathbb{K}) \rightarrow \mathbb{K}$ como $$D_{n+1}(A) = \sum_{i=1}^{n+1} (-1)^{i+1} a_{i1}\cdot D_n(A(i|1)) \quad \text{si } A= (a_{jl})_{1 \leq j,l \leq n}$$ Lo que estamos haciendo acá es suprimir la fila $i$ y la columna 1 lo cual genera una matriz $n \times n$, si a cada una de estas la multiplicamos por su respectivo elemento en $A$ de la primera columna. Probemos que es una función multilineal alternada y que $D_{n+1}(Id_{n+1}) = 1$. Primero veamos que es lineal en cada entrada. 
	 Sea $A = (\alpha_1, \dots, \alpha_k, \dots, \alpha_{n+1})$,  $A' = (\alpha_1, \dots, \alpha_k', \dots, \alpha_{n+1})$ y $\lambda \in \mathbb{K}$, tal que $\tilde{A} = (\alpha_1, \dots, \lambda \alpha_k + \alpha_k', \dots, \alpha_{n+1})$. Entonces, $$\begin{align} D_{n+1}(\tilde{A}) &= \underset{i \neq k}{\sum_{i=1}^{n+1}}(-1)^{i+1}a_{i1}D_n(\tilde{A}(i|1)) + (-1)^{k+1}(\lambda a_{k1} + a_{k1}')D_n(\tilde{A}(k|1)) \\
	&= \underset{i \neq k}{\sum_{i=1}^{n+1}}(-1)^{i+1}a_{i1}D_n(A(i|1))  + \underset{i \neq k}{\sum_{i=1}^{n+1}}(-1)^{i+1}a_{i1}D_n(A'(i|1)) \\ & + (-1)^{k+1}\lambda a_{k1} \cdot D_n(A(k|1)) + (-1)^{k+1}a_{k1'} \cdot D_n(A'(k|1)) \\
	& = \lambda D_{n+1}(A) + D_{n+1}(A')\end{align}$$
	Probemos ahora que es alternada. Sea $A = \alpha_1, \dots, \alpha_j, \dots, \alpha_j, \dots, \alpha_{n+1}$ donde la $k$-ésima fila es igual a la $j$-ésima ($k > j$). Entonces, $$D_{n+1}(A) = \underset{i \neq k, i \neq j}{\sum_{i=1}^{n+1}} (-1)^{i+1}a_{1i}D_n(A(i|1)) + (-1)^{j+1}a_{j1}D_n(A(j|1)) + (-1)^{k+1}a_{j1}D_n(A(k|1))$$
	Observemos que la matriz  $A(i|1)$ tiene dos filas iguales, por lo tanto por el lema anterior tenemos que como por hipótesis inductiva $D_n$ es alternada $D_n(A(i|1)) = 0$, luego por el lema anterior ya vimos que $A(j|1)$ y $A(k|1)$ solo difieren en la posición de una fila, ya que las filas $j$ y $k$ son iguales al sacar una nos queda la otra, por lo tanto podemos cambiar de posición en $A(j|1)$ a la fila $j-1$ con la fila $k$ y obtenemos la matriz $A(k|1)$ usando $k-(j-1)$ intercambios de filas. Luego $D_n(A(k|1)) = (-1)^{k-1-j}D_n((A(j|1))$ lo cual podemos reemplazar en $$\begin{align} D_{n+1}(A) &= (-1)^{j+1}a_{j1}D_n(A(j|1)) + (-1)^{k+1}a_{j1} (-1)^{k-1-j}D_n((A(j|1)) \\
	&= ((-1)^{j+1} + (-1)^{2k-j}) a_{1j} D_n(A(1|j)) = 0\end{align}$$
	Por último, probemos que $D_{n+1}$ es una función determinante sabiendo que $D_n$ lo es: 
	$$D(Id_{n+1}) = \sum_{i=1}^{n+1}(-1)^{i+1}(Id_{n+1})_{i1}D_n(Id_{n+1}(i|1)) = (-1)^2 \cdot 1 \cdot D_n(Id_n) = 1$$
- **Unicidad**: Se sigue por inducción en $n$. $\blacksquare$

En teorema anterior no solo nos da la existencia y unicidad del determinante, sino también la formula para obtenerlo. Observemos que si bien sumas las filas para obtener una fórmula del determinante, podríamos haber usado columnas.  
Otro dato que podemos analizar del teorema anterior, es que podríamos haber generalizado que toda función alternada es única con $f(Id_n) = a, a \in \mathbb{K}$. 

> [!Corolario 3.1.47. Formula para el determinante]
> Sea $A \in M_{n \times n}(\mathbb{K})$. Si para cada $r \in \mathbb{N}$, $\det : M_{r \times r}(\mathbb{K}) \rightarrow \mathbb{K}$ denota la función determinante de orden $r$, entonces $$\det (A) = \sum_{i=1}^n (-1)^{i+1}a_{i1}\det(A(i|1)) = \sum_{i=1}^n (-1)^{i+1} a_{1i} \det(A(1|i))$$

## Propiedades del determinante
El determinante es útil para obtener si una matriz es invertible. Si probamos un par de propiedades, podremos obtener si otras matrices son invertibles a partir de solamente tener 1. 

> [!Proposición 4.48. El determinante de la transpuesta]
> Sea $A \in M_{n \times n}(\mathbb{K})$. Entonces $\det(A) = \det(A^t)$

**Demostración.** Probemos la igualdad por inducción en $n$:
- Para $n=1$, no hay nada que probar. 
- Supongamos que vale para $n$ y sea $A = (a_{ij}) \in M_{(n+1) \times (n+1)}(\mathbb{K})$. Entonces, $$\begin{align} \det(A^t)  & =  \sum_{i=1}^{n+1} (-1)^{i+1} (A^t)_{i1}\det(A^t(i|1)) = \sum_{i=1}^{n+1} (-1)^{i+1} a_{1i} \det(A(1|i))  = \det (A)\end{align} $$
Que es a lo que queríamos llegar. $\blacksquare$ 

Queríamos ahora ver que ocurre cuando a la matriz $n \times n$  

> [!Proposición 5.49.]
> Sea $A = (a_{ij}) \in M_{n \times n}(\mathbb{K})$ una matriz triangular superior. Entonces $\det(A) = \prod_{i=1}^n a_{ii}$.

**Demostración.** Probaremos la validez de la fórmula por inducción en $n$. Para $n = 1$, no hay nada que hacer. Supongamos que vale para $n$ y sea $A = (a_{ij}) \in M_{(n+1) \times (n+1)}(\mathbb{K})$ una matriz triangular superior. Entonces, $$\det(A) = \sum_{i=1}^{n+1}(-1)^{i+1} a_{i1}\det(A(i|1)) = a_{11}\det(A(1|1)),$$
puesto que en la primera fila el único valor que no es 0 es el primero. Luego, la matriz $A(1|1) \in M_{n \times n}(\mathbb{K})$ es triangular superior y entonces, por hipótesis inductiva, $\det (A(1|1)) = \prod_{j=1}^n (A(1|1)) = \prod_{i=2}^{n+1} a_{ii}$. En consecuencia,
$$\det(A) = a_{11}\det(A(1|1)) = \prod_{i=1}^{n+1} a_{ii}$$
que es lo que quería probar. $\blacksquare$ 

Existen otras formas para el determinante además de la expuesta en el corolario 3.1. En ciertas ocasiones no siempre es conveniente tomar la primera fila (o columna) para poder obtener el determinante, a veces es conveniente tomar otra columna $j$ o fila $j$. Si cambiamos la fila $1$ por la fila $j$ podemos obtener una formula más general. Tal que $$\begin{align} \det(A) & = (-1)^{j-1} \det (\alpha_{j}, \alpha_1, \dots, \alpha_{j-1}, \alpha_{j+1}, \dots, \alpha_n ) \\ & = (-1)^{j-1}\Big( \sum_{j=1}^{n} (-1)^{1+i} a_{ij} \det(A(i|j)) \Big) \\ & = \sum_{j=1}^n (-1)^{i+j} a_{ij} \det(A(i|j)) \end{align}$$
> [!Proposición 6.50. El producto de determinantes]
> Sean $A, B \in M_{n \times n}(\mathbb{K})$. Entonces, $\det (A \cdot B) = \det(A) \cdot \det(B)$ 

**Demostración.** Se define $D: M_{n \times n}(\mathbb{K}) \rightarrow \mathbb{K}$ como $D(X) = \det(X \cdot A)$. Nuestro objetivo es probar que para cada $B \in M_{n \times n}(\mathbb{K})$ se tiene que $D(B) = \det B \cdot \det A$. Probemos que la función $D$ es multilineal alternada y calculamos su valor en $Id_n$:
1. Para $i$ con $1 \leq i \leq n$, y sea $\lambda \in \mathbb{K}$ 
$$\begin{align} D(\alpha_1, \dots, \lambda \alpha_i + \alpha_i', \dots, \alpha_n) &= \det ((\alpha_1, \dots, \lambda \alpha_i + \alpha_i', \dots, \alpha_n) \cdot A) \\
  &= D(A\alpha_1, \dots, \lambda A\alpha_i + A\alpha_i', \dots, A\alpha_n) \\
  &= \lambda \det(A\alpha_1, \dots, A\alpha_i, \dots, A\alpha_n) + \det(A\alpha_1, \dots, A\alpha_i, \dots, A\alpha_n) \\
  &= \lambda D(\alpha_1, \dots, \alpha_i, \dots, \alpha_n) + D(\alpha_1, \dots, \alpha_i', \dots, \alpha_n)\end{align}$$
  2. Probemos que es alternada, para cada $1 \leq i \leq n$ 
$$\begin{align} D(\alpha_1, \dots, \alpha_i, \dots, \alpha_i, \dots, a_n) &= \det((\alpha_1, \dots, \alpha_i, \dots, \alpha_i, \dots, \alpha_n) \cdot A) \\
&= \det(A\alpha_1, \dots, A\alpha_i, \dots, A\alpha_i, \dots, A\alpha_n) = 0 \end{align}$$
3. Por último, $D(Id_n) = \det(I_n \cdot A) = \det(A)$. 

Entonces por la unicidad de las funciones alternadas (Teorema 3) tenemos que la función $D$ es única y que por lo tanto $D(B) = \det(A) \cdot \det(B)$ para todo $B \in M_{n \times n}(\mathbb{K})$. $\blacksquare$ 

Por último, estamos listos para demostrar que para que una matriz $n \times n$ sea invertible es necesario que su determinante sea distinto de 0. 

> [!Proposición 7.51. El determinante para Matrices Invertibles]
> Sea $A  \in M_{n \times n} (\mathbb{K})$. Entonces, $A$ es invertible si y sólo si $\det A \neq 0$. 

**Demostración.** ($\Rightarrow$) Supongamos que $A \in M_{n \times n}(\mathbb{K})$ es invertible. Entonces existe una matriz $B \in M_{n \times n}(\mathbb{K})$ tal que $A \cdot B = Id_n$. Aplicando el resultado de la proposición 6 se obtiene que $$1 = \det(Id_n) = \det(A \cdot B) = \det(A) \cdot \det(B)$$
de donde se deduce que $\det A \neq 0$.
($\Leftarrow$) Si $\det(A) \neq 0$, entonces las columnas de $A$ son LI  (Lema 2) por lo tanto es invertible. $\blacksquare$

> [!Corolario 7.1.51.]
> Si $\det A \neq 0$ entonces $\det A^{-1} = \frac{1}{\det A}$.
 

# Autovalores y Autovectores
En [[Cambio de Base y Rango de una matriz]] nos concentramos en las [[Matrices Invertibles]], que pertenecen al conjunto de matrices cuadradas $M_{n \times n} (\mathbb{K})$. Ya definimos que existe un claro isomorfismo entre $M_{n \times n}(\mathbb{K})$ y $\mathrm{Hom}(V,V)$ ( con $V$ de dimensión $n$, proposición 4 de [[Matrices de Transformaciones Lineales]]). Por lo tanto, hablar de matrices cuadradas es lo mismo que hablar de transformaciones lineales de espacio vectorial a sí mismo, estas tienen un nombre especial, se llaman **operadores lineales**.
Desde ahora en adelante trabajaremos con  $\mathbb{K} = \mathbb{R}$ y $\mathbb{K} = \mathbb{C}$. 

> [!Operador Lineal]
> #Definición Sea $V$ un $\mathbb{K}$[^1]-espacio vectorial. Una transformación lineal de un espacio vectorial a sí mismo, es decir toda $T : V \rightarrow V$, es llamada _operador lineal_. La notación $\mathrm{Hom(V)}$ denota al conjunto de todos los operadores en $V$.

Al igual que no toda matriz cuadrada es invertible, no todo operador lineal es un isomorfismo (es decir, tiene inversa). Observemos que al trabajar con operadores lineales, el corolario 1.1 del [[Teorema de la dimensión]] vale siempre para espacios vectoriales finitos. 

## Subespacios Invariantes
Supongamos que ya sabemos de antemano que $V = U_1 \oplus \dots \oplus U_m$, es decir que el espacio vectorial $V$ se puede separar en $m$ subespacios con una [[Suma de subespacios]] directa.  Entonces, para entender el comportamiento de un operador lineal $T: V \rightarrow V$ solo necesitamos entender cada $T|_{U_j}$, donde $T|_{U_j}: U_j \rightarrow V$ para cada $j = 1, \dots, m$. Tratar con $T|_{U_j}$ debería ser más sencillo que trabajar con $T$ pues $U_j$ es un espacio vectorial más chico que $V$. 
Sin embargo, es obvio que no siempre $T|_{U_j}$  va darnos valores dentro de $U_j$, en otras palabras, puede que $T|_{U_j}$ no sea un operador sobre $U_j$. Se pueden obtener resultados muy utiles en el caso en el que sí lo sea. Esto inspira el concepto de  **subespacio invariante**. 

> [!Subespacio Invariante]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial. Supongamos $T: V \rightarrow V$. Un subespacio $U$ de $V$ es llamado _invariante_ si para cada $u \in U$ ocurre que $T(u) \in U$. 

El siguiente ejemplo muestra la utilidad de esta definición. 

---
**Ejemplo 1.** Sea $V = \mathbb{R}^2$ con su base canónica $\{e_1, e_2\}$ y supongamos $T \in \mathrm{Hom}(\mathbb{R}^2)$ dada por $T(e_1) = (2,0)$ y $T(e_2) = (1,1)$. Tal que entonces su matriz transformación lineal sea $[T]_E = \begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix}$ y su imagen está generada por $\mathrm{Im}(T) = <(2,0), (1,1)>$. Notemos que el plano cartesiano se puede separar en $\mathbb{R}^2 = U_1 \oplus U_2$ con $U_1 = <e_1>$ y $U_2 = <e_2>$. Notemos que $<e_1>$ genera el eje $x$ tal que $<e_1> = \{x(1,0), \; x \in \mathbb{R}\}$  y alplicarle la transformación tenemos que se genera $<(2,0)>$ sigue siendo el eje $x$, lo único que hicimos fue *multiplicar al vector de la base canónica por $2$ lo cual no modifica el subespacio generado*. Por lo tanto $T|_{U_1} U_1 \rightarrow U_1$, $U_1 = <e_1>$ es un subespacio invariante. Sin embargo, $U_2$ no es un subespacio invariante pues al aplicar la transformación sobre $y(0,1), \forall y \in \mathbb{R}$ (que es el eje $y$) genera $y(1,1), \forall y \in \mathbb{R}$ que ya no es el mismo subespacio, por lo tanto $T|_{U_2} : U_2 \nrightarrow U_2$. 

---

Otros ejemplos de subespacios invariantes son $\{0\}$, $V$, $\mathrm{Nu}(T)$ y $\mathrm{Im}(T)$. 

Resulta que si observamos otras transformaciones lineales, notaremos que los subespacios invariantes ocurren cuando la única modificación que yo le hago a un vector de mi base es _multiplicarlo por un escalar_. Tomemos cualquier $v \in V$ con $v \neq 0$ y sea $U$ un subespacio con todos los múltiplos escalares de $V$: $U = \{\lambda v : \lambda \in \mathbb{K}\} = <v>$. Entonces, $U$ es un subespacio de $V$ de una dimensión. Si $U$ es invariante bajo el operador $T: V \rightarrow V$, luego $T(v) \in U$ por lo tanto existe un escalar $\lambda \in \mathbb{K}$ tal que 
$$T(v) = \lambda v$$
Cuando esto ocurre en operadores, llamamos a los vectores que cumplen esto **autovectores** y a las escalares que los acompañan **autovalores**.

> [!Autovalor y autovector] 
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial y $T: V \rightarrow V$ un operador lineal. Un escalar $\lambda \in \mathbb{K}$ es llamado _autovalor_ de $T$ si existe un $v \in V$ llamado _autovector_ tal que $v \neq 0$ y $T(v) = \lambda v$.

Notemos que $v \neq 0$ pues todo escalar cumple $T(0) = \lambda 0$, sin embargo nada impide que $\lambda = 0$.  

La siguiente proposición habla sobre como encontrar autovalores:
> [!Proposición 1. Condiciones equivalentes para ser un autovalor]
> **(NEF)** Supongamos $V$ un $\mathbb{K}$-espacio vectorial de dimensión finita, $T: V \rightarrow V$ un operador lineal y $\lambda \in \mathbb{K}$. Recordemos que $Id: V \rightarrow V$ es la transformación identidad. Entonces las siguientes son equivalentes:
> 1. $\lambda$ es un autovalor de $T$.
> 2. $T-\lambda  \cdot Id$ no es un monomorfismo.
> 3. $T- \lambda \cdot Id$ no es un epimorfismo.
> 4. $T- \lambda \cdot Id$ no es un isomorfismo y por lo tanto no es invertible.

**Demostración.** Las condiciones (1) y (2) son claramente equivalentes pues si $\lambda$ es un autovalor esto significa que existe un $v \in V$ tal que $T(v) = \lambda v \rightarrow T(v) - Id(\lambda v) = 0 \rightarrow (T- \lambda \cdot Id)(v) = 0$. Luego, (2), (3) y (4) son equivalentes por el corolario 1.1 del [[Teorema de la dimensión]].  $\blacksquare$ 

De esta manera, como $T(v) = \lambda v$ si y solo si $(T - \lambda Id)(v) = 0$, entonces tenemos que todos los autovectores de $V$ que corresponden al autovalor $\lambda$ viven en $\mathrm{Nu}(T- \lambda Id)$. Y encontramos nuestra primera manera de obtener autovalores y autovectores, si $\dim( \mathrm{Nu}(T- \lambda Id)) \neq 0$ entonces $\lambda$ es un autovalor de $T$. Otra forma de verlo es pasando las transformaciones a sus respectivas matrices, tal que $[T]_{B_1B_2}$ es la matriz de la transformación lineal, entonces $\lambda$ es un autovalor si $\det([T]_{B_1B_2} - \lambda Id_n) = 0$, pues en ese caso la matriz $[T]_{B_1B_2}- \lambda Id_n$ no es invertible. Sin embargo, quedemos por ahora con nuestra definición inicial y tratemos de dejar de lado el determinante por ahora. 

Al subespacio $\mathrm{Nu}(T- \lambda Id)$ es tan especial que le damos su propio nombre. 
> [!Autoespacio]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial y sea $T: V \rightarrow V$ un operador lineal con un autovalor $\lambda \in \mathbb{K}$ . El _autoespacio_ correspondiente a $\lambda$ es un espacio vectorial tal que $$E(\lambda, T) = \mathrm{Nu}(T- \lambda Id)$$ 

Es claro que los autoespacios son subespacios de $V$, pues el núcleo de $T- \lambda Id$ lo es.

---
**Ejemplo 2.** Sea $T : \mathbb{K}^2 \rightarrow \mathbb{K}^2$ está definida por $T(w,z) = (-z, w)$. Queremos encontrar todos los autovalores y autovectores tomando $\mathbb{K} = \mathbb{R}$ y luego $\mathbb{K} = \mathbb{C}$. 

Notemos primero que la transformación $T$ representa una rotación de 90° de forma antihoraria sobre el origen en $\mathbb{R}^2$. **Un operador tiene un autovalor si y solo si hay un vector no nulo en su dominio que es llevado por el operador a un múltiplo escalar de sí mismo**.  Entonces para encontrar autovalores de $T$, debemos encontrar escalares $\lambda$ tales que $T(w,z) = \lambda (w,z)$ tiene otra solución que no sea $w=z= 0$. Lo cual es equivalente al sistema de ecuaciones $-z = \lambda w$ y $w = \lambda z$. Sustituyendo el valor de $w$ dado por la segunda ecuación en la primera nos da $-z = \lambda^2 z$ o $(\lambda^2 +1)z = 0$ como $z$ no puede ser igual a 0 (pues entonces esto implicaría que $w = 0$) tenemos que $\lambda^2 +1 = 0$. 

Veamos que para $\mathbb{K} = \mathbb{R}$ no existe solución para esta ecuación, lo cual tiene sentido pues implicaría que no existen vectores sobre una línea que se vean multiplicados por un escalar al producir una rotación de $90°$. Sin embargo, si existe una solución para $\mathbb{K} = \mathbb{C}$ y es $\lambda = i$ ó $\lambda = -i$. Luego, se pueden obtener los autoespacios de $\lambda = i$, $\mathrm{Nu}(T- (i)Id) = \{(-z,w) + (iw, iz), \; \forall z, w \in \mathbb{C}\} = <(-1,i), (i, 1)> = <(-1,i)>$ y lo mismo con $\lambda = -i$.  

---
> [!Lema 2. Autovectores linealmente independientes]
> **(NEF)** Sea $T: V \rightarrow V$ un operador lineal. Supongamos $\lambda_1, \dots, \lambda_m$ es una lista de autovalores distintos de $T$ y sean $v_1, \dots, v_m$ sus correspondientes autovectores (uno de cada autovalor). Entonces, $v_1, \dots, v_m$ son linealmente independientes.

**Demostración.** Usa el lema 2 de [[Independencia Lineal]] y se inicia pensando por el absurdo que los vectores son LD. $\blacksquare$ 

> [!Corolario 2.1. el número de autovalores]
> **(NEF)** Supongamos que $V$ es un espacio vectorial de dimensión infinita. Entonces, cada operador lineal en $V$ tiene como máximo $\dim V$ autovalores distintos.

**Demostración.** Sea $T: V \rightarrow V$ un operador lineal con $\lambda_1, \dots, \lambda_m$  autovalores distintos entre sí. Sean $v_1, \dots, v_m$ son sus correspondientes autovectores y por la proposición son LI, entonces por la proposición 1 de [[Independencia Lineal]] tenemos que $m \leq \dim V$. $\blacksquare$ 

Un resultado muy interesante que podemos probar es **la existencia de los autovalores en $\mathbb{C}$**. Resulta, que al calcular los autovalores siempre tengo que encontrar las raíces de un polinomio, como hicimos en el ejemplo 2. Ahora, no siempre existen soluciones para estos polinomios en $\mathbb{R}$ pero podemos estar seguros de que existe al menos una solución en $\mathbb{C}$ gracias al [[Teorema Fundamental del Álgebra]]. Este teorema, plantea justamente que todo polinomio de grado $m$ en los complejos tiene como máximo $m$ raíces. 

## Diagonalización
Uno de los principales objetivos del Álgebra 2 es mostrar que dado un operador $T: V \rightarrow V$, existe una base de $V$ con respecto a la cual $T$ tiene una matriz razonablemente simple. Esto es porque si bien las [[Matrices de Transformaciones Lineales]] nos simplificaron bastante el entendimiento de las transformaciones lineales, algunas matrices siguen siendo muy complicadas de operar (sobre todo si tienen muchas filas y columnas). Pero vamos a ver que si encontramos la base correcta para expresar la matriz, podemos hacerla mucho más simple, tal que obtener información de ella sea muy simple. 
Notemos que la forma de matriz más simple, es claramente una matriz diagonal. 

> [!Matriz diagonal]
> #Definición La matriz _diagonal_ es una matriz cuadrada $n \times n$ tal que las entradas en la diagonal principal sean las únicas no nulas, es decir $a_{ii} \neq 0, \forall i = 1, \dots, n$ pero $a_{ij} = 0$ para $i \neq j$. 

Empecemos ahora nuestro intento para encontrar una forma de encontrar una base tal que al expresar $[T]_B$ sea una matriz diagonal. Empecemos definiendo lo siguiente. 

> [!Matrices semejantes]
> #Definición Dadas $A, B \in M_{n \times n}(\mathbb{K})$ se dicen semejantes y se denota $A \sim B$ si $\exists C \in GL(n, \mathbb{K})$ (el conjunto de [[Matrices Invertibles]]) tal que $B = CAC^{-1}$

Esta definición tiene sentido, pues multiplicar de ambos lados a una matriz por matrices invertibles no modifica su rango, por lo visto en [[Cambio de Base y Rango de una matriz]]. Se puede probar que la relación semejanza de matrices $\sim$ es una relación de equivalencia ([[Relaciones entre conjuntos]]). Esta definición viene de expresar a un mismo operador en diferentes bases, al hacerlo no modifico la dimensión de la imagen, ni la del núcleo. Entonces, esto motiva la siguiente prueba

> [!Proposición 3.52. Matrices semejantes son un mismo operador en diferentes bases]
> Sean $A, B \in M_{n \times n}(\mathbb{K})$. Tenemos que $A \sim B$ si y sólo si existe un único operador lineal $T: \mathbb{K}^n \rightarrow \mathbb{K}^n$ con bases $B_1, B_2$ de $\mathbb{K}^n$ tal que $[T]_{B_1} = A$ y $[T]_{B_2} = B$.

**Demostración.** ($\Leftarrow$) Usando la proposición 2 de [[Cambio de Base y Rango de una matriz]] para pasar de la matriz transformación $[T]_{B_1}$ a la matriz $[T]_{B_2}$ usamos la matriz cambio de base $C(B_1,B_2)$ tal que $[T]_{B_2} = C(B_1, B_2)[T]_{B_1}C^{-1}(B_1,B_2)$. Eligiendo $C= C(B_1,B_2)$ y sabiendo que $A = [T]_{B_1}$ y $B= [T]_{B_2}$ entonces $B = CAC^{-1}$. 
($\Rightarrow$) Supongamos existe una matriz $C$ tal que $B = CAC^{-1}$ tomando $B_1 = E$ (la base canónica) y $B_2$ como las columnas de la matriz $C$, tenemos que $C = C(B_1, B_2)$ es la matriz cambio de base. Definimos $T: \mathbb{K}^n \rightarrow \mathbb{K}^n, \; T(v) = Av$, entonces veamos luego que la matriz asociada a la TL en la base canónica es $A = [T]_{B_1}$, luego la matriz $B$ por la proposición 2 de [[Cambio de Base y Rango de una matriz]] es igual a la matriz $[T]_{B_2}$ tal que $[T]_{B_2} = C(B_1, B_2)[T]_{B_1} C^{-1}(B_1, B_2)$. $\blacksquare$ 


[^1]: 

