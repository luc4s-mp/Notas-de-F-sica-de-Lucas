# Espacios Vectoriales Finitos
Ya vimos en [[Sistemas de Ecuaciones Lineales]] el concepto de **sistemas de generadores** de un espacio vectorial. Que ya vimos que en $\mathbb{R}^2$ tenemos que el subespacio generado por un vector $v$, nos da una recta que pasa por el origen, luego en $\mathbb{R}^3$ si tomamos el subespacio ([[Subespacios]]) generado por dos vectores, tenemos que _muchas veces nos da_ un plano que pasa por el origen y contiene a los dos vectores. Observemos también que el subespacio de soluciones de un sistema de ecuaciones homogéneo (visto en [[Cantidad de soluciones de un SEL]]) de 1 ecuación y 3 incógnitas es también un plano que pasa por el origen, pues está generado por dos vectores.

Resaltemos el hecho de que en el párrafo anterior nos dicen que "muchas veces", es decir no siempre, se puede formar un plano con dos vectores _¿Cuándo esto no ocurre?_ Tomemos por ejemplo los vectores $(1,-1,4), \; (1/2, -1/2, 2)$ no generan un plano, sino una recta en el espacio. Esto ocurre porque el segundo vector $(1/2, -1/2,2)$ al multiplicarlo por 2 obtenemos el primero $(1,-1,4)$ lo cual hace que al escribirlos como combinación lineal $a(1,-1,4) + b(1/2,-1/2,2)$ podemos reescribir a el secundo vector como $1/2(1,-1,4)$ tal que $(a+b/2)(1,-1,4)$ y al final todo depende de un solo vector, de ahí obtenemos la recta. 

Entonces, observemos que es muy importante entender que cuando un conjunto de vectores genera un subespacio, en el pueden existir vectores "de más" que no son necesarios incluirlos en el conjunto de generadores. Desarrollaremos un método para deshacernos de estos vectores. 

> [!Proposición 1. El sist. de generadores es el subespacio más chico.]
> **(NEF)** Sea $V$ un $\mathbb{K}$-espacio vectorial. El subespacio generado por una lista de vectores $v_1, \dots, v_m$ en $V$ es el subespacio más chico de $V$ que contiene a todos los vectores de la lista.

**Demostración. (NEF)**[^1]  Supongamos $\{v_1, \dots, v_m\}$ es una lista de vectores en $V$. Sabemos que $<v_1, \dots, v_m>$ es un subespacio de $V$. Para cada $v_j \in \{v_1, \dots, v_m\}$, pertenece a $<v_1, \dots, v_m>$ pues en la combinación lineal $a_1v_1 + a_2v_2 + \cdots + a_mv_m$ eligiendo $a_j = 1$ y el resto igual a 0 se genera $v_j$. 
Luego, como todos los subespacios están cerrados en multiplicaciones por escales y sumas (por la proposición 1 en [[Subespacios]]), cada subespacio de $V$ que contiene a todos los $v_j$ a su vez contiene a $<v_1, \dots, v_m>$. Para entender mejor esto supongamos $S$ un subespacio de $V$ tal que $v_1, \dots, v_m \in S$, entonces $\sum_{i=1}^n \alpha_i v_i \in S, \; \forall \alpha_i \in \mathbb{K}$. Luego, $<v_1, \dots, v_n> \subseteq S$. 
En conclusión, $<v_1, \dots, v_m>$ es el subespacio más chico de $V$ que contiene todos los vectores de $v_1, \dots, v_m$. $\blacksquare$ 

> [!Corolario. (PROP. 1)]
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

> [!Lema 2.]
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