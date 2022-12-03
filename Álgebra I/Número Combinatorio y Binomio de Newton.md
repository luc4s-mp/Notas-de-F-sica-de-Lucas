# Números Combinatorios
Ya formalizamos las nociones de contar más básicas en [[Principios del Conteo]] y en [[Acciones Combinatorias]] vimos una de las acciones más comunes de la combinatoria: formas de ordenar. Ahora, nos dedicaremos a explorar la segunda más importante: formas de elegir elementos de un mónton. Seguimos trabajando en [[Z]]

---
## Problema Inicial - Maneras de elegir a un equipo
Supomgamos que tenemos una clase de $n$ estudiantes, ¿de cuántas maneras se puede formar un equipo de $m$ integrantes donde unx de ellxs es designado como líder? Y en general, ¿De cuántas maneras se puede formar un equipo con un ingresante designado como líder?

---
## Acción 2: Elegir
Buscamos formalizar el significado de la palabra "elegir elementos de un montón". Veamos que sea un conjunto $A = \{a_1, a_2, \dots, a_n\}, \; |A| = n$ podemos decir que preguntarnos ¿Cuántas formas de "elegir 3 elementos" de un conjunto existen? es lo mismo que decir _¿Cuántos subconjuntos de 3 elementos existen?_ Para entender esto pongamos el siguiente ejemplo:

**Ejemplo:** Sea $A = \{1,2,3,4,5,6\}$ ¿Cuántos subconjuntos de 3 elementos existen?
$$\begin{align}
\{1,2,3\}, \; \{1,2,4\}, \; \{1,4,6\}, \; \{1,2,5\}, \; \{1,2,6\}, \\ \{1,3,4\}, \;
\{1,3,5\}, \; \{1,3,6\}, \; \{1,4,5\}, \; \{1,5,6\} \\
\{2,3,4\}, \; \{2,3,5\}, \; \{2,3,6\}, \; \{2,4,5\}, \; \{2,4,6\}, \\ \{2,5,6\}, \; \{3,4,5\}, \; \{3,4,6\}, \; \{3,5,6\}, \; \{4,5,6\} \;   
\end{align}$$
Son en total 20 combinaciones. Pero nuestro objetivo es contar estas combinaciones sin necesidad de enumerarlas. Notemos que en los subconjuntos no importa el **orden** en el que esten puestos, entonces $\{1,2,3\} = \{1,3,2\}$. Lo cual tiene sentido pues cuando elegimos $1,2,3$ del conjunto $A$ es lo mismo que elegir $1,3,2$ (a no ser que el orden en el que los saquemos importe). 
Si el orden en el que lo saquemos importara entonces tendríamos un **arreglo** (visto en [[Acciones Combinatorias]]), es decir primero tendríamos 6 opciones para elegir, luego 5 (porque la elegimos una primero) y por último nos quedan 4 elementos para elegir por lo cual $A(6,3) = 6 \cdot 5 \cdot 4$ o también se puede calcular usando $A(6,3) = \frac{6!}{(6-3)!}$. 
Pero en este caso, como el orden en el que elijamos no importa sino simplemente los elementos, entonces tenemos que eliminar todos las elecciones donde estos se cambian de lugar, o sea hay que eliminar elecciones como $\{1,3,2\}$ si ya existe $\{1,2,3\}$ . Si las formas de ordenar los 3 elementos es $3! = 3 \cdot 2 \cdot 1 = 6$ entonces debemos dividir por este número a la cantidad de arreglos que teníamos anteriormente. 
$$\frac{A(6,3)}{3!} = \frac{6 \cdot 5 \cdot 4}{3 \cdot 2} = 5 \cdot 4 = 20$$
Y obtenemos que existen 20 combinaciones distintas de subconjuntos de $A$, lo mismo que obtuvimos contando.

> Es importante distinguir entre **elegir con orden** y **elegir sin orden**. Cuando el orden importa al elegir, entonces tenemos que usar nuestro conocimiento en arreglos. Pero si el orden no importa entonces debemos calcular el arreglo y luego dividirlo por la cantidad de permutaciones entre los elementos.

Ahora nos podemos preguntar _¿De cuantás maneras se pueden elegir elementos de un conjunto?_ O simplemente _¿Cuántos subconjuntos existen?_ Recordemos según lo que vimos en [[Conjuntos]] que **Partes de un conjunto A** $\mathcal{P}(A)$ nos daba todos los subconjuntos de un conjunto $A$, entonces queremos enontrar $|\mathcal{P}(A)| = ?$

