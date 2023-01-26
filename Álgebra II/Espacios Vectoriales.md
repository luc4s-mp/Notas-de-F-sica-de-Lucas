# Espacios Vectoriales
En la Física (más específico en [[Vectores]]) introducimos el concepto de **vector** como aquel objeto geométrico que proviene de darle sentido a un segmento definido por dos puntos $A$ y $B$ tal que $\overrightarrow{AB} \neq \overrightarrow{BA}$, o como un elemento que tiene tres componentes: una **amplitud**, una **dirección** y un **sentido** tal que se podían describir como un punto en $\mathbb{R}^2$ o $\mathbb{R}^3$. 

Sin embargo, en la matemática formal se definen los **espacios vectoriales** donde sus elementos se llaman "vectores" aunque no parecieran tener nada que ver con las definiciones previas que teníamos de vector. Resulta que los conjuntos $\mathbb{R}^2$, $\mathbb{R}^3$, $\mathbb{R}[x]$ (el conjunto de todos los [[Polinomios Generalizados]]), $\mathbb{C}^2$, $\mathbb{C}^3$, $\mathbb{Z}^3_{11} = \{(c_1, c_2, c_3) : c_i \in \mathbb{Z}_{11}, \;  i = 1,2,3\}$, entre otros, tienen características en común o parecen venir de la misma estructura. 

Observemos que todos los ejemplos dados anteriormente, vienen de **cuerpos** como $\mathbb{R}$ ([[R]]), $\mathbb{C}$ ([[C]]) y $\mathbb{Z}_{11}$ ([[Enteros Modulares]]), y otro punto que tienen en común que podemos definir la suma de sus respectivos vectores (recordemos que son los elementos) y esta siempre nos da otro vector dentro del conjunto. Por ejemplo $\mathbb{C}^3 = \{(z_1,z_2,z_3) : z_i \in \mathbb{C}, \; i=1,2,3\}$ definimos la suma como que si $\alpha, \beta \in \mathbb{C}^3$, es decir $\alpha = (z_1,z_2,z_3)$ y $\beta = (z_4,z_5,z_6)$ con $z_i \in \mathbb{C}, \; i = 1,2,\dots, 6$, entonces su suma es $\alpha + \beta = (z_1+z_4, z_2+z_5, z_3+z_6)$ que también pertenece a $\mathbb{C}^3$ pues $z_1 +z_2 \in \mathbb{C}, \; z_2 + z_5 \in \mathbb{C}, \; z_3 + z_6 \in \mathbb{C}$ y podríamos comprobar esto para todos los ejemplos anteriores.
De la misma manera, podemos notar que si multiplicamos un elemento del cuerpo $\lambda \in \mathbb{C}$ con el que trabajamos con un vector del conjunto $v \in \mathbb{C}^3$, esto también nos da otro elemento del conjunto $\lambda v = (\lambda z_1, \lambda z_2, \lambda z_3) \in \mathbb{C}^3$, y de vuelta esto se cumple para cada conjunto anteriormente mencionado. 

> [!Operación.]
> #Definición Sea $A$ un conjunto no vacío. Una _operación_ de $A$ es una función $*: A \times A \rightarrow A$.

> [!ACCIÓN.]
> #Definición Sea $A$  y $B$ dos conjuntos no vacíos. Una _acción_ de $A$ en $B$ es una función $\cdot: A \times B \rightarrow A$.

Entonces, podemos decir que para todos los conjuntos anteriores la suma es una **operación** y la multiplicación por $\lambda$ (un número sobre el conjunto en el que estamos trabajando) es una **acción** sobre el conjunto.

