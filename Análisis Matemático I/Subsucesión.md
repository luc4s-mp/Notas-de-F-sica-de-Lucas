# Subsucesiones
Por lo que vimos en [[Sucesión]] podemos probar que una sucesión **converge** a un número $l$ probando que dado un intervalo cualquiera alrededor de $l$ de largo $\epsilon > 0$  existe un $N \in \mathbb{N}$ a partir del cual todos los elementos que siguen de la sucesión a ese $N$ pertenecen al intervalo. Ya vimos que para encontrar si una sucesión es divergente tendríamos que negar la definición de convergencia, lo cual nos quedaría:
$$\exists \; \epsilon > 0 : \forall \; N \in \mathbb{N}, \exists \; n > N :  |a_n - l| \geq \epsilon$$
Sin embargo, encontrar que una sucesión diverge usando esta definición puede ser muy complicado y largo. Supongamos que queremos ver que la sucesión $a_n = (-1)^n$ **diverge** (es obvio que lo hace pues sus valores van alternando de $1$ a $-1$ y no se acercan a ningún número en particular). 
![[Pasted image 20220806102041.png]]

Supongamos por el absurdo que existe un límite, tomemos cualquier número real, por ejemplo $l = 1$.  Debe existir un **al menos un** intervalo alrededor de $l$, $(1-\epsilon, 1+\epsilon)$ para el cual cualquier $N \in \mathbb{N}$ que tomemos como el "inicio de nuestra cola" a partir del cual todos los valores que son mayores entran en ese intervalo, debe existir un $a_n$ con $n \geq N$ que no pertenece al intervalo. Esto debe ocurrir **para todo** $l$ que tomemos. 
Podrá ver porque es difícil encontrar que una sucesión diverge por definición, justamente tenemos que encontrar lo de arriba para todo  $l \in \mathbb{R}$ y eso puede ser complicado de lograr.

En esta nota presentaremos un concepto nuevo llamado **subsucesión** que nos ayudará a demostrar que una sucesión diverge.

---
 Para tener una **subsucesión** de $\{a_n\}$ definida en [[R]] se debe cumplir la siguiente condición: elegimos infinitos puntos de la sucesión, llamamos a estos puntos $a_{n_1}, \; a_{n_2}, a_{n_3}, \dots,$ con la condiciòn que $n_1 < n_2 < n_3 < n_4 < \dots$. Entonces la nueva sucesión: $$\{a_{n_j}\} \;\;\;\;\; \text{ donde } \; j \in \mathbb{N}$$es una subsucesión de $\{a_n\}$.

> #Definición 


> **Lema.** Toda sucesión tiene una subsucesión creciente o una subsucesión decreciente.

**Demostración.** Sea $\{a_n\}$ una sucesión. En el caso que $\{a_n\}$ tenga infinitos *puntos cumbres*, entonces hay infinitos índices. Si $j_1 < j_2 < j_3 < j_4 < \dots$ son puntos cumbres, entonces $a_{j_1} < a_{j_2} < a_{j_3} < a_{j_4} < \dots$; por lo cual la subsucesión $a_{n_j}$ es decreciente y se cumple el lema.
Por otro lado, si $\{a_n\}$ tiene finitos puntos cumbres (o ninguno), elegimos el mayor de ellos, y sino hay ninguno elegimos $a_1$. Entonces tenemos un índice $j_1$ que no es un punto cumbre, entonces existe un $j_2$ tal que $j_2 > j_1$ y $a_{j_1} \leq a_{j_2}$. Luego, $j_2$ no es un punto cumbre, entonces tomamos $j_3$ tal que $j_3 > j_2$ y $a_{j_2} \leq a_{j_3}$. Siguiendo este razonamiento, conseguimos armar una subsucesión $a_{j_k}$ que cumple que $a_{j_k} \leq a_{j_{k+1}}$, lo cual es creciente. Esto completa la prueba del lema. $\blacksquare$

> **Teorema de Bolzano-Weistrass** Toda sucesión acotada tiene una subsucesión convergente.

**Demostración.** Por el Lema anterior, si una subsucesión es creciente o decreciente y a su vez está acotada, entonces es convergente por el teorema visto en [[Sucesión]]. 

> **Teorema.** Sea una subsucesión convergente de $\{a_n\}$, converge al mismo límite que $\{a_n\}$



>**Corolario (Criterio de Divergencia de Subsucesiones)** Si una sucesión posee dos subsucesiones que convergen a dos límites distintos, entonces la sucesión original es divergente.

---

## Definición
Sea $\{a_n\}$ una sucesión, diremos que es una **sucesión de Cauchy** si: para todo $\epsilon > 0$ existe $N \in \mathbb{N}$ tales que $|a_n - a_m| < \epsilon$ para cada par $n, m \in \mathbb{N}$. Es decir, una sucesión es convergente si y solo si es de Cauchy.

