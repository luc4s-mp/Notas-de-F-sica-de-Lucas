En [[R]] ya intentamos hacer nuestro primer acercamiento de como definir los números reales a partir de los números racionales, intentando "agregar" al conjunto las soluciones de ecuaciones que no eran resolvibles en los racionales, como $x^2 = 2$ o $x^2 = 3$. Pero vimos que esto fue un intento en vano porque pueden existir infinitas de estas ecuaciones que requieren de números irracionales para ser resueltas. 
Esto fue un problema muy discutido en las matemáticas del siglo 19, varias formas de definir a los números reales a partir de los racionales [[Q]] fueron propuestas. _¿Por qué? ¿Cúal era el objetivo de definir formalmente a los reales?_ Definir a los reales es útil para tener unas bases muy sólidas sobre las cuales apoyar nuestros teoremas, a fines del siglo 19 la matemática entró en crisis porque cada vez se creaban estructuras más complicadas pero ni siquiera existía un concepto formal de **función**, para los matemáticos de este tiempo una función era todo tipo de polinomios, senos, cosenos, raíces, etc. No existia una clara distinción acerca de qué era y no era una función. 
Siguiendo el modelo histórico presentaremos una definición inicial de los reales que no esta totalmente completa. La profundización de esta definición será vista más adelante.  

## Una mejor definición de $\mathbb{R}$ 
Como sabemos $\mathbb{Q} \subseteq \mathbb{R}$, por lo cual todas las propiedades que se cumplen en [[Q]] se cumplen en [[R]]. Los números reales son un #Cuerpo , es más es un #CuerpoOrdenado pues tienen las propiedades de ordenación (es decir podemos decir si un número real $a$ es más grande o más chico que otro $b$). Tenemos que encontrar una manera de claramente definir a que nos referimos cuando decimos que $\mathbb{R}$ no contiene los "huecos" que dejan los $\mathbb{Q}$. Como esto es lo que diferencia a ambos conjuntos, vamos a formalizar esta noción en un axioma nuevo (que se a agrega los [[Axiomas (Básicos) de los números reales]]) propio de los números reales a la cual llamaremos **Axioma del supremo y el ínfimo**.

> (P13) **Axioma del supremo e ínfimo**. Todo subconjunto no vacío de números reales $\mathbb{R}$ que está _acotado superiormente_ tiene una "cota superior mínima" o _supremo_. Análogamente, todo subconjunto no vacío de los números reales $\mathbb{R}$ que está _acotado inferiormente_ tiene una "cota inferior máxima" o _ínfimo_.

Para entender este axioma tenemos que definir:
> **Definición.** Un subconjunto $A \subset \mathbb{R}$ esta _acotado superiormente_ si existe un $b \in \mathbb{R}$ tal que $a \leq b$ para todo $a \in A$. El número $b$ es llamado **cota superior de $A$**.

> **Definición**. Un subconjunto $A \subset \mathbb{R}$ está _acotado inferiormente_ si existe un $l \in \mathbb{R}$ tal que $l \leq a$ para todo $a \in A$. El número $l$ es llamado **cota inferior de $A$**.

 No todos los subconjuntos de $\mathbb{R}$ están acotados, a partir de estas definiciones podemos probar:
> **Teorema**. $\mathbb{R}$ no está acotado superiormente.

**Demostración**. Supongamos por el absurdo que existe un $a \in \mathbb{R}$ y es cota superior de $\mathbb{R}$. Sabemos por la definición anterior que $x \leq a$ para todo $x \in \mathbb{R}$. Pero, como $a +1 \in \mathbb{R}$ y que $a < a+1$ entonces se genera una contradicción. $\blacksquare$

Notemos que esto puede parecer un poco obvio, en el sentido que obviamente que no existe un número que sea más grande que todos los números reales. 
Nos faltan definir estos conceptos de "supremo" e "ínfimo". 

> **Definición**. Un número real $s$ es un **supremo** de un conjunto $A \subseteq \mathbb{R}$ si cumple los siguientes requisitos:
> 1. $s$ es una **cota superior** de A.
> 2. si $\forall b \in \mathbb{R}$ que es una cota superior de A, entonces $s \leq b$. 
> Lo denotamos $\sup (A) = s$.

> **Definición**. Un número real $i$ es un **ínfimo** de un conjunto $A \subseteq \mathbb{R}$ si cumple los siguientes requisitos: 
> 1. $i$ es una cota inferior de A. 
> 2. si $\forall l \in \mathbb{R}$ que es una cota inferior de A, entonces $i \geq l$. 
> Lo denotamos $\inf(A) = i$.

