# Acciones Combinatorias
En nuestra vida cotidiana tenemos problemas más complicados como los que se nos presentan con los [[Principios del Conteo]], en particular trataremos dos: contar la cantidad de formas de ordenar los elementos de un conjunto y cuantas formas hay de elegir elementos de un conjunto.  Veremos que escencialmente usaremos los principios de conteo como base para demostrar todo lo que veamos en esta lección. Recordemos que estamos en los números enteros [[Z]].

---
## Acción 1: Ordenar
Nos podemos hacer la siguiente pregunta: _¿Cuántos números de 3 cifras hay que sean múltiplos de 9?_
Sabemos por las Reglas de Divisibilidad (vistas en [[Sistemas s-adicos]]) un número $x \in \mathbb{N}$ es múltiplo de 9 sí y sólo sí la suma de las cifras de $x$ da múltiplo de 9. Quiero un número $x = a \; b \; c$ donde $a = \{0,1,2, \dots, 9\}, \; b = \{0,1,2, \dots, 9\}$ y $c = \{0,1,2, \dots, 9\}$ tal que $a + b +c = 0, 9, 18, 27$ veamos que la suma máxima puede ser 27 porque $9+9+9 = 27$. 
- Suma 0: No hay ninguna.
- Suma 9: si lo razonamos lógicamente, eligiendo un número al principio, por ejemplo $x = 1 \; \_ \; \_$ entonces en la segunda posición podemos poner cualquier número del 0 al 8 (recordemos que queremos que la suma nos de 9, entonces 9 no es una opción) son 9 opciones  y en la última posición tenemos un número que depende del segundo que hayamos elegido, por ejemplo si elegimos $x = 1 \; 8 \; \_$ pues es obvio que el último número es 0; luego para $x = 1 \; 7 \; \_$ el último número debe ser 1. Como solo nos queda una opción por elegir, tenemos que la cantidad de números eligiendo 1 al principio es $9 \cdot 1 = 9$ (por el principio de múltiplicación). Luego, si reemplazamos el 1 por $x = 2 \; \_ \; \_$ notaremos que nos quedan 8 opciones para poner en el segundo número del 0 al 7 y en el tercer número nos queda solo una opción (como con el 1), entonces nos quedan $8 \cdot 1 = 8$ formas. Si luego analizamos que ocurre para $x = 3 \; \_ \; \_$ nos quedan 7 formas, para $x = 4 \; \_ \; \_$  serían 6 formas, 5 para $x = 5 \; \_ \; \_$, 4 para $x = 6 \; \_ \; \_$, 3 para $x = 7 \; \_ \; \_$  (720, 711, 702), 2 para $x = 8 \; \_ \; \_$ (810, 801) y 1 para $x = 9 \; \_ \; \_$ (900). De esta manera, $9 + 8+7+6+5+4+3+2+1 = 45$ números de 3 digitos que suman 9.
- Suma 18: si usamos la misma estratégia, que con la suma del nueve obtendremos que los números de 3 cifras que suman 18 van a ser para $x = 1 \; \_ \; \_$ serían 2 (198, 189), $x = 2 \; \_ \; \_$ serían 3 (297, 288, 279), $x = 3 \; \_ \; \_$ serían 4, $x = 5 \; \_ \; \_$ serían 5, ..., $x = 9 \; \_ \; \_$ serían 10. Entonces $2+3+4+5+6+7+8+9+10 = 54$ por el principio de adición.
- Suma 27: hay solo 1 (999).
En total, $45 + 54 + 1 = 100$ digitos que son divisibles por 3.

Intentemos formalizar todo lo que vimos en el ejemplo de arriba. ¿Cómo expresamos matemáticamente que buscamos no repetir y ordenar los números de manera tal que al principio tenemos que "elegir" entre los que tenemos los que son múltiplo de 3?

Plantemos la siguiente situación  ¿Cuántas [[Funciones]] posibles existen que va de un conjunto finito a otro?

> **Teorema** Si $|A| = n$ y $|B| = m$, entonces hay un total de $m^n$ funciones $A \rightarrow B$. 

**Demostración**. Sabemos que $f$ es una relación a la cual a cada elemento de $B$ se la asigna un único elemento de $A$. Entonces si para todo $a \in A$ existe un $b \in B$ (que puede ser cualquiera), puede ocurrir que $f(a) = b$ y $f(c) = b$ entonces un elemento de A puede tomar cualquier elemento de $b$ entonces existen $m$ posibilidades para elegir para ese elemento y podemos usar el *principio de multiplicación* entonces $\underbrace{m \cdot m \cdot m \cdots m}_{n \text{ veces}} = m^n$. $\blacksquare$ 

