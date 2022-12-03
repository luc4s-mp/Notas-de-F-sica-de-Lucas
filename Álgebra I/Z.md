# Los Números Enteros
Anteriormente, en el sistema de números naturales [[N]] vimos que la operación "resta" no está bien definida. Si proposiciones como $2 < 4$ son verdaderas en [[N]], entonces $4 < 2$ no tiene sentido (por la propiedad de la tricotomía), por lo que $2-4$ no es posible en $\mathbb{N}$. De todas formas, sabemos por intuición que nos conviene tener soluciones para este tipo de ecuaciones. Expandiremos a los números naturales para construir un nuevo sistema en el cual existan este tipo de soluciones, el sistema de los números enteros $\mathbb{Z}$.

*Queremos crear este sistema tal que $\mathbb{N} \subseteq \mathbb{Z}$ y se mantengan las mismas propiedades para la suma y la multiplicación, tal que el nuevo sistema no tenga la restricción $a > b$  para que la ecuación $b+x =a$ tenga solución. 

Al igual que hicimos con [[N]], supongamos un conjunto $Z$ del cual no sabemos que elementos, le pedimos que tiene que cumplir que
1. $\mathbb{N} \subseteq Z$ y debe tener las operaciones suma y multiplicación definidas tal que $a +_N b = a +_Z b$ y $a \cdot_N b = a \cdot_Z b, \forall a,b \in \mathbb{N}$
2. La ecuación $x+a = b$ tiene solución para todo $a, b \in \mathbb{N}$
3. Las siguientes propiedades se cumplen:
	- la propiedad **asociativa** y **conmutativa** de la suma
	- la propiedad **asociativa** y **comutativa** de la multiplicación
	- la propiedad **distributiva** de la multiplicación sobre la suma 
	- la propiedad **cancelativa**

Notemos que por (2) existe un cierto elemento en $Z$, al que llamaremos $z$ tal que $a+z = a$ para todo $a \in \mathbb{N}$. 
Ahora supongamos que $c,u \in \mathbb{N}$ y $c + z = u$. Veamos que no es posible que $c \neq u$, pues por (2) de vuelta, existe un $y \in Z$ tal que $y+a = c$, entonces $z + (a+y) = u$ y por asociatividad $(z+a) + y = u \rightarrow a+y = u \rightarrow c = u$. Por lo cual, $z+c = c, \; \forall \; c \in \mathbb{N}$. Es decir, existe un número en $Z$ tal que al sumarlo por cualquier otro elemento de $Z$, obtenemos este mismo elemento. A este elemento tan distinguido lo vamos a llamar **neutro**. 
Veamos como se comporta el neutro $z$ en la multiplicación. Sea $v$ un elemento cualquiera de $Z$ tal que $z \cdot v + 1 \cdot v = (z+1) \cdot v$ (por la propiedad distributiva) , tal que $z \cdot v + 1 \cdot v = 1 \cdot v$ (porque $z+1=1$ por lo que vimos anteriormente). Luego, por la propiedad que probamos arriba que sumar por el neutro no afecta: $z \cdot v + 1 \cdot v = z + 1 \cdot v$, por la propiedad cancelativa nos queda entonces que $z \cdot v = z$ para cualquier $v \in Z$. 

_¿Puede suceder $z \in \mathbb{N}$?_ No. Pues si $z = a \in \mathbb{N}$, entonces $z +a = a$ es lo mismo en los números naturales $a +_N a = a$, pero esto es imposible pues es obvio que en los números naturales $a +_N a > a$, esto es una contradicción que vino de suponer que el neutro estaba en los naturales.

El **neutro** es comúnmente conocido como "cero" y se representa con $0$. (No se si alguna vez han oído hablar de él).

De vuelta, por (2) sabemos que debería existir un $u \in Z$ tal que $u + 2 = 1$ . Sabiendo que $z+1 = 1$, tenemos 
$$\begin{align}
u+(1+1) & = z+1 \\
u+1 & = z \quad \quad \quad \text{ (por la propiedad cancelativa)}
\end{align}$$
Es obvio ver que si el neutro no pertenece a $\mathbb{N}$, entonces $u$ tampoco, pues por definición $u$ es menor que $z$. A este número $u$ lo llamaremos "el **opuesto de 1**" por la propiedad de que al sumarlo por 1 obtenemos el neutro.
Luego, para cada $a \in \mathbb{N}, \; u \cdot a \in Z$ y para este elemento tenemos 
$$u \cdot a + a = u \cdot a + 1 \cdot a= (u+1)\cdot a = z \cdot a = a$$
Parece ser que ser que en $Z$ deben existir estos números del tipo $u \cdot a$ que son únicos para cada número natural a los cuales llamaremos "**opuestos**". Es más, 
si tomamos $a = u$ 
$$u \cdot u + u \cdot 1 =u(u+1) = u \cdot z = z$$
entonces $u \cdot u + u = 1+u \rightarrow u \cdot u = 1$. Entonces, al multiplicar dos opuestos obtenemos un número natural pues $(u \cdot a) \cdot (u \cdot b) = (u \cdot u) \cdot (a \cdot b) = 1 \cdot (a \cdot b)$. 

Por lo cual podemos armar un conjunto $\mathbb{N}^-$ con todos los opuestos de los naturales tal que $\mathbb{N}^- = \{ u  \cdot a, \; \forall a \in \mathbb{N}\}$. Entonces, $\{z\}$ y $\mathbb{N}^-$ son subconjuntos de $Z$ tal que podemos concluir que (a partir de ahora llamaremos a $z= 0$), $Z = \mathbb{N} \cup \{0\} \cup \mathbb{N}^-$ (en realidad hasta ahora solo demostramos $\subseteq$ y nos faltaría demostrar que $\supseteq$ pero esta parte se vuelve un poco más complicada).[^1] 

De ahora en más al opuesto del 1 ($u$) lo denotaremos $-1$ y a los opuestos de cualquier número natural $a$ ($u \cdot a$) lo denotaremos $-a$.

> #Definición Los **números enteros**. Sea $\mathbb{N}^-$ definido de tal manera que $\mathbb{N}^- \cap \mathbb{N} = \emptyset$ y $\mathbb{N}^- = \{-a, \forall \; a \in \mathbb{N}\}$ y sea $0$ (cero) definido como un número no contenido en $\mathbb{N} \cup \mathbb{N}^-$. El conjunto de los números enteros queda definido como  $\mathbb{Z} = \mathbb{N} \cup \{0\} \cup \mathbb{N}^-$.

Una de las propiedades básicas de [[R]] es la existencia de inversos, que luego probaremos únicos. No existen inversos en $\mathbb{Z}$ y esta es la diferencia fundamental entre estos dos conjuntos. 
Notemos que nuestros horizontes se expanden con la aparición de los números enteros, podemos empezar a hablar de la **división**  lo cual trateremos en [[Divisibilidad]]. 
 
---
[^1]: El resto de la demostración la podrá encontrar en "Number Systems of Analysis" G. Cuthbert Webber.


#Matemática #Primer-año 