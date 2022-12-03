# Aritmética Modular
Muchos problemas que involucran enteros [[Z]] grandes pueden ser simplificados con una técnica llamada **aritmética modular**, donde usamos congruencias en lugar de ecuaciones normales en los enteros. La idea básica es elegir un entero particular $m$ (depende del problema), llamarlo *módulo*, y reemplazar cada entero con su resto al dividirlo por $m$. En general, este módulo es chico y por lo tanto fácil de lidear. 
Planteemos las siguientes dos preguntas:
- _¿Qué día de la semana va a ser en 100 días si hoy es Lunes?_
- _¿Es 22051946 un cuadrado perfecto?_

> #Definición Dado $n \in \mathbb{N}$, $a, b \in \mathbb{Z}$ se dice que **$a$ es congruente a $b$ módulo $n$** si y solo sí $n|a-b$. A  esto lo denotamos $a \equiv b \mod(n)$ o $a \equiv b \; (n)$.

Para ser más precisos, si escribimos a $a$ y $b$ con el algoritmo de la división (visto en [[Divisibilidad]]) tal que $a= qn+r$ y $b=q'n+r'$ para que $a \equiv b \; (n)$ se cumpla $n| (qn+r) - (q'n+r') = n(q-q') + (r-r')$ entonces para que esto suceda tiene que ocurrir que $r-r' = 0$ o $r = r'$. Por ejemplo, $17 \equiv 3 \; (7)$ .

## Clases de Congruencia

> **Lema. (Propiedades básicas de la Congruencia)** Para cualquier módulo $m \geq 1$ se cumple:
> 1. $a \equiv a$ para todo $a \in \mathbb{Z}$; (Propiedad Reflexiva)
> 2. Si $a \equiv b$ entonces $b \equiv a$, para todos los $a,b \in \mathbb{Z}$; (Propiedad Simetría)
> 3. Si $a \equiv b$ y $b \equiv c$ entonces $a \equiv c$. (Propiedad Transitiva)

**Demostración.** (1) $m|(a-a)$ para todo $a$. (2) Si $m|(a-b)$ entonces $m|(b-a)$. (3) Si $m|(a-b)$ y $m|(b-c)$ entonces $m|(a-b) + (b-c) = a-c$. $\blacksquare$ 

Notará que estas tres propiedades son las de una **relación de equivalencia** (vista en [[Relaciones entre conjuntos]]) entonces el lema anterior prueba que la congruencia $\mathrm{mod} \; n$ es una relación de equivalencia (que es un subconjunto de $\mathbb{Z} \times \mathbb{Z}$). 
Observe lo siguiente: si tomamos $m = 3$ y dividimos cualquier entero por 3 los restos obtenidos son 0, 1 y 2. Luego, [[Z]] quedó dividido en 3 conjuntos disjuntos (o clases de equivalencia). 
$$\{\dots, -9, -6, -3, 0, 3, 6, 9, 12, \dots\} (r = 0)$$
$$\{\dots, -8, -5, -2, 1, 4, 7, 10, 13, \dots\} (r = 1)$$
$$\{\dots, -7, -4, -1, 2, 5, 8, 11, 14, \dots\} (r = 2)$$
Entonces, esto ocurre para cualquier $m$ fijo; tal que tenemos las clases de equivalencia (o también llamadas *clases de congruencia*):
$$[a]_m = \{b \in \mathbb{Z} : a \equiv b \; (m)\} = \{\dots, a-2m, a-m, a, a+m, a+2m, \dots\}$$
para $a \in \mathbb{Z}$. Cada clase corresponde a uno de los posibles restos $r = 0,1,\dots,m-1$ con cada división por $m$, así que hay $m$ clases de congruencia.  Estas son 
$$\begin{align}
[0] & = \{\dots, -2m, -m, 0, m, 2m, \dots\} \\
[1] & = \{\dots, 1-2m, 1-m, 1, m+1, 1+2m, \dots\} \\
& \; \vdots \\
[m-1] & = \{\dots, -m-1, -1, m-1, 2m-1, 3m-1, \dots\}
\end{align}$$
No hay más clases distintas a estas, el resto son iguales, por ejemplo
$$[m] = \{\dots, -m, 0, m, 2m,3m, \dots\} = [0]$$
Veamos también que del ejemplo anterior $[3] = [0]$ y $[4] = [1]$. Más generalmente tenemos que $[a] = [b]$ si y solo si $a \equiv b \; (m)$ (es decir las clases de congruencia son iguales si y solo si tienen el mismo resto al dividirlo por $m$). 
Como las clases de congruencia son todas disjuntas entre si tenemos que 
$$\mathbb{Z} = [0]_m \cup [1]_m \cup \cdots \cup [m-1]_m$$
Para cualquier $m \geq 1$, denotamos al conjunto que tiene todas las clases de congruencia de $m$, $\mathbb{Z}_m$. Nuestro proximo objetivo sería ver como hacer aritmética con los elementos de conjuntos _¿Por qué nos interesa?_ porque estos tienen una propiedad muy interesante en ciertos casos que nos permite **dividir en todos los casos** o otra manera de decirlo es que **existen inversos en este sistema numerico**, el desarrollo de esto se verá en [[Enteros Modulares]].