Aunque un conjunto puede tener infinitas cotas superiores e inferiores solo puede tener **un supremo** o/y  **un ínfimo**.

> **Teorema**. $\mathbb{N}$ no está acotado superiormente. 

**Demostración**. Supongamos por el absurdo que está acotado superiormente y existe (por P13) un $\sup(\mathbb{N}) \in \mathbb{R}$, llamamos $\alpha = \sup(\mathbb{N})$. Luego se dice que $n \leq \alpha$ para todo $n \in \mathbb{N}$. En consecuncia, como sabemos que $n+1 \in \mathbb{N}$, se debe cumplir $n+1 \leq \alpha$ o lo que es lo mismo $n \leq \alpha-1$. Pero entonces $\sup(\mathbb{N}) = \alpha -1$ y se llega a una contradicción, porque el supremo de un conjunto es único. $\blacksquare$  

> **Colorario (propiedad arquimediana)**. Para cada número $\epsilon > 0, \; \exists \; n \in \mathbb{N}, \frac{1}{n} < \epsilon$ 

Esta propiedad nos dice que **existen infinitos números** entre 0 y 1 por lo cual sin importar el $\epsilon$ que tomemos siempre va a existir un $\frac{1}{n}$ más chico. Esto lo sabemos del teorema de arriba que nos dice que justamente no importa que $\alpha$ muy grande tomemos para ser nuestra cota superior, siempre va a existir un número natural más grande.

**Ejemplo**. Sea $A = \{\frac{1}{n} : n \in \mathbb{N}\} = \{1,\frac{1}{2}, \frac{1}{3}, \cdots\}$ 
Decimos que $A$ esta acotado superior e inferiormente. Una buena cota superior que podríamos tomar sería $3, \; 2,\; 3/2$. Para el supremo podrá observar que puede ser $\sup(A) = 1$. Pero esto lo tenemos que demostrar usando la definición de supremo. Veamos que (1) se cumple pues $1 \geq 1/n$ para todo $n \in \mathbb{N}$. Para verificar (2), empezamos asumiendo que estamos en poseción de otra cota superior $b$. Como $1 \in A$, y $b$ es una cota superior de $A$, debemos tener que $1 \leq b$. Y queda demostrado (2). 
Luego, para calcular $\inf(A)$ tengamos en cuenta que $0$ es una cota inferior de A, entonces $0 \leq \inf(A)$ por (2) de la definición de ínfimo. Supongamos por un momento que $\inf(A) > 0$. Por la propiedad arquimediana, existe un $n_0 \in \mathbb{N}$ tal que $0 < \frac{1}{n_0} < \inf(A)$. Pero $\frac{1}{n_0} \in A$, por lo que se debería cumplir que $\inf(A) \leq \frac{1}{n_0}$. Pero esto genera una contradicción pues si $\frac{1}{n_0} < \inf(A) \leq \frac{1}{n_0}$, que viene de suponer que el infimo es mayor que 0,  $\inf(A) = 0$.  $\blacksquare$ 

De este ejemplo podemos concluir que el supremo e ínfimo **pueden pertencer o no al conjunto**, cuando sí pertencen los llamamos de manera diferente:

> **Definición**. Un número real $a_0$ es un **máximo** del conjunto $A \subseteq \mathbb{R}$ si $a_0$ es un elemento de $A$ y $a_0 \geq a$ para todo $a \in A$. Similarmente, un número $a_1$ es un **mínimo** del conjunto $A$ si $a_1$ es un elemento de $A$ y $a_1 \leq a$ para todo $a \in A$.

> **Proposición.** Sea $A \subseteq \mathbb{R}$, $A \neq \emptyset$ acotado superiormente e inferiormente.
> 1. Sea $-A = \{x \in \mathbb{R} | \; -x \in A \}$. Entonces, $-A \neq \emptyset$, $-A$ está acotado superiormente y  $\inf(A) = - \sup(-A)$ 
> 2. Sea $B = \{y : y \leq a, \forall a \in A\}$ = {cotas inferiores de A}. Entonces $B \neq \emptyset$, y está acotado superiormente $\sup(B) = \inf(A)$.

### Lema Útil
Lo llamaremos de esta manera porque será muy usado en el Ánalisis 1. 

> **Lema (Útil).** Sea $A \subseteq \mathbb{R}$, $A \neq \emptyset$, acotado superiormente e inferiormente:
> 1. Sea $\alpha$ una cota superior de $A$. Luego $\alpha = \sup(A)$ si y solo si para todo $y < \alpha$ existe un $a \in A$ tal que $y < a \leq \alpha$ .
> 2. Sea $\beta$ una cota inferior de $A$. Luego $\beta = \inf(A)$ sí y solo sí  para todo $y > \beta$ existe un $a \in A$ tal que $\beta \leq a < y$.

