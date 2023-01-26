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

> [!Teorema de Gauss]
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



