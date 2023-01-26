# Sistemas de Generadores
A partir de la definición de [[Espacios Vectoriales]]  y por lo concluido en el ejemplo 4 de [[Subespacios]], podemos obtener nuevos elementos de un $\mathbb{K}$-espacio vectorial $V$ a partir de elementos sabidos de un subconjunto $G \subseteq V$ considerando sumas finitas de múltiplos por escalares de los elementos de $G$. Sigue entonces la noción de **combinación lineal**:

> [!COMBINACIÓN LINEAL]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial, y sea $G = \{v_1, \dots, v_r\} \subseteq V$. Una **combinación lineal de** $G$ es un elemento de $v \in V$ tal que $v = \sum_{i=1}^r \alpha_i v_i$ con $\alpha_i \in \mathbb{K}$ para cada $1 \leq i \leq r$. 

Un ejemplo de esta definición es por ejemplo que si tomamos $V = \mathbb{R}^3$ entonces el vector $(17,-4,2)$ es una combinación lineal de $(2,1,-3),(1,-2,4)$ porque 
$$(17,-4,2) = 6(2,1,-3) + 5(1,-2,4)$$
pero $(17,-4,5)$ no es una combinación lineal de los 2 vectores anteriores, porque no existen $a_1, a_2 \in \mathbb{R}$ tal que 
$$(17,-4,5) = a_1(2,1,-3) + a_2(1,-2,4)$$
¿Cómo sabemos esto? Porque si distribuimos los escalares en los vectores y los sumamos nos queda que 
$$(17,-4,5) = (2a_1 + a_2, a_1-2a_2, -3a_1+4a_2) \quad \rightarrow \quad \begin{cases} 2a_1+a_2 = 17 \\ a_1-2a_2 = -4 \\ -3a_1 + 4a_2 = 5 \end{cases}$$
Entonces, si podemos encontrar que el sistema de ecuaciones de arriba no tiene solución (lo cual aprenderemos más adelante), listo!

La definición de combinación lineal se puede extender al caso de subconjuntos no necesariamente finitos considerando $I$ como el conjunto de índices tal que $G = \{v_i / i \in I\}$ y para cada elemento de $v \in V$ podemos escribir $\sum_{i\in I} \alpha_i v_i$ donde $\alpha_i = 0$ salvo para finitos $i \in I$.

> [!Sistema de Generadores]
> #Definición Sea $V$ un $\mathbb{K}$ espacio vectorial y sea $G \subseteq V$, Se dice que $G$ es un _sistema de generadores de_ $V$ (y se denota $<G> = V$) si todo elemento de $V$ es una combinación lineal de elementos de $G$. 

Esta definición es muy importante, porque implica que si puedo expresar un espacio vectorial con una cantidad finita de vectores, se vuelve mucho más fácil obtener que vector pertenece o no al espacio (nos basta con resolver un sistema de ecuaciones). También quiere significar que si yo quiero manipular al espacio vectorial (por ejemplo, en funciones) se vuelve mucho más fácil tratar únicamente con los vectores que generan el espacio. 

# Sistemas de Ecuaciones Lineales
El ejemplo 5 de [[Subespacios]] vimos que una ecuación de las coordenadas de un vector es un subespacio de $\mathbb{K}^n$. Entonces por la proposición 2 de [[Subespacios]] tenemos que 
$$S = \Bigg\{(x_1,\dots,x_n) \in \mathbb{K}^n : \begin{cases} a_{11}x_1 + \dots + a_{1n}x_n = 0 \\ \quad \quad \quad \quad \vdots \\ a_{m1}x_1 + \dots + a_{mn}x_n = 0 \end{cases} \Bigg\}$$
es un subespacio de $\mathbb{K}^n$, pues $S = \bigcap_{i=1}^m S_i$ donde $S_i = \{(x_1,\dots, x_n) \in \mathbb{K}^n : a_{i1} x_1 + \dots + a_{in} x_n = 0\}$ y cada $S_i$ es un subespacio por lo tanto la intersección es un subespacio de $\mathbb{K}^n$. 
Los sistemas de ecuaciones aparecerán constantemente en Álgebra 2, por esto es muy importante saber como resolverlos. Queríamos describir el conjunto $S$ usando un _sistema de generadores de este subespacio_, para de esta manera obtener las soluciones del sistema de forma mucho más sencilla.