Sabiendo esto podemos resolver las dos preguntas al principio de la nota. Veamos que una de las soluciones obvias de la primera pregunta es ir contando uno a uno los días hasta llegar al 100. Pero esto sería un desperdicio de nuestro tiempo, observemos que si sabemos cuantas veces entra 7 (los días de la semana) en 100 podemos obtener cuantas semanas hay en esos 100 días y su resto sería simplemente el número de días que tenemos que contar desde el lunes, de esta manera $100 = 7(14) + 2$ o $100 \equiv 2 \; (7)$ y entonces obtenemos la respuesta que sería el miércoles (pues está a dos días del lunes).
Luego, la segunda pregunta se puede resolver usando el algoritmo de la división (visto en [[Divisibilidad]]) observemos se puede calcular el resto que tiene un número al cuadrado $m^2$ al dividirlo por 4, teniendo en cuenta que $m=4q + r$ con $r = 0,1,2,3$. Si usted realiza este calculo obtendrá el resultado de que los restos de un cuadrado perfecto al dividir por 4 pueden ser 0 o 1. Entonces, como queremos encontrar si $22051946$ es un cuadrado perfecto:
$$22051946 \equiv 46 \; (100) \rightarrow 22051900 \equiv 0 \; (100)$$
Lo que hicimos acá fue que como sabemos que $100 = 25 \times 4$ basta que un número sea multiplo de 100 para que sea un múltiplo de 4, observemos que este no es el caso pero veamos el resto de dividir por 4 de $46 \equiv 2 \; (4)$ (pues $46 = 11 \times 4 + 2$) observemos que el número no tiene un resto de 0 ni 1 al dividirlo por 4, entonces no es un cuadrado perfecto. 

Estos dos ejemplos muestran porque a veces trabajar con los restos de números muy grandes es más útil que trabajar con los números en si mismos. La aritmética modular se dedica a resolver problemas como estos. No es un técnica del mundo moderno, de hecho muchas civilizaciones han utilizado varios de sus teoremas (aunque sin las demostraciones) por siglos. 

---

### Otras Propiedades de la congruencias
La relación de congruencia se comporta de "buena manera" con las sumas y productos bajo un mismo módulo. 

> **Proposición.** Sean $a, b \in \mathbb{Z}, \; n \in \mathbb{N}$. Entonces se cumplen las siguientes propiedades:
> 1. Si $a \equiv b \; (n)$ entonces $a + c \equiv b+c \; (n)$.
> 2. Si $a \equiv b \; (n)$ entonces $ac \equiv bc \; (n)$.

**Demostración.** Sale por la definición de congruencia y las propiedades de [[Divisibilidad]]. $\blacksquare$ 

