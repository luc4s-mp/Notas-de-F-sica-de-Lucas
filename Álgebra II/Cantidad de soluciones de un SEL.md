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

> [!Teorema 1.]
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

> [!Teorema 2.] 
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

> [!Proposición 3]
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

Sin embargo, es complicado encontrar que un sistema tiene soluciones a simple vista y es más difícil aún es encontrar una solución particular, entonces esta proposición no es tan útil más que para mostrarnos como se estructura el conjunto de soluciones de un sistema no homogéneo. 
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



 

