# Sistemas de ecuaciones lineales en congruencias
En [[Ecuación Lineal en Congruencia]] vimos como resolver la ecuación $ax \equiv b \;(n)$ o su equivalente $[a][x]  =[b]$ en cualquier $\mathbb{Z}_n$. Nos podemos preguntar, _¿Cómo hacemos para resolver ecuaciones con un módulo muy grande al cual no podemos reducir?_ Por ejemplo, veamos la ecuación $13x \equiv 71 \; (380)$ no se puede reducir pues $(13,380) = 1$ y sabemos que tiene solución pues $1|71$. En estos casos, nos conviene usar el siguiente teorema:

> **Teorema.** Sea $n$ un entero con una factorización $n= p_1^{e_1} p_2^{e_2} \cdots p_k^{e_k}$ donde $p_1, p_2, \dots, p_k$ son primos todos distintos entre si. Entonces, para cualquier entero $a \equiv b \; (n)$ si y solo si $a \equiv b \; (p_i^{e_i})$ para cada $i \in \{1, 2, \cdots, k\}$.  

**Demostración.** ($\Rightarrow$) Este teorema es una extensión del teorema de "producto de modulos" visto en [[Congruencia de Enteros]]. Para demostrarlo veamos que 
$$ax \equiv b \; (n) \iff n|ax-b \Rightarrow ny = ax-b, \; y \in \mathbb{Z} \Rightarrow b = ax + n(-y)$$
Como $n= p_1^{e_1} p_2^{e_2} \cdots p_k^{e_k}$ podemos reemplazar en 
$$b = ax + (p_1^{e_1} p_2^{e_2} \cdots p_k^{e_k})(-y) \Rightarrow b = ax + p_1^{e_1}\underbrace{(-y(p_2^{e_2} \cdots p_k^{e_k}))}_{\; \in \; \mathbb{Z}}$$
Luego $p_1^{e_1}|ax-b \Rightarrow ax \equiv b \; (p_1^{e_1})$ y podemos repetir este proceso para todo $p_i^{e_i}$. 
Para probar ($\Leftarrow$ ) usamos el colorario de "producto de modulos" tal que si $a \equiv b \; (p_1^{e_1})$, $a \equiv b \; (p_2^{e_2}), \quad \cdots \quad, a \equiv b \; (p_k^{e_k}) \implies a \equiv b \; (n)$. $\blacksquare$ 

Entonces, usando este teorema puedo dividir la ecuación anterior $13x \equiv 71 \; (380)$ (como $380 = 2^2 \cdot 5 \cdot 19$) en tres ecuaciones más sencillas: 
$$13x \equiv 71 \; (4) \quad 13x \equiv 71 \; (5) \quad 13x \equiv 71 \; (19)$$
Sin embargo, tendríamos que resolver estas tres ecuaciones **simultaneamente**. Es decir, en todas tiene que ser la misma clase de congruencia $[x]$ pero en módulos diferentes. Sin embargo desconocemos como hacer esto, veamos en primera intancia como resolver un **sistema de ecuaciones lineales en congruencia** para 2 ecuaciones. 

> **Teorema.** Sean $b_1, b_2 \in \mathbb{Z}, \; n_1, n_2 \in \mathbb{N}$ ([[Z]]). Entonces el sistema de ecuaciones en congruencia $$\begin{cases}
 x \equiv b_1 \; (n_1) \\
 x \equiv b_2 \; (n_2)
 \end{cases}$$Tiene solución entera si y sólo si $(n_1, n_2) | (b_1 - b_2)$. Sea  $x_0$ una solución particular, entonces el conjunto de soluciones está dado por $$\{x = x_0 + k[n_1, n_2], \; k \in \mathbb{Z}, \; x_0 \text{ solución particular} \}$$
 
