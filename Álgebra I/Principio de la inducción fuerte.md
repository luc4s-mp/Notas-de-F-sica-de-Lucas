# Principio de la inducción fuerte 

## Principio de la inducción (II)
#Definición Sea $P(n)$, $n \in \mathbb{N}$ , una afirmación sobre los números naturales. Si P satisface
- (Caso Base) $P(1)$ y $P(2)$ son verdaderas. 
- (Paso Inductivo) $\forall h \in \mathbb{N}$, $P(h)$ y $P(h+1)$ Verdaderas $\implies P(h+2)$
Este principio suele ser aplicado para aquellas proposiciones que utiliza [[Principio de la inducción]] en los números naturales las cuales necesiten de dos proposiciones anteriores para poder estar definido el término general.
---
## Problema Inicial - La sucesión de Fibonacci
Leonardo Pisano Bigollo (1170-1240) o más conocido como Fibonacci publicó su libro Liber Abaci en el año 1202, donde propuso el siguiente problema: ¿Cuántos conejos habrá si luego de $n$ meses 
- los conejos nunca mueren,
- cada pareja de conejos produce una nueva pareja de conejos cada mes
- y comienzan a tener parejitas luego de dos meses de nacidos?

En el mes 1 hay una sola pareja de conejos bebés. En el mes 2 está la misma pareja (que ya es adulta y se está preparando para tener bebés). En el mes 3 está la pareja original (adulta) y una pareja  bebé (2) (hijos de la pareja original), o sea tenemos 2 parejas. En el mes 4, la pareja original tiene otra pareja de bebés y la pareja (2) ahora es adulta y se está preparando para tener bebés (hay 3 parejas). De esta manera, si seguimos calculando números, encontraremos que la sucesión sigue 5, 8, 13, 21, 43 ...

Para encontrar una fórmula para esta sucesión, llamemos $A_n$ al número de parejas adultas en el mes $n$ y $B_n$ al número de parejas bebés en el mes $n$.Y si llamamos $F_n$ al total de parejas, es claro que $F_n = A_n + B_n$. Observe la siguiente tabla, donde colocamos a las parejas de adultos y bebes ordenadas, recuerde que cada vez que pasa un mes $B_{n+1} = A_n$ (la cantidad de parejas de bebes en un mes nuevo es igual a la cantidad de parejas de adultos del mes anterior) y $A_{n+1} = A_n + B_n = F_n$ (la cantidad de adultos en un mes nuevo es igual a la cantidad de adultos que había en el mes anterior más los bebés que se convirtieron en adultos):
![[Pasted image 20220703192756.png | 300]]
Notemos que parece ser que el número de parejas en el mes ${n+2}$ es la suma de las parejas del mes $n+1$ y del mes $n$ por lo cual podemos definir la siguiente sucesión por recurrencia ([[Definiciones Recursivas]]):
$$F_0 = 0, \; F_1 = 1, \; F_{n+2} = F_{n+1} + F_n, \;\;\forall n \in \mathbb{N}_0$$
Esta sucesión es muy famosa y sus primeros terminos son 0, 1, 2, 3, 5, 8, 13. 21, 34, 55, 89, 144, 233, ...
Al igual que nos preguntamos con el problema de las torres de hanoi (visto en [[Definiciones Recursivas]]) _¿Existe una fórmula que nos permita decir cuantas parejas hay sin necesidad de tener definidos dos los dos elementos anteriores?_  En caso de que exista, _¿Cómo podemos probar que funciona?_

## Principio de la Buena Ordenación
A estas alturas probablemente ya resulte intuitivo, que todo conjunto inductivo contiene a los naturales [[N]]. Pero hasta ahora, con los conocimientos que tenemos, no podemos demostrarlo. 

> #Definición Un subconjunto $H \subseteq \mathbb{R}$ tiene **primer elemento** $h$, si 
> 1. $h \in H$
> $h \leq k$ para todo $k \in H$.

