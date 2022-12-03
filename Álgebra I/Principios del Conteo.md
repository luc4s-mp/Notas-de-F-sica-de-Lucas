# Principios del Conteo
La combinatoria se refiere al arte de contar sin enumerar. En está parte del Álgebra se habla sobre cuanta cantidad de algo hay, de posibilidades, de combinaciones, de elementos, etc. Trataremos principalmente con los números enteros [[Z]].
Cuando nos referimos a contar sin enumerar, hablamos de calcular el números de casos que nos interesan sin hacer una lista concreta. Usted se habrá encontrado con estos problemas alguna vez en su vida, le preguntan cuantas combinaciones diferentes existen de colores de pintura puede haber en una habitación pintando cada pared de un color diferente, esa clase de problemas en las que siempre se termina olvidando de alguna combinación al intentar hacer una lista de todas. Nuestro proposito es contar sin hacer la lista. 

## Principio del Palomar (o de Casilleros)
> **Principio del Palomar**. Si $m, n \in \mathbb{N}$ y $n > m$, entonces **no existe** una función inyectiva tal que $f: \; [[1, n]] \rightarrow [[1, m]]$.

Básicamente lo que nos dice este principio es la noción que tenemos de "contar de uno en uno". Se le llama "del palomar" porque nacío de la analogía de querer poner una cierta cantidad de palomas en un palomar con una cierta cantidad de casilleros, es obvio de que si nos sobran casilleros en el palomar es porque tenemos más casilleros que palomas y si nos sobran palomas tenemos más palomas que casilleros. Entonces, este principio intenta formalizar la idea de que *si la cantidad de palomas $n$ es más grande que la cantidad de casilleros $m$ entonces no existe forma de poner todas las palomas en los casilleros* (sabiendo que cada casillero tiene espacio para una paloma). 
Esto nos puede parecer obvio a simple vista, pero es necesario formalizar esta idea con funciones y conjuntos para poder tener claro que es lo que estamos hablando.

**Demostración.** Sea $A = \{ n, m \in \mathbb{N}, n < m : \exists \;  f:[[1, m]] \rightarrow [[1,n]] \text{ es inyectiva } \}$ el teorema nos dice que $A = \emptyset$ , supongamos por el absurdo que $A \neq \emptyset$. Usemos el principio de la buena ordenación (visto en [[Principio de la inducción fuerte]]), $A$ tiene un primer elemento pues es un subconjunto de $\mathbb{N}$ que llamaremos $m_0$ , es decir: hay un $m < m_0, f:[[1, m_0]] \rightarrow [[1, m]]$ es inyectiva. Notemos que $m_0 \neq 1$ pues 1 es el más chico de los naturales. 
Luego, si $1 < m < m_0$ pueden ocurrir dos situaciones: (i) $f(m_0) = m$ o (ii) $f(m_0) = c < m$ para un $c \in [[1, m]]$. Si ocurre la primera situación (i) entonces $f: [[1, m_0 - 1]] \rightarrow [[1, m-1]]$ sigue siendo inyectiva, pero entonces $m - 1 < m_0 - 1$ y se contradice que $m_0$ es el primer elemento. 
Para afrontar (ii) construyamos una función biyectiva $g:[[1,m]] \rightarrow [[1, m]]$ definida como $g(c) = m$ , $g(m) = c$ y $g(x) = x, \forall x \in \{m,c\}$, es decir creamos una función que relaciona los elementos de $[[1,m]]$ con sigo mismos a excepsión de $c$ y $m$ que los cambia de lugar. Ahora si armamos una nueva función $\tilde{f} : [[1, m_0]] \rightarrow [[1, m]]$, definida como $\tilde{f}(x) = (g \text{ o } f) (x), \; x \in [[1, m_0]]$ , como $\tilde{f}$ es una composición de funciones inyectivas, entonces es inyectiva. El objetivo de hacer esto es que $\tilde{f}$ ahora apunta a $\tilde{f}(m_0) = g(f(m_0)) = g(c) = m$ tal cual teniamos en el caso (i), entonces podemos hacer el mismo proceso que en este caso y nos quede $\tilde{f} : [[1, m_0 - 1]] \rightarrow [[1, m-1]]$ es inyectiva por lo cual nuevamente tendríamos que $m_0 - 1 \in A$ y se contradice que $m_0$ es el primer elemento de A. Las contradicciones vienen de haber supuesto que existe un primer elemento en $A$, por lo que $A = \emptyset$ . $\blacksquare$  

