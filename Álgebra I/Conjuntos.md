# Teoría de Conjuntos
> Un conjunto es una colección de objetos, llamados **elementos**, que tiene la propiedad que dado un objeto cualquiera, se puede decidir si ese objeto es un elemento del conjunto o no.

**Ejemplos**:
- $A = \{1, 2, 3\}, C = \{1, \{1\}, \{2,3\}\}$
- $\mathbb{N} = \{1, 2, 3, 4, \cdots\}$
- $\emptyset$ o $\{\}$ el **conjunto vacío**, o sea el conjunto que no posee ningún elemento

Una observación importe a hacer es que el orden de los elementos no importa en un conjunto, y en un conjunto no se tiene en cuenta las repeticiones de elementos.

## Pertenencia, Inclusión e Igualdad
Decimos que un elemento "$x$" está dentro de un conjunto usando el simbolo $\in$ que se lee como "pertenece". Entonces "$x$ pertenece a A" se escribe como $x \in A$. En cambio, si queremos decir que "$x$ no pertenece a A" escribirmos $x \notin A$ . 
Los conjuntos pueden estar relacionados a otros de muchas maneras. Por ejemplo, $A= B$ implica que ambos conjuntos tienen los mismos elementos. Es decir, todo elemento de A pertence a B y todo elemento de B pertenece a A. Esta proposición de decir "todo elemento de un conjunto A está en el conjunto B" la acortamos diciendo que el conjunto A está **incluido** en el conjunto B.
Es decir, decimos que el conjunto B *está contenido en* A, y se denota $A \subseteq B$, si todo elemento de B es elemento de A. 
$$A \subseteq B = \{\forall \; x \in A \implies x \in B\}$$
También decimos que B *está incluido en* A, o que B *es un subconjunto de* A.

Decimos que dos conjuntos son **iguales** cuando:
$$A = B \iff B \subseteq A \wedge A  \subseteq B $$
Los conjuntos se pueden reepresentar en unos diagramas llamados "**diagramas de Venn**" en los cuales se puede ver visualmente la situación de los conjuntos con los que tratamos. En estos diagramas, los conjuntos son representados por círculos o elípses. Por ejemplo, para reepresentar que $A \subseteq B$ en un diagrama de Venn nos queda
![[Pasted image 20220627110329.png]]
En la teoría de conjuntos existen dos conjuntos distinguidos que son el **conjunto universal** (denotado $\mathrm{U}$) que es el conjunto que contiene a todos los conjuntos con los que estamos trabajando y el **conjunto vacío** (denotado $\emptyset$) que no posee ningún elemento, también se suele denotar $\{\}$. Es importante, al trabajar con conjuntos saber cual es su universal, sino tenemos este definido entonces no sabemos cuales son nuestros límites al operar los conjuntos o sus elementos. 
Todo conjunto $A$ está contenido en el conjunto universal $A \subseteq \mathrm{U}$ y contiene al vacío $\emptyset \subseteq A$.

### Conjunto de Partes
El **conjunto de partes** de A, que se denota $\mathcal{P}(A)$, es el conjunto formado por todos los subconjuntos de A. 
$$\mathcal{P}(A) = \{B: B \subseteq A\}$$


## Cómo definir conjuntos
Existen dos formas de definir un conjunto, por **extensión** (listando todos los elementos del conjunto entre llaves, esto solo es posible hacerlo cuando el conjunto es finito) y por **compresión** (a través de una propiedad que describe los elementos del conjuntos). 
Un conjunto definido por comprensión se denota usando llaves y la proposición definidora $P$. Por ejemplo, si B es el conjunto de todos los elementos de $x$ que cumplan la propiedad $P(x)$ se escribe 
$$B = \{x \in \mathrm{U}: P(x)\}$$
**Conjutos numéricos**
- $\mathbb{N} = \{1, 2, 3, 4, \cdots\}$ Números Naturales [[N]]
- $\mathbb{Z} = \{\cdots, -2, -1, 0, 1, 2, \cdots\}$ Números Enteros [[Z]]
- $\mathbb{Q} = \{\forall m, n \in \mathbb{Z}: \frac{m}{n}\}$ Números Racionales [[Q]]
- $\mathbb{R}$ Números Reales . Es más complicado entender como los números racionales entran dentro de los números reales [[R]] e incluimos a los **números irracionales** (normalmente representados $\mathbb{R} - \mathbb{Q}$),  que son aquellos números que no se pueden escribir como la división de dos enteros, para entender como se forman los números reales usamos el [[Axioma del supremo y el ínfimo]]
- $\mathbb{C}$ Números Complejos. Se forman usando los números imaginarios ($i = \sqrt{-1}$) y los números reales.

