# Congruencias con módulo primo
Como vimos en [[Sistema de Ecuaciones lineales de Congruencia]], una congruencia $\mod (n)$ es equivalente a resolver un sistema de ecuaciones con los primos $\mod (p^e)$ de la factorización de $n$. Ahora, estudiaremos las congruencias $\mod (p)$, donde $p$ es primo. Una razón para hacer esto es que, por lo que vimos en [[Enteros Modulares]], la división **siempre** funciona pues $\mathbb{Z}_p$ es un cuerpo y existen los inversos.
Vimos que en [[Ecuación Lineal en Congruencia]] la ecuación $ax \equiv b \; (n)$ tiene como solución una única clase de congruencia (o entero modular) $[x]_n$ si $(a,n) = 1$. Ahora, si $n$ es un primo $p$ tenemos que el [[Máximo Común Divisor]] puede ser $(a,p) = 1$ ó $(a,p) = p$, si lo primero ocurre entonces la congruencia $ax \equiv b \; (p)$ tiene como solución una clase de congruencia para todo $b \in \mathbb{Z}$, pero si lo segundo ocurre entonces ($p|a$) todas las $x$ son soluciones (cuando $p|b$), o ningúna $x$ es una solución (cuando $p \nmid b$). 

Podemos decir entonces que el polinomio  $ax-b \equiv 0 \mod (p)$ tiene grado $d=1$ y tiene como máximo una solución (cuando $a$ no es congruente a $0 \mod (p)$) en $\mathbb{Z}_p$. El [[Teorema Fundamental del Álgebra]] nos dice que un polinomio con grado $d$ tiene, en los números complejos [[C]], como máximo $d$ raíces distintas, es razonable preguntarnos si esto sucede también en $\mathbb{Z}_p$ pues este es también un cuerpo (al igual que [[C]]). 

El llamado "Teorema de Lagrange" (el cual no probaremos)[^1] nos dice que es posible encontrar $d$ clases de congruencias raíces de cualquier polinomio de grado $d$ en $\mathbb{Z}_p$ solo con la condición de que los coeficientes $a_i$ no sean congruentes con $0 \mod (p)$ para cualquier $i$.  Este teorema no nos dice nada con respecto a que sucede cuando el grado del polinomio $d \geq p$, solo hay $p$ clases de congruencias en $\mathbb{Z}_p$ entonces no podrían existir $d$ clases de congruencias distintas como raíces. Los siguientes teoremas son útiles para tratar con estos casos:

> **Pequeño Teorema de Fermat.** Sea $p$ uno de los [[Números primos]] en [[N]]. Entonces para todo $a \in \mathbb{Z}$ ([[Z]]):  $$a^p \equiv a \mod (p)$$

**Demostración.**  Si $p = 2$, $a^2 - a = a(a -1)$, o sea tenemos el producto de 2 enteros consecutivos, luego alguno de ellos es par y el producto resulta par $\implies 2|a^2 - a \implies a^2 \equiv a \; (2)$.
Sea $p > 2$, tomemos $a > 0$, $a \in \mathbb{N}$, ahora tenemos una afirmación sobre $\mathbb{N}$ para poder utilizar el [[Principio de la inducción]]. 
$$P(a): \; a^p \equiv a \; (p), \; \forall \; p \text{ es primo }, \; p > 2$$
- (Caso Base) Veamos el caso base: $a = 1, \; 1^p = 1, \; 1^p - 1 = 0 \text{ y } p|1^p -1 \implies 1^p \equiv 1 \; (p)$ es Verdadero.
- (Paso Inductivo) Supongamos que $P(a)$ es verdadera para un $a \in \mathbb{N}$, o se $a^p \equiv a \; (p)$. Queremos mostrar que $P(a+1): (a+1)^p \equiv a+1 \; (p), \; p > 2$ verdadera también.
Utilizaremos el Binomio de Newton (visto en [[Número Combinatorio y Binomio de Newton]]) para desglosar este polinomio:
$$(a+1)^p = \sum_{j=0}^p \binom{p}{j} a^j$$
Sabemos que el primer y último termino están definidos en los números naturales, pero para los terminos $1 \leq j \leq p-1$ veamos que estrictamente $\binom{p}{j}$ es divisible por $p$.
$$\binom{p}{j} = \frac{p!}{j!(p-j)!} = p \cdot \frac{(p-1)!}{j!(p-j)!}$$
Tenemos que ver que $\frac{(p-1)!}{j!(p-j)!} \in \mathbb{N}$. Como todos los números del denominador son menores estrictos que $p$, entonces $p$ no se puede cancelar con ningún factor del denominador, por lo tanto los factores primos del denominador se deben cancelar con los factores primos del factorial $(p-1)!$. En conclusión, $\frac{(p-1)!}{j!(p-j)!} \in \mathbb{N}$. 
$$p \Bigg| \binom{p}{j} \implies \binom{p}{j} \equiv 0 \; (p) \implies \binom{p}{j} a^j \equiv 0 \; (p); \;\;\;\; 1 \leq j \leq p-1$$
Luego,
$$(a+1)^p =  \sum_{j=0}^p \binom{p}{j} a^j \equiv 1+a^p \; (p)$$
Ahora comprobemos $a+1$ usando la HI ($a^p \equiv a \; (p)$):
$$(a+1)^p \equiv a^p + 1 \equiv a+1 \; (p)$$
Que era lo que queríamos comprobar, $P(a+1)$ es verdadera, luego por el principio de inducción dice que $P(n)$ es verdadera en todo $n \in \mathbb{N}$.  $\blacksquare$ 