A veces, se vuelve complicado demostrar el supremo y el ínfimo de un conjunto, entonces la proposición anterior y este lema nos facilitan un poco este proceso. El lema nos dice que si queremos probar que un número es el supremo tenemos que demostrar que para todo número mayor existe un elemento de A en el medio. 

**Demostración**. 
- ($\Rightarrow$) Supongamos $\alpha = \sup(A)$. Ahora como $y < \alpha$, $y$ no es una cota superior de $A$. Pero entonces existe un $a \in A$ tal que $y < a$ y ya sabemos que $a \leq \alpha$. Luego, $y \leq a \leq \alpha$.
- ($\Leftarrow$) Supongamos $\alpha$ una cota superior de $A$ y que para todo $y < \alpha$ existe un $a \in A$ tal que $y < a \leq \alpha$. Como  $\alpha$ es una cota superior, $\sup(A) \leq \alpha$. Si llegara a suceder que $\sup(A) < \alpha$. Entonces, según nuestra hipótesis, debería existir un $a \in A$ tal que $\sup(A) < a \leq \alpha$, pero esto último es una contradicción pues el supremo de $A$ es mayor que todos los elementos de $A$ por definición. Por lo tanto, $\sup(A) = \alpha$. $\blacksquare$  

Usemos el lema útil en un ejemplo.

**Ejemplo.** $A = \Big{\{} 3 + \frac{1}{n^3} : n \in \mathbb{N} \Big{\}}$ encontremos el supremo y el ínfimo de este conjunto. Notemos que $n>1 \rightarrow 3n^3 + 1 > 3n^3$ esto nos lleva a $\frac{3n^3 + 1}{n^3} > 3 \rightarrow 3+ \frac{1}{n^3} > 3$ luego 3 es una cota inferior del conjunto. Luego, por el axioma del supremo e ínfimo el conjunto tiene infimo. Veamos que $\inf (A) = 3$.
Sea un número $y > 3$ el lema útil nos dice que si 3 es el ínfimo entonces siempre existe un $t \in A$ tal que $3<t<y$. Si tenemos que $y > 3 \rightarrow y-3>0$, luego por la propiedad arquimediana existe un $n_0 \in \mathbb{N}$ tal que $0 < \frac{1}{n_0} < y-3 \rightarrow 0 < \frac{1}{n_0} < y-3$ se sigue entonces que $0 < \frac{1}{n^3} < \frac{1}{n_0} < 3-y$ por último sumando $3$ en todas las desigualdades obtenemos $3 < \underbrace{\frac{1}{n_{0}^3} + 3}_{\in A} < y$  y listo!
Lo siguiente que haremos será ver si está acotado superiormente, como $n>1 \rightarrow n^3>1$ y 
$\rightarrow_{+3n^3} \; 4n^3 > 3n^3 + 1 \rightarrow 4 > \frac{3n^3+1}{n^3} = 3 + \frac{1}{n^3}$   y tenemos que 4 es una cota superior del conjunto A.
Veamos ahora que $\sup(A) = 4$. Por el lema útil si podemos demostrar que para todo $y < 4$, existe un $t \in A$ tal que $y < t \leq 4$ entonces 4 es el supremo. Si $n=1$ tal que $4 \in A$ y entonces para todo $y < 4$ podemos elegir siempre $t =4 \in A$ y este es el supremo. En estos casos en el que el supremo pertenece al conjunto lo llamamos **máximo** y cuando el ínfimo pertenece al conjunto (lo cual no ocurre en este caso) decimos que tiene **mínimo**.

Notemos que el conjunto $\{x \in \mathbb{Q}: x^2< 2\}$ no tiene supremo en este caso pues no existe un número en los racionales tal que $x^2 = 2$ (lo probamos en [[Axiomas (Básicos) de los números reales]]), está acotado superiormente por valores como $2$, $3/2$, e inclusive $1415/1000$ pero no existe la más chica de las cotas superiores. De esta manera, este conjunto solo tiene supremo en los números reales ya que tenemos la certeza de que este número existe en el conjunto. Ahora, ¿Cómo lo calculamos? El tema es que al tener infinitos decimales es practicamente imposible calcularlo, pero podemos _aproximarlo_. Las técticas para aproximarlode forma precisa se ven en Análisis II, concretamente en [[Aproximando el Error]]. 
Veremos algunas propiedades que se concluyen de este axioma en [[Consecuencias del Axioma de Completitud]]