Si $V= \mathbb{R}^2 = \{(x,y) ; x,y \in \mathbb{R}\}$ a quien podemos pensar como el _plano cartesiano_, cada uno de los elementos es una **lista** ordenada con largo 2 y si $V = \mathbb{R}^3 = \{(x,y,z): x,y,z \in \mathbb{R}\}$ que puede ser pensado como el espacio de 3D, sus elementos son una lista ordenada de largo 3. Podríamos generalizar que si $V = \mathbb{R}^n = \{(x_1,x_2, \cdots, x_n) : x_i \in \mathbb{R}, \; i = 1, \cdots, n\}$ a que los elementos son una lista ordenada de largo $n$ o en general los matemáticos lo llaman una $n$-tupla. Para $n \geq 4$ es prácticamente imposible visualizar el conjunto. Para $\mathbb{C}^n$ es imposible visualizar nada para $n \geq 2$, pero notemos que a pesar de esto, ***tanto en $\mathbb{C}^n$ como en $\mathbb{R}^n$ se cumplen las mismas propiedades con respecto a la operación suma y a la acción ($\cdot$) de $\mathbb{C}^n$ en $\mathbb{C}$ y  de $\mathbb{R}^n$ en $\mathbb{R}$*** (para cada uno respectivamente) como por ejemplo si $a \in \mathbb{R}$ y $v, w \in \mathbb{R}^n$ ($v = (x_1,x_2, \dots, x_n)$ y $w = (y_1, y_2, \dots, y_n)$) se cumple que 
$$\begin{align} 
a \cdot (v + w) &= a \cdot ((x_1,x_2, \dots, x_n) + (y_1, y_2, \dots, y_n)) = a(x_1+y_1, x_2 + y_2, \dots, x_n+y_n) \\
& = (ax_1+ay_1, ax_2+ay_2, \cdots + ax_n + ay_n) \\
& = (ax_1, ax_2, \cdots, ax_n) + (ay_1, ay_2, \cdots, ay_n) \\ 
& = a(x_1,x_2, \dots, x_n) +  a (y_1, y_2, \dots, y_n) = av + aw
\end{align}$$
Esta propiedad se cumple también para $\mathbb{C}^n$ y se prueba de forma muy parecida. Podemos entonces darle un nuevo nombre a todos estos conjuntos que cumplen unas ciertas propiedades con respecto a una operación y una acción.
Podemos generalizar tal que el conjunto $\mathbb{K}$ que es un #Cuerpo (cualquiera) y a cuyos elementos llamamos **escalares** y tenemos otro conjunto $V$ a cuyos elementos llamamos **vectores**, podemos definir un **espacio vectorial** $V$ sobre $\mathbb{K}$.   

> [!Espacio Vectorial]
> #Definición Sea $(\mathbb{K}, + , \cdot)$ un **cuerpo**. Sea $V$ un conjunto no vacío, sea $+$ una operación en $V$ y sea $\cdot$ una acción de $K$ en $V$. Se dice que $(V, +, \cdot)$ es un **$K$-espacio vectorial** si cumplen las siguientes condiciones:
>  1. $(V,+)$ es un **grupo abeliano**. Es decir, $+$ es asociativa, conmutativa, tiene neutro y opuesto.
>  2. La acción $\cdot : K \times V \rightarrow V$ satisface: 
> 	 i. $a \cdot (v+w) = a \cdot v + a \cdot w, \quad \forall \; a \in \mathbb{K}, \; \forall v, w \in V$ 
> 	 ii. $(a+b) \cdot v = a \cdot v + b \cdot v, \quad \forall a,b \in K; \; \forall v \in V$ 
> 	 iii. $1 \cdot v = v, \forall v \in V$ 
> 	 iv. $(a \cdot b) \cdot v = a \cdot (b \cdot v), \forall a,b \in K; \; v \in V$ 

Un ejemplo trivial de un conjunto que es un espacio vectorial es $V = \{0\}$  basado en $\mathbb{K}$  pues cumple:
(i) Sean $a \in \mathbb{K}$ y $v, w \in V$ tenemos que $v = w = 0$ por lo tanto, $a(0+0) = 0 \in V$.
(ii) Sean $a, b \in \mathbb{K}$ y $v \in V$ tenemos que $v = 0$ por lo tanto, $(a+b)0 =0 \in V$
(iii) Sea $v \in V$ entonces $v=0$ por lo tanto, $1 \cdot 0 = 0 \in V$.
(iv) Sea $a,b \in \mathbb{K}$ y $v \in V$ entonces $v=0$ y se cumple $(a \cdot b) 0 = a (b \cdot 0) = 0 \in V$. 
También, otro ejemplo trivial es eligiendo $V = \mathbb{K}$ basado en $\mathbb{K}$ es un espacio vectorial. Lo que no es tan obvio es si podemos encontrar un subconjunto de $\{0\} \subset W \subset \mathbb{K}$ tal que este sea un espacio vectorial. Adelantándonos, la respuesta es no.  

