# Enteros Modulares
> #Definición Recordemos las clases de equivalencia de las [[Congruencia de Enteros]] de módulo $m$, $n \in \mathbb{N}: \; a \in \mathbb{Z}$ ([[Z]]).  $$\bar{a} = [a]_n = \{m \in \mathbb{Z}: m \equiv a \; (n)\}$$Sea $n \in \mathbb{N}$, se define el conjunto finito  $$\mathbb{Z}_n = \{[0], \; [1], \; \dots \;, [n-1]\}$$ $\mathbb{Z}_n$ es un [[Conjuntos]] finito de $n$ elementos. Los elementos de $\mathbb{Z}_n$ se llaman **enteros modulares**. 

En $\mathbb{Z}_n$ introducimos 2 operaciones, de suma y producto entre elementos:
- $(+): \; \mathbb{Z}_n \times \mathbb{Z}_n \rightarrow \mathbb{Z}_n \implies [a] + [b] = [a+b]$
- $(\cdot): \; \mathbb{Z}_n \times \mathbb{Z}_n \rightarrow \mathbb{Z}_n \implies [a] \cdot [b] = [a \cdot b]$
Podemos preguntarnos si existen elementos neutros en estas operaciones: $[0]$ es el operador neutro de la suma y $[1]$ es el operador neutro de la multiplicación. Notemos que escribir $a \equiv b \; (n)$ es equivalente a escribir $[a]_n = [b]_n$. 

Antes de continuar, necesitamos mostrar que estas operaciones se comportan bien. Es decir, queremos ver que si $[a] = [a']$ y $[b] = [b']$, entonces $[a+b] = [a'+b']$, $[a-b] = [a'-b']$ y $[ab] = [a'b']$. 

---
## Propiedades de los Enteros Modulares


> **Propiedades de la suma.** Las propiedades que existen en la suma de $\mathbb{Z}_n$:
> 1. Es asociativa: $[a] + ([b]+[c]) = ([a]+[b])+[c] = [a]+[b]+[c]$
> 2. Es conmutativa: $[a]+[b] = [b]+[a]$
> 3. Existe un elemento neutro $[0]$
> 4. $\forall [a] \in \mathbb{Z}_n, \; \exists \; [b]$ tal que $[a]+[b] = [0]$  


>**Propiedades de la múltiplicación.** Las propiedades que existen en el producto $\mathbb{Z}_n$:
> 1. Es asociativo, $[a] \cdot ([b] \cdot [c]) = ([a] \cdot [b]) \cdot [c] = [a] \cdot [b] \cdot [c]$ 
> 2. Es conmutativo, $[a] \cdot [b] = [b] \cdot [a]$ 
> 3. Existe un único elemento identidad $[1]$
> 4. Es distributivo el producto respecto de la suma $[a] \cdot ([b] + [c]) = [a] \cdot [b] + [a] \cdot [c]$ 

