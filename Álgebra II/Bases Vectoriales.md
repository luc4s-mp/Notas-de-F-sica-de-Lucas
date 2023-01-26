# Bases Vectoriales
Ya exploramos los conceptos de [[Independencia Lineal]] y Sistemas de Generadores (visto en [[Sistemas de Ecuaciones Lineales]]). Ahora, juntemos estos dos conceptos.

> [!Bases Vectoriales]
> Una _base_ de un $\mathbb{K}$-espacio vectorial $V$ es un conjunto de vectores en $V$ que es linealmente independiente y genera a $V$. 

Sabemos que la lista $E = \{(1,0,\dots, 0), (0,1,\dots, 0), \dots, (0,0,\dots, 1)\}$ es un sistema de generadores de $\mathbb{K}^n$ y sabemos que es linealmente independiente pues al aplicar el método visto en [[Independencia Lineal]] de formar una matriz con los vectores como columnas, tenemos que las soluciones del sistema son $x_1 = 0, \dots, x_n = 0$. Luego, $E$ es una _base de_ $V$ y se llama la **base canónica estándar**.  
El siguiente teorema nos ayuda de forma rápida a descartar algunos casos de listas de vectores que no pueden ser bases pues no so LI:

> [!Proposición 1. Largo de una lista LI < Largo del conj de generadores]
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

> [!Proposición 2. (Criterio para la base)]
> Una lista de vectores en $V$ es una base de $V$ si y solo si cada $v \in V$ puede ser escrito de forma única en $v = a_1v_1 + \cdots + a_n v_n$ donde $a_1, \dots, a_n \in \mathbb{K}$.

**Demostración.** ($\Rightarrow$) Primero supongamos que $v_1,\dots, v_n$ es una base de $V$. Sea $v \in V$. Debido a que $v_1, \dots, v_n$ genera a $V$, existen $a_1, \dots, a_n \in \mathbb{K}$ tal que escriben como una combinación lineal a $v$. Para mostrar que son únicos, supongamos que $c_1, \dots, c_n$ son otros escalares tal que $v = c_1v_1 + \dots + c_n v_n$. Restando las dos ecuaciones tenemos que $0 = (a_1 - c_1)v_1 + \dots + (a_n - c_n)v_n$, esto implica que como los vectores de la lista son LI entonces $a_1 = c_1, \dots, a_n = c_n$.
($\Leftarrow$) Supongamos que $v \in V$ puede ser escrito de manera única como combinación lineal tal que $v = a_1v_1 + \dots + a_nv_n$. Claramente, esto implica que $<v_1, \dots, v_n> = V$. Para mostrar que la lista de vectores es LI, supongamos que $a_1, \dots, a_n \in \mathbb{K}$ tal que $0 = a_1v_1 + \dots + a_nv_n$, por hipótesis sabemos que los coeficientes son únicos por lo tanto $a_1 = \dots = a_n = 0$. Entonces, $v_1, \dots, v_n$ es linealmente independiente y es una base de $V$. $\blacksquare$ 

De esta manera, una forma clara obtener si una lista de vectores es una base, es igualando $a_1 v_1 + \dots + a_nv_n = 0$ ó expresándolo como $A\vec{x} = \vec{0}$ ($A$ es la matriz con los vectores como columnas y $\vec{x} = (a_1, \dots, a_n)$) y la solución de este sistema es única y  es la trivial, tenemos que las columnas son LI. Ya vimos que cuando el sistema tiene solución única en $A\vec{x} = \vec{b}$ entonces $A$ es invertible (como vimos en [[Matrices Invertibles]]) y la solución única es $\vec{x} = A^{-1}\vec{b}$ . Entonces, podemos probar fácilmente el siguiente corolario:

> [!Corolario. (prop 2.)]
> Si $A \in M_{n \times n}(\mathbb{K})$ invertible, entonces las columnas de $A$ son LI y forman una base de $\mathbb{K}^n$ 

Un sistema de generadores de un espacio vectorial puede no ser una base porque no es LI. La siguiente proposición dice que cualquier sistema de generadores, puede ser reducida a un conjunto de vectores LI y que sigua generando a todo el espacio vectorial.

> [!Proposición 3. Sist. de generadores contiene una base]
> Sea $v_1, \dots, v_n$ un sistema de generadores de $V$. Entonces, existe un subconjunto $G \subseteq \{v_1, \dots, v_n\}$ que es una base de $V$. 

