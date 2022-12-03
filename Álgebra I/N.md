# Los Números Naturales
Ahora, a partir de nuestro conocimiento en [[Conjuntos]], [[Relaciones entre conjuntos]] y [[Funciones]] podemos formar a las números naturales. Son los números que usamos para contar $\mathbb{N} = \{1,2,3,4,\dots\}$ desde primaria los conocemos. Pero supongamos que somos una computadora que no entiende la forma en la cual pensamos los humanos en estos símbolos 2, 3, 4, etc, ella entiende que es un conjunto y una relación porque están bien definidos, entonces _¿Cómo podemos contruir a los números naturales usando solo nuestro conocimiento de conjuntos?_  
Supongamos que tenemos el conjunto $\mathbb{N}$ del cual no sabemos que elementos tiene ni como está construido. Sabemos que tenemos un elemento denotado por el símbolo $1 \in \mathbb{N}$ y también una operación entre los elementos del conjunto llamada "suma" (denotada por ahora como $+_N$, pero más adelante simplemente la llamaremos $+$) y llamamos $1 +_N 1$ al "sucesor de 1" que este pertenece también al conjunto y lo denotamos con el símbolo $2$. Luego, si operamos para obtener  $2 +_N  1 = 1 +_N 1 +_N 1 \in \mathbb{N}$ , a este elemento lo llamamos el "sucesor de 2" y lo denotamos $3$. Esta es una manera de definir a los números naturales, sin embargo usted podrá notar que no es muy completa, pues no me determina que números están en el conjunto y cuales no, por ejemplo ¿Está el 0 en los números naturales? es obvio que no pues no puede construirse como una suma de uno's. 

Podemos hablar de 3 axiomas que me definen concretamente a este conjunto:

>**Axiomas de Peano**
>1. $1 \in \mathbb{N}$ , 1 no es el sucesor de nadie, y es el único natural así.
>2. Si $n \in \mathbb{N}$, $m \in \mathbb{N}$ y $n \neq m$, entonces $n+_N 1 \neq m+_N 1$. "Dos números naturales distintos tienen sucesores distintos".
>3. Si $K \subseteq \mathbb{N}$,  $1 \in K$ y $m \in K$ tal que $m +_N 1 \in K$, entonces $K = \mathbb{N}$.  

Notemos que los primeros 2 axiomas son obvios, pero el tercero no tanto. Basicamente lo que nos está tratando de decir es que los números naturales son el conjunto "más chico" de números capaz de contener a todo número "entero" y sus sucesores.
Cualquier conjunto que cumpla estos 3 axiomas es igual al conjunto de los números naturales $\mathbb{N}$. 