> **Colorario.** Si $m, n \in \mathbb{N}$ y $m \neq n$ entonces *no existen funciones biyectivas entre* $[[1, n]]$ y $[[1, m]]$. 

**Demostración.** Sabemos por el principio del palomar que para $n > m$ no existen funciones inyectivas $f: [[1, n]] \rightarrow [[1, m]]$ y luego si $m > n$ suponemos que si existe una función biyectiva $f: [[1, m]] \rightarrow [[1, n]]$ entonces existe su inversa $f^{-1}: [[1, n]] \rightarrow [[1, m]]$ que es biyectiva también pero ya vimos que esto no puede ocurrir **ABSURDO!** La contradicción viene de suponer que si existe una función biyectiva. $\blacksquare$ 

## Principio de adición
**Si una acción A se puede realizar de $n$ formas distintas y otra acción B se puede realizar de $m$ formas distintas, siendo A y B excluyentes (si se hace A no se hace B y vicecersa), entonces la cantidad de formas posibles de realizar la acción A ó B es $n + m$.**

Supongamos que quiero viajar de Córdoba a Buenos Aires. Considerando distintos horarios, rutas y empresas hay 3 formas de viajar en avión, 5 formas de ir en colectivo y 2 formas de ir en tren. Es obvio lo que hay que hacer si queremos obtener todas las formas de viajar $3+5+2 = 10$. 

Formalicemos esto en términos de [[Conjuntos]] , [[Relaciones entre conjuntos]] y [[Funciones]]. Supongamos que tenemos un conjunto A con las formas de viajar en avión, hay 3 días en los que podemos viajar $A = \{\text{ miércoles 3, jueves 12, sábado 30 } \}$; el conjunto C con las formas de viajar en colectivo,  hay 5 días $B = \{\text{ lunes 1, martes 10, viernes 13, martes 17, viernes 30 } \}$; y el conjunto T con las formas de viajar en tren, hay 2 días $T = \{ \text{ martes 2, lunes 16 }\}$ . _¿Cuantas formas de viajar en total?_

Pero a nosotros no nos interesan los días, nos interesa la **cantidad de días** que podemos viajar. Se ve que entonces necesitamos de una operación unitaria en los conjuntos que nos diga cuantos elementos tiene, a esta la llamaremos **cardinal**.

> **Cardinal de un conjunto**. Dado $n \in \mathbb{N}$, decimos que un conjunto $A$ tiene $n$ elementos si hay una función en $f: [[1, n]] \rightarrow A$ [^1] biyectiva y lo denotamos $|A| = n$.

Tengamos en cuenta que para que el cardinal de un conjunto existe, tiene que ser **finito** (sus elementos se deben poder contar). Por ejemplo, $A$, $C$ y $T$ son finitos, entonces podemos calcular a la cantidad total de formas como
$$|A \cup C \cup T| = |A| + |C| + |T| = 3 + 5 + 2 = 10$$
>  **Principio de la Adición**. Sean $A$ y $B$ conjuntos finitos tal que $A \cap B = \emptyset$ , y sea $|A| = n$ y $|B| = m$ : $$|A \cup B| = |A| + |B| = n+m$$Si $A_1, A_2, \dots, A_n$ son conjuntos disjuntos tal que $A_i \cap A_j = \emptyset$ para todo $1 \leq i$, $j \leq n$ con $i \neq j$, entoces $$|A_1 \cup A_2 \cup \dots \cup A_n| = |A_1| + |A_2| + \dots + |A_n|$$