### Paradojas
No cualquier propiedad o proposición es aceptable para definir un conjunto. Esto sucese por ejemplo si quisieramos considerar "el conjunto" formado por todos los conjuntos que no se tienen a sí mismos como uno de sus elementos. Entonces, tenemos
$$M = \{X : X \notin X\}$$
Ahora tomemosal mismo $M$ y veamos si pertenece al conjunto $M$ o no. Veamos que si $M \in M$ entonces $M \notin M$ pero si $M \notin M$ entonces $M \in M$ !!! Es una contradicción, entonces $M$ no puede ser un conjunto. Esta paradoja es muy famosa y es conocida como la **paradoja de autoreferencia de Russell**. Una versión de esta paradoja que es muy conocida es la paradoja del barbero.

## El descubrimiento de Cantor y los inicios de la teoría de conjuntos
A veces es dificil entender de donde los matemáticos sacaron esas ideas tan abstractas que fundan a la matemática, es por esto que pasaré a explicar un poco de la historia de la teoría de conjuntos, con el fin de entender para que surgío y cual lugar en las matemáticas. La verdad es que a día de hoy la mayoría de las teorías de la matemática se basan en los Conjuntos, así que usted mismo notará su importancia cuando avance en su aprendizaje.

A fines del siglo 19, Georg Cantor inicio el estudio de la que luego se llamaría **Teoría de Conjuntos** al hacer el increíble descubrimiento de que los números reales no son _"contables"_, es decir, el probó que estos números no pueden ser contados usando números naturales. Esto puede causar muchas preguntas, ¿Cómo es posible "contar" un conjunto con infinitos elementos? ¿Qué quiere significar exactamente esto? En respuesta a esta última pregunta, lo que quiere decir es que el conjunto de los números reales tiene *más elementos* que el conjunto de los números naturales, es decir, que existen _infinitos más grandes que otros_. Lo cual nos genera aún más preguntas, las cuales no responderemos (por ahora), lo importante para entender de todo esto es que Cantor inicio muchos problemas en la matemática. 

Antes de él en el siglo 19 todavía se seguía usando a "los elementos" de Euclides (300 a.C.) como fundamentos de la matemática, pero desde los tiempos de euclides se habían desarrollado ramas de las matemáticas muy importantes como el Cálculo Diferencial e Integral y se habían descubierto las geometrías no euclidianas. Esto hizo a las matemáticos revisar  más profundidad las definiciones más básicas y encontraron que estaban pobremente definidas. Cosas tan simples como las funciones no estaban claramente definidas, por lo que no se entendía que es una función y que no.

Cantor planteaba una nueva forma de definir a estas ramas usando la teoría de conjuntos, esto dividió a los matemáticos entre los "intuicionistas" que pensaban que las matemáticas son una creación de la mente humana, por lo tanto no se pueden formalizar al 100% y pensaban que la idea de Cantor de que hay conjuntos infinitos más grandes que otros era absurda y los "formalistas" pensaban que la matemática si se podía formalizar en unas bases lógicas fuertes usando este nuevo descubrimiento de Cantor. 
El paso del tiempo demostró que ambos tenian razón en ciertos aspectos, resulta que siempre van a existir proposiciones que no se pueden demostrar y tenemos que asumir que son verdaderos (los conocidos "axiomas") para poder demostrar todas las siguientes (este problema es conocido como "Teorema de la Incompletitud de Göbel").

