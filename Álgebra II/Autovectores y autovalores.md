En [[Cambio de Base y Rango de una matriz]] nos concentramos en las [[Matrices Invertibles]], que pertenecen al conjunto de matrices cuadradas $M_{n \times n} (\mathbb{K})$. Ya definimos que existe un claro isomorfismo entre $M_{n \times n}(\mathbb{K})$ y $\mathrm{Hom}(V,V)$ ( con $V$ de dimensión $n$, proposición 4 de [[Matrices de Transformaciones Lineales]]). Por lo tanto, hablar de matrices cuadradas es lo mismo que hablar de transformaciones lineales de espacio vectorial a sí mismo, estas tienen un nombre especial, se llaman **operadores lineales**.

> [!Operador Lineal]
> #Definición Sea $V$ un $\mathbb{K}$[^1]-espacio vectorial. Una transformación lineal de un espacio vectorial a sí mismo, es decir toda $T : V \rightarrow V$, es llamada _operador lineal_. La notación $\mathrm{Hom(V)}$ denota al conjunto de todos los operadores en $V$.

Al igual que no toda matriz cuadrada es invertible, no todo operador lineal es un isomorfismo (es decir, tiene inversa). Observemos que al trabajar con operadores lineales, el corolario 1.1 del [[Teorema de la dimensión]] vale siempre para espacios vectoriales finitos. 

## Subespacios Invariantes
Supongamos que ya sabemos de antemano que $V = U_1 \oplus \dots \oplus U_m$, es decir que el espacio vectorial $V$ se puede separar en $m$ subespacios con una [[Suma de subespacios]] directa.  Entonces, para entender el comportamiento de un operador lineal $T: V \rightarrow V$ solo necesitamos entender cada $T|_{U_j}$, donde $T|_{U_j}: U_j \rightarrow V$ para cada $j = 1, \dots, m$. Tratar con $T|_{U_j}$ debería ser más sencillo que trabajar con $T$ pues $U_j$ es un espacio vectorial más chico que $V$. 
Sin embargo, es obvio que no siempre $T|_{U_j}$  va darnos valores dentro de $U_j$, en otras palabras, puede que $T|_{U_j}$ no sea un operador sobre $U_j$. Se pueden obtener resultados muy utiles en el caso en el que sí lo sea. Esto inspira el concepto de  **subespacio invariante**. 

> [!Subespacio Invariante]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial. Supongamos $T: V \rightarrow V$. Un subespacio $U$ de $V$ es llamado _invariante_ si para cada $u \in U$ ocurre que $T(u) \in U$. 

El siguiente ejemplo muestra la utilidad de esta definición. 

---
**Ejemplo 1.** Sea $V = \mathbb{R}^2$ con su base canónica $\{e_1, e_2\}$ y supongamos $T \in \mathrm{Hom}(\mathbb{R}^2)$ dada por $T(e_1) = (2,0)$ y $T(e_2) = (1,1)$. Tal que entonces su matriz transformación lineal sea $[T]_E = \begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix}$ y su imagen está generada por $\mathrm{Im}(T) = <(2,0), (1,1)>$. Notemos que el plano cartesiano se puede separar en $\mathbb{R}^2 = U_1 \oplus U_2$ con $U_1 = <e_1>$ y $U_2 = <e_2>$. Notemos que $<e_1>$ genera el eje $x$ tal que $<e_1> = \{x(1,0), \; x \in \mathbb{R}\}$  y alplicarle la transformación tenemos que se genera $<(2,0)>$ sigue siendo el eje $x$, lo único que hicimos fue *multiplicar al vector de la base canónica por $2$ lo cual no modifica el subespacio generado*. Por lo tanto $T|_{U_1} U_1 \rightarrow U_1$, $U_1 = <e_1>$ es un subespacio invariante. Sin embargo, $U_2$ no es un subespacio invariante pues al aplicar la transformación sobre $y(0,1), \forall y \in \mathbb{R}$ (que es el eje $y$) genera $y(1,1), \forall y \in \mathbb{R}$ que ya no es el mismo subespacio, por lo tanto $T|_{U_2} : U_2 \nrightarrow U_2$. 

