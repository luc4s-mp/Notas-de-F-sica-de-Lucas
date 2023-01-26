# Dimensión de un espacio vectorial

La siguiente proposición trata sobre la dimensión, ya definida en [[Bases Vectoriales]], como el módulo del conjunto de vectores den la base del espacio vectorial, tenemos ahora una proposición que habla sobre la dimensión de los [[Subespacios]] de $V$.

> [!Proposición 1.] 
> Sean $S$ y $T$ subespacios de un $\mathbb{K}$-espacio vectorial ([[Espacios Vectoriales]]) $V$ de dimensión finita. Entonces: 
> 1. $S \subseteq T \implies \dim S \leq \dim T$
> 2. $S \subseteq T$ y $\dim S = \dim T \implies S = T$.

**Demostración.** 
1. Sea $\{s_1, \dots, s_r\}$ una base de $S$ , $\dim T = n$ y $\dim S = r$. Como $S \subseteq T$, tengo entonces que $\{s_1, \dots, s_r\} \subseteq T$, y es un conjunto LI. Luego, por la proposición 4 en [[Bases Vectoriales]], tenemos que la base de $S$ puede ser extendida a una base de $T$, y en consecuencia, $r \leq n$. 
2. Siguiendo el razonamiento de (1), al extender la base de $\{s_1,\dots, s_r\}$ como $n = r$ entonces no se agrega ningún vector y $S = <s_1, \dots, s_r> = T$. $\blacksquare$ 

El ítem (2) de la proposición anterior es muy útil para facilitar la verificación de la igual de dos subespacios. 
Por ejemplo, sean $S$ y $T$ dos subespacios de $\mathbb{R}^3$ definidos como $S = <(1,-k^2+1,2), (k+1, 1-k,-2)>$ y $T = \{x \in \mathbb{R}^3 : x_1+x_2+x_3\}$. Nos piden hallar los valores de $k$ para los cuales $S=T$. Probemos inicialmente que $S \subseteq T$ usando la proposición 1 de [[Independencia Lineal]], que nos dice que $S$ es el subespacio más chico que contiene a $(1,-k^2+1,2)$ y $(k+1,1-k,-2)$ entonces si $(1,-k^2+1,2) \in T$ y $(k+1,1-k,2) \in T$ se cumple $S \subset T$, notemos que esto ocurre cuento $k = \pm 2$. Luego, usando la proposición anterior para probar $S=T$ solo basta con ver $\dim S = \dim T$ lo cual se puede hacer simplemente reemplazando los posibles valores de $k$ obtenidos. Si $k = -2$ entonces $S = <(1,-3,2)>$, $\dim S =1$, y si $k = 2$ tenemos que $S = <(1,-3,2),(-1,3,-2)>$, $\dim S = 2$. Concluimos entonces que $S=T$ si y solo si $k=2$. 

Para probar que una lista de vectores en $V$ es una base en $V$, debe satisfacer ser LI y debe ser un sistema de generadores de $V$. La siguiente proposición demuestra que si la lista en cuestión tiene el largo correcto, entonces solo necesitamos chequear una de las 2 propiedades requeridas.

> [!Proposición 2.]
> Supongamos que $V$ es un $\mathbb{K}$-espacio vectorial de dimensión finita.
> 1. Toda lista de vectores LI en $V$ con un módulo $\dim V$ es una base de $V$.
> 2. Toda lista de vectores que es un sistema de generadores de $V$ con módulo $\dim V$ es una base de $V$. 

**Demostración.** (1) Supongamos $\dim V = n$ y $v_1,\dots, v_n$ es linealmente independiente en $V$. La lista $v_1, \dots, v_n$ puede ser extendida a una base de $V$ por la proposición 3 de [[Bases Vectoriales]]. Pero, cada base de $V$ tiene largo $n$, por lo tanto la extensión en este caso es la trivial, es decir no se agregan elementos a $v_1, \dots, v_n$. En otras palabras, $v_1, \dots, v_n$ es una base. 
(2) La lista de vectores $v_1, \dots, v_n$ que genera a $V$ puede ser reducida a una base por la proposición 4 de [[Bases Vectoriales]]. Pero por la misma razón que (1), no es necesario reducirla, por lo tanto $v_1, \dots, v_n$ es una base. $\blacksquare$ 

Un gran error que se suele cometer, es que como $\mathbb{R}^2$ tiene dimensión 2, se puede llegar a que $\mathbb{C}$ también tiene dimensión 2. Esto sería un error, que viene de que como conjuntos $\mathbb{R}^2$ puede ser identificado con $\mathbb{C}$. Sin embargo, _la dimensión de $\mathbb{C}$ es 1_. Por lo tanto, cuando hablamos de la dimensión de un espacio vectorial, la elección del cuerpo $\mathbb{K}$ no afecta a la dimensión. 