> #Definición Un subconjunto de los reales $K \subseteq \mathbb{R}$ se dice **bien ordenado**, si todo subconjunto $H \subseteq K$, no vació tiene primer elemento.

 > **Principio de la buena ordenación**. $\mathbb{N}$ es _bien ordenado_.

**Demostración**. Procedemos a demostrar por el absurdo. Queremos demostrar que todo subconjunto $H \subseteq \mathbb{N}$, no vacío, tiene primer elemento. Supongamos que existe un $H \subseteq \mathbb{N}$ , no vacío, que _no tiene primer elemento_  y sea $H'$ su complemento en $\mathbb{N}$, o sea $H' = \mathbb{N} - H$. Como $H$ es no vacío, entonces $H' \neq \mathbb{N}$ . Consideremos ahora el conjunto 
$$K = \{ n \in \mathbb{N} :  [[1, n]] \subseteq H'\} $$ [^1]
Tenemos que $1 \in K$ dado que $\{1\} \subseteq H'$, pues $1 \notin H$ , ya que de lo contrario sería el primer elemento de $H$. Además, si $h \in K$, entonces ninguno de los elementos de $\{1,2, \dots, h \}$ están en $H$, luego $h + 1$ tampoco está en $H$, pues de lo contrario sería su primer elemento. Así hemos probado que $K$ es un subconjunto inductivo de $\mathbb{N}$ y por lo tanto $K = \mathbb{N}$ lo que significa que $H' = \mathbb{N}$ y llegamos a que $H = \emptyset$ **ABSURDO!** Pues empezamos suponiendo que H no es vacío $\blacksquare$ .

Fijemosnos que usamos el [[Principio de la inducción]] para demostrar el principio de la buena ordenación, de la misma manera podemos demostrar al principio de la inducción usando el principio de buena ordenación, lo cual nos dice que ambos son equivalentes. Es decir podemos probar cualquier proposición en los números naturales ya sea por el principio de la inducción o el de buena ordenación. Normalmente se hace mucho más sencillo usar el principio de inducción.

Observemos el caso del problema de la sucesión de fibonacci tenemos que $F_{n+2} = F_n + F_{n+1}$, ¿Cómo sabemos que la sucesión está definida para todos los números naturales? Bueno, lo podemos probar usando el principio de la buena ordenación. Es obvio que el conjunto $H = \{n \in \mathbb{N} : F_n \text{ está definida } \}$ es igual a $\mathbb{N}$. Pero supongamos que no, es decir que existe en un subconjunto de los naturales $H'$ en el que $F_n$ no está definida. Como $\mathbb{N}$ es un conjunto bien ordenado, $H'$ debe tener un primer elemento que debe ser $n_0 \geq 1$ porque $F_0$ y $F_1$ están definidas. Pero si $n_0 \geq 1$ entonces $F_{n_0}$ está definida por dos términos anteriores (que deben estar definidos porque $F_{n_0}$ es el más chico de los que están definidos) Por lo tanto, $F_{n_0}$ está definido, lo cual contradice lo que supusimos al principio y $H = \mathbb{N}$.
Podríamos haberlo demostrado también con el principio de la inducción, lo cual muestra, su equivalencia.

Usando el principio de la buena ordenación, podemos demostrar que todos los conjuntos inductivos continen a los números naturales.

> **Proposición**. Si $H \subseteq \mathbb{R}$ es inductivo, entonces $\mathbb{N} \subseteq H$. 

**Demostración.** Supongamos que $\mathbb{N} \nsubseteq H$ y $K = \{n \in \mathbb{N} : n \notin H  \}$. Por ser $K$ no vacío. Sea $m$ su primer elemento, $m \neq 1$, pues $1 \in H$ por ser inductivo. Luego $m-1 \in \mathbb{N}$ y $m-1 \notin K$. Así $m-1 \in H$ y por ser $H$ inductivo, su sucesor $m \in H$. Esto contradice el de ser $m$ elemento de $K$. Por lo tanto $K$ es vacío y $\mathbb{N} \subseteq H$. 

> **Colorario.** $\mathbb{N}$ es el menor de todos los conjuntos inductivos de $\mathbb{R}$. Es decir, está contenido en todo conjunto inductivo y no contiene propiamente ningún otro conjunto inductivo.

## Principio de la inducción fuerte o inducción completa
Ahora, fijemosnos que la situación con la que nos encontramos al empezar a abordar el problema de la sucesión de fibonacci es que tenemos una sucesión que no solo requiere de que $P(k)$ sea verdadera, sino también que $P(k+1)$ sea verdadera, para demostrar que $P(k+2)$ sea verdadera. En este tipo de situaciones en los que requerimos de considerar más de una hipótesis como cierta es conveniente usar el principio de inducción completa, que supone como verdaderas a $P(1), P(2), \dots, P(k)$ para demostrar $P(k+1)$, lo cual es muy útil porque de esta manera podemos no solo resolver recursiones como la sucesión de fibonacci (que requiere de saber los dos términos anteriores) sino también nos permite probar recursiones que utilicen cualquier término que esté anterior (o todos).
Vamos a demostrarlo usando el principio de la buena ordenación.

> #Definición **Principio de inducción fuerte**. Sea $P(n)$, $n \in \mathbb{N}$, una afirmación sobre los números naturales. Si P satisface
> - (Caso Base) $P(1)$ es Verdadera,
> - (Paso Inductivo) $\forall h \in \mathbb{N}$, $P(1), \cdots, P(n)$ Verdaderas $\implies P(h+1)$ Verdadera.
Entonces $P(n)$ es Verdadero, $\forall n \in \mathbb{N}$.

**Demostración**. Sea $H = \{n \in \mathbb{N} : P(n) \text{ es verdadera } \}$. Supongamos $H \varsubsetneq \mathbb{N}$ y sea $H' = \mathbb{N} - H \neq \emptyset$. Sea $k'$ el primer elemento de $H'$. Notamos que $k' > 1$. pues $1 \in H$ por hipótesis. Se sigue que si $k < k'$, entonces $k \notin H'$, es decir $k \in H$. Así tenemos que $1, 2, \dots, k'-1 \in H$, es decir $P(1), \dots, P(k'-1)$ son todas verdaderas. Luego por hipótesis, $P(k')$ es también verdadera y así $k' \in H$, lo cuál contradice el hecho de estar $k'$ en $H'$, el complemento de $H$. El absurdo proviene de suponer que $H \neq \mathbb{N}$ y la prueba está completa. $\blacksquare$ 

### Inducción generalizada
Nos gustaría generalizar la inducción para poder demostrar enunciados como
- _"Probar que para todo número real $x$ de la forma $\cos (k\pi/4)$, con $k$ múltiplo positivo de 3, la función $f$ satisface $f(x) = 0$"._
En este caso tenemos que fijarnos en la variable $k$ (no $x$ que es real). Vemos que podemos aplicar inducción en este enunciado, porque $k$ es un múltiplo **positivo** de 3, que son todos naturales. De hecho podemos reemplazar $k = 3m$, con $m \in \mathbb{N}$, y ahora queda más claro que podemos aplicar inducción.

> **Principio de Inducción Generalizado**. Sea $P(a)$ una función proposicional, $a \in Im(a_n)$, donda $(a_n)$ es una [[Sucesión]] dada. Si 
> 1. $P(a_1)$ es verdadera y, 
> 2. asumiendo que $P(a_n)$ verdadera para un $a_n$ arbitrario se deduce que $P(a_{n+1})$ es verdadera. 

 ---
## Resolución del problema de la sucesión de fibonacci
Queremos obtener una formula que nos diga el termino siguiente de la sucesión de fibonacci sin necesidad de tener definido los dos elementos anteriores. Por ejemplo, que ocurre si queremos saber el elemento ¿$a_{365}$? 

A simple vista no parece haber un patrón que podamos identificar, porque los números parecen aleatorios. Resulta que la sucesión de fibonacci está relacionada con el *número de oro* o *número de la proporsión divina o proporsión áurea*. Miles de civilizaciones a lo largo de la historia se han topado con este número, porque resulta que está en todos los lados de la naturaleza.  En los patrones de flores, en los copos de nieve, el cuerpo humano, y muchas civilizaciones la usaron para contruir sus templos (los griegos, por ejemplo). El número es el resultado de preguntarnos que ocurre si tenemos un segmento dividido en dos partes de longitudes $\phi$ y 1, con $\phi \geq 1$ , _¿Cómo tiene que ser $\phi$ para que la proposición entre esas dos partes $\phi$ y 1 sea la misma que la proposición entre todo el segmento $\phi+1$ y $\phi$?_
![[Pasted image 20220706095314.png | 250]]
$$\frac{\phi}{1} = \frac{\phi + 1}{\phi} \quad \Rightarrow \quad \phi^2 = \phi + 1 \quad \Rightarrow \quad \phi^2 -  \phi - 1 = 0$$
Entonces, si encontramos las soluciones de la ecuación $x^2 - x -1 = 0$ serían
$$\phi = \frac{1+\sqrt{5}}{2} \sim 1,61803 \geq 1 \quad \text{ y } \quad \bar{\phi} = \frac{1- \sqrt{5}}{2} < 0$$
($\bar{\phi}$ no se dice "el conjugado de $\phi$" como en los números complejos, esto es solo notación).
La formula para obtener el término general de la sucesión de fibonacci sería 
$$P(n) : F_n = \frac{1}{\sqrt{5}}(\phi^n - \bar{\phi}^n), \; n \in \mathbb{N}$$
Ahora, demostremos por inducción fuerte que esta formula es verdadera. 
- Caso Base: $P(0) : F_0 = \frac{1}{\sqrt{5}} \cdot 0$ es verdadera pues $F_0 = 0$ y $P(1) : F_1 = \frac{1}{\sqrt{5}}(\phi - \bar{\phi}) = \frac{1}{\sqrt{5}} \cdot \sqrt{5} = 1 = F_1$ es verdadera también.    
- Paso inductivo: Dado un $k \in \mathbb{N}$, supongamos $P(1), \dots, P(k)$ verdaderas y queremos demostrar $P(k+1)$ verdadera.
	(HI) $F_k = \frac{1}{\sqrt{5}}(\phi^k - \bar{\phi}^k)$, $F_{k-1} = \frac{1}{\sqrt{5}}(\phi^{k-1} - \bar{\phi}^{k-1})$ , $\dots, \; F_1$  verdaderas
	$$\begin{align}
	F_{k+1} & = F_{k} + F_{k-1} = \frac{1}{\sqrt{5}}(\phi^k - \bar{\phi}^k) + \frac{1}{\sqrt{5}}(\phi^{k+1} - \bar{\phi}^{k+1}) \\
	& = \frac{1}{\sqrt{5}}(\phi^k - \bar{\phi}^k + \phi^{k-1} - \bar{\phi}^{k-1}) = \frac{1}{\sqrt{5}}\Big(\phi^{k-1}(1+\phi) - \bar{\phi}^{k-1}(1+\phi)\Big) \\
	& \underset{*}{=}  \frac{1}{\sqrt{5}}(\phi^{k-1}(\phi^{2}) - \bar{\phi}^{k-1}(\phi^2)) = \frac{1}{\sqrt{5}}(\phi^{k+1} - \bar{\phi}^{k+1})
	\end{align}$$
	(En * aplicamos la igualdad $\phi^2 = \phi + 1$)
	Que era a lo que queríamos llegar. 
Entonces, hemos probado que $P(n)$ es verdadero, $\forall n \in \mathbb{N}$.

Con esta formula podemos obtener todos los términos que queramos sin necesidad de tener definidos los anteriores.

---
[^1]: Los dobles corchetes representan un intervalo de números enteros.