**Demostración.**
- ($\Rightarrow$) Sea $x_0$ la solución entera del sistema 
  $$\begin{cases}
   x \equiv b_1 \; (n_1) \\
   x \equiv b_2 \; (n_2)
   \end{cases} 
   \implies n_1 | x_0 - b_1 \;\;\; n_2 | x_0 - b_2$$
   Como $(n_1, n_2)|n_1$ y $(n_1, n_2)|n_2 \implies (n_1, n_2) | x_0 - b_1$ y $(n_1, n_2) | x_0 - b_2$ $\implies (n_1, n_2) | (x_0 - b_1) -  (x_0 - b_2) \implies (n_1, n_2) | b_1 - b_2$. Que era a lo que queríamos llegar.
 - ($\Leftarrow$) Supongamos que $(n_1, n_2) | b_1 - b_2$ encontremos una solución al sistema de ecuaciones. Si planteamos la ecuación en congruencia.  $$n_1x \equiv b_1 - b_2 \; (n_2)$$
   Esta ecuación tiene solución por el teorema ya visto. Sea $h \in \mathbb{Z}$ una solución de esta ecuación. Luego, $n_1h - (b_1 -b_2) = n_2 k, \; k \in \mathbb{Z}$ $\implies n_1 h - b_1 + b_2 = n_2 k \implies b_2 - n_2 k = b_1 - n_1 h  \implies x_0$ (denotamos a ambos números de esta forma).
   $$\begin{cases}
   x_0 - b_1 = -n_1 h \\
   x_0 - b_2 = -n_2 k
   \end{cases} 
   \implies 
   \begin{cases}
   x_0 \equiv b_1 \; (n_1) \\
   x_0 \equiv b_2 \; (n_2)
   \end{cases} $$
   De esta manera $x_0$ es una solución del sistema. Ahora comprobemos que todos los $x = x_0 + k[n_1, n_2], \; k \in \mathbb{Z}$ son soluciones del sistema. 
   $$\begin{align}
   k[n_1, n_2] \equiv 0 \; (n_1) \\
   k[n_1, n_2] \equiv 0 \; (n_2)
   \end{align}$$
   Pues $n_1 | [n_1, n_2]$ y $n_2 | [n_1, n_2]$. De esto concluimos que $x_0 + k[n_1, n_2] \equiv b_1 + 0 \; (n_1) \equiv b_1 \; (n_1)$ y $x_0 + k[n_1, n_2] \equiv b_2 + 0 \; (n_2) \equiv b_2 \; (n_2)$. 
   Sean $x_1$ y $x_2$ son dos soluciones del sistema de ecuaciones. 
   $$
   \begin{cases}
   x_1 \equiv b_1 \; (n_1) \\
   x_1 \equiv b_2 \; (n_2)
   \end{cases}
   \;\;\text{ y } \;\;
   \begin{cases}
   x_2 \equiv b_1 \; (n_1) \\
   x_2 \equiv b_2 \; (n_2)
   \end{cases}
   \implies
   \begin{cases}
   x_1 - x_2 \equiv 0 \; (n_1) \\
   x_1 - x_2 \equiv 0 \; (n_2)
   \end{cases}$$
   Entonces, $n_1 | x_1 - x_2$ y $n_2 | x_1 - x_2$. Notemos que como $x_1 - x_2$ es un múltiplo de $n_1$ y $n_2$, la definición de mcm dice que $[n_1, n_2] | (x_1 - x_2)$ ((2) condición para que un número sea el mcm de dos números). Entonces existe un $k' \in \mathbb{Z}$ tal que $x_1 - x_2 = k'[n_1, n_2]$. De tal manera que $x_1 = x_2 + k'[n_1, n_2]$.  $\blacksquare$ 

Sabiendo esto podemos concluir que sistemas como 
$$\begin{cases} 
x \equiv 3 \; (9) \\
x \equiv 2 \; (6)
\end{cases}$$
No tienen solución pues $mcd(9,6) = 3$ y $3 \nmid 3-2$. Lo cual tiene sentido pues si sabemos $x \equiv 3 \; (9)$ por lo cual $x$ es divisible por 3 y que $x \equiv 2 \; (6)$ significa que $x$ no divide a 3. 
Sin embargo, en nuestro problema inicial buscamos resolver un sistema de 3 ecuaciones. En estos casos podemos hacer un teorema parecido al anterior que resuelva este tipo de sistemas, pero nos conviene generalizarlo para poder resolver cualquier sistema de $k$ ecuaciones. 

---

## Teorema Chino del Resto (TCR)[^1]
>**Teorema. (Del Resto Chino)** Sean $b_1, b_2, \dots, b_r \in \mathbb{Z}$ y $n_1, n_2, \dots, n_k \in \mathbb{Z}$ son enteros positivos tal que $(n_i, n_j) = 1$, $\forall \; i \neq j, \; i, j \in \{1, 2, \dots, k\}$. Entonces las soluciones del sistema de ecuaciones  $$
\begin{cases} x \equiv b_1 \; (n_1) \\
   x \equiv b_2 \; (n_2) \\
   \vdots \\
   x \equiv b_k \; (n_k)
   \end{cases}$$ Forman una única clase de congruencia $\mod (N)$ donde $N = n_1 n_2 \dots n_k$. Y el conjunto de soluciones está dado por $$\Big\{x = x_0 + r \cdot N, \; r \in \mathbb{Z}, \; x_0 \text{ es una solución particular} \Big\}$$Donde $x_0$ es una solución particular del sistema que satisface $0 \leq x_0 \leq N$. 
 

