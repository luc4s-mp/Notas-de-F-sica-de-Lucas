# Relaciones
> #Definición Sean A y B [[Conjuntos]]. Una **relación** $\mathcal{R}$ de A en B es un subconjunto cualquiera de $\mathcal{R}$ del producto cartesiano $A \times B$. Es decir, $\mathcal{R} \subseteq A \times B$.  O equivalentemente, $\mathcal{R} \in \mathcal{P}(A \times B)$.

Si el elemento *x* que pertence al conjunto A está relacionado con *y* del conjunto B, es decir $(x, y) \in \mathcal{R}$ escribimos $x \mathcal{R} y$ o $x \sim y$. 

Existen diversas maneras de graficar una relación: usando diagramas de Venn (representando con flechas a las relaciones de un conjunto a otro), usando un gráfico cartesiano, entre otros. Si la relación es de un conjunto en sí mismo (es decir $\mathcal{R} \subseteq A \times A$) podemos representarla también utilizando un **grafo dirigido** (es decir como un conjunto de puntos llamados vértices, que son los elementos de A, y flechas representando las relaciones). 
Para ver mejor en que consiste un grafo y sus aplicaciones matemáticas ver [[Teoría de Grafos]].

Por ejemplo, supongamos que tenemos el conjunto $A = \{a,b,c,d\}$, entonces
$$\mathcal{R}_1 = \{(a,a), (a,b), (b,b), (a,d), (c,c),(c,d),(b,a), (d,d)\}$$
podemos representarlo de la siguientes maneras;
![[Pasted image 20220628103350.png]]
Y la representación en un grafo dirigido nos quedaría,
![[Pasted image 20220628103414.png | 200]]
 
## Propiedades de las Relaciones
Entre las propiedades usuales de relaciones que aparecen naturalmente están las siguientes. 
Una relación $\mathcal{R} \subseteq A \times A$ puede ser:
- Se dice que $\mathcal{R}$ es **reflexiva** si $(x,x) \in \mathcal{R}$, $\forall x \in A$. En terminos de un grafo de la relación, $\mathcal{R}$ es reflexiva si en cada vértice hay una fecha que es un "bucle", es decir que parte de él y llega a él. 
- Se dice que $\mathcal{R}$ es **simétrica** si cada vez que un par $(x,y) \in \mathcal{R}$, entonces el par "simétrico" $(y,x) \in \mathcal{R}$ . En términos del grafo de la relación, $\mathcal{R}$ es simétrica si por cada fecha que une a dos vértices en un sentido, hay una fecha (entre los mismos vértices) en el sentido opuesto.
- Se dice que $\mathcal{R}$ es **antisimétrica** si cada vez que un par $(x,y) \in \mathcal{R}$ con $x \neq y$ , entonces el par $(y,x) \notin \mathcal{R}$ (o dicho de otra manera $\forall x,y \in \mathcal{R}, \; x \mathcal{R} y \text{ e } \; y \mathcal{R} x \;\Rightarrow y = x$) . En términos del grafo de la relación, $\mathcal{R}$ es antisimétrica si no hay un par de flechas en sentidos opuestos que unen dos vértices distintos.
- Se dice que $\mathcal{R}$ es **transitiva** si para toda terna de elementos $x, y, z \in A$ tales que $(x,y) \in \mathcal{R}$ y $(y,z) \in \mathcal{R}$, entonces $(x,z) \in \mathcal{R}$ . En términos del grafo de la relación, $\mathcal{R}$ es transitiva si hay un "camino directo" por cada "camino con paradas".
- Se dice que $\mathcal{R}$ es **total** si para $\forall x, y \in A$, se tiene que $(x,y) \in \mathcal{R}$ ó $(y,x) \in \mathcal{R}$. 
Además puede satisfacer:
- Se dice que $\mathcal{R}$ satisface la **dicotomía** si $\forall x,y \in A$, se tiene que $x \mathcal{R} y$ ó $y \mathcal{R}x$ y solo una de ellas.
- Se dice que $\mathcal{R}$ satisface la **tricotomía** si $\forall x,y \in A$, se tiene que $x \mathcal{R}y$, $y \mathcal{R}x$ ó $y = x$ y solo una de ellas.