La mayoría de las propiedades son heredadas de los enteros, sin embargo no todo está bien definido en los enteros modulares, veamos que ocurre cuando intentamos definir la potenciación en $\mathbb{Z}_n$. 
Podríamos definir $[a]^{[b]} = [a^b]$ restringuiendo a $b > 0$ para mantener que $a^b$ es un entero [[Z]].  Si tomamos $\mathbb{Z}_3$, $a=2$ y $b=1$ , por ejemplo, esto nos da $[2]^{[1]} = [2^1] = [2]$ pero veamos que $[1] = [4]$ en $\mathbb{Z}_3$ por lo cual $[2]^{[4]} = [2^4] = [16] = [1] \neq [2]$, entonces obtenemos diferentes resultados si elegimos dos elementos $b$ y $b'$ de la misma clase $[b]$. Esto es porque si $a \equiv a'$ y $b \equiv b'$ no implica que $(a')^{b'} \equiv a^b$ .

Por lo tanto, restringuimos la aritmética en $\mathbb{Z}_n$ a operaciones bien definidas como la suma, la resta y la multiplicación. Veremos que existe una forma de hacer que la división también sea bien definida, lo cual nos va a permitir resolver ecuaciones como $[a][x] = [b]$ para todo $[a], [b] \in \mathbb{Z}_n$, algo que no podríamos hacer en los enteros.

---

## El anillo $\mathbb{Z}_n$ y el cuerpo $\mathbb{Z}_p$
En general, no hay inversos en $\mathbb{Z}_n$. Analicemos que sucede cuando $n=6$ o sea $\mathbb{Z}_6$. Podemos armar un cuadro con todos los resultados posibles de sumar dos clases cualquiera:

| $+$ | $0$ |  $1$  |  $2$  |  $3$  | $4$ | $5$ |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| $0$ | $0$ |  $1$  |  $2$  |  $3$  | $4$ | $5$ |
| $1$ | $1$ |  $2$  |  $3$  |  $4$  | $5$ | **0** |
| $2$ | $2$ |  $3$  |  $4$  |  $5$  | **0** | $1$ |
| $3$ | $3$ |  $4$  |  $5$  | **0** | $1$ | $2$ |
| $4$ | $4$ |  $5$  | **0** |  $1$  | $2$ | $3$ |
| $5$ | $5$ | **0** |  $1$  |  $2$  | $3$ | $4$ |

Los $0$ resaltados en negrita son el resultado de sumar un número con su opuesto, veamos que $[1]_6 + [5]_6 = [1+5]_6 = [6]_6 = [0]_6$ por lo cual la clase del 1 es el opuesto a la clase del 5 y viceversa. Esto tiene sentido pues $[-1]_6 = [5]_6$ entonces $[1] + [-1] = [0]$. 
Construyamos la misma tabla para la múltiplicación:

| $\times$ | $0$ | $1$ | $2$ | $3$ | $4$ | $5$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| $0$ | $0$ | $0$ | $0$ | $0$ | $0$ | $0$ | 
| $1$ | $0$ | **1** | $2$ | $3$ | $4$ | $5$ |
| $2$ | $0$ | $2$ | $4$ | $0$ | $2$ | $4$ | 
| $3$ | $0$ | $3$ | $0$ | $3$ | $0$ | $3$ | 
| $4$ | $0$ | $4$ | $2$ | $0$ | $4$ | $2$ |
| $5$ | $0$ | $5$ | $4$ | $3$ | $2$ | **1** | 
Veamos que las operaciones que dan $1$ en negrita representan a los números que tienen **inversos**, decimos que el inverso de la clase $[1]_6$ es inversa de si misma pues $[1]_6 \cdot [1]_6 = [1 \cdot 1]_6 = [1]_6$ y también existe el inverso de la clase $[5]_6$ pues $[5]_6 \cdot [5]_6 = [5 \cdot 5]_6 = [25]_6 = [1]_6$, el inverso de la clase del 5 también es inverso de si mismo.

Notemos que tiene sentido que estos sean los únicos que tienen inverso pues en los números reales [[R]] los únicos números que son inversos de si mismos son el $1$ y el $-1$ (recordemos $[5]_6 = [-1]_6$). Existen clases que al multiplicarlas por otras obtenemos la clase del $[0]$, por ejemlo $[4][3] = [0]$, estas clases se las llama **divisor de cero**. 

El hecho de que existan inversos en el sistema $\mathbb{Z}_n$ nos permite resolver es ecuaciones como $[5]_6[x]_6 = [b]$ para cualquier $[b] \in \mathbb{Z}_6$. Pues como $[5]$ es invertible podemos despejar $[x]$, entonces por ejemplo $[5][x] = [4]$ tiene solución pues $[5]\cdot [5][x] = [5] \cdot [4] \rightarrow [5 \cdot 5][x] = [4 \cdot 5] \rightarrow [1][x] = [2] \rightarrow [x] = [2]$ . 
Sin embargo, la ecuación $5x = 4$ no tiene solución en los números enteros. 

Pero no todas las ecuaciones del tipo $[a][x] = [b]$ en $\mathbb{Z}_6$ se pueden resolver, solamente se pueden resolver para clases $[a]$ que tienen inversos (en este caso $[1]$ y $[5]$). Nos podemos preguntar entonces, _¿Existe un sistema $\mathbb{Z}_n$ en donde para un $n$ entero existan siempre inversos y por lo tanto podamos resolver siempre la ecuación $[a]_n[x]_n = [b]_n$?_ La respuesta es que sí, de hecho existen varios. 

Antes de presentarlos diferenciemos a sistemas que **sí tienen inversos** y sistemas que **no tienen inversos**. En general, las estructuras algebráicas que cumplen todas las propiedades vistas arriba y no tienen inversos las llamamos #Anillo. Y a las estructuras que **sí tienen inversos** y cumplen todas las propiedades de arriba los llamamos #Cuerpo . 

> #Definición El conjunto $\mathbb{Z}_n$, con las propiedades enunciadas se dice que tiene una estructura de **anillo conmutativo con identidad**. 

Un conjunto $A \neq \emptyset$ con dos operaciones, $+: A \times A \rightarrow A$ ("suma") y $\cdot : A \times A \rightarrow A$ ("producto"), que sean respectivamente asociativas y conmutativas siendo el producto distributivo respecto de la suma y con exisistencia de un neutro para la suma y de una identidad para el producto, entonces dicho conjunto se llama **anillo conmutativo con identidad**.

> #Definición Un conjunto A que es anillo conmutativo con identidad se denomina **cuerpo** si $\forall a \in A, \; a \neq 0$  existe $\bar{a} \in A$ tal que $a \cdot \bar{a} = 1$.

Podemos decir que $\mathbb{Z}$ y $\mathbb{Z}_n$ son anillos conmutativos con identidad, $\mathbb{Z}$ no es cuerpo, $\mathbb{Q}$ y $\mathbb{R}$ son cuerpos. 

Algunos $\mathbb{Z}_n$ son cuerpos, otros no; para encontrar si es cuerpo o no lo que podemos hacer es una tabla con todos los valores (como la de arriba) que resultan de sumar y multiplicar los enteros modulares y entonces si existen todos los inversos multiplicativos para cada uno, es un cuerpo.

> #Definición Sea $n \in \mathbb{N}$, $n \geq 2$, sea $[a] \in \mathbb{Z}_n - \{[0]\}$. Entonces 
> 1. $[a]$ se dice **que tiene inverso multiplicativo** si $\exists [b] \in \mathbb{Z}_n- \{[0]\}$ tal que $[a][b] = 1$.
> 2. $[a]$ se dice **divisor de cero** si $\exists [b] \in \mathbb{Z}_n - \{[0]\}$ tal que $[a][b] = 0$. 


> **Proposición.** Sea $[a] \in \mathbb{Z}_n - \{[0]\}, \; n \in \mathbb{N}, \; n \geq 2$. Entonces, $[a]$ tiene un inverso multiplicativo si y solo si $(a, n) = 1$.

**Demostración.**  Tenemos que $(a,n) = 1 \iff_{(1)} \; \exists r,s \in \mathbb{Z} : ra + sn = 1 \iff_{(2)} \; ra = 1-sn$  $\iff_{(3)} \; ra \equiv 1 \; (n)$. En (1) ocurre por el colorario (1) visto en [[Máximo Común Divisor]], luego en (2) pasamos $sn$ del otro lado y por último en (3) obtenemos una ecuación de congruencia equivalente a $[r][a] = [1]$ en $\mathbb{Z}_n$, por lo cual debe existir un $[r]$ que es el inverso. $\blacksquare$ 

>**Corolario.**  $\mathbb{Z}_p$ es un #Cuerpo si y solo si $p$ es primo.

**Demostración.** Sabemos que la clase $[a] \in \mathbb{Z}_p$ es inversible si y solo si $(a,p) = 1$. Supongamos por el absurdo que existe una clase $[a] \neq [0]$ (pues la clase del $[0]$ no es invertible) para la cual $(a,p) \neq 1$, veamos que la única posibilidad que esto ocurra por un lema (1) visto en [[Números primos]] es que $(a,p) = p$ pero entonces $[a] = [p] = [0]$, absurdo pues empezamos asumiendo $[a] \neq 0$. $\blacksquare$ 

De esta manera, la ecuación $[a][x] = [b]$ siempre tiene solución para el cuerpo $\mathbb{Z}_p$. 

 #Estructura-matematica 