---

Otros ejemplos de subespacios invariantes son $\{0\}$, $V$, $\mathrm{Nu}(T)$ y $\mathrm{Im}(T)$. 

Resulta que si observamos otras transformaciones lineales, notaremos que los subespacios invariantes ocurren cuando la única modificación que yo le hago a un vector de mi base es _multiplicarlo por un escalar_. Tomemos cualquier $v \in V$ con $v \neq 0$ y sea $U$ un subespacio con todos los múltiplos escalares de $V$: $U = \{\lambda v : \lambda \in \mathbb{K}\} = <v>$. Entonces, $U$ es un subespacio de $V$ de una dimensión. Si $U$ es invariante bajo el operador $T: V \rightarrow V$, luego $T(v) \in U$ por lo tanto existe un escalar $\lambda \in \mathbb{K}$ tal que 
$$T(v) = \lambda v$$
Cuando esto ocurre en operadores, llamamos a los vectores que cumplen esto **autovectores** y a las escalares que los acompañan **autovalores**.

> [!Autovalor y autovector] 
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial y $T: V \rightarrow V$ un operador lineal. Un escalar $\lambda \in \mathbb{K}$ es llamado _autovalor_ de $T$ si existe un $v \in V$ llamado _autovector_ tal que $v \neq 0$ y $T(v) = \lambda v$.

Notemos que $v \neq 0$ pues todo escalar cumple $T(0) = \lambda 0$, sin embargo nada impide que $\lambda = 0$.  

La siguiente proposición habla sobre como encontrar autovalores:
> [!Proposición 1. Condiciones equivalentes para ser un autovalor]
> **(NEF)** Supongamos $V$ un $\mathbb{K}$-espacio vectorial de dimensión finita, $T: V \rightarrow V$ un operador lineal y $\lambda \in \mathbb{K}$. Recordemos que $Id: V \rightarrow V$ es la transformación identidad. Entonces las siguientes son equivalentes:
> 1. $\lambda$ es un autovalor de $T$.
> 2. $T-\lambda  \cdot Id$ no es un monomorfismo.
> 3. $T- \lambda \cdot Id$ no es un epimorfismo.
> 4. $T- \lambda \cdot Id$ no es un isomorfismo y por lo tanto no es invertible.

**Demostración.** Las condiciones (1) y (2) son claramente equivalentes pues si $\lambda$ es un autovalor esto significa que existe un $v \in V$ tal que $T(v) = \lambda v \rightarrow T(v) - Id(\lambda v) = 0 \rightarrow (T- \lambda \cdot Id)(v) = 0$. Luego, (2), (3) y (4) son equivalentes por el corolario 1.1 del [[Teorema de la dimensión]].  $\blacksquare$ 

De esta manera, como $T(v) = \lambda v$ si y solo si $(T - \lambda Id)(v) = 0$, entonces tenemos que todos los autovectores de $V$ que corresponden al autovalor $\lambda$ viven en $\mathrm{Nu}(T- \lambda Id)$. Y encontramos nuestra primera manera de obtener autovalores y autovectores, si $\dim( \mathrm{Nu}(T- \lambda Id)) \neq 0$ entonces $\lambda$ es un autovalor de $T$. Otra forma de verlo es pasando las transformaciones a sus respectivas matrices, tal que $[T]_{B_1B_2}$ es la matriz de la transformación lineal, entonces $\lambda$ es un autovalor si $\det([T]_{B_1B_2} - \lambda Id_n) = 0$, pues en ese caso la matriz $[T]_{B_1B_2}- \lambda Id_n$ no es invertible. Sin embargo, quedemos por ahora con nuestra definición inicial y tratemos de dejar de lado el determinante por ahora. 

Al subespacio $\mathrm{Nu}(T- \lambda Id)$ es tan especial que le damos su propio nombre. 
> [!Autoespacio]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial y sea $T: V \rightarrow V$ un operador lineal con un autovalor $\lambda \in \mathbb{K}$ . El _autoespacio_ correspondiente a $\lambda$ es un espacio vectorial tal que $$E(\lambda, T) = \mathrm{Nu}(T- \lambda Id)$$ 

