# Matrices Invertibles
De lo que vimos en [[Operaciones con Matrices]], queremos definir la matriz ([[Matrices]]) inversa sobre $M_{n\times n}(\mathbb{K})$ es el conjunto de matrices **cuadradas** (es decir matrices con el mismo número de filas que de columnas): 

> [!Matrices Invertibles]
> #Definición Una matriz $A \in M_{n\times n}(\mathbb{K})$ se dice _invertible_ si existe una matriz $B \in M_{n\times n}(\mathbb{K})$ tal que $A \cdot B = B \cdot A = I_n$.

Podemos probar que la inversa de una matriz es **única**. 

> [!Proposición 1.]
> Sea $A, B \in M_{n\times n}(\mathbb{K})$ y $B$ es la inversa de $A$ es única.

**Demostración.** Supongamos por el absurdo que existe $C \in M_{n\times n}(\mathbb{K})$ tal que sea el inverso de $A$ también, es decir $AC = CA = I_n$ y $AB = BA = I_n$. Entonces
$$B = I_n B = (CA)B = C(AB) = CI_n = C \quad \blacksquare$$
Entonces, como sabemos que las inversas de _algunas_ matrices en $M_{n\times n}(\mathbb{K})$ existen, por ejemplo si $A = \begin{pmatrix} 0 & 1 \\ 2 & 0 \end{pmatrix}$ tiene inversa $B = \begin{pmatrix} 0 & 1/2 \\ 1 & 0 \end{pmatrix}$ pues 
$$AB = \begin{pmatrix} 0 & 1 \\ 2 & 0 \end{pmatrix} \cdot \begin{pmatrix} 0 & 1/2 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 0\cdot 0 + 1 \cdot 1 & 0 \cdot 1/2 + 1 \cdot 0 \\ 2 \cdot 0 + 0 \cdot 1 & 2 \cdot 1/2 + 0 \cdot 0\end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1\end{pmatrix}$$
Podemos definir entonces $GL(n,\mathbb{K}) = \{A \in M_{n\times n}(\mathbb{K}) / A \text{ es inversible }\}$. Se pueden probar de este las siguientes propiedades: 

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

## Una ojeada a la Teoría de Grupos
El grupo es una de las estructuras más simples posibles en el álgebra y son ubicuos en la física, principalmente en la mecánica cuántica. Vale la pena detenerse un segundo a analizarlos. Resulta que en los grupos (sobre todo es más fácil de visualizar a los finitos) se mantiene una cierta "simetría" de los elementos. Veamos un ejemplo de esto último muy general, para entender como los grupos pueden encontrarse en todos lados.

Supongamos que tenemos 6 bolitas idénticas $\bigcirc \; \bigcirc \; \bigcirc \; \; \bigcirc \; \; \bigcirc \; \; \bigcirc$ y a cada una le asigno un orden $\bigcirc_1 \; \bigcirc_2 \; \bigcirc_3 \; \; \bigcirc_4 \; \; \bigcirc_5 \; \; \bigcirc_6$ entonces supongamos que yo me armo un conjunto $G$ que contiene todas las posibles permutaciones que le puedo aplicar a estas bolitas (incluida la permutación de no hacer nada), por ejemplo la permutación $g_1: \bigcirc_1 \mapsto \bigcirc_2, \; \bigcirc_2 \mapsto \bigcirc_3, \; \bigcirc_4 \mapsto \bigcirc_4, \; \bigcirc_5 \mapsto \bigcirc_6 \text{ y } \bigcirc_6 \mapsto \bigcirc_5$ pertenece al conjunto y de cierta manera se mantiene la simetría pues a pesar que yo les asignara números a las bolitas si yo las reordeno se ven de igual manera. Algo que rompería la simetría sería por ejemplo asignar $\bigcirc_2 \mapsto \bigcirc_7$ pero la bolita 7 sería una que no existe, por lo tanto esta permutación no esta permitida. Gracias a [[Principios del Conteo]] sabemos que la cantidad de elementos en este conjunto es $6!$. Veamos que ahora yo puedo crear una operación $\otimes$ tal que si $g_i, g_j, g_k \in G, \; g_i \otimes g_j = g_k$  significa "aplicar la permutación $g_i$ y luego $g_j$ nos da lo mismo que directamente aplicar $g_k$". Entonces, se puede probar que $(G,\otimes)$ es un **grupo**. 

La propiedad más complicada de demostrar de que $(G, \otimes)$ es un grupo probablemente sea que de que para toda permutación $g_i$ se puede probar que existe una "permutación inversa" $g_i^{-1}$ tal que al hacer $g_i \otimes g_i^{-1} = id$ donde $id$ es la permutación que "no hace nada", es decir, que los deja como estaban inicialmente. Por ejemplo, la permutación inversa de $g_1$ sería $g_1^{-1}: \bigcirc_2 \mapsto \bigcirc_1, \; \bigcirc_3 \mapsto \bigcirc_2, \; \bigcirc_4 \mapsto \bigcirc_4, \; \bigcirc_6 \mapsto \bigcirc_5 \text{ y } \bigcirc_5 \mapsto \bigcirc_6$   
tal que al hacer $g_1 \otimes g_1^{-1} = id$ es decir, es como no hacer nada. 

Lo importante a entender de este ejemplo, es el hecho de que en los grupos parece mantenerse una "simetría" en cierta manera. Otros ejemplo de grupo son  $(\mathbb{Z}_n, +)$, visto en [[Enteros Modulares]], o las posibles rotaciones que le puedo realizar a un cubo en el espacio. 

En las matemáticas existe toda un área de estudio dedicada exclusivamente a los grupos llamada "Teoría de Grupos". Probablemente una de las conclusiones más grandes a las que ha llegado esta área de la matemática, (a grandes rasgos) es que todos los grupos parecen venir del mismo lugar y se pueden descomponer en subgrupos  (como si hubiéramos descubierto que las moléculas se pueden separar en átomos). 

