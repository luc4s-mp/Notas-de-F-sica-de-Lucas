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

> [!Proposición 1.]
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