> **Colorario.**  Si $a \in \mathbb{Z}$, $p \in \mathbb{N}$ primo si cumple que $(a, p) = 1$ entonces vale que  $$a^{p -1} \equiv 1 \mod p$$

**Demostración.** Nuestra hipotesis es que $(a, p) = 1$. Sabemos que $a^p \equiv a \; (p)$, luego como $a$ y $p$ son coprimos existe una única clase de congruncia $[b]_p$ tal que $[a]_p[b]_p = [1]_p$ entonces si múltiplicamos de ambos lados por el inverso $b \cdot a^p \equiv a \cdot b \; (p) \rightarrow (ab)a^{p-1} \equiv 1 \; (p)$ por último $a^{p-1} \equiv 1 \; (p)$. $\blacksquare$ 

El teorema y el colorario son muy utiles para lidear con potencias muy grandes en congruencias. El siguiente teorema nos sirve para identificar si un número es primo, o en sí encontrar todos los números primos que cumplen una cierta propiedad, pero antes de verlo probemos el siguiente lema.

> **Lema.** Sea $p$ un primo.  $x^2 \equiv 1 \; (p)$ tiene como soluciones $x \equiv \pm 1 \; (p)$.

**Demostración.** Supongamos que $x^2 \equiv 1 \; (p) \implies x^2 - 1 \equiv 0 \; (p) \implies p|x^2 -1 \implies p|(x-1)(x+1)$. Luego gracias a las propiedades de los [[Números primos]], sabemos que $p$ divide o uno u otro multiplo, $p|x-1$ o $p|x+1$. Luego por la definición de congruencia, $x \equiv 1 \; (p)$ o $x \equiv -1 \; (p)$.
Notemos que este lema nos habla de como utilizar la congruencia para que los números enteros se "comporten" como números reales, fijemosnos que lo que nos dice es que la única solución para $x^2$ en congruencia es +1 o -1. $\blacksquare$ 

Este lema, en otras palabras, lo que nos dice es que las únicas congruencias que son inversas de sí mismas son $[1]_p$ y $[-1]_p = [p-1]_p$.

> **Teorema de Wilson.** $p \in \mathbb{N}$ ([[N]]) es primo si y solo si  $(p-1)! \equiv -1 \; (p)$ ([[Z]]). 

**Demostración.** ($\Leftarrow$) Supongamos $(p-1)! \equiv -1 \; (p)$ verdadero e intentemos llegar a que $p$ tiene que ser primo. Supongamos que existe un divisor $n|p$ con $n \neq p$, entonces si llegamos a que $n=1$ completamos la prueba. Como $n|p \Rightarrow |n| \leq |p| \Rightarrow n \in \{1,2, \dots, p-1\}$ entonces $n|(p-1)!$. Por hipótesis sabemos que $p|(p-1)!+1$ pero entonces $n|(p-1)!+1$ también.
Ahora, sabemos que $n|(p-1)!$ y $n|(p-1)!+1$, por lo tanto $n|(p-1)!+1-(p-1)! = 1 \Rightarrow n|1$ y completamos la ida. 
($\Rightarrow$) Notemos que $p=2$ funciona pues $(2-1)! \equiv 1 \equiv -1 \; (2)$ y $p = 3$ también funciona pues $(3-1)! \equiv 2 \equiv -1 \; (3)$. Supongamos que $p \geq 5$ y es un primo. Consideremos el conjunto $\{2,3, 4, \dots, p-2\}$, para todos los $a \in \{2,3,4, \dots, p-2\}$ por el lema anterior tenemos que $a^2$ no es congruente con $1 \mod (p)$ pues como ya vimos los únicos números que son inversos de si mismos en un cuerpo $\mathbb{Z}_p$, con $p$ primo, son las clases del $[1]$ y $[p-1]$. Veamos que estas dos clases están excluidas del conjunto de valores que puede tomar $a$.  También sabemos que existe una (y solo una) clase $b \in \{2, \dots, p-2\}$ que al multiplicarla por $a$ nos queda que $ab \equiv 1 \; (p)$. 
Notemos que en $(p-1)(p-2)\cdots 2 \cdot 1$ podemos agrupar cada número con su inverso en $\mathbb{Z}_p$ (que sabemos que existe y es único para cada número por lo que planteamos arriba). El único número que queda libre es el $p-1$ por lo tanto $(p-1)! \equiv p-1 \equiv -1 \; (p)$. $\blacksquare$ 


[^1]: La demostración la puede encontrar en *Elementary Number Theory* de Gareth A. Jones y J. Mary Jones (pág. 66)