## Sistemas lineales homogéneos
> [!Sistemas Lineales Homogéneos]
> #Definición Un **sistema lineal homogéneo** de $n$ ecuaciones y $m$ incógnitas a coeficientes en un cuerpo $\mathbb{K}$ es un sistema del tipo 
>  $$\begin{cases} a_{11}x_1 + a_{12}x_2 + \dots + a_{1m}x_m = 0 \\ \quad \quad \quad \quad \vdots \\ a_{n1}x_1 + a_{n2}x_2 + \dots + a_{nm}x_m = 0 \end{cases}$$ donde $a_{ij} \in \mathbb{K}$ para cada $1 \leq i \leq n$, $1 \leq j \leq m$. 

Este sistema de ecuaciones **siempre tiene solución** pues siempre existe la opción de elegir $(x_1,x_2, \dots, x_m) = (0,0, \dots, 0)$ la cual se llama **solución trivial**. Podemos probar que las __soluciones de un sistema homogéneo es un subespacio__, pues por la Prop. 1 de [[Subespacios]], sea $S$ el conjunto de soluciones de un sistema homogéneo de $n$ ecuaciones y $m$ incógnitas: 
- $(0,0,\dots,0) \in S$ (porque la solución trivial siempre existe).
- Si $v,w \in S$ tal que $v = (x_1, \dots, x_m)$ y $w = (y_1, \dots, y_m)$, tenemos que $S$ se puede expresar como $S = \bigcap_{i=1}^m E_i$ siendo $E_i$ el conjunto de soluciones de la ecuación $i$. Tenemos que $v$ y $w$ cumplen la ecuación $i$ por hipótesis tal que $a_{i1}x_1 + \dots + a_{im}x_m = 0$ y $a_{i1}y_1 \dots + a_{im}y_m = 0$ sumando ambas tenemos que $a_{i1}(x_1 + y_1) + \dots + a_{im}(x_m + y_m) = 0$ por lo tanto $v+w \in E_i$. Como esto se cumple para todas las ecuaciones tenemos que $v+w \in S$.
- Si $v \in S$ y $\lambda \in \mathbb{K}$ tenemos que $v = (x_1, \dots, x_m)$ y para la ecuación $i$ se cumple que esta es una solución por lo tanto $v \in E_i$ tal que $a_{i1}x_1 + \dots + a_{im}x_m = 0$, luego multiplicándola por $\lambda$ tenemos que $a_{i1}(\lambda x_1) + \dots + a_{im}(\lambda x_m) = 0$. En conclusión, $\lambda v \in E_i$ y como esto se cumple para toda ecuación tenemos que $\lambda v \in S$. 
Queda comprobado que el conjunto de soluciones de un sistema homogéneo es un subespacio. 

> [!Sistemas Equivalentes]
> #Definición Dos sistemas de ecuaciones homogéneos (SEH) se dicen _equivalentes_ si sus conjuntos de soluciones son iguales.