## Propiedades de los números naturales
Podemos armar a la **función sucesor** $s: \mathbb{N} \rightarrow \mathbb{N}$ que a cada $n \in \mathbb{N}$ se le asigna su sucesor. En terminos de $s$, el primer axioma nos dice que no existe sucesor tal que $1 = s(n)$, es decir 1 no está en la imagen de $s$ , mientras que el axioma 2 nos dice que $s$ es una función inyectiva. Si tenemos definida entonces la suma con el elemento 1 podemos definir la suma de cualquier elementro con otro usando esta función. 
Sabemos que $n +_N 1 = s(n)$, entonces $n +_N 2 = (n +_N 1) +_N 1 = s(n +_N 1 = s(s(n))$. 
En general, tenemos que
$$n+_N m = s(s(\dots(s(m))\dots)) = s^n(m)$$
Y de esta manera tenemos definida la suma para cualquier número natural a otro. (Notar que $s^n(m) = s^m(n)$). 

Usando estos axiomas podemos demostrar que las siguientes propiedades se cumplen para la "suma" $+_N$  (a partir de ahora será $+$) y luego para la multiplicación $\cdot$ (que se puede definir como la suma aplicada muchas veces):
- _Conmutatividad_: $m + n = n + m, \; \forall n,m \in \mathbb{N}$ y $m \cdot n = n \cdot m$
- *Asociatividad:* $(m+n) + k = m + (n+k), \; \forall n,m,k \in \mathbb{N}$ y $(m \cdot n) \cdot k = m \cdot (n \cdot k)$. 
- *Distributividad del producto respecto a la suma*: $m \cdot (n + k) = m \cdot n + m \cdot k, \; \forall m, n, k \in \mathbb{N}$.

También podemos definir una **relación de orden**, "es menor que" o "es mayor que" teniendo por definición que $1 < 1+1$ (lo cual sabemos por el axioma 1), entonces todo lo siguiente está permitido. 

A partir de estos axiomas podemos caracterizar a los números naturales, es decir podemos decir que es un número natural y que no. Por ejemplo $1/2$ no es un número natural porque no se puede construir usando una sucesión de unos. Todavía nos podemos hacer un par de preguntas, como ¿Es 1 el menor número natural? ¿Podemos "restar" en los números naturales? 

Notemos que para contestar muchas de estas preguntas es necesario usar los axiomas, pero esto puede resultar un poco abrumante. Si suponemos que ya sabemos que son los números reales [[R]] y como estos se comportan a partir de los [[Axiomas (Básicos) de los números reales]] podemos entonces maniobrar con mayor facilidad a los números naturales sabiendo como anticipación que $\mathbb{N} \subset \mathbb{R}$. 

> **Proposición** Si $n \in \mathbb{N}$, entonces $n > 0$.

**Demostración.** Usaremos el axioma n°3. Sea $K \subseteq \mathbb{R}$ , consideremos $K = \{n \in \mathbb{N} : n > 0\}$. Queremos ver $K = \mathbb{N}$ entonces cumple los 3 axiomas, probemos que se cumple el axioma n°3 de los números naturales. Como $1 > 0$, entonces $1 \in K$. Además si $n \in K$, es decir si $n > 0$, sucesor $n+1 > 0 + 1 = 1 > 0$, y por lo tanto $s(n) = n+1 \in K$. Se sigue entonces que $K = \mathbb{N}$ como queríamos.

Observe detenidamente esta demostración, es muy importante entenderla porque a partir de demostraciones como esta nace uno de los principios más importantes de la matemática, usado muy comunmente, el [[Principio de la inducción]].

### Restas
La oración usada para definir $b < a$ puede ser escrita de la siguiente manera: $b < a \iff b + x = a, \; x \in \mathbb{N}$ . Notemos que esta ecuación no siempre tiene solución. Lo cual tiene sentido porque no todos los números $b$ son menores que 
$a$, por ejemplo $4 < 2$ no es verdadero pues no existe un $x \in \mathbb{N}$ tal que $4+x = 2$ . 

Podemos razonar que este número $x$ (si existe) es único. Supongamos que existen un $y,z \in \mathbb{N}, \; b + y = a$ y $b+z = a$. Luego, $b+y = b+z$ y por la propiedad cancelativa tenemos que $y = z$. Por lo tanto, concluimos que este número si es único.

> **Definición. (Resta)** Para todos los $a,b \in \mathbb{N}$, donde $a>b$ , la función subtracción $s$ esta descripta por $s(a,b) = \text{ un número único en } \mathbb{N} \text{ tal que cumple } b+x = a$ . Será denotada $a-b$.

De vuelta, veamos que para que la resta tenga sentido en los números naturales se tiene que cumplir $a > b$ de otra forma no se puede resolver la ecuación $x+b = a$. Podemos luego crear un conjunto en el que esta ecuación siempre tenga soluciones, lo cual veremos en los números enteros [[Z]].

## Conjunto inductivo 
> #Definición  Diremos que un conjunto $K \subseteq \mathbb{R}$ será **inductivo** si:
> 1. $1 \in K$
> 2.  $m \in K \implies m + 1 \in K, \forall m \in K$
A $m + 1$ se lo llama el *sucesor de* $m$

Ejemplos: el conjunto de los números reales $\mathbb{R}$ *es un conjunto inductivo*. $K = \{x \in \mathbb{R}: x > 1\}$ ***no** es un conjunto inductivo* ya que la condición (2) no se cumple. Sin embargo, $K = \{x \in \mathbb{R}: x \geq 1\}$ ***sí** es inductivo* porque cumple con la (1) y (2) condición.

Notemos que la definición de inductividad en los reales, nace a partir del 3er axioma de los números naturales.

>**Lema.** Sea $\{k_i, i \in I\}$ familia de [[Conjuntos]] inductivos en $\mathbb{R}$. Entonces el conjunto $K = \bigcap_{i \in I} K_i$ **es inductivo**.

 **Demostración**
- $1 \in \bigcap_{i \in I} K_i \implies 1 \in K$
- $n \in K \implies n \in \bigcap_{i \in I} K_i$ por la definición de intersección que nos dice que son los elementos que comparten todos los conjuntos operados de forma que $n \in K_i, \forall i \in I$, como $K_i$ es inductivo entonces $n + 1 \in K_i, \forall i \in I \implies (n + 1) \in \bigcap_{i \in I} K_i \implies (\pi + 1) \in K$
De esta forma, queda demostrada la proposición inicial.

Lo que nos dice este lema es que la intersección de todos los conjuntos inductivos en $\mathbb{R}$ es también inductivo. 

---

Podemos definir a los números naturales usando la definición de conjunto inductivo.

> #Definición Se llama **conjunto de números naturales** $\mathbb{N}$ al conjunto obtenido al intersectar *todos los conjuntos inductivos de* $\mathbb{R}$.

Lo cual tiene sentido pues la definición de conjunto inductivo nace del 3er axioma de peano, y dijimos al principio que los números naturales es el único conjunto que lo cumple.

Un lema muy sencillo nos asegura que no existe un conjunto más chico que el de los números naturales. Es el conjunto inductivo más básico de todos y en el se puede utilizar el llamado [[Principio de la inducción]].