> **Teorema.** Sea $A = \{a_1, a_2, \dots, a_n\}$ finito. Entonces $\mathcal{P}(A)$ es finito y $|\mathcal{P}(A)| = 2^{|A|}$ .

 **Demostración**. Definamos la siguiente función$$f: \mathcal{P}(A) \mapsto \{0,1\} \times \{0,1\} \times \cdots\times \{0,1\} = \{0,1\}^n$$
 asignando a cada $S \subseteq A$ la $n$-tupla $(e_1, e_2, \dots, e_n)$ de ceros y unos definida por 
$$e_i = \begin{cases}
1 & \text{ si } a_i \in S \\
0 & \text{ si } a_i \notin S
\end{cases}$$
Por ejemplo, $f(\emptyset) = (0,0,\dots,0)$ y $f(A) = (1,1,\dots,1)$. Es fácil probar que $f$ es biyectiva, lo cual nos permite usar el principio de multiplicación y entonces
$$|\mathcal{P}(A)| = |\{0,1\}^n| = (|\{0,1\}|)^n = 2^n \quad \blacksquare$$
Usando este teorema podemos responder nuestra pregunta anterior. 
Veamos la necesidad de definir a la "cantidad de formas de elegir $n$ en $m$ elementos" y evitar usar los arreglos:

> **Definición**. Llamamos a el número $\binom{n}{k}$ "**número combinatorio $n$ en $k$**" y se lee simplemento "$n$ en $k$". Si $k < 0$ o $k > n$ definimos $\binom{n}{k} = 0$. Cada una de estas formas de seleccionar $k$ elementos en un conjunto de $n$ la llamamos **combinación**.

De esta manera, el número combinatorio que queremos encontrar en el problema de arriba se escribe $\binom{6}{3}$ "6 en 3" porque queremos elegir en un conjunto de 6, 3 elementos. 

> **Teorema.** Dado $n \in \mathbb{N}_0$, para todo $0 \leq k \leq n$ se tiene $$\binom{n}{k} = \frac{n!}{k!(n-k)!}=\frac{n(n-1)\cdots (n-k+1)}{k!}$$

**Demostración.** Sea un conjunto $A = \{a_1, a_2, a_3, \dots, a_n\}$ , $|A| = n$ queremos elegir $k$ de estos elementos. Sabemos que existen $n!$ formas de ordenar los elementos de $a_1, a_2, \dots, a_n$. Si dividimos al conjunto en dos partes:
$$\underbrace{a_1, a_2, a_3, \dots, a_k}_{k} \; | \; \underbrace {a_{k+1}, \dots, a_n}_{n-k}$$
y fijamos los primeros $k$ elementos de la lista, $(n-k)!$ reordenaciones de los elementos del segundo bloque. Luego, hay
$$\frac{n!}{(n-k)!}$$
listas ordenadas de $k$ elementos (los "arreglos"). Las $k!$ ordenaciones distintas de $a_1, a_2,\dots, a_k$ dan lugar al mismo conjunto; por lo tanto hay
$$\binom{n}{k} = \frac{\frac{n!}{(n-k)!}}{k!} = \frac{n!}{k!(n-k)!} \quad \blacksquare$$
### Propiedades básicas del número combinatorio
De la definición de $\binom{n}{k}$ se siguen las siguientes propiedades
1. $\binom{n}{0} = \binom{n}{n} = 1$
2.  $\binom{n}{1} = \binom{n}{n-1} = n$
3.  $\binom{n}{2} = \frac{n(n-1)}{2}$
Notemos que lo que nos dice el segundo inciso es que existen $n$ maneras de elegir un elemento en un conjunto de $n$ elementos como en un conjunto de $n-1$ elementos, pues simplemente quitamos cualquiera de los elementos del conjunto y tenemos una combinación. 
Esto se puede generalizar, es decir, un conjunto de $n$ elementos tiene la misma cantidad de subconjuntos de $k$  que de subconjuntos de $n-k$ elementos.

> **Lema. (Simetría)** Para todo $n,k \in \mathbb{N}$ se tiene $$\binom{n}{k} = \binom{n}{n-k}$$

**Demostración.** Tenemos
$$\binom{n}{n-k} = \frac{n!}{(n-k)!(n-(n-k))!} = \frac{n!}{(n-k)!k!}= \binom{n}{k} \quad \blacksquare$$
> **Proposición (Identidad de Pascal)** Dado $n \in \mathbb{N}$, para todo $0 \leq k \leq n$ se tiene que $$\binom{n+1}{k} = \binom{n}{k-1} + \binom{n}{k}$$