Es claro que los autoespacios son subespacios de $V$, pues el núcleo de $T- \lambda Id$ lo es.

---
**Ejemplo 2.** Sea $T : \mathbb{K}^2 \rightarrow \mathbb{K}^2$ está definida por $T(w,z) = (-z, w)$. Queremos encontrar todos los autovalores y autovectores tomando $\mathbb{K} = \mathbb{R}$ y luego $\mathbb{K} = \mathbb{C}$. 

Notemos primero que la transformación $T$ representa una rotación de 90° de forma antihoraria sobre el origen en $\mathbb{R}^2$. **Un operador tiene un autovalor si y solo si hay un vector no nulo en su dominio que es llevado por el operador a un múltiplo escalar de sí mismo**.  Entonces para encontrar autovalores de $T$, debemos encontrar escalares $\lambda$ tales que $T(w,z) = \lambda (w,z)$ tiene otra solución que no sea $w=z= 0$. Lo cual es equivalente al sistema de ecuaciones $-z = \lambda w$ y $w = \lambda z$. Sustituyendo el valor de $w$ dado por la segunda ecuación en la primera nos da $-z = \lambda^2 z$ o $(\lambda^2 +1)z = 0$ como $z$ no puede ser igual a 0 (pues entonces esto implicaría que $w = 0$) tenemos que $\lambda^2 +1 = 0$. 

Veamos que para $\mathbb{K} = \mathbb{R}$ no existe solución para esta ecuación, lo cual tiene sentido pues implicaría que no existen vectores sobre una línea que se vean multiplicados por un escalar al producir una rotación de $90°$. Sin embargo, si existe una solución para $\mathbb{K} = \mathbb{C}$ y es $\lambda = i$ ó $\lambda = -i$. Luego, se pueden obtener los autoespacios de $\lambda = i$, $\mathrm{Nu}(T- (i)Id) = \{(-z,w) + (iw, iz), \; \forall z, w \in \mathbb{C}\} = <(-1,i), (i, 1)> = <(-1,i)>$ y lo mismo con $\lambda = -i$.  

---
> [!Lema 2. Autovectores linealmente independientes]
> **(NEF)** Sea $T: V \rightarrow V$ un operador lineal. Supongamos $\lambda_1, \dots, \lambda_m$ es una lista de autovalores distintos de $T$ y sean $v_1, \dots, v_m$ sus correspondientes autovectores (uno de cada autovalor). Entonces, $v_1, \dots, v_m$ son linealmente independientes.

**Demostración.** Usa el lema 2 de [[Independencia Lineal]] y se inicia pensando por el absurdo que los vectores son LD. $\blacksquare$ 

> [!Corolario 2.1. el número de autovalores]
> **(NEF)** Supongamos que $V$ es un espacio vectorial de dimensión infinita. Entonces, cada operador lineal en $V$ tiene como máximo $\dim V$ autovalores distintos.

**Demostración.** Sea $T: V \rightarrow V$ un operador lineal con $\lambda_1, \dots, \lambda_m$  autovalores distintos entre sí. Sean $v_1, \dots, v_m$ son sus correspondientes autovectores y por la proposición son LI, entonces por la proposición 1 de [[Independencia Lineal]] tenemos que $m \leq \dim V$. $\blacksquare$ 

Un resultado muy interesante que podemos probar es **la existencia de los autovalores en $\mathbb{C}$**. Resulta, que al calcular los autovalores siempre tengo que encontrar las raíces de un polinomio, como hicimos en el ejemplo 2. Ahora, no siempre existen soluciones para estos polinomios en $\mathbb{R}$ pero podemos estar seguros de que existe al menos una solución en $\mathbb{C}$ gracias al [[Teorema Fundamental del Álgebra]]. Este teorema, plantea justamente que todo polinomio de grado $m$ en los complejos tiene como máximo $m$ raíces. 