> **Proposición. (Linearidad)** Sean $a,b,c,c',m \in  \mathbb{Z}$ con $m > 0$. Si $a \equiv b \; (m)$ y $c \equiv c' \; (m)$, entonces:
> 1. $a+c \equiv b+c' \; (m)$ 
> 2. $ac \equiv bc' \; (m)$ 

**Demostración.** (1) Como $a \equiv b \; (m)$ y $c \equiv c' \; (m)$, entonces $m|a-b$ y $m|c-c'$. Luego por el colorario visto en [[Divisibilidad]] $m|(a-b) + (c-c') = (a+c) - (b+c')$ de donde se sigue $a+c \equiv b+c' \; (m)$.  (2) Notar que $ac - bc' = c(a-b)+b(c-c')$ y como sabemos $m|a-b$ y $m|c-c'$ entonces $m|ac-bc'$ de donde sigue $ac \equiv bc' \; (m)$. $\blacksquare$ 

Las propidades anteriores pueden ser iteradas y combinadas entre sí. Sea
$$f(x) = c_n x^n + c_{n-1}x^{n-1} + \cdots + c_2x^2 + c_1 x + c_0$$
donde $c_0,c_1, \cdots, c_n \in \mathbb{Z}$ con $c \neq 0$ y $x \in \mathbb{Z}$ una varible libre. Tal $f(x)$ se dice un polinomio con coeficientes enteros o *polinomio entero* y se lo denota $f(x) \in \mathbb{Z}[x]$ (veremos más acerca de polinomios con variables en [[Polinomios Generalizados]]) 

> **Colorario.** Si $a \equiv b \; (m)$ y $\alpha \equiv \beta \; (m)$ entonces:
> 1. $ax+by \equiv \alpha x + \beta y \; (m)$ para todo $x,y \in \mathbb{Z}$. 
> 2. $a^n \equiv b^n \; (m)$ para todo $n \in \mathbb{Z}$ 
> 3. $f(a) \equiv f(b) \; (m)$ para todo $f(x) \in \mathbb{Z}[x]$. 

**Demostración.** Sale de aplicar las propiedades de linearidad varias veces. $\blacksquare$ 

Muchas veces no nos dan un módulo chico, una forma que podemos buscar de reducirlo es viendo que todos las partes de de una congruencia son divisibles por este número, por ejemplo $48 \equiv 18 \; (10)$ todos los términos son divisibles por 2 por lo que vale también $24 \equiv 9 \; (5)$. La siguiente proposición lo verifica

> **Proposición. (Reducción de Módulo)** Si $c > 0$, entonces $a \equiv b \; (m)$ si y solo si $ac \equiv bc \; (mc)$. 

 **Demostración.** Si $m|a-b$ entonces $mc|c(a-b)$, solo si $c > 0$.  $\blacksquare$ 

> **Proposición. (Ley de Simplificación)** Si $ac \equiv bc \; (m)$  y $d = (m,c)$, entonces $$a \equiv b \; (\frac{m}{d})$$ En particular, si $c=p$ es primo y $p \nmid m$, entonces $a \equiv b \; (m)$.

En otras palabras, un factor común se puede simplificar si el módulo es divisible por el [[Máximo Común Divisor]] entre ambos. En particular, un factor común primo, coprimo con módulo, siempre puede ser simplificado.  

**Demostración.** Por hipótesis, $m|c(a-b)$ de donde $\frac{m}{d}|\frac{c}{d}(a-b)$. Como $(\frac{m}{d}, \frac{c}{d}) = 1$ tenemos que $\frac{m}{d}$ debe dividir a $a-b$ (por un teorema visto en [[Máximo Común Divisor]]) y por lo tanto $a \equiv b \; (\frac{m}{d})$ como queriamos. $\blacksquare$ 

> **Teorema. (Producto de Modulos)** Supongamos que $a \equiv b \; (m)$ y $a \equiv b \; (n)$. Si $(m,n) = 1$ entonces $a \equiv b \; (mn)$. 

**Demostración.** Tenemos que $m|a-b$ y $n|a-b$ y como $(m,n) = 1$ entonces (por el colorario 3 visto en [[Máximo Común Divisor]]) tenemos $mn|a-b$. $\blacksquare$ 

> **Colorario.** Si $a \equiv b \; (p)$ y $a \equiv b \; (q)$ con $p, q$ primos entonces $a \equiv b \; (pq)$. 

---

## Reglas de divisibilidad
Gracias a las propiedades vistas arriba (en concreto las de linearidad) podemos encontrar las famosas "reglas de divisibilidad" para cada número. Sabemos por conocimiento general que un número es divisible por 9 si la suma de sus digitos también es divisible por 9, o que si un número termina en 0 o en 5 es divisible por 5 pero _¿Como podemos probar esto?_
Ya hemos visto en [[Sistemas s-adicos]] que la forma de representar un número usando base 10 $a = (a_r a_{r-1} \dots a_1 a_0)_{10}$ es una abreviatura de 
$$a = a_r10^r + a_{r-1}10^{r-1} + \cdots + a_1 10 + a_0$$
Si queremos estudiar $m|a$, tomando la congruencia modulo $m$ arriba tenemos 
$$a \equiv a_r10^r + \cdots + a_1 10 + a_0 \; (m)$$
y a partir de aquí deducimos condiciones para los digitos $a_0, \dots, a_r$, de modo tal de asegurar que $a \equiv 0 \; (m)$. 
Notemos que por el teorema de producto de módulo solo **basta con encontrar las reglas de divisibilidad de los [[Números primos]]** para poder encontrar todos las otras. Por ejemplo, la regla de divisibilidad del 9 es la misma que la del 3 o también la regla de divisibilidad del 10 es una combinación de la regla de divisibilidad del 2 y el 5.

## Regla del 3
Sea $x \in \mathbb{N} \Rightarrow  x = \sum_{i = 0}^N a_i \cdot 10^i, \; 0 \leq a_i \leq 9$. Tenemos entonces que $10 = 9 + 1 \Rightarrow 10 \equiv 1 \; (3) \Rightarrow 10^j \equiv 1^j \; (3), \; \forall j  \in \mathbb{N} \Rightarrow 10^j \equiv 1 \; (3)$
$\Rightarrow a_j \cdot 10^j \equiv a_j \; (3)$. Luego, $$x = a_0 + a_1 \cdot 10 + \dots + a_N \cdot 10^N \equiv a_0 + a_1 + a_2 + \dots + a_N \; (3)$$
O sea obtuvimos que $3 \Big| x - \sum_{i=0}^N a_i$. Luego
> **Regla del 3.** Sea $x \in \mathbb{Z}$ y $a_i$ los digitos de este número $x = (a_ra_{r-1}\cdots a_1 a_0)_{10}$$$3|x \iff 3 \Big| \sum_{i=0}^N a_i$$

## Regla del 2
Sea $x \in \mathbb{N} \Rightarrow  x = \sum_{i = 0}^N a_i \cdot 10^i, \; 0 \leq a_i \leq 9$. Veamos que $10 \equiv 0 \; (2)$ tenemos entonces que aplicando sucesivamente las propiedades de linearidad $a \equiv a_0 \; (2)$. Ahora, $a_0 \equiv 0 \; (2)$ si y solo sí es par, es decir $a_0 = 0,2,4,6,8$. 
Luego, 
$$x = a_0 + a_1 \cdot 10 + \dots + a_N \cdot 10^N \equiv a_0 \; (2)$$
O sea obtuvimos que $3|x- a_0$. 
> **Regla del 2.** Sea $x \in \mathbb{Z}$ y $a_i$ los digitos de este número $x = (a_ra_{r-1} \cdots a_1 a_0)_{10}$ $$2|x \iff 2|a_0$$ Entonces $a_0 = 0,2,4,6,8$.

## Regla del 5
Sea $x \in \mathbb{N} \Rightarrow  x = \sum_{i = 0}^N a_i \cdot 10^i, \; 0 \leq a_i \leq 9$. Veamos que como $10 \equiv 5 \; (5)$ tenemos que $x \equiv a_0 \; (5)$ y para que $a_0 \equiv 0 \; (5)$ entonces $a_0 = 0,5$.
> **Regla del 5.** Sea $x \in \mathbb{Z}$ y $a_i$ los digitos de este número $x = (a_ra_{r-1} \cdots a_1 a_0)_{10}$ $$5|x \iff 5|a_0$$ Entonces $a_0 = 0,5$.

## Regla del 7
Sea $x \in \mathbb{N} \Rightarrow  x = \sum_{i = 0}^N a_i \cdot 10^i, \; 0 \leq a_i \leq 9$. Notemos que $10 \equiv 3 \; (7)$, $10^2 \equiv 2 \; (7)$, $10^3 \equiv 6 \; (7)$, $10^5 \equiv 5 \; (7)$ y $10^6 \equiv 1 \; (7)$. Luego, para todo $k$ se tiene que $10^{6k} \equiv 1 \; (7)$ y por lo tanto
$$\begin{array}{rcrr}
10^{6 k} \equiv 1 & (\text{mód} \; 7) & 10^{6 k+3} \equiv-1 & (\operatorname{mod} 7) \\
10^{6 k+1} \equiv 3 & (\text{mód } 7) & 10^{6 k+4} \equiv-3 & (\operatorname{mod} 7) \\
10^{6 k+2} \equiv 2 & (\text{mód } 7) & 10^{6 k+5} \equiv-2 & (\operatorname{mod} 7)
\end{array}$$
Así nos queda 
$$x = a_0 + a_1 \cdot 10 + \dots + a_N \cdot 10^N \equiv a_0 + 3a_1 + 2a_1 - a_3 - 3a_4 -2a_5 + a_6 + \dots \; (7)$$
> **Regla del 7.** Sea $x \in \mathbb{Z}$ y $a_i$ los digitos de este número $x = (a_ra_{r-1} \cdots a_1 a_0)_{10}$  $$7|x \iff 7 \Bigg| \sum_{k=0}^{[r/6]} -2a_{6k+5} - 3a_{6k+4} - a_{6k+3} + 2a_{6k+2} + 3a_{6k+1} + a_{6k}$$

## Regla del 11
Sea $x \in \mathbb{N} \Rightarrow  x = \sum_{i = 0}^N a_i \cdot 10^i, \; 0 \leq a_i \leq 9$. Notemos que $10 \equiv -1 \; (11)$. Luego, $10^2 \equiv 1 \; (10)$. Entonces las sucesivas potencias de 10 son congruentes a 1 o -1 dependiendo de si son pares o impares. Nos queda entonces,
$$x = a_0 + a_1 \cdot 10 + \dots + a_N \cdot 10^N \equiv a_0 - a_1 + a_2 -a_3 + \cdots + (-1)^N a_N$$
> **Regla del 11.** Sea $x \in \mathbb{Z}$ y $a_i$ los digitos de este número $x = (a_ra_{r-1} \cdots a_1 a_0)_{10}$ $$11|x \iff 11 \Bigg| \sum_{k=0}^r (-1)^r a_r$$

Para encontrar las reglas de números compuestos como la del 9, podemos decir que es la misma que la del 3 pues $10 \equiv 1 \; (3)$ como $10 \equiv 1 \; (9)$ pero esto no siempre ocurre con todas las reglas. Por ejemplo la regla del 4 no es la misma que la del 2 pues $10 \equiv 2 \; (4)$ y $10 \equiv 0 \; (2)$. 
Para encontrar la regla del 4 veamos que $10^2 \equiv 0 \; (4)$ entonces para todo $10^k \equiv 0 \; (4)$ con $k \geq 2$. Esto nos dice que $x$ es divisible por 4 si el número formado por sus dos primeros digitos es divisible por 4. Más aún tenemos 
$$x \equiv 2a_1 + a_0 \; (4) \rightarrow 4|x-(2a_1 + a_0) \rightarrow 4|2a_1 \iff 4|a_0$$

$$$$