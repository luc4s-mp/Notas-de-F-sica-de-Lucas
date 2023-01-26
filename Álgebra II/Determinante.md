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

De esta manera, lo que hacemos es aplicar las propiedades del lema 2 para obtener funciones más simples, 

A partir de esta proposición, concluimos que el determinante 

El siguiente teorema redefine al determinante como una función **única**.

> [!Teorema 3. El determinante es único]
> Para cada $n \in \mathbb{N}$, existe una **única función multilineal alternanda** de $D: M_{n \times n}(\mathbb{K}) \rightarrow \mathbb{K}$ tal que $D(\mathrm{Id}_n) = 1$.

**Demostración.** Dada $A \in M_{(n+1) \times (n+1)}(\mathbb{K})$ notemos que $A(i|j) \in M_{n \times n}(\mathbb{K})$ es la matriz que se obtiene _al suprimir la fila $i$ y la columna $j$ de $A$_. 
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

> [!Corolario 3.1. Formula para el determinante]
> Sea $A \in M_{n \times n}(\mathbb{K})$. Si para cada $r \in \mathbb{N}$, $\det : M_{r \times r}(\mathbb{K}) \rightarrow \mathbb{K}$ denota la función determinante de orden $r$, entonces $$\det (A) = \sum_{i=1}^n (-1)^{i+1}a_{i1}\det(A(i|1)) = \sum_{i=1}^n (-1)^{i+1} a_{1i} \det(A(1|i))$$

## Propiedades del determinante
El determinante es útil para obtener si una matriz es invertible. Si probamos un par de propiedades, podremos obtener si otras matrices son invertibles a partir de solamente tener 1. 

> [!Proposición 4. El determinante de la transpuesta]
> Sea $A \in M_{n \times n}(\mathbb{K})$. Entonces $\det(A) = \det(A^t)$

**Demostración.** Probemos la igualdad por inducción en $n$:
- Para $n=1$, no hay nada que probar. 
- Supongamos que vale para $n$ y sea $A = (a_{ij}) \in M_{(n+1) \times (n+1)}(\mathbb{K})$. Entonces, $$\begin{align} \det(A^t)  & =  \sum_{i=1}^{n+1} (-1)^{i+1} (A^t)_{i1}\det(A^t(i|1)) = \sum_{i=1}^{n+1} (-1)^{i+1} a_{1i} \det(A(1|i))  = \det (A)\end{align} $$
Que es a lo que queríamos llegar. $\blacksquare$ 

Queríamos ahora ver que ocurre cuando a la matriz $n \times n$  

> [!Proposición 5.]
> Sea $A = (a_{ij}) \in M_{n \times n}(\mathbb{K})$ una matriz triangular superior. Entonces $\det(A) = \prod_{i=1}^n a_{ii}$.

**Demostración.** Probaremos la validez de la fórmula por inducción en $n$. Para $n = 1$, no hay nada que hacer. Supongamos que vale para $n$ y sea $A = (a_{ij}) \in M_{(n+1) \times (n+1)}(\mathbb{K})$ una matriz triangular superior. Entonces, $$\det(A) = \sum_{i=1}^{n+1}(-1)^{i+1} a_{i1}\det(A(i|1)) = a_{11}\det(A(1|1)),$$
puesto que en la primera fila el único valor que no es 0 es el primero. Luego, la matriz $A(1|1) \in M_{n \times n}(\mathbb{K})$ es triangular superior y entonces, por hipótesis inductiva, $\det (A(1|1)) = \prod_{j=1}^n (A(1|1)) = \prod_{i=2}^{n+1} a_{ii}$. En consecuencia,
$$\det(A) = a_{11}\det(A(1|1)) = \prod_{i=1}^{n+1} a_{ii}$$
que es lo que quería probar. $\blacksquare$ 

Existen otras formas para el determinante además de la expuesta en el corolario 3.1. En ciertas ocasiones no siempre es conveniente tomar la primera fila (o columna) para poder obtener el determinante, a veces es conveniente tomar otra columna $j$ o fila $j$. Si cambiamos la fila $1$ por la fila $j$ podemos obtener una formula más general. Tal que $$\begin{align} \det(A) & = (-1)^{j-1} \det (\alpha_{j}, \alpha_1, \dots, \alpha_{j-1}, \alpha_{j+1}, \dots, \alpha_n ) \\ & = (-1)^{j-1}\Big( \sum_{j=1}^{n} (-1)^{1+i} a_{ij} \det(A(i|j)) \Big) \\ & = \sum_{j=1}^n (-1)^{i+j} a_{ij} \det(A(i|j)) \end{align}$$
> [!Proposición 6. El producto de determinantes]
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

> [!Proposición 7. El determinante para Matrices Invertibles]
> Sea $A  \in M_{n \times n} (\mathbb{K})$. Entonces, $A$ es invertible si y sólo si $\det A \neq 0$. 

**Demostración.** ($\Rightarrow$) Supongamos que $A \in M_{n \times n}(\mathbb{K})$ es invertible. Entonces existe una matriz $B \in M_{n \times n}(\mathbb{K})$ tal que $A \cdot B = Id_n$. Aplicando el resultado de la proposición 6 se obtiene que $$1 = \det(Id_n) = \det(A \cdot B) = \det(A) \cdot \det(B)$$
de donde se deduce que $\det A \neq 0$.
($\Leftarrow$) Si $\det(A) \neq 0$, entonces las columnas de $A$ son LI  (Lema 2) por lo tanto es invertible. $\blacksquare$

> [!Corolario 7.1.]
> Si $\det A \neq 0$ entonces $\det A^{-1} = \frac{1}{\det A}$.
 