## Diagonalización
Uno de los principales objetivos del Álgebra 2 es mostrar que dado un operador $T: V \rightarrow V$, existe una base de $V$ con respecto a la cual $T$ tiene una matriz razonablemente simple. Esto es porque si bien las [[Matrices de Transformaciones Lineales]] nos simplificaron bastante el entendimiento de las transformaciones lineales, algunas matrices siguen siendo muy complicadas de operar (sobre todo si tienen muchas filas y columnas). Pero vamos a ver que si encontramos la base correcta para expresar la matriz, podemos hacerla mucho más simple, tal que obtener información de ella sea muy simple. 
Notemos que la forma de matriz más simple, es claramente una matriz diagonal. 

> [!Matriz diagonal]
> #Definición La matriz _diagonal_ es una matriz cuadrada $n \times n$ tal que las entradas en la diagonal principal sean las únicas no nulas, es decir $a_{ii} \neq 0, \forall i = 1, \dots, n$ pero $a_{ij} = 0$ para $i \neq j$. 

Empecemos ahora nuestro intento para encontrar una forma de encontrar una base tal que al expresar $[T]_B$ sea una matriz diagonal. Empecemos definiendo lo siguiente. 

> [!Matrices semejantes]
> #Definición Dadas $A, B \in M_{n \times n}(\mathbb{K})$ se dicen semejantes y se denota $A \sim B$ si $\exists C \in GL(n, \mathbb{K})$ (el conjunto de [[Matrices Invertibles]]) tal que $B = CAC^{-1}$

Esta definición tiene sentido, pues multiplicar de ambos lados a una matriz por matrices invertibles no modifica su rango, por lo visto en [[Cambio de Base y Rango de una matriz]]. Se puede probar que la relación semejanza de matrices $\sim$ es una relación de equivalencia ([[Relaciones entre conjuntos]]). Esta definición viene de expresar a un mismo operador en diferentes bases, al hacerlo no modifico la dimensión de la imagen, ni la del núcleo. Entonces, esto motiva la siguiente prueba

> [!Proposición 3. Matrices semejantes son un mismo operador en diferentes bases]
> Sean $A, B \in M_{n \times n}(\mathbb{K})$. Tenemos que $A \sim B$ si y sólo si existe un único operador lineal $T: \mathbb{K}^n \rightarrow \mathbb{K}^n$ con bases $B_1, B_2$ de $\mathbb{K}^n$ tal que $[T]_{B_1} = A$ y $[T]_{B_2} = B$.

**Demostración.** ($\Leftarrow$) Usando la proposición 2 de [[Cambio de Base y Rango de una matriz]] para pasar de la matriz transformación $[T]_{B_1}$ a la matriz $[T]_{B_2}$ usamos la matriz cambio de base $C(B_1,B_2)$ tal que $[T]_{B_2} = C(B_1, B_2)[T]_{B_1}C^{-1}(B_1,B_2)$. Eligiendo $C= C(B_1,B_2)$ y sabiendo que $A = [T]_{B_1}$ y $B= [T]_{B_2}$ entonces $B = CAC^{-1}$. 
($\Rightarrow$) Supongamos existe una matriz $C$ tal que $B = CAC^{-1}$ tomando $B_1 = E$ (la base canónica) y $B_2$ como las columnas de la matriz $C$, tenemos que $C = C(B_1, B_2)$ es la matriz cambio de base. Definimos $T: \mathbb{K}^n \rightarrow \mathbb{K}^n, \; T(v) = Av$, entonces veamos luego que la matriz asociada a la TL en la base canónica es $A = [T]_{B_1}$, luego la matriz $B$ por la proposición 2 de [[Cambio de Base y Rango de una matriz]] es igual a la matriz $[T]_{B_2}$ tal que $[T]_{B_2} = C(B_1, B_2)[T]_{B_1} C^{-1}(B_1, B_2)$. $\blacksquare$ 




[^1]: En particular, desde ahora en adelante trabajaremos con  $\mathbb{K} = \mathbb{R}$ y $\mathbb{K} = \mathbb{C}$. 