Este teorema nos sirve si nos preguntamos cuantas relaciones del tipo función existen entre los elementos de dos conjuntos. Por ejemplo, sea $A = \{9, 18, 27\}$ (que es el conjunto con las sumas de los elementos múltiplos de 3 y sea $B = \{1, 2, \dots, 9\} \times \{0,1,2, \dots,9 \} \times \{0,1,2,\dots, 9\}$ que es el conjunto con todos los números de 3 digitos. Podemos ver que $|A| = 3$ y $|B| = 9 \cdot 10 \cdot 10 = 900$ , entonces la cantidad total de funciones que van de $B \rightarrow A$ serían $3^{900}$ y solo una de estas funciones es la que buscamos (la que nos de que la suma de los digitos son 9, 27 y 18).

### Permutaciones
Ahora, otra pregunta que nos pueden hacer es ¿Cuantas formas hay de ordenar los números 1, 2, 3 en números de 3 digitos (sin haber repeticiones de los digitos)? Es obvio que si nos pondemos a contar usando el método que aprendimos arriba de fijar un número al principio, por ejemplo $x = 1 \; \_ \; \_$ podemos ver que las formas en las que podemos poner al 2 y al 3 son 2 (123, 132). Y veamos que esto es lo mismo con el 2 y el 3 nos queda $2+2+2 = 6$. Pero veamos que otra forma de pensarlo es decir que en el primer lugar tenemos 3 digitos para elegir, en el segundo lugar como ya elegimos un digito nos quedan 2 y en el tercero nos queda 1, entonces podemos calcular esto como $3 \cdot 2 \cdot 1 = 6$. De aquí viene el concepto de **factorial** (visto en [[Definiciones Recursivas]]), de ordenar elementos (sin repeticiones). 
Formalizando usando funciones, queremos ver que para cada elemento del conjunto $A = \{1,2,3\}$ corresponda *un y solo un* elemento del conjunto $B = \{ \text{ 1er lugar, 2do lugar, 3er lugar } \}$. Entonces lo que estamos buscando es cuantas funciones **biyectivas** existen.  

> **Teorema**. Si $|A| = n$ y $|B| = m$, entonces hay funciones biyectivas $h: A \rightarrow B$ si y solo sí $m = n$ y en ese caso hay $m!$.

**Demostración**. Si $|A| = n$, entonces por definición del cardinal existe una función $f: [[1, n]] \rightarrow A$ biyectiva, y si $|B| = m$ existe una función $g:[[1, m]] \rightarrow B$ biyectiva. Podemos armar el siguiente diagrama y concluir que $j(x) = f(h(g^{-1}(x))$ entonces  $j:[[1,n]] \rightarrow [[1,m]]$  es biyectiva y por un colorario del principio del palomar (visto en [[Principios del Conteo]]) tiene que ocurrir que $m=n$  para que $j$ sea biyectiva.
![[Pasted image 20220708114246.png | 300]]
Ahora, como sabemos que $j$ es inyectiva, basta ver que existen $n!$ funciones $j:[[1,n]] \rightarrow [[1,n]]$ (recordemos que $n=m$). Probemos por inducción esto. El caso base nos dice  $[[1,1]] \rightarrow [[1,1]]$  existe solo 1 función de este tipo y es verdad. Luego, supongamos $P(k)$ es verdadera, es decir exiten $k!$ funciones del tipo $j: [[1,k]] \rightarrow [[1,k]]$. Entonces, demostremos que existen $(k+1)!$ funciones tal que $j: [[1, k+1]] \rightarrow [[1,k+1]]$ . 
Veamos que $(k+1)! = k! \cdot (k+1)$ y que se cumple que si $i \in [[1, k+1]]$ tenemos que $[[1,k+1]] - \{i\}$ está en clara biyección con $[[1,k]]$ por la primera parte del teorema. Por ejemplo podemos tener la siguiente función $\phi$ 
$$\begin{align}
1 & \mapsto 1 \\
2 & \mapsto 2 \\
& \; \; \vdots \\
i-1 & \mapsto i-1 \\
i+1 & \mapsto i \\
& \; \; \vdots \\
k+1 & \mapsto k \\
\end{align}$$
Como $|[[1,k+1]]-\{i\}| = |[[1,k]]| = k$, por la hipótesis inductiva, existen $k!$ funciones en $[[1,k+1]]-\{i\}$, luego si existen $(k+1)$ formas de elegir $i$ entonces por el principio de multiplicación $k!(k+1) = (k+1)!$. Y por lo tanto, existien $n!$ funciones biyectivas $j: [[1,n]] \rightarrow [[1,n]]$, $\forall n \in \mathbb{N}$.  [^1] $\blacksquare$ 

> **Definición.** Sea $A = \{a_1, a_2, \dots, a_n\}$. Llamamos a una **permutación de A** a una $n$-tupla con exactamente todos los elementos de $A$. La cantidad total de permitaciones de A se calcula con el factorial $n!$.

Es decir, que existen $n!$ formas distintas de ordenar los elementos de un conjunto de n elementos, para $n \in \mathbb{N}$. 

### Arreglos
Supongamos ahora que nos preguntan _¿Cuantos números de 3 digitos existen sin tener que repetir ningún digito?_ Por ejemplo, 911 no sería uno de los números que buscamos pues se repite el 1. 
Tratemoslo igual que un problema normal de permutaciones, tenemos 9 posibilidades para el primer digito $\{1,2,3,4,5,6,7,8,9\}$. Luego una vez que elijamos este no se puede volver a repetir en el segundo (que puede tomar valores de $\{0,1,2,3, \dots, 9\}$) por lo cual le quedan 9 posibilidades si descartamos 1. Por último, en el tercer digito que elijamos no se puede repetir ni el primero ni el segundo, entonces debemos descartar 2 posibilidades y nos quedan 8. Por lo cual, usando el mismo razonamiento que las permutaciones, encontramos que la cantidad de posibilidades es $9\cdot 9 \cdot 8$ . 
¿Cómo podemos formalizar esto en términos de funciones y conjuntos?

Sea  $D = \{0,1,2,3, \dots, 9\}$ siendo los posibles digitos (vamos a suponer por ahora que números como $001$ o $030$ son de tres digitos) y sea $L = \{ \text{ 1er lugar, 2do lugar, 3er lugar } \}$, notemos que no pueden existir funciones biyectivas tales que $f:L \rightarrow D$ pues $|D| \neq |L|$ (por un colorario visto en [[Principios del Conteo]]), pero si pueden existir **funciones inyectivas** pues $|L| \leq |D|$ por el principio del palomar (visto en [[Principios del Conteo]]). Entonces, fijemosnos que tiene sentido preguntarnos cuantas funciones *inyectivas* existen para encontrar la cantidad de números de 3 digitos (con digitos distintos existen) pues cada elemento de L puede relacionarse con un elemento de D. 

> **Teorema.** Si $|A| =n$ y $|B| = m$ entonces hay funciones inyectivas $A \rightarrow B$ cuando $n \leq m$ y en ese caso hay $m(m-1)\cdots (m-n+1)$ o $\frac{m!}{(m-n)!}$.

**Demostración**. Sabemos por el principio del palomar que no existen funciones del tipo $n > m$ inyectivas así que la primera parte del teorema queda demostrada. Luego, la segunda parte del teorema la podemos demostrar por inducción. $\blacksquare$ 

> **Definición**. Sea $m,n \in \mathbb{N}, \; X = \{a_1, a_2, \dots, a_m \}$ y lamamos a un **arreglo** de $n$ elementos a una $n$-tupla con elementos distintos de $X$. Se denota $A(n,m)$ y se lee "la cantidad de arreglos de n en m". La cantidad de arreglos posibles se calculan usando $\frac{m}{(m-n)!}$.


### Ordenar en círculos
_¿De cuántas formas se pueden sentar 6 personas alredor de una mesa circular?_
A simple vista este problema parece otra aplicación de encontrar las **permutaciones** posibles. Podemos elegir a 6 personas para sentarse en el primer asiento, una vez que elegimos una nos quedan 5 para elegir en el segundo puesto, y así sucesivamente. Entonces, podríamos decir que existen $6!$ formas de sentarlos. Pero, esto sería incorrecto pues existe un problema en nuestros calculo con respecto a cual asiento es el "primer asiento", pues en un círculo no podemos definir un principio ni un final. A lo que nos referimos con esto es que tenemos que tener en cuenta que entre las posibilidades que contamos existen algunas que son "rotaciones" de los asientos, es decir notemos que todas las siguientes son tienen la misma posición de los asientos para las mismas personas pero nomás que están rotadas. 
![[Pasted image 20220711085846.png]]
Si nos pusieramos todos de acuerdo y definieramos a un asiento como el primero y el que está a la derecha como el segundo y así sucesivamente, no existe ningún problema con nuestro calculo. Pero si nos antisiparan que solamente nos importan las _posiciones relativas_ de las personas (es decir, quién está a la izquierda y a la derecha de quíen) entonces tendríamos que eliminar estas "rotaciones". Notemos que tendríamos que sacar las rotaciones para cada permutación posible, entonces debemos dividir por 6. Por lo cual la cantidad total de permutaciones posibles es $6!/6 = 5!$.



[^1]: Sino lo entiende de esta manera, otra forma de verlo es fijando uno de los $m$ elementos (como vimos en el ejemplo del principio) y ver cuantas posibilidades existen de "permutar" el resto de los elementos. Las posibilidades son las mismas para todos los elementos que fijemos. Luego, sumamos $m$ veces esas posibilidades y es lo mismo que multiplicar directamente por $m$.
