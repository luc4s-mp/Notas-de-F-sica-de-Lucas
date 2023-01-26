# Matrices de Transformaciones Lineales
Primero, obtengamos un resultado muy importante que es una conclusión de lo visto en [[Bases Vectoriales]]. Resulta que teniendo una base ordenada de un espacio vectorial de dimensión $n$, puedo asociar todos sus vectores a un vector de coordenadas en $\mathbb{K}^n$. Esto nos permite de manera mucho más simple, trabajar con espacios vectoriales más complicados como los polinomios, las matrices, etc. 

> [!Proposición 1. Vectores coordenadas]
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

> [!Proposición 2.]
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

> [!Proposición 3.]
> Sean $V$, $W$ y $U$, 3 $\mathbb{K}$-espacios vectoriales y sean $B_1$, $B_2$ y  $B_3$ bases ordenadas de $V,W$ y $U$ respectivamente. Sean $T: V \rightarrow W$ y $S:W \rightarrow U$ transformaciones lineales. Entonces
> $$[S \circ T]_{B_1B_3} = [S]_{B_2B_3}[T]_{B_1B_2}$$

**Demostración.** Sean $n = \dim V$, $m = \dim W$ y $p = \dim U$. Entonces, $[S]_{B_2 B_3} \in M_{p \times m}(\mathbb{K})$ y $[T]_{B_1B_2} \in M_{m \times n}(\mathbb{K})$ con lo que se puede multiplicar a las matrices y $[S]_{B_3B_2} \cdot [T]_{B_1B_2} \in M_{p \times n}(\mathbb{K})$. Para cada $v \in V$ se tiene 
$$[S]_{B_2B_3}[T]_{B_1B_2}(v)_{B_1} = [S]_{B_2B_3}(T(v))_{B_2} = (S(T(v)))_{B_3} = ((S \circ T)(v))_{B_3} = [S \circ T]_{B_1B_3}(v)_{B_1}$$
Usando repetidas veces la proposición 2. Luego, $[S \circ T]_{B_1B_3} = [S]_{B_2B_3}[T]_{B_1B_2}$. $\blacksquare$ 

Notemos que cuando la transformación lineal sea un isomorfismo, sabemos que es **invertible**. Y su matriz sería la inversa ([[Matrices Invertibles]]) de $[T]_{B_1B_2}$ por la proposición anterior. 

> [!Corolario 3.1]
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