## ¿Cómo obtenemos una inversa?
Ahora que entendimos bien el comportamiento de un grupo, podemos entender mejor a $(GL(n, \mathbb{K}), \cdot)$. El hecho de que esta estructura sea un grupo es fundamental y un hecho muy utilizado en álgebra lineal al que volveremos continuamente.  

Encontrar la inversa de una matriz no es tan simple como encontrar la inversa de la permutación como vimos arriba. Sin embargo, la idea de que las acciones son "simétricas" en un grupo nos puede ayudar bastante. 

> [!Proposición 3.]
> Sea $e$ una una operación elemental por fila y sea $E \in M_{n \times n}(\mathbb{K})$ sea una _matriz elemental_ $E= e(Id)$ (aplicarle la operación por fila a la identidad). Entonces, para cada $n \times m$ matriz $A$ tenemos que $e(A) = EA$. 

**Demostración.** El punto de esta prueba es que la entrada de la fila $i$ y la comuna $j$ del producto de matrices (visto en [[Operaciones con Matrices]]) es obtenida por la fila $i$ de $E$ y la columna $j$ de $A$. Probemos que $e(A) = EA$ para la operación $e_4: F_i + cF_j$ y los otros dos casos son aún más fáciles que este. Supongamos que $r \neq s$, tanto que $1 \leq r \leq n$ y $1 \leq s \leq n$, y $e_4$ es la operación de reemplazar la fila $F_r$ por la fila $F_r$ más un $c \in \mathbb{K}$  multiplicado por la fila $F_s$. Entonces, 
$$E_{ik} = \begin{cases} \delta_{ik}, & i \neq r \\ \delta_{rk}+ c\delta_{sk}, & i = r \end{cases}$$
donde $\delta_{ik} = 0$ ó $\delta_{ik} =1$ son los valores de la matriz identidad $Id_{ik} = \begin{cases} 0, & i \neq k \\ 1, & i = k \end{cases}$ . Luego,
$$(EA)_{ij} = \sum_{k=1}^n E_{ik}A_{kj} = \begin{cases} A_{ik}, & i \neq r \\ A_{rj} + cA_{sj}, & i = r\end{cases}$$
En otras palabras, $EA = e_4(A)$ . $\blacksquare$

Entonces, observemos que las matrices elementales pueden ser nuestro "bloques de construcción" para la inversa. Pues al multiplicarla por la matriz para obtener una matriz triangular obtenemos que estamos acercando cada vez más la matriz a la identidad, pero luego si una vez que llegamos a la matriz triangular superior las seguimos aplicando para generar también una _matriz triangular inferior_ ($A_{ij} = 0$ cuando $i < j$) llegamos a la matriz identidad. Por lo tanto una matriz $A$ se puede escribir como $A = E_1 \cdot E_2 \cdots E_l \cdot I_n$ siendo $l$ un número finito de operaciones elementales por fila realizadas, luego por la proposición 2(2) tenemos que $A^{-1} = E_l^{-1} \cdots E_{2}^{-1} \cdot E_{1}^{-1} \cdot I_n$. Pero para esto tendríamos que probar dos proposiciones antes: (1) Que las matrices elementales son invertibles y (2) que toda matriz $A$ que es un producto de matrices elementales es invertible.

> [!Proposición 4.]
> Una matriz elemental $E \in M_{n \times n}(\mathbb{K})$ es invertible, o también $E \in GL(n,\mathbb{K})$. 

**Demostración.** 
- (Operación 1) Sea $e^{(ij)}$ la operación para cambiar la fila $i$ por la fila $j$ y $E^{(ij)}$ su respectiva matriz elemental. Tenemos que si volvemos a aplicar la operación otra vez  $E^{(ij)}$ obtenemos la matriz identidad , es decir $e^{(ij)}(e^{(ij)}(Id_n)) = Id_n$ por lo tanto $E^{(ij)} \cdot E^{(ij)} = Id_n$. Luego, por definición $E^{(ij)}$ es inversa de sí misma. 
- (Operación 2) Sea $e^{(i)}_c$ la operación que multiplica la fila $i$ por una constante $c \in \mathbb{K}$ y $E_c^{(i)} = e_{c}^{(i)}(Id_n)$ su respectiva matriz elemental. Tenemos que al aplicar $e_{c^{-1}}^{(i)}$ sobre la matriz elemental $E_c^{(i)}$ tenemos de vuelta a la matriz identidad $e^{(i)}_{c^{-1}}(e^{(i)}_c(Id_n))$ por lo tanto $E_{c^{-1}}^{(i)} \cdot E_{c}^{(i)} = Id_n$. Luego, por definición $E^{(i)}_{c^{-1}}$ es la inversa. 
- (Operación 3) Es trivial.
- (Operación 4) Sea $e_c^{(ij)}$ la operación para cambiar fila $i$ por la fila $i$ más una constante $c$ por la fila $j$  y $E^{(ij)}_{c} = e_{c}^{(ij)}(Id_n)$ su respectiva matriz elemental. Tenemos que si aplicamos la operación $e_{-c}^{(ij)}$ sobre la matriz elemental $E_{c}^{(ij)}$ obtenemos la matriz identidad, es decir $e_{-c}^{(ij)}(e_{c}^{(ij)}(Id_n)) = Id_n$ por lo tanto $E_{-c}^{(ij)} \cdot E_{c}^{(ij)} = Id_n$. Luego, por definición $E_{-c}^{(ij)}$ es la inversa. $\blacksquare$ 

> [!Teorema 5. (Inversibilidad / Operaciones por fila)]
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
> 




