# Definiciones recursivas
## Las Torres de Hanoi [^1]
Tenemos 3 estacas, y un cierto número $n$ de discos de distinto diámetro ensartados en la primer estaca, ordenados por tamaño, de mayor a menor estando el menor arriba, como en la foto de abajo.
![[Pasted image 20220630090055.png| 350]]
El objetivo del juego es lograr mover toda la pila de discos a otra estaca, con las condiciones siguientes:
- no se puede mover más de un disco a la vez,
- sólo se puede sacar el disco de la parte superior de cada pila de discos,
- en todo momento los discos de cada estaca deben estar ordenados por tamaño, de mayor a menor con el menor encima.
___¿Cuántos movimientos alcanzan para realizar la operación?___ 
Al final de esta lección con los conocimientos que adquirimos podremos resolver el problema. 

---

## Sumatoria y productoria
Notemos que el ejemplo dado en [[Principio de la inducción]] de la suma de Gauss usamos la notación $1 + 2 + 3 + \dots + n$ para representar la suma de los primeros $n$ números naturales ([[N]]). Pero notemos que los puntos suspensivos pueden llevar a problemas de definición porque no estamos diciendo específicamente que elementos están en la suma y cuales no, existe una manera de evitar esto que es usando el concepto de **sucesión**. Una [[Sucesión]] en $\mathbb{R}$ es una función $f: \mathbb{N} \rightarrow \mathbb{R}$ donde denotamos $f(n) = u_n$ o $\{u_n\}_{n \in \mathbb{N}}$. Decimos que una sucesión está **definida recursivamente** si $u_n$ está definida en terminos de elementos anteriores. 

> #Definición Dada una sucesión finita de números reales $x_1, x_2, ..., x_n$, entonces vamos a dar sentido a la suma $x_1 + x_2 + ... + x_n$ o al producto $x_1 \cdot x_2 \cdot ... \cdot x_n$ del siguiente modo: $$\sum_{i=1}^{n} x_i$$ **Sumatoria de los elementos** "$x_i$" moviendose desde el índice "i" entre 1 y n. $$\prod_{i=1}^{n} x_i$$**Productoria de elementos** "$x_i$" moviendose desde el índice "i" entre 1 y n.

### Definición recursiva de la sumatoria y productoria
Queremos darle sentido a las expresiones usando la definición recursiva, para hacerlo vamos a utilizar el [[Principio de la inducción]] que se aplica en [[N]] (el dominio de la sucesión):
Tomemos $n = 1$ para el caso base:
$$\sum_{i=1}^1 x_i = x_1 \;\; \text{   y   } \;\; \prod_{i=1}^1 x_i = x_1$$
Ahora, tomemos un número $k$ tal que $k \in \mathbb{N}$: $\sum_{i=1}^{k} x_i$ y $\prod_{i=1}^{k} x_i$ y para comprobar si es verdadera definimos recursivamente a su sucesor $k+1$:
$$\sum_{i=1}^{k+1} x_i = \sum_{i=1}^{k} x_i + x_{k+1}$$
$$\prod_{i=1}^{k+1} x_i = \prod_{i=1}^{k} x_i \cdot x_{k+1}$$
Cuando encontramos estas definiciones en sucesiones, normalmente queremos desacernos de ellas y transformarlas en definiciones más simples de encontrar. Tal cual hicimos con la suma de Gauss que obtuvimos que la suma de los primeros $n$ números $\sum_{i=1}^n i$  nos da lo mismo que $n(n+1)/2$. Muchas veces utilizamos el [[Principio de la inducción fuerte]] para resolverlas en los casos en los cuales un elemento de una sucesión se define con varios elementos anteriores, pero para definiciones recurrentes simples, podemos simplemente usar el [[Principio de la inducción]].

---
## Resolución del problema de las Torres de Hanoi
Usaremos las definiciones recursivas para resolver este problema, buscamos la cantidad de movimientos que alcanza para pasar todos los discos de una estaca a otra. Observenos que ocurre con 2 discos:
![[Pasted image 20220703130749.png]]
O sea que alcanza con 3 movimientos. Veamos ahora que ocurre con 3 discos:
![[Pasted image 20220703130859.png]]
Alcanza con 7 movimientos. Con esto sabido, es más fácil saber cuantos movimientos se requieren para mover 4 discos. Tenemos que mover los primeros 3 discos a otra estanca con 7 movimientos, luego mover el disco más grande que quedó solo a la estaca libre (1 movimiento) y por último volver a mover la pila de 3 discos arriba del más grande, realizando nuevamente 7 movimientos. Entonces, nos queda que para 4 discos son necesarios $2  \cdot 7 + 1 = 15$ movimientos.

Notemos que podemos replicar este proceso para $n$ discos sabiendo cuantos movimientos usamos para $n-1$ discos, entonces armar una sucesión de elementos $a_1 = 1$, $a_2 = 3$. $a_3 = 7$, $a_n = 2a_{n-1} +1$. Fijemosnos que $a_3$ y $a_2$ también se pueden obtener siguiendo nuestro razonamiento, entonces nos queda $a_1 =1, \; a_n = 2a_{n-1} + 1$, esto es lo que llamados una sucesión definida *por recurrencia*, es necesarios saber la cantidad de movimientos de $n-1$ discos para poder obtener la siguiente. Pero nos podemos preguntar ¿No existe una formula capaz de decirnos cuantos movimientos necesitamos, sin necesidad de tener definido el término anterior? 
Veamos:
$$a_1 = 1, \; a_2 = 3, \; a_3 = 7, \; a_4 = 15, \; a_5 = 31, a_6 = 36$$
Pareciera ser que puede valer $a_n = 2^n -1, \; \forall n \in \mathbb{N}$. Pero ahora tenemos que probarlo, podemos hacerlo usando inducción.
- Caso base: $P(1)$ vale pues $2^1 - 1 = 1 = a_1$.
- Paso inductivo: Dado $k \in \mathbb{N}$, supongamos $P(k)$ verdadero, entonces probemos $P(k+1)$  verdadero también. La hipótesis inductiva es $a_k = 2^k - 1$. Por la definición de la sucesión sabemos que $a_{k+1} = 2a_k + 1$, entonces
$$a_{k+1} = 2a_k + 1 = 2(2^k -1)+1 = 2(2^k) - 2 + 1 = 2^{k+1} + 1$$
	como se quería probar $\blacksquare$. 
De esta manera, podemos obtener ahora los movimientos para cualquier cantidad de $n$ discos.
	
[^1]: El problema de las torres de Hanoi fue inventado por el matemático francés Edouard Lucas en 1883.