**Demostración.**
Denotemos $N_i = \frac{N}{n_i}$, y veamos que es obvio pensar que $(N_i, n_i) = 1$. Por un teorema visto en [[Máximo Común Divisor]] existe un $x_i$ y un $y_i$ con los cuales podemos escribir $N_i x_i + n_i y_i = 1$.  Luego, $N_i x_i \equiv 1 \; (n_i)$ tiene como solución una sola clase de congruencia $[x_i]$ en $\mod (n_i)$.  Definamos el entero $$x_0 = (N_i b_i)x_i + (N_2 b_2)x_2 + \dots + (N_k b_k)x_k$$y veamos que satisface simultaneamente todas las congruencias, es decir, $x_0 \equiv b_i \; (n_i)$ para cada $i$. Para ver esto, notemos que $N_j$ (diferente a $N_i$) es divisible por $n_i$, entonces $b_jN_jx_j \equiv 0 \; (n_i)$ y por lo tanto $x_0 \equiv b_i N_i x_i \equiv b_i \; (n_i)$; pues $N_ix_i \equiv 1 \; (n_i)$. Con lo cual llegamos a la conclusión de que $x_0$ resuelve cualquiera de las ecuaciones en el sistema y es una solución particular ya que se encontra entre $0 \leq x \leq N$. 
Entonces, ahora que tenemos una solución que es la clase $[x_0]_N$, demostremos que es la única. Supongamos que $x_1$ es otra solución:
$$\begin{cases}
   x_0 \equiv b_1 \; (n_1) \\
   x_0 \equiv b_2 \; (n_2) \\
   \vdots \\
   x_0 \equiv b_k \; (n_k)
   \end{cases}
   \;\;\; \text{ y } \;\;\;
  \begin{cases}
   x_1 \equiv b_1 \; (n_1) \\
   x_1 \equiv b_2 \; (n_2) \\
   \vdots \\
   x_1 \equiv b_k \; (n_k)
   \end{cases}$$
Restemos cada ecuación con su par y obtenemos:
$$\begin{cases}
   x_0-x_1 \equiv 0 \; (n_1) \\
   x_0-x_1 \equiv 0 \; (n_2) \\
   \vdots \\
   x_0-x_1 \equiv 0 \; (n_k)
   \end{cases}
   \implies
   n_1|x_0-x_1 ,\; n_2|x_0-x_1, \; \cdots \;, n_k| x_0-x_1
   $$
Luego, como todos los $n_i$ son coprimos entre sí $n_1 n_2 \dots n_k \mid x_0 - x_1$. Por último, nos queda que 
$$n_1 \cdot n_2 \; \dots \; \cdot n_k \mid x_0 - x_1 \implies N | x_0 -x_1 \implies x_1 \equiv x_0 \; (N)$$
Lo cual comprueba que $[x_0]_N = [x_1]_N$ y entonces la solución es única. $\blacksquare$ 

A partir de esto, podemos ver que el primer teorema que vimos al principio de esta nota sale como un colorario de este teorema (pues en la factorización de primos es obvio que cada uno de las factorizaciones es coprimo con las otras). 

Y ahora podemos resolver nuestro problema incial de $13x \equiv 71 \; (380)$.  Veamos que $71 \equiv 3 \; (4)$, $71 \equiv 1 \; (5)$ y $71 \equiv 14 \equiv -5 \; (19)$, también $13 \equiv 1 \; (4)$ y $13 \equiv 3 \; (5)$. Reemplazando esto en las tres ecuaciones que teníamos (usando las propiedades vistas en [[Congruencia de Enteros]]), nos quedan más simplificadas: 
$$\begin{cases}
x \equiv 3 \; (4) \\
3x \equiv 1 \; (5) \\
13x \equiv -5 \; (19)
\end{cases}$$
Primero, veamos que tendríamos que lograr que cada ecuación por separado quede de la forma $x \equiv b_i \; (n_i)$ para poder aplicar el teorema. Tenemos que multiplicar en todas ellas por el inverso de la clase $[a_i]$ en cada módulo. 