**Demostración.** Sale por definición $\blacksquare$.

Luego, notemos que si los números combinatorios de A representan cuantos subconjuntos de m elemtentos existen siendo $|A| = n$  y si  $\mathcal{P}(A)$ tiene todos los subconjuntos de A, entonces podemos llegar a la siguiente conclusión.
> **Teorema.** El número total de subconjuntos de un conjunto $A$ de $n$ elementos es $2^n$. En particular, $$|\mathcal{P}(A)| = \sum_{k=0}^n \binom{n}{k}= 2^n$$

**Demostración.** Sea $X$ un conjunto con $n$ elementos. El número de subconjuntos de $X$ está dado por la suma de subconjuntos de $X$ de cardinales $0,1,2, \cdots, n$ respectivamente, es decir
$$|\mathcal{P}(X)| = \sum_{k=0}^n |\mathcal{P}(X)| = \sum_{k=0}^n \binom{n}{k}$$
Basta ver que $\sum_{k=0}^{n} \binom{n}{k} = 2^n$. Podemos probarlo usando el [[Principio de la inducción]].
- (caso base) $n= 1$ tenemos que $\sum{k= 0}^1 \binom{1}{k} = \binom{1}{0} + \binom{1}{1} = 1+1 = 2$
- (paso inductivo) supongamos $P(k) : \sum_{i=0}{k} \binom{k}{i} = 2^k$ verdadero y veamos que vale $P(k+1)$. Usando la identidad de pascal tenemos que
	$$\begin{align} \sum_{i=0}^{k+1} \binom{k+1}{i} & = \binom{k+1}{0} + \sum_{i=0}^{k+1} \binom{k+1}{i} = \binom{k}{0} + \sum_{i=1}^k \binom{k}{i} + \binom{k}{k-1} \\
	& = \sum_{i=0}^{k} \binom{k}{i} + \sum_{i=0}^{k} \binom{k}{i} = 2 \sum_{i=0}^{k} \binom{k}{i} = 2 \cdot 2^k = 2^{k+1}
	\end{align} $$
	de esta manera demostramos $P(k+1)$ verdadera y queda demostrado que la proposición es verdadera para todo $n \in \mathbb{N}$. $\blacksquare$  

Los resultados de esta nota y [[Acciones Combinatorias]] se pueden escribir en el siguiente cuadro
 ![[Pasted image 20220711172528.png]]
 ---
 ## Resolución del problema "maneras de elegir un equipo"

Fijemosnos que lo primero que nos piden es elegir un líder entre el curso de $n$ estudiantes, entonces tenemos $n$ posibilidades distintas para elegir (o también $\binom{n}{1}$). Luego, de entre el grupo de $n-1$ de estudiantes que restan tenemos que elegir $m-1$ para formar el equipo, $\binom{n-1}{m-1}$. Otra manera de pensarlo es que tenemos que elegir $n$ estudiantes en un equipo de $m$ participantes $\binom{n}{m}$ y luego tenemos que elegir entre los $m$ participantes a un líder $\binom{m}{1}$ . De tal manera que 
$$m\binom{n}{m}=n\binom{n-1}{m-1}$$
Estos métodos lo podemos generalizar para elegir $l$ líderes entre los $m$ integrantes de la siguiente manera

> **Proposición.** Para toda tripla de enteros $n, \; m, \; l \in \mathbb{N}$ se tiene $$\binom{n}{m}\binom{m}{l}=\binom{n}{l}\binom{n-l}{m-l}$$

**Demostración**. Por un lado tenemos
$$\binom{n}{m}\binom{m}{l} = \frac{n!}{m!(n-m)!} \cdot \frac{m!}{l!(m-l)!} = \frac{n!}{l!(n-m)!(m-l)!}$$
y por el otro
$$\binom{n}{l}\binom{n-l}{m-l} = \frac{n!}{l!(n-l)!} \cdot \frac{(n-l)!}{(m-l)!((n-l)-(m-l))!} = \frac{n!}{(n-m)!l!(m-l)!}$$
de donde la identidad sigue. $\blacksquare$

