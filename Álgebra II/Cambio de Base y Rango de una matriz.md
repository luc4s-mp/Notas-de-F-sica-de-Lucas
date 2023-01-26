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

> [!Proposición 1.]
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

> [!Proposición 2.]
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

> [!Lema 3.]
> Sea $A \in K^{n \times m}$. Sean $G \in G L(n, K)$ y $D \in G L(m, K)$. Entonces$$ \mathrm{rg}_C(A)=\operatorname{rg}_C(C \cdot A \cdot D)$$

**Demostración.** Sea $f_A: K^m \rightarrow K^n$ la transformación lineal inducida por la multiplicación a izquierda por $A$. Si $E$ y $E^{\prime}$ son las bases canónicas de $K^m$ y $K^n$ respectivamente, se tiene que $\left|f_A\right|_{E E^{\prime}}=A$ y por lo $\operatorname{rg}(A)=\operatorname{dim}\left(\operatorname{Im}\left(f_A\right)\right)$.
Por la Proposición 1, puesto que $D \in G L(m, K)$, existe una base $B_1$ de $K^m$ tal que $D=C\left(B_1, E\right), y$ como $C \in G L(n, K)$, existe una base $B_2$ de $K^n$ tal que $C=C\left(E^{\prime}, B_2\right)$.
Entonces por la proposición 2,
$$
 { C \cdot A \cdot D }=C\left(E^{\prime}, B_2\right) \cdot\left|f_A\right|_{E E} \cdot C\left(B_1, E\right)=\left|f_A\right|_{B_1 B_2}
$$
la dimensión de la imagen no cambia por haber cambiado las bases, por lo tanto $\operatorname{rg}_C(C . A . D)=\operatorname{dim}\left(\operatorname{Im}\left(f_A\right)\right)=\operatorname{rg}_C(A)$. $\blacksquare$ 

El siguiente lema prueba de que multiplicando por las matrices invertibles apropiadas se puede llegar a una matriz más sencilla tal que el rango de la misma sea muy claro. 

> [!Lema 4.]
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

> [!Proposición 5. El rango filas es igual al rango colum]
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