**Demostración.** Supongamos $v_1, \dots, v_n$ es un sistema de generadores de $V$. Si la lista es LI, entonces listo. Si es LD, queremos remover algunos de los vectores de $v_1, \dots, v_n$ tal que los que queden sean una base de $V$. Haremos esto usando un proceso descrito abajo.
Si $B$ es igual a la lista $v_1, \dots, v_n$.
- _Paso 1:_ Si $v_1 = 0$, eliminemos $v_1$ de $B$. Si $v_1 \neq 0$, deja a $B$ sin cambiar.
- _Paso $j$:_ Si $v_j$ esta en el subespacio $<v_1, \dots, v_{j-1}>$ (por el Lema 2 de [[Independencia Lineal]]), eliminemos $v_j$ de $B$ y nos queda $B_j$. Si $v_j$ no esta en $<v_1, \dots, v_{j-1}>$, deja $B$ sin cambiar. 
Paramos el proceso después del paso $n$, obteniendo la lista $B_n$. El proceso termina cuando ningún vector en $B_n$ es el conjunto de generadores de los previos. Entonces, $B_n$ es LI, por el Lema 2. Entonces $B$ es una base de $V$. $\blacksquare$ 

> [!Proposición 4. Una lista LI se puede expandir a una base]
> Sea $V$ un $\mathbb{K}$-espacio vectorial de dimensión finita y sea $w_1, \dots, w_r$ una lista linealmente independiente de $V$. Entonces existen elementos $w_{r+1}, \dots, w_{n} \in V$ tales que $w_1, \dots, w_r, w_{r+1}, \dots, w_n$ es una base de $V$. 

**Demostración.** Sea $B= z_1, \dots z_n$ una base de $V$. 
Consideremos $G_0 = <w_1, \dots, w_r>$ un subespacio de $V$. Veamos que podemos definir a un conjunto $G_1 = w_1, \dots, w_r, z_1$ como linealmente independiente si $z_1 \notin G_0$ ó de otra manera si $z_1 \in G_0$ entonces $G_1 = w_1, \dots, w_r$. Podemos repetir este proceso, creando $G_i = G_{i-1} \cup \{z_i\}$ si $z_i \notin G_{i-1}$ ó $G_i = G_{i-1}$ si $z_i \in G_{i-1}$ con cada $G_i, 1 \leq i \leq n$ linealmente independiente, hasta que lleguemos a $G_n$ que nos dice que $V = <z_1, \dots, z_n> \subseteq <G_n>$ y $G_n$ es linealmente independiente. Luego, $G_n$ es una base de $V$. $\blacksquare$ 

Notemos que en toda la nota usamos el concepto de lista en vez de conjuntos, aunque podríamos haberlo hecho, las proposiciones vistas funcionan de igual manera aunque conjuntos en vez de listas. 
Una de las propiedades más útiles de las bases en un espacio vectorial finito $V$ es que nos permiten introducir coordenadas en $V$ análogas a las "coordenadas naturales" de un vector $v = (x_1, x_2, \dots, x_n)$ en un espacio $\mathbb{K}^n$. Si $B = \{v_1, \dots, v_n\}$ es una base de $\mathbb{K}^n$ tenemos que existen únicos coeficientes $a_1, \dots, a_n$ tal que para todo $v  \in V, \; y = a_1v_1 + \dots + a_nv_n$, entonces podemos definir a los coeficientes como "las coordenadas del vector $v$ en la base $B$". Tal que $v = (x_1, x_2, \dots, x_n)$ es un vector en las coordenadas de la **base estándar o canónica**. Notemos que en estos casos, el orden en el que estén los vectores sí importa, pues por ejemplo si cambiamos de orden en la combinación lineal a $v_j$ por $v_j$ entonces tenemos el nuevo vector de coordenadas $(a_1, \dots, a_j, \dots, a_i, \dots, a_n) \neq (a_1, \dots, a_i, \dots, a_j, \dots, a_n)$. Es por esto que usamos listas en vez de conjuntos, pues al hablar de las coordenadas generadas por las bases el orden importa. 
Aquellas bases que se escriben como listas de vectores se las suele llamar **bases ordenadas**. 