### Relación de equivalencia y la relación de orden
Existen tres relaciones muy importantes y frecuentes en la matemática que son:
> #Definición Sea $\mathcal{R} \subseteq A \times A$.  
> 1. R se dice **relación de equivalencia** si es ==reflexiva==, ==simétrica== y ==transitiva==. 
> 2. R se dice **relación de orden parcial** si es ==reflexiva==, ==antisimétrica== y ==transitiva==. 
> 3. R se dice de **orden total** si es de orden parcial tal que $\forall a, b \in A$ se cumple que $a \mathcal{R} b$ o $b \mathcal{R} a$.

Nos podemos preguntar ¿Cuál es la aplicación de todo esto? Ya vimos que los conjuntos nos sirven para definir a diversos conjuntos númericos en los cuales podemos realizar diversas operaciones, que son cada vez más interesantes a medida que van creciendo en complejidad, por ejemplo en los números enteros solo podemos dividir en algunas ocasiones especiales pero en los números racionales siempre podemos hacerlo. Ahora podemos preguntarnos ¿Como definimos en estos conjuntos relaciones entre los elementos como "es menor que" $<$ o "es menor o igual que" $\leq$ o "es igual a" $=$ de forma concisa y sin problemas? ¿Cómo hariamos para expresar con proposiciones lógicas que si podemos decir que _"a es menor o igual que a"_ pero no que *"a es menor que a"* ?  Veamos que justamente podemos definir a estas como **relaciones entre los conjuntos**. 

Por ejemplo, sea $A = \mathbb{R}$, queremos definir la relación $\mathcal{R}_1$, "es menor que" . Es decir, $(a,b) \in \mathcal{R}$ si $a < b$ . Notemos que esta relación **no es reflexiva** porque no existe en ella $a < a$ , para ningún $a \in \mathbb{R}$, pero si es **antimétrica**, **transitiva** y se cumple la **tricotomía**. 
Luego, si definimos una relación $\mathcal{R}_2$, "es menor o igual que". Tenemos que si $(a,b) \in \mathcal{R}$ si $a \leq b$.  Esta relación sí es **reflexiva**, es **antisimétrica**, es **transitiva**, es **total** y se cumple la **dicotomía**.

En muchas **estructuras algebráicas** (lugares definidos por un conjunto y operaciones entre los elementos de ese conjunto) podemos definir a las operaciones como relaciones de diversos tipos. 

#### Relación de Orden
Podemos notar entonces que la relación $\mathcal{R}_2$ cumple todas las condiciones para ser una **relación de orden**.  Mientras que la relación $\mathcal{R}_1$ no lo es porque no es reflexiva.

Un ejemplo muy interesante de una relación de orden que todo el mundo conoce es la del **orden del alfabeto**. Que a su vez nos ayuda a luego ordenar a palabras alfabéticamente, por ejemplo sabemos que "aereo < bala < barral < mero" por la primera letra de estas palabras (la primera empieza con "a" que es la primera en el orden alfabético y luego va la palabra que empieza con "b" y  así sucesivamente). Y si dos palabras empiezan con la misma letra, nos movemos a la segunda y las comparamos, y si estas son iguales nos movemos a la tercera y así sucesivamente. A esto lo llamamos **orden lexicográfico**. 

Podemos basarnos en el orden lexicográfico para ordenar un producto cartesiano, obviamente para poder realizar esto **los elementos del conjunto A tienen que estar relacionados con un orden**. Si tenemos
$$A^n = {A \times \dots \times A}$$
el orden lexicográfico esta definifo como: dados $(a_1, \dots, a_n) \neq (b_1, \dots , b_n)$ sea $i$ el primer índice tal que $a_i \neq b_i$ . Entonces, 
- Si $a_i < b_i$, entonces $(a_1, a_2, \dots, a_n) < (b_1, b_2, \dots, b_n)$.
- Si $a_i > b_i$ entonces $(a_1, a_2, \dots, a_n) > (b_1, b_2, \dots, b_n)$

