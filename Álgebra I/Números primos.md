# Números Primos
> #Definición  Si $p \in \mathbb{Z}$ ([[Z]]), $p$ se dice **número primo** si $p \neq 1$ y $p \neq -1$ y además $p$ *sólo admite como divisores a 1, -1, p y -p*. 

NOTA: 0 no es primo pues $m|0, \; \forall \; m\in \mathbb{Z} - \{0\}$, 1 tampoco es primo. 
Podemos comparar a los números primos como **átomos de los números enteros**. Es decir, siendo los átomos una párticula que es indivisible (al menos sabieamos esto hasta el siglo 20) y única en su tipo que forma a todas las móleculas y por lo tanto a todas las cosas, se los compara con los números primos porque vamos a ver que estos, conforman a todos los enteros en cuanto a hablamos de la división hablamos. Decimos que 1 no es primo porque el 1 divide a todos los números, entonces es como el **conjunto vacío** (que habíamos dicho en la teoría de conjuntos que era un subconjunto de todos los conjuntos). 
Sigue una lista con los primeros primos $< 1000$, trate de observarlos y ver como están distruibuidos, algunas de las preguntas que nos haremos en esta sección será _¿Podemos predecir donde están los números primos?_ y _¿Existen infinitos primos?_
![[Pasted image 20220715111247.png]]

---

## Propiedades de los números primos

> **Lema.** Sea $p$ primo, y sea $a,b \in \mathbb{Z}$. Entonces,
> 1. O ocurre que $p|a$, o $a$ y $p$ son coprimos.
> 2. Si $p|ab$, entonces $p|a$ o $p|b$. (Propiedad fundamental de los primos)

**Demostración.** (1) Por su definición, $\mathrm{mcd}(a,p)$ (el [[Máximo Común Divisor]]) es un divisor positivo de $p$, así que solo puede ser 1 o $p$. Si $\mathrm{mcd}(a,p)=p$ entonces $p|a$, y si $\mathrm{mcd}(a,p) = 1$ entonces son coprimos. (2) Sea $p|ab$. Si $p \nmid a$ entonces por (1) esto implica que $\mathrm{mcd}(a,b) = 1$ luego existen unos números $s, t \in \mathbb{Z}$ tal que $as + pt =1$, y si multiplicamos por $b$ nos queda $bas + bpt = b$. Por hipótesis tenemos que $p|bas$ y sabemos que $p|bpt$, entonces por el colorario visto en [[Divisibilidad]] nos queda que $p|b$. Podemos obtener que $p|a$ si empezamos asumiendo que $p \nmid b$. $\blacksquare$ 

Estos resultados pueden fallar si tomamos un $p$ no primo, por ejemplo $p=4$, $a=6$ y $b=10$. El apartado (2) del lema puede ser expandido para cualquier número de factores.

> **Colorario.** Sea $p$ primo y p divide a $a_1, a_2, \dots, a_k \in \mathbb{Z}$, entonces $p|a_i$ para un $i \in [[1,k]]$. 

 **Demostración.** Se sigue por inducción. $\blacksquare$ 

Este lema es fundamental para entender que son los números primos. Es más podriamos definir a los números primos como: **p es un número primo si y solo si cada vez que p divide a un producto divide a alguno de los factores**. 

> #Definición  A quellos números que son divisibles por más de un primo se llaman **números compuestos**.

> **Lema.** Sea $m \in \mathbb{Z} - \{1,-1,0\}$, entonces existe un $p$ primo tal que $p|m$. 

 **Demostración.** Sea $H = \{m \in \mathbb{N}-\{1\} : m \text{ no tiene divisores primos }\}$ queremos ver que $H= \emptyset$. Usemos el principio de la buena ordenación (visto en [[Principio de la inducción fuerte]]), entonces suponemos por el absurdo que $H \neq \emptyset$ y tiene primer elemento $n_0 \in H$. El primer elemento $n_0$ no puede ser primo pues si lo fuera $n_0|n_0$, entonces $n_0 \notin H$, y llegamos a un absurdo. Como $n_0$ no es primo tiene que tener un divisor $1 < k < n_0$ y $k|n_0 \Rightarrow k \notin H$ (pues $n_0$ es el primer elemento). Luego, $k$ tiene un divisor primo $p|k$ y como $k|g$ entonces $p|g$, y llegamos a un absurdo. Las contradicciones vienen de suponer que $H \neq \emptyset$. $\blacksquare$ 

Podemos ahora afrontar la primer pregunta que nos hicimos _¿Cómo encontramos números primos?_ Para encontrar todos los números primos que hay debajo de un conjunto de números usamos la **Criba de Eratóstones** que consiste en escribir en una cuadrícula todos los números menores al máximo que determinamos e ir tachando los que son divisibles por un número primo.

Por ejemplo, si queremos encontrar los primos hasta el 57, escribimos:
![[Pasted image 20220715123154.png]]
El primer primo que encontramos en la lista es el 2, entonces tachamos todos los pares
![[Pasted image 20220715123243.png]]
Luego, el primer número que "sobrevivio" fue el 3, entonces tachamos todos los múltiplos de 3,
![[Pasted image 20220715123411.png]]
De esta manera, vamos descartando todos los números que no sirven porque son múltiplos de un primo. El siguiente número que nos queda es el 5, entonces tachamos sus múltiplos
![[Pasted image 20220715123558.png]]
Y se sigue el procedimiento con 7:
![[Pasted image 20220715123637.png]]
Notemos que este procedimiento puesde ser un tanto tedioso porque hay que ir viendo cuales son los múltiplos de cada número e ir encontrando el siguiente no tachado (fue ideado por un señor llamado eratóstones en el año 200 A.C. así que mucho no podemos esperar). 
Podemos demostrar, que con llegar hasta el 7 nos basta (observe que todos los números que no están tachados son primos). 

> **Lema. (Criterio de la Raíz)** Si $a \in \mathbb{N}-\{1\}$ y $a$ *no es primo* entonces  $\exists \; p \in \mathbb{N}-\{1\}$ divisor primo de $a$ tal que $p \leq \sqrt{a}$.

**Demostración.**  Sea $H = \{h \in \mathbb{N}: h \text{ es primo y } h|a\}$. Sea $q$ el 1er elemento de $H \Rightarrow a= q \cdot x, \; x \in \mathbb{N}, \; x \neq 1$ pues $q$ es primo y $a$ no es primo. $\Rightarrow x \in \mathbb{N}-\{1\}$ entonces el lema previo dice que $x$ tiene un divisor primo $r \Rightarrow x = r \cdot s, \; s \in \mathbb{N}, \; r \leq x$. Como $r|x$ y  $x|a \Rightarrow r|a, \; r \in H$. Como $q$ es el primer elemento de H, $q \leq r \leq x$, multiplicando por $q$: $q^2 \leq rq \leq xq = a \Rightarrow q^2 \leq a \Rightarrow q \leq \sqrt{a}$ $\blacksquare$ 

Lo que nos dice que este lema, es que dado un número que queremos saber si es primo o no, todos los posibles divisores primos están **antes de la raíz cuadrada** del número. En realidad la raíz cuadrada no está definida en los números enteros, así que tenga en cuenta que cuando la aplica, lo hace en los números reales [[R]]. Es por esto que en el ejemplo anterior si queremos ver si el número 57 es primo, nos basta ver si es divisible por números primos hasta el 7, pues $7^2 = 49 \leq 57$, el siguiente primo es 11 y $11^2 = 121 > 57$.  