Notemos que en la primera ecuación ya la simplificamos para que nos quede de la forma que queríamos. En la segunda tenemos que múltiplicar de ambos lados por el inverso de $[3]$, que debe existir por un teorema visto en [[Enteros Modulares]], pues $(3,5)=1$.  Como $[3]_5[2]_5 = [6]_5 = [1]_5$ el inverso de $[3]$ es $[2]$, entonces $2 \cdot 3x \equiv 1 \cdot 2 \; (5) \rightarrow x \equiv 2 \; (5)$. Por último, para encontrar el inverso de $[13]_{19}$ es un poco más complicado (sabemos que existe pues $(13,19) = 1$), vamos a usar el algoritmo de euclides extendido (visto en [[Máximo Común Divisor]]) para formar una combinación lineal que nos dé el inverso:  
$$\begin{align}
19 & = 13(1) + 6 \\
13 & = 6(2) + \boxed{1} \\
6 & = 1(6) +  0 & \rightarrow \quad 1 & = 13 + 6(-2) \\
\; & \; & 1 & = 13 + (-2)(19+13(-1)) \\
\; & \; & 1 & = 13 + 19(-2) + 13(3) \\
\; & \; & 1 & = 13(3) + 19(-2) & \rightarrow \quad 19\mid 1-13(3) \\
\; & \; & \; & \; & 13(3) \equiv 1 \; (19) \\
\end{align}$$
Entonces, si multiplicamos de ambos lados por $[3]_{19}$ tal que $3 \cdot 13x \equiv -5 \cdot 3 \; (19)$ lo cual nos da $x \equiv -15 \equiv 4 \; (19)$. De esta manera, tenemos el siguiente sistema
$$\begin{cases}
x \equiv 3 \; (4) \\
x \equiv 2 \; (5) \\
x \equiv 4 \; (19)
\end{cases}$$
Y ahora sí podemos aplicar el teorema del resto chino. Encontremos la solución particular
$x_0 = (N_1 b_1)x_1 + (N_2 b_2)x_2 + (N_3 b_3)x_3$, sabiendo que $b_1 = 3, \; b_2 = 2$ y $b_3 = 4$, y que $N_1 = 5 \cdot 19 = 95$, $N_2 = 4 \cdot 19 = 76$ y $N_3 = 4 \cdot 5 = 20$. 
Luego, necesitamos encontrar las soluciones particulares de $95x_1 \equiv 1 \; (4)$, $76x_2 \equiv 1 \; (5)$ y $20x_3 \equiv 1 \; (19)$. La solución de la primer ecuación se puede reducir a $95x_1 \equiv 3x_1 \equiv 1 \; (4)$ notemos que el inverso de la clase $[3]_4$ es sí mismo (pues $[3]_4 [3]_4 = [9]_4 = [1]_4$) nos queda $x_1 = 3$, la segunda ecuación se encuentra de igual manera $76x_2 \equiv x_2 \equiv 1 \; (5)$ tal que $x_2 = 1$ y la tercera $20x_3 \equiv x_3 \equiv 1 \; (19)$ tal que $x_3 = 1$. 
Ahora, podemos encontrar $x_0 = (95 \cdot 3)3 + (76 \cdot 2)1 + (20 \cdot 4)1 = 1087$. Entonces, tenemos que esta solución particular forma una única clase de congruencia $1087 \mod (380)$, notemos que podemos reducirla a $1087 \equiv 327 \mod (380)$, tal que la solución general sería $x = 327 + 380t, \; t \in \mathbb{Z}$. 

---

## Procedimiento para resolver un sistema de ecuaciones en congruencia

1. Reducir las ecuaciones de la forma $a_ix \equiv b_i \; (n_i)$ a ecuaciones del tipo $x \equiv b_i \; (n_i)$ para poder aplicar el teorema del resto chino.
2. $(n_i, n_j) = 1, \; \forall \; i \neq j, \; i, j \in \{1, 2, \dots, k\}$ es decir que sean coprimos. 
3. $x \equiv x_0 \mod (n_1 \cdot n_2 \cdot \; \dots \; \cdot n_k)$, $N = n_1 \cdot n_2 \; \dots \; n_k \implies x \equiv x_0 \mod N$. 
4. Tenemos que hallar $x_0$, recordemos que $0 \leq x_0 \leq N$. 
	- Encontremos $N_1, \; N_2, \; N_3, \; \dots \;, N_k$
	- Planteamos para encontrar $x_1, \; x_2, \dots$ sacamos: $N_i \cdot x_i \equiv b_i \; (n_i)$.
	- Ahora podemos formar $x_0 = (N_1 b_1) x_1 + (N_2 b_2) x_2 + \dots + (N_k b_k) x_k$.
5. Una vez encontrada $x_0$ el conjunto de soluciónes nos queda formado por $x = x_0 + k \cdot \prod_{i = 1}^r n_i, \; k \in \mathbb{Z}$


[^1]: El teorema tiene muchas aplicaciones en diversas áreas, incluida astronomía: si $k$ eventos ocurren regularmente, cuyos periódos sean $n_1, n_2, \dots, n_k$ , y con el $i$-evento ocurriendo en un tiempo $x = a_i, a_i + n_i, a_i + 2n_i, \dots$, entonces los $k$ eventos ocurren simultaneamente al tiempo $x$ donde $x \equiv a_i \; (n_i)$ para todo $i$. Esto se cumpliría solo en el caso de que los periódos $n_i$ sean coprimos. Los movimientos planetarios y eclipses son ejemplos obvios de estos eventos regulares, y es por lo cual muchas civilizaciones (entre ellas la antigua china) lo han usado para predecirlos.  