Luego, nos preguntan cuantas combinaciones existen en total armando los equipos lo más grande que podamos. Entonces, sabemos que eligiendo un líder tenemos que
$$\binom{n}{1} \cdot \binom{n-1}{n-1} + \binom{n}{1} \cdot \binom{n-1}{n-2}+ \cdots + \binom{n}{1} \cdot \binom{n-1}{1} = \sum_{i=0}^{n}n\binom{n-1}{n-i}$$
Pero luego, por la propiedad básica (2) tenemos que 
$$\sum_{i=0}^{n} n \binom{n-1}{n-i} = n \underbrace{\sum_{i=0}^n \binom{n-1}{i}}_{\mathcal{P}(B)} = n \cdot \mathcal{P}(B) = n2^{n-1}$$
Donde $B$ es un conjunto con los mismos elementos de $A$ menos uno. 

---
## Binomio de Newton
Sabemos por la matemática básica que $(a+b)^2 = a^2 + 2ab+ b^2$ y podemos calcular, sin demasiado trabajo, potencias más altas. Es fácil chequear que:
![[Pasted image 20220711190222.png]]
Una pregunta que nos podemos hacer es _¿Podemos adivinar una expresión para $(a+b)^6$?_ debería involucrar los términos de la forma
$$a^6, \quad a^5b, \quad a^4 b^2, \quad a^3 b^3, \quad a^2 b^4, \quad ab^5, \quad b^6$$
O de manera general, debería incluir terminos del tipo
$$a^k b^{6-k} \quad 0 \leq k \leq 6$$
Para encontrar los coeficientes, lo podemos pensar como combinaciones. Por ejemplo, para obtener $a^4 b^2$, debemos multiplicar 4 a's y 2 b's que esten en el producto, existen muchas formas de hacer esto tres de ellas son 
![[Pasted image 20220711191247.png]]
Veamos que la cantidad total de formas de hacer esto es el número combinatorio $\binom{6}{4}$ pues tenemos que elegir 4 $a$'s entre 6, o si no lo podríamos ver como que tenemos que elegir 2 b's entre 6, o sea $\binom{6}{2}$ y por la propiedad de simetría se ve que $\binom{6}{4}=\binom{6}{6-2} = \binom{6}{2}$ . De esta forma, obtenemos que 
$$(a+b)^6 = a^6 + \binom{6}{5}a^5 b + \binom{6}{4}a^4b^2 + \binom{6}{3}a^3 b^3 + \binom{6}{2}a^2 b^4 + \binom{6}{1}ab^5 + b^6$$
Fijemosnos que podemos usar el mismo método para obtener cualquier binomio del tipo $(a+b)^n, n \in \mathbb{N}$ ; esta es comunmente conocida como **expansión binómica o binomio de newton**. 

> **Teorema (Binomio de Newton)** Para todo $(a+b) \in \mathbb{R}$ y para todo $n \in \mathbb{N}$ se tiene $$(a+b)^n = \sum_{k=0}^n \binom{n}{k}a^k b^{n-k}$$

**Demostración.** Usando el [[Principio de la inducción]] y la identidad de pascal sale. $\blacksquare$ 

### Tríangulo de Pascal
Notemos que no es coincidencia que la identidad de pascal aparezca en el binomio de Newton. Si ordenamos los los números combinatorios formando un tríangulo isósceles, con la fila $n$-ésima correspondiendo a los números $\binom{n}{0}, \binom{n}{1}, \dots, \binom{n}{n}$. Para los primeros valores tenemos que
![[Pasted image 20220711193110.png]]
En este triángulo se ilustan dos de las propiedades más importantes de los números combinatorios, la simetría y la identidad de pascal. Observe atentamente que ocurre si resolvemos con la formula los números combinatorios
![[Pasted image 20220711193312.png]]
Note que los números azules y violetas son iguales por simetría y que cada número de cada fila se puede obtener sumando los dos de la fila de arriba. Por ejemplo, en la 5ta fila $1 = 1+0,\; 5 = 1+4, \; 10 = 4+6, \; 10 = 4+6, \; 5 = 4+1, \; 1 = 1+0$. Curiosamente estos mismos números son los coeficientes del binomio de newton para $n=5$. 

Otra propiedad que se cumple es que la suma de los elementos de cada fila nos da una potencia de 2, lo cual ocurre por el teorema que vimos anteriormente que nos dice que la cantidad de subconjunto de un conjunto $|A| = n$ es $2^{|A|}$.
![[Pasted image 20220711193847.png | 350]]
Este  triángulo  siempre  ha  atraído  a  mucha  gente  por  su  belleza  y  por  la  cantidad de  propiedades  que  encierra.