> [!Proposición 1.]
> No existe un subconjunto $W$ ($\{0\} \subset W \subseteq \mathbb{K}$) tal que este sea un espacio vectorial sobre $\mathbb{K}$. 

**Demostración.** Supongamos que $W$ es un espacio vectorial. Sabemos que si $w \in W \subseteq \mathbb{K}$  y $\mathbb{K}$ es cuerpo entonces existe su inverso $\underset{\in \mathbb{K}}{\underbrace{w^{-1}}} \cdot w = 1 \in W$ y por la (iv) propiedad que se tiene que cumplir del espacio vectorial, si tomamos $a \in \mathbb{K}$ y $b = w^{-1} \in \mathbb{K}$ tenemos que $(a \cdot w^{-1}) \cdot w = a \cdot (w \cdot w^{-1}) = a \in W$ y como esto se cumple $\forall a \in \mathbb{K}$ entonces $\mathbb{K} \subseteq W$ pero luego por hipótesis sabemos que $W \subseteq \mathbb{K}$ por lo tanto $W = \mathbb{K}$.  $\blacksquare$ 

## Otros espacios vectoriales 
Podemos probar que $\mathbb{K}^n$ es un espacio vectorial probando las propiedades de la definición también, es más nuestra definición de $\mathbb{K}^n$ motivo la definición de espacio vectorial. 

**Ejemplo 1.**
Un conjunto muy interesante que nos interesaría estudiar podría ser $\mathbb{K}^{\infty} = \{(x_1,x_2, \dots) : x_i \in \mathbb{K}, \; \forall \; i \in I\}$ siendo $I$ un conjunto de índices (tiene infinitos elementos). La operación $+$ y la acción $\cdot$ están bien definidas:
$$(x_1, x_2, \dots) + (y_1, y_2, \dots) = (x_1+y_1, x_2 + y_2, \dots) \in \mathbb{K}^{\infty} \quad \lambda\in \mathbb{K}, \; \lambda(x_1,x_2, \dots) = \underset{\in \mathbb{K}^\infty}{\underbrace{(\lambda x_1, \lambda x_2,\dots)}}$$
Y luego se cumplen las 4 propiedades por lo tanto es un espacio vectorial. 

> [!Espacio Vectorial de Funciones.]
> #Definición Sea $S$ un conjunto. Se define a $\mathbb{K}^S = \{f : S \rightarrow \mathbb{K} / \; f \text{ es una función }\}$  como el conjunto de todas las funciones que van de $S$ a $\mathbb{K}$. 
> - Sea $f,g \in \mathbb{K}^S$, la suma $f+g \in \mathbb{K}^S$ es la función definida por $(f+g)(x) = f(x) + g(x)$ para todo $x \in S$.
> - Sea $f \in \mathbb{K}^S$, el producto $\lambda f \in \mathbb{K}^S$ es la función  $(\lambda f)(x) = \lambda f(x)$ para todo $x \in S$. 

**Ejemplo 2.**
Se puede probar usando las 4 propiedades de un espacio vectorial que si $S$ es no vacío, entonces $\mathbb{K}^S$ es un espacio vectorial. La identidad aditiva de $\mathbb{K}^S$ es la función $0: S \rightarrow \mathbb{K}$ definida por $0(x) = 0$.
Notemos que $\mathbb{K}^S$ es la generalización de los ejemplos anteriores $\mathbb{K}^n$ y $\mathbb{K}^{\infty}$. Pues una lista de largo $n$ de números en $\mathbb{K}$ puede ser pensada como una función de $\{1,2,\dots, n\} \rightarrow \mathbb{K}$ por lo tanto si juntamos todas las funciones posibles tenemos $\mathbb{K}^n$ y una sucesión de números en $\mathbb{K}$ puede ser pensada como una función desde los números naturales a $\mathbb{K}$ y si tomamos todas las sucesiones posibles tenemos $\mathbb{K}^{\infty}$. En otras palabras, podemos pensar en $\mathbb{K}^n$ como $\mathbb{K}^{\{1,2,\dots,n\}}$ y $\mathbb{K}^{\infty}$ como $\mathbb{K}^\mathbb{N}$.