### Ejemplo. Bases de funciones polinómicas
Un ejemplo claro de una aplicación de la proposición 2 es probar que $1, (x-5)^2, (x-5)^3$ es una base del subespacio $U = \{p \in \mathbb{R}_3[x]: p'(5) = 0\}$ de $\mathbb{R}_3[x]$. Claramente cada uno de los polinomios $1 \in U$, $(x-5)^2 \in U$ y $(x-5)^3 \in U$, por lo que por la proposición 1 en [[Independencia Lineal]], tenemos que $<1, (x-5)^2, (x-5)^3> \subseteq U$. 
Luego, $a + b(x-5)^2 + c(x-5)^3 = 0$ para todo $x \in \mathbb{R}$. Es claro que sin necesidad de expandir el lado izquierdo de la ecuación que $a = b = c = 0$, entonces la lista de vectores es LI. 
Notemos que $\dim U \geq 3$  por la proposición (1.1). Como $U$ es un subespacio de $\mathbb{R}_3[x]$, tenemos que $\dim U \leq \dim \mathbb{R}_3[x] = 4$. No obstante no puede ocurrir que $\dim U = 4$ pues sino $U = \mathbb{R}_3[x]$ lo cual no es verdad pues por ejemplo $(x-5) \notin U$. Entonces $\dim U =3$ y esto implica que la lista LI $1, (x-5)^2, (x-5)^3$ es una base de $U$. 

## Aplicaciones de las bases y el concepto de dimensión
Se puede generalizar la dimensión del subespacio de soluciones de un sistema homogéneo, del trabajo que hicimos en [[Cantidad de soluciones de un SEL]]. 
> [!Teorema 3.]
> Dado un sistema de ecuaciones $A\vec{x} = \vec{0}$, $A \in M_{n \times n}(\mathbb{K})$ ([[Matrices]]) el subespacio $S \subseteq \mathbb{K}^n$ de soluciones tiene dimensión $n-r$ donde $r$ es la cantidad de pivotes de la matriz reducida.

**Demostración.** Se sigue de pensar que la matriz $A$ al reducirla por filas tenemos que puede tener filas nulas, lo cual nos daría un sistema equivalente con más incógnitas que ecuaciones y por el Teorema 1 visto en [[Cantidad de soluciones de un SEL]] existen soluciones no nulas. 
Ahora, las variables que tienen un pivote $1$ son las variables dependientes de otras, entonces si $r$ es la cantidad de pivotes que hay (hay $r$ variables dependientes) y hay $n$ incógnitas en total, tenemos entonces que hay $n-r$ variables independientes. Las variables independientes (o libres) al reordenarlas en vectores nos quedan $x_i(\times, \times,  \cdots, \times) + \cdots + x_j(\times, \times, \cdots, \times)$ tal que el conjunto de soluciones es generado por $n-r$ vectores. Luego, $\dim(S) = n-r$. $\blacksquare$

### Ejemplo. Bases Infinitas.
Resulta que nuestra definición de Base (vista en [[Bases Vectoriales]]) no especifica nada acerca de que solos los espacios vectoriales de dimensión finita pueden tener bases. 

Demos ahora un ejemplo de una base infinita. Sea $\mathbb{K}$ un subcuerpo de los número complejos [[C]], y sea $\mathbb{K}[x]$ el espacio de funciones polinomiales de $\mathbb{K}$ a $\mathbb{K}$. Ahora es obvio que si consideramos $f_k(x) = x^k, \; k = 0, 1, 2, \dots$ entonces veamos que el conjunto infinito $\{f_0, f_1, f_2, \dots\}$ es una base para $\mathbb{K}[x]$. Claramente el conjunto es un sistema de generadores de $V$. Para ver que el conjunto es LI lo más normal en estos casos es _probar que cada subconjunto finito es LI_. Es suficiente con probar que, para cada $n$, el conjunto $\{f_0, \dots, f_n\}$ es LI. Supongamos que 
$$c_0f_0 + \cdots + c_nf_n = 0$$
es lo mismo que $$c_0 + c_1x + \cdots + c_nx^n = 0$$
para todo $x \in \mathbb{K}$, en otras palabras, cada $x \in \mathbb{K}$ es una raíz del polinomio $f(x) = c_0 + c_1x + \dots + c_nx^n$. Por el [[Teorema Fundamental del Álgebra]] sabemos que un polinomio con grado $n$ (en los complejos) no puede tener más de $n$ raíces. Entonces, se sigue que $c_0 = c_1 = \dots = c_n = 0$. 