**Demostración**. Por hipotesis $|A| = n$ y $|B| = m$ y $A \cap B = \emptyset$ , entonces sea $f: [[1, n]] \rightarrow A$ biyectiva y $g : [[1, m]] \rightarrow B$ biyectiva. Quiero probar que hay una función $f: [[1, n+m]] \rightarrow A \cup B$ biyectiva. 
Definamos 
$$h(x) = \begin{cases} 
f(x) & \text{si } x \in [[1,n]] \\
g(x-n) & \text{si } x \in [[n+1, n+m]]
\end{cases}$$
Esta $h$ esta definida en $[[1, n+m]]$ es suryectiva pues para todo $a \in A$ , como $f$ es suryectiva también, $\exists x \in [[1, n]] : f(x) = a \rightarrow h(x) = a$. Y lo mismo para todo $b \in B$. Las funciones tienen que inyectivas, podemos demostrarlo por casos: Supongamos que $\forall x_1,x_2 \in [[1, n+m]], h(x_1) = h(x_2)$ queremos llegar a que $x_1 = x_2$ 
- (i) si tenemos un $x_1, x_2 \in [[1, n]]$  $\rightarrow h(x_1) = f(x_1)$  y $h(x_2) = f(x_2)$, f es inyectiva por hipótesis $f(x_1) = f(x_2) \Rightarrow x_1 = x_2$ .
- (ii) si tenemos $x_1, x_2 \in [[n+1, n+m]] \rightarrow h(x_1) = g(x_1-n)$ y $h(x_2) = g(x_2 - n)$, g es inyectiva por hipótesis $g(x_1 - n) = g(x_2 - n) \Rightarrow x_1 = x_2$.
- (iii) $x_1 \in [[1, n]]$ y $x_2 \in [[n+1, n+m]]$ $\rightarrow h(x_1) = f(x_1) \in A$ y $h(x_2) = g(x_2-n) \in B$ pero plantear $f(x_1) = g(x_2 -n)$ es absurdo pues A y B no comparten elementos por hipótesis. 
Entonces $h : [[1, n+m]] \rightarrow A \cup B$ inyectiva y suryectiva, entonces $h(x)$ es biyectiva. 
La segunda parte del teorema se puede demostrar usando inducción. $\blacksquare$   

> **Colorario**.  Para dos conjuntos $A$ y $B$ finitos **pero no disjuntos** $|A \cup B| = |A| + |B| - |A \cap B|$.

**Demostración.** Llamamos $C = A - B = A - A \cap B$ y resulta $A = C \cup (A \cap B)$.  Como $C \cap (A \cap B) = \emptyset$, entonces el principio de adición indica que $|A| = |C| + |A \cap B|$. Además $A \cup B = C \cup B$ y por lo visto $C \cap B = \emptyset \rightarrow |A \cup B| = |C| + |B|$ entonces reemplazando una ecuación en la otra nos queda $|A \cup B| = |A| + |B| - |A \cap B|$. $\blacksquare$ 

---
## Principio de Multiplicación
**Si una acción A se puede realizar de $n$ formas distintas y una acción B se puede realizar de $m$ formas distintas, siendo A y B acciones independientes, entonces la cantidad de formas de realizar la acción A y B es $nm$.**

Supongamos ahora que queremos viajar ahora de Salta a Mar del Plata, pasando por Tucumán y Córdoba. Si hay 3 formas de ir de Salta a Tucumán, 2 formas de ir de Tucumán a Córdoba y 3 formas de ir de Córdoba a Mar de Plata. Nos podemos preguntar ¿Cuántas formas hay de ir de Salta a Mar del Plata? 
En este caso no podemos simplemente sumar los casos porque porque podemos elegir una y luego otra, es decir podemos elegir por ejemplo una forma de viajar de Salta a Tucumán y luego una de Tucumán a Córdoba y podemos ir convinando las formas en las cuales viajamos en ambas. Entonces, existen $3 \cdot 2 = 6$ formas de ir de Salta a Córdoba, pasando por tucumán. Ahora, podemos combinar cada una de estas 6 formas con las 3 formas de ir de Córdoba a Mar de Plata. Por lo cual existen $6 \cdot 4 = 24$ formas en total de viajar de Salta a Mar del Plata, pasando por Córdoba.