Notemos que dos sistemas equivalentes no necesariamente tienen la misma cantidad de ecuaciones, por ejemplo 
$$\begin{cases} x+y= 1 \\ 2x+2y = 2\end{cases} \iff \{x+y = 1$$
tienen las mismas soluciones, esto es porque la segunda ecuación en el sistema de la izquierda es un múltiplo de la primera, por lo tanto no produce ningún cambio en el conjunto de soluciones por lo que podemos simplemente eliminarla.
Sería útil tener un método que _me permita obtener las soluciones de un sistema de ecuaciones lineales obteniendo sistemas equivalentes cada vez más sencillos_. De esta manera, nace el método de triangulación o de eliminación de Gauss. 

> [!Proposición 1. (Método de Gauss 1)]
> Dado un SEH, los siguientes cambios en las ecuaciones dan lugar a sistemas equivalentes:
> 1. Intercambiar dos ecuaciones de lugar. ($e^{(ij)}$)
> 2. Multiplicar una ecuación por una constante no nula. ($e_c^{(i)}$)
> 3. Al tener una ecuación con todos sus coeficientes nulos, podemos sacarla del sistema. 
> 4. Reemplazar una ecuación por ella misma más un múltiplo de otra. ($e_c^{(ij)}$)

Entre paréntesis se encuentran las notaciones de cada operación, cada una de estos cambios en las ecuaciones se llaman **operaciones elementales por fila**. 
Notemos que para ver que dos sistemas son equivalentes:
$$ S_1\begin{cases} 
a_{11}x_1 + a_{12}x_2 + \dots + a_{1m}x_m = b_1 \\ 
\quad \quad \quad \quad \vdots \\ 
a_{n1}x_1 + a_{n2}x_2 + \dots + a_{nm}x_m = b_n 
\end{cases} \quad \quad \quad S_2 \begin{cases} 
c_{11}x_1 + c_{12}x_2 + \dots + c_{1m}x_m = b_1 \\ 
\quad \quad \quad \quad \vdots \\ 
c_{r1}x_1 + c_{r2}x_2 + \dots + c_{rm}x_m = b_r
\end{cases}$$
Si $A_1 = \{v \in \mathbb{K}^m : v \text{ cumple } S_1\}$ y si $A_2 = \{v \in \mathbb{K}^m : v \text{ cumple } S_2\}$ queremos ver que $A_1 = A_2$ (recordemos que esto significa que $A_1 \subseteq A_2$ y $A_1 \supseteq A_2$). 

**Demostración.** Sea $S_1$ el conjunto de soluciones del SEH de $m$ ecuaciones y $n$ incógnitas antes del cambio y $S_2$ el conjunto de soluciones después del cambio, queremos ver en todos los casos que $S_1 = S_2$:
1. Si vemos al conjunto de soluciones del sistema como la intersección de los conjuntos de soluciones de cada una de las ecuaciones que lo integran $S = \bigcap_{i=1}^m E_i$ entonces cambiar de orden las ecuaciones, corresponde a intercambiar dos conjuntos en la intersección. Como la intersección es conmutativa, el conjunto que resulta es el mismo. Por ejemplo, si intercambio la ecuación $i$ con la $j$ : $$\begin{align} S_1 = E_1 \cap E_2 \cap \dots \cap E_i \cap \dots \cap E_j \cap \dots \cap E_m \\  S_2 = E_1 \cap E_2 \cap \dots \cap E_j \cap \dots \cap E_i \cap \dots \cap E_m\end{align}$$
	Notemos que $S_1 = S_2$.
2. Sea $x = (x_1, \dots, x_n) \in \mathbb{K}^n$ una solución de $$\begin{cases}  a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n & = 0 \\ \quad \quad \quad \quad \quad \vdots \\ a_{i1}x_1 + a_{i2}x_2 + \dots + a_{1n}x_n & = 0 \\ \quad \quad \quad \quad \quad \vdots \\ a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n & = 0 \end{cases}$$ Al multiplicar la $i$-ésima ecuación por $\lambda \in \mathbb{K}, \; \lambda \neq 0$, resulta el sistema $$\begin{cases}  a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n & = 0 \\ \quad \quad \quad \quad \quad \vdots \\ \lambda a_{i1}x_1 + \lambda a_{i2}x_2 + \dots + \lambda a_{1n}x_n & = 0 \\ \quad \quad \quad \quad \quad \vdots \\ a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n & = 0 \end{cases}$$ Tenemos que en este sistema el conjunto de soluciones de la ecuación multiplicada por un escalar es $\tilde{E}_i = \{v \in \mathbb{K}^n : \lambda a_{i1}x_1 + \lambda a_{i2}x_2 + \dots + \lambda a_{1n}x_n  = 0 \}$  nos basta ver que $\tilde{E}_i = E_i$ para que $S_1 = S_2$. Veamos $E_i \subseteq \tilde{E}_i$, si $x \in E_i$ es una solución de la ecuación tenemos que $$a_{i1}x_1 + a_{i2}x_2 + \dots + a_{1n}x_n  = 0 \underset{\lambda \in \mathbb{K}}{\implies} \lambda(a_{i1}x_1 + a_{i2}x_2 + \dots + a_{1n}x_n) = 0$$ Luego, $x \in \tilde{E}_i$ por lo que se cumple la contención. Para ver $E_i \supseteq \tilde{E}_i$ si $x \in \tilde{E}_i$ multiplicando de ambos lados por $\lambda^{-1} \in \mathbb{K}$ tenemos que $x \in E_i$. Por lo tanto, $\tilde{E}_i = E_i \implies S_1 = S_2$.
3. Si tengo una ecuación $i$ nula tenemos que $E_i = \{(x_1,\dots, x_n) \in \mathbb{K}^n : 0 x_1 + \dots + 0 x_n = 0\}$ y notemos que toda $x \in \mathbb{K}^n$ resuelve esta ecuación $E_i = \mathbb{K}^n$ pero luego $$\begin{align} S_1 & = E_1 \cap \dots \cap E_{i-1} \cap E_i \cap E_{i+1} \cap \dots \cap E_m = E_1 \cap \dots \cap E_{i-1} \cap \mathbb{K}^n \cap E_{i+1} \cap \dots \cap E_m \\ &= E_1 \cap \dots \cap E_{i-1} \cap E_{i+1} \cap \dots \cap E_n = S_2\end{align} $$
4. Como ya demostramos la operación 1, tenemos que no importa el orden en el que estén las ecuaciones, si puedo probar para dos cualquiera esta operación entonces queda probada para todas. Elijamos por ejemplo la primera y segunda ecuación sus conjunto solución son $E_1 = \{(x_1, \dots, x_n) \in \mathbb{K}^n : a_{11}x_1 + \dots + a_{1n}x_n = 0\}$ y $E_2 = \{(x_1, \dots, x_n) \in \mathbb{K}^n : a_{21}x_1 + \dots + a_{2n}x_n = 0\}$ entonces si multiplicamos a la segunda ecuación por una constante $c \in \mathbb{K}$ y las sumamos para luego reemplazarla en $E_1$ tenemos que $\tilde{E}_1 = \{(x_1, \dots, x_n) \in \mathbb{K} : (a_{11} + ca_{21})x_1 + \dots + (a_{1n}+ca_{2n})x_n = 0\}$. Veamos que si $E_1 \cap \tilde{E}_2 = E_1 \cap E_2$ entonces $S_1 = S_2$. 
	Veamos primero que $E_1 \cap E_2 \subseteq E_1 \cap \tilde{E}_2$, si $(y_1, \dots, y_n) \in E_1 \cap E_2$ es una solución de ambos por lo tanto se cumple $a_{11}y_1 + \dots + a_{1n}y_n = 0$ y $a_{21}y_1 + \dots + a_{1n}y_n = 0$. Multiplicando a la segunda ecuación por $c$ y sumándola a la otra tenemos que $(a_{11} + ca_{21})y_1 + \dots + (a_{1n}+ca_{2n})y_n = 0$ entonces $(y_1, \dots, y_n) \in \tilde{E}_2 \cap E_1$ y se cumple la contención. Se prueba $E_1 \cap E_2 \supseteq E_1 \cap \tilde{E}_2$ de manera inversa o lo anterior sabiendo que la ecuación 1 se cumple si la multiplicamos por $c$ y la restamos a nuestra ecuación 2 modificada obtenemos la ecuación 2 anterior. $\blacksquare$ 

Podemos generalizar la proposición anterior para un sistema de ecuaciones no homogéneo demostrándolo de forma prácticamente idéntica. Usando este método podemos resolver cualquier sistema de ecuaciones con muchas variables.

Notemos que al usar este método (en un sistema no homogéneo), si obtenemos un absurdo como por ejemplo $0x_1 + \cdots + 0x_n = 4$ esto quiere significar que nuestro sistema **no posee soluciones**. 