> “Nadie  podrá expulsarnos  del  paraíso  que  Cantor  creó  para  nosotros”
> 	  - **David Hilbert**,  matemático  alemán  (1862 – 1943

<iframe width="560" height="315" src="https://www.youtube.com/embed/RRg38oNQ9vk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# Operación de Conjuntos
Muchas veces, cuando operamos con conjuntos es importante tener el *conjunto referencial* U. 

## Complemento $^{c}$
Llamamos al complento de A (en U), al cual denotamos $A^{c}$ o $A'$ o $\bar{A}$, al conjunto de elementos de U que no pertenecen a A. 
$$A^c = \{x \in U: x \notin A \}$$
Otra manera de definir esta operación es $A^c = U - A$
![[Pasted image 20220627120255.png]]

---

## Unión $\cup$
Sean A, B subconjuntos de un conjunto referencial U. La **unión** de A y B es el conjunto de elementos $A \cup B$ que pertenecen al conjunto A o al conjunto B.
$$A \cup B = \{x \in U: x \in A \space o \space x \in B \}$$

## Intersección $\cap$
Llamamos a la intersección de dos conjuntos A y B, denotada $A \cap B$, es el conjunto de elementos de U que pertenecen tanto a A como a B. 
$$A \cap B = \{x \in U: x \in A \text{ y } x \in B\}$$
### La unión y intersección de una familia de conjuntos
Las operaciones de unión e intersección de conjuntos pueden realizarse para cualquier número finito n de conjuntos $A_1, A_2, \dots, A_n$:
$$\begin{align}
\bigcup_{i=1}^n A_i = A_1 \cup A_2 \cup \dots \cup A_n = \{x : x \in A_1 \wedge x \in A_2 \wedge \dots \wedge x \in A_n\} \\
\bigcap_{i= 1}^n A_i = A_1 \cap A_2 \cap \dots \cap A_n = \{x : x \in A_1 \vee x \in A_2 \vee \dots \vee x \in A_n \}
\end{align}$$

## Diferencia $-$
Dados dos conjuntos $A$ y $B$, la diferencia entre A y B, denotada $A-B$ , es el conjunto formado por los elementos de A que no pertenecen a B. En simbólos,
$$A - B = \{x : x \in A \;\mathrm{y}\; x \notin B\}$$
O visto de otra manera
$$x \in A - B \iff A \cap B^c \iff x \in A \text{ y } x \in B^c \iff x \in A \text{ y }  x \notin B$$

---

## Diferencia Simétrica $\triangle$
$A \triangle B$ es el conjunto de lo los elementos de U que pertenecen a A o a B pero no los dos a la vez. Es decir,
$$A \triangle B = \{c \in U: (c \in A \text{ y } c \notin B) \text{ o } (c \in B \text{ y } c \notin A)\}$$
Vale:
$$A \triangle B = (A-B) \cup (A-B) = (A \cap B^c) \cup (B \cap
 A^c) = (A \cup B) - (A \cap B)$$

---

## Identidades de conjuntos
> **Teoremas del complemento, unión y intersección**. Para todo par de conjuntos A y B vale que:
> -  Ley del complemento o de la idempotencia: $(A^c)^c = A$
> - Leyes de De Morgan: $(A \cup B)^c =  A^c \cap B^c$ y $(A \cap B)^c = A^c \cup B^c$
> -  Leyes distributivas: $$A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$$$$A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$$

> **Proposición**. Para todo par de conjuntos A y B vale que:
> -$A \subseteq B \iff B^c \subseteq A^c$ 
-$A \cup B = B \iff A \subseteq B$
-$A \cap B = A \iff A \subseteq B$
-$A-B = A \cap B^c = (A^c \cup B)^c$
-$A \triangle B = (A \cap B^c) \cup (B \cap A^c)$  o $A \triangle B = (A \cup B) - (A \cap B)$

---

## Producto Cartesiano
Sean dos conjuntos A y B, el producto cartesiano de A en B es otro conjunto denotado $A \times B$. A diferencia de las operaciones que hablamos anteriormente, porque cuando operabamos dos conjuntos obteniamos otro conjunto en el mismo universo, en este caso lo que obtenemos es un conjunto de **pares ordenados** (denotado con parentesis) que representan cada elemento de este nuevo conjunto. Es decir, supongamos que tenemos un $a \in A$ y un $b \in B$ al hacer $A \times B$ obtenemos que uno de los elementos de este conjunto va a ser $(a, b)$. 
$$A \times B := \{(x,y) : x \in A, y \in B\}$$
Notemos que en los pares ordenados el *orden y las repetisiones sí importan*, a diferencia de los conjuntos donde el orden y las represiones no. Por ejemplo, $\{a, b\} = \{b, a\}$ pero $(a,b) \neq (b,a)$ y $\{a,a,b\} = \{a,b\}$ pero $(a,a,b) \neq (a,b)$.  Veamos que si hacemos el producto cartesiano de más de dos conjuntos obtenemos una $n$-tupla de elementos ordenados.

**Si los respectivos conjuntos universales para A y B son $\mathrm{U}_A$ y $\mathrm{U}_B$ , el conjunto universal de $A \times B$ es el producto de los conjuntos universales $\mathrm{U}_{A \times B} = \mathrm{U}_A \times \mathrm{U}_B$ .**

Una de las maneras más conocidas de representar un producto cartesiano $A \times B$ es usando un **sistema cartesiano**, en el que usando dos rectas, una horizontal y otra vertical (que representan a $\mathrm{U}_A$ y $\mathrm{U}_B$ ). Todos los elementos del conjunto $A \times B$ viven dentro de un rectángulo en el plano:
![[Pasted image 20220627195336.png]]
Uno de los productos cartesianos más conocidos es quizás $\mathbb{R} \times \mathbb{R}$. 

> **Propiedades del producto cartesiano**. Para A, B y X conjuntos arbitrarios valen las siguientes identidades.
> 1. $(A \cup B) \times X = (A \times X) \cup (B \times X)$
> 2. $(A \cap B) \times X = (A \times X) \cap (B \times X)$
> 3. $(A-B) \times X = (A \times X) - (B \times X)$

Notemos que el producto cartesiano, **no es conmutativo ni distributivo ni asociativo**. 