De nuevo, formalicemos esto en términos de [[Conjuntos]], [[Relaciones entre conjuntos]] y [[Funciones]]. Digamos que el conjunto con las formas de viajar de Salta a Tucumán es $A = \{\text{ avión, auto, colectivo }\}$, luego el conjuntos con las formas de viajar de Tucumán a Córdoba es $B = \{\text{ avión, colectivo } \}$ y el conjuto de formas de viajar de Córdoba a Mar de Plata son $C = \{ \text{ avíon, auto, colectivo, caracol } \}$. Queremos elegir una forma de cada conjunto y notemos que importa el orden en el que los elijamos. Entonces, fijemosnos que podemos expresar a la elección de las tres formas usando el **producto cartesiano** $A \times B \times C$ para tener ternas de 3 elementos, esto es necesario porque no es lo mismo viajar primero en colectivo, luego en avión y por último en caracol que haber viajado primero en avión, luego en colectivo y por último en caracol $( \text{ colectivo, avión, caracol } ) \neq ( \text{ avión, colectivo, caracol } )$ (el orden importa). Por lo cual nos queda que la cantidad de formas de viajar de Salta a mar del plata es
$$|A \times B \times C| = |A| \cdot |B| \cdot|C| = 3 \cdot 2 \cdot 4 = 24$$
> **Principio de Multiplicación**. Si $A$ y $B$ son conjunto finitos, entonces $$|A \times B| = |A| \cdot |B|$$
> Si $A_1, A_2, \dots, A_n$ son conjuntos finitos entonces $$|A_1 \times A_2 \times \cdots \times A_n| = |A_1| \cdot |A_2| \cdots |A_n|$$

**Demostración**. Si $|A| = n$ y $|B| = m$, $A = \{a_1, a_2, \cdots, a_n \}$, tal que $a_1, a_2, \cdots, a_n$ son disjuntos. Por lo cual 
$$\begin{align}
A \times B & = \{(a,b) : a \in A, b \in B\} \\
& = (\{a_1\} \times B) \cup (\{a_2\} \times B) \cup \dots \cup (\{a_n\} \times B) \\
& = \underbrace{\{(a_1, b), b \in B\} \cup \{(a_2,b), b \in B\} \cup \cdots \cup \{(a_n, b), b\in B\}}_{n \text{ conjuntos disjuntos}}
\end{align}$$
Cada uno de los $\{(a_i, b), b\in B\}$ tiene en total $m$ elementos y por el teorema de la adición: $|A \times B| = |\bigcup_{i=1}^n \{(a_i, b), b \in B\}| = \underbrace{m + m + \cdots + m}_{n \text{ veces}} = n \cdot m$ . La segunda parte del teorema se puede demostrar por inducción $\blacksquare$. 

---
## Principio del Complemento
**Supongamos que hay $n$ formas de realizar una determinada acción A y, de éstas, hay exactamente $k$ que no cumplen con una propiedad $P$ dada. Entonces, la cantidad de formas de realizar la acción A cumpliendo con la propiedad P es $n − k$.**

Esta propiedad es muy útil cuando los casos que queremos contar son muchos entre el total de casos posibles. Nos conviene descartar simplemente los casos que no nos interesan del total.

Veamos un ejemplo, supongamos que tenemos dos dados, uno blanco y otro negro, la cantidad de combinaciones que se pueden tener de ambos se pueden obtener usando el principio de múltiplicacion $6 \cdot 6 = 36$ y juntos forman pares ordenados del tipo $(x,y)$ como por ejemplo ⚁⚄ $= (2,5)$.  ¿Cuántos pares se pueden obtener que no sean "dobles"? Por ejemplo ⚄⚄ $= (5,5)$ es un doble. 
En este caso, podríamos empezar a contar todos los casos por ejemplo si fijamos el primer dado en ⚀ (1) y contar los casos que pueden ocurrir con el otro dado (el único valor que no puede tomar es el 1) y así sucesivamente cambiando el número al cual fijamos el primer dado. Pero usted podrá notar, que es mucho más simple restarle a la cantidad total de casos aquellos casos que darian dobles que serían: ⚀⚀ $= (1,1)$ ,   ⚁⚁ $= (2,2)$, ⚂⚂ $= (3,3)$, ⚃⚃ $= (4,4)$, ⚄⚄ $= (5,5)$ y ⚅⚅ $= (6,6)$ (6 casos). Entonces, nos quedan $36 - 6 = 30$ casos.

> **Principio del Complemento**. Si $A$ es un conjunto  y $A \subseteq \mathrm{U}$ con $|\mathrm{U}| = n$ entonces $|A| = n - |A^c|$ .

**Demostración**. Como $\mathrm{U} = A \cup A^c$ y $A \cap A^c = \emptyset$, por el principio de adición tenemos que $|\mathrm{U}| = |A| + |A^c|$, de donde $|A| = n - |A^c|$.


[^1]: Los dobles corchetes denotan a un conjunto de números naturales tal que $[[1, n]] = \{ k \in \mathbb{N} \; | \; 1 \leq k \leq n \}$.