#### Relación de equivalencia
Notemos que al dividir un número entero por 2 obtenemos que este puede ser par o impar (esta es una relación de equivalencia), tiene que ser alguno de los dos no puede ocurrir que un número sea par e impar al mismo tiempo. También en la geometría se clasifica a los tríangulos que son semejantes si tienen los mismos ángulos, notemos que no existen dos tríangulos que sean semejantes pero que tengan ángulos distintos. 

Parece ser que en las relaciones de equivalencia, el conjunto A se "parte" en pezados que no comparten ningún elemento entre sí. Al conjunto de los números enteros lo podemos dividir en dos: los pares e impares, y estos no comparten elementos. Entonces veamos que **tener una relación de equivalencia en A es lo mismo que tener una partición en A**.
A esta partición del conjunto la llamamos *clase de equivalencia*.

---
## Clase de Equivalencia
A es un conjunto tal que $\mathcal{R} \subseteq A \times A$. Sea $a \in A$, se llama a **clase de equivalencia de a** al subconjunto de A definido como:
$$\bar{a} = \{ b \in A: a \mathcal{R} b  \space (o \space a \sim b)\} \subseteq A$$
>  **Proposición (Propiedad fundamental de las clases de equivalencia)** Sea $\mathcal{R} \subseteq A \times A$ una relación de equivalencia y $a, b \in A$, se cumple que $\bar{a} = \bar{b} \vee \bar{a} \cap \bar{b} = \emptyset$.

**Demostración.** Supongamos que $\bar{a} \cap \bar{b} \neq \emptyset$. Existe un $c \in A$ tal que $c \in \bar{a} \cap \bar{b}$, es decir $c \mathcal{R}a$ y $c \mathcal{R}b$ . Pero, por simetría, $a \mathcal{R} c$ y luego por transitividad $a \mathcal{R}c$ y $c \mathcal{R}b \implies a \mathcal{R} b$ por lo cual $a \in \bar{b}$ (podemos aplicar otra vez el proceso para obtener $b \in \bar{a}$). Pero luego, para todo elemento $c' \in \bar{a}$   ocurre que $c' \mathcal{R} a$ y como $a \mathcal{R}b$ por transitividad $c' \mathcal{R} b$, entonces $c' \in \bar{b}$ y nos queda $\bar{a} \subseteq \bar{b}$ (aplicamos el mismo proceso otra vez y obtenemos que $\bar{b} \subseteq \bar{a}$). $\blacksquare$ 


## La Relación Inversa
Se llama a la relación inversa a un subconjunto de $B \times A$ de la forma 
$$\mathcal{R}^{-1} = \{(b, a) \in B \times A: (a, b) \in \mathcal{R} \}$$

### Lema
> $\mathcal{R} \subseteq A \times A$. Entonces, se cumple que $\mathcal{R} = \mathcal{R}^{-1}$ sí y solo sí $\mathcal{R}$ es simétrica.


#### Demostración
- $(\Rightarrow)$ Suponemos que $\mathcal{R} = \mathcal{R}^{-1} \implies \forall (a, b) \in \mathcal{R}$ se cumple $(a, b) \in \mathcal{R}$ y viceversa.  Por la definición del concepto de simetría podemos concluir que como $(a, b) \in \mathcal{R}^{-1}$ entonces $(b, a) \in \mathcal{R} \implies \mathcal{R}$ es simétrica.

- $(\Leftarrow)$ Supongamos que $\mathcal{R}$ es simétrica, queremos concluir que $\mathcal{R} = \mathcal{R}^{-1}$, tomemos $(a, b) \in \mathcal{R}^{-1}$. Por la definición de la relación inversa debe ocurrir que $(a, b) \in \mathcal{R}^{-1} \implies (b, a) \in \mathcal{R} \implies (a, b) \in \mathcal{R} \implies \mathcal{R} = \mathcal{R}^{-1}$ lo cual cumple la definición de simetría en una relación.
De esta forma, demostramos el lema planteado inicialmente. $\blacksquare$

---
Las relaciones son utilizadas en matemática para definir con formalidad a las [[Funciones en R]].

#Estructura-matematica 

