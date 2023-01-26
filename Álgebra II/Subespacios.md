# Subespacios 
Dentro de un $\mathbb{K}$-espacio vectorial ([[Espacios Vectoriales]]) $V$, hay subconjuntos del mismo que heredan la estructura de $V$, es decir, que también son espacios vectoriales con la misma operación, el mismo elemento neutro y la misma acción en $V$. Por ejemplo, tomando $V = \mathbb{R}^2$ tenemos que este es un plano, veamos que el subconjunto $W = \{(2x, -x): x \in \mathbb{R}\}$ es también un espacio vectorial, y es más forma una recta que pasa por el $(0,0)$ (notemos que si no lo hiciera no podría ser un espacio vectorial pues sí o sí tiene que tener un elemento neutro):
![[Pasted image 20230103092259.png | 400]]
Veamos que viéndolo de otra manera podemos reescribir el conjunto como $W = \{x(2,-1): x \in \mathbb{R}\}$ tal que todos los puntos de la recta son "generados" por multiplicar por un escalar al vector $(-2,1)$. Entonces, a estos espacios vectoriales que están dentro de otros los llamamos **subespacios vectoriales**.

> [!Subespacios Vectoriales]
> #Definición Sea $V$ un $\mathbb{K}$- espacio vectorial. Un subconjunto $S \subseteq V$ no vacío se dice _subespacio de $V$_ si la suma y el producto por escalares  son una operación y una acción en $S$ que lo convierten en un $\mathbb{K}$-espacio vectorial. 

Un ejemplo obvio de un subespacio vectorial de $\mathbb{R}^2$ por ejemplo es $S = \{(0,0)\}$ (lo puede comprobar por usted mismo probando las propiedades de espacio vectorial que tienen que cumplir la operación y la acción, note que es muy parecido a probar que $\{0\}$ es un espacio vectorial). Y también, por lo que vimos en nuestro ejemplo inicial, si $S$ tiene un elemento $v$ no nulo tal que para todo $\lambda \in \mathbb{R}, \;\lambda \cdot v \in S$ y estos son todos los elementos de $S$ entonces $S$ es un subespacio (que gráficamente es una recta que pasa por el origen).

Si realizó el mismo proceso que usábamos para determinar que $V$ es un espacio vectorial, notará que este proceso se vuelve tedioso al repetirlo con los subespacios. Existe un método más sencillo, gracias a que sabemos que estamos dentro de un espacio vectorial donde se cumplen las propiedades, resulta que solo basta con saber que $0 \in S$, $v,w \in S \Rightarrow v+w \in S$ y $\lambda \in \mathbb{K}, \; v \in S \Rightarrow \lambda v \in S$ (esta dos últimas quieren significar que las operaciones de suma y multiplicación por un escalar son cerradas). 

> [!Proposición 1.]
> Sea $V$ un $\mathbb{K}$ espacio vectorial y sea $S \subseteq V$. Entonces $S$ es un subespacio de $V$ si y sólo si valen las siguiente condiciones:
> 1. $0 \in S$ 
> 2. $v,w \in S \implies v+w \in S$ 
> 3. $\lambda \in \mathbb{K}, \; v \in S \implies \lambda \cdot v \in S$

**Demostración.** 
- ($\Rightarrow$) Si $S$ es un subespacio es obvio que se tiene que cumplir (1), (2) y (3). 
- ($\Leftarrow$ ) La condición (1) nos asegura que $S$ es no vacío, por las condiciones (2) y (3) tenemos que la suma $+$ y la multiplicación escalar $\cdot$ están bien definidas en $S$. Veamos que un espacio vectorial:
	- Probemos primero las propiedades que tiene que cumplir la suma, como $v+w \in S \subseteq V$ entonces la conmutatividad y la asociatividad en $S$ son validas gracias a que ocurren dentro de $V$ y por la condición (1) $0 \in S$ tiene neutro, por último existen los inversos aditivos gracias a que $-1 \in \mathbb{K}$ y por la condición (3) tenemos que si $v \in S, \; (-1)v \in S \implies -v \in S$.
	- Las 4 propiedades que tiene que cumplir la acción $\cdot$ salen también gracias a que valen en $V$, por ejemplo la 1era es verdad pues $v+w \in S$ por (2) y luego por (3) tenemos que $a(v+w) \in S$, siguiendo sabemos que $av \in S$ y $aw \in S$ por (3) por lo tanto por (2) tenemos que $av+aw \in S$ entonces se cumple $a(v+w) = av+aw$. $\blacksquare$  

Algunos ejemplos de subespacio vectorial:
1. $\{0\}$ es un subespacio de $V$.
2. $V$ es un subespacio de $V$.
3. Si $v \in V$, $S = \{\lambda v / \lambda \in \mathbb{K}\}$ es un subespacio de $V$ pues por la Prop.(1):
	1. $0 = 0 \cdot v \in S$ 
	2. Si $\lambda v \in S, \; \mu v \in S$ entonces $\lambda v + \mu v = (\lambda + \mu)v \in S$. 
	3. Si $\lambda v \in S$ y $\alpha \in \mathbb{K}$ entonces $\alpha (\lambda v) = (\alpha \lambda) \cdot v \in S$. 
Este ejemplo es muy interesante pues nos hace preguntarnos _¿Podemos combinar una cierta cantidad de vectores cualquiera que pertenezcan a $V$ y formar un subespacio con ellos multiplicándolos por escalares y sumándolos?_ La respuesta es sí y lo probaremos en el siguiente ejemplo:
4. Si $v_1, \dots, v_n \in V$ entonces $S = \{\alpha_1 v_1 + \alpha_2 v_2 + \cdots + \alpha_n v_n : \alpha_i \in \mathbb{K}, \; 1 \leq i \leq n\}$ es un subespacio, pues 
	1. Eligiendo $\alpha_i = 0$ para todo $1 \leq i \leq n$ entonces $0v_1 + \cdots + 0v_n = 0 \in S$. 
	2. Si $\alpha_1 v_1 + \alpha_2 v_2 + \cdots + \alpha_n v_n \in S$ y $\beta_1 v_1 + \beta_2 v_2 + \cdots + \beta_n v_n \in S$ entonces $\alpha_1 v_1 + \alpha_2 v_2 + \cdots + \alpha_n v_n + \beta_1 v_1 + \beta_2 v_2 + \cdots + \beta_n v_n$ $= (\alpha_1 + \beta_1)v_1 + (\alpha_2 + \beta_2)v_2 + \cdots + (\alpha_n + \beta_n)v_n \in S$
	3. Si $\alpha_1 v_1 + \alpha_2 v_2 + \cdots + \alpha_n v_n \in S$ y $\lambda \in \mathbb{K}$ entonces $\lambda(\alpha_1 v_1 + \alpha_2 v_2 + \cdots + \alpha_n v_n) = (\lambda\alpha_1) v_1 + (\lambda\alpha_2) v_2 + \cdots + (\lambda \alpha_n) v_n \in S$. 
	En este caso se dice que los vectores $v_1, v_2, \dots, v_n$ _generan el subespacio S_ y se denota $S = <v_1, \cdots, v_n>$. 
5. Sean $a_1, \dots, a_n \in \mathbb{K}$ fijos. Sea $S = \{(x_1, \dots, x_n) \in \mathbb{K}^n : a_1 x_1 + \dots + a_n x_n = 0\}$ es fácil ver que es un subespacio de $\mathbb{K}^n$ 

Pasaremos a responder la siguiente pregunta _¿Es la intersección de subespacios un subespacio también? ¿Y la unión?_ 

> [!Proposición 2]
> Sea $V$ un $\mathbb{K}$-espacio vectorial y sean $W_1$ y $W_2$ dos subespacios tenemos que $W_1 \cap W_2$ es un subespacio de $V$.

**Demostración.** Usemos la proposición (1): 
1. $0 \in W_1 \cap W_2$ pues $0 \in W_1$ y $0 \in W_2$ 
2. Si $v,w \in W_1 \cap W_2$ entonces $v,w \in W_1$ y $v, w \in W_2$ luego como $W_1$ es un subespacio entonces $v+w \in W_1$ lo mismo para $v+w \in W_2$ luego $v+w \in W_1 \cap W_2$.
3. Si $v \in W_1 \cap W_2$ y $\lambda \in \mathbb{K}$ entonces $v \in W_1$ y $v \in W_2$ luego como ambos son subespacios tenemos que $\lambda v \in W_1$ y $\lambda v \in W_2$, por lo tanto $\lambda v \in W_1 \cap W_2$. $\blacksquare$ 

Entonces, acabamos de probar que la intersección de subespacios de $V$ nos da otro subespacio. Sin embargo, __la unión de subespacios no necesariamente es subespacio__. Por ejemplo, supongamos que tenemos el espacio vectorial $\mathbb{R}^2$ y los subespacios $S = <(0,1)>$ y $T = < (1,0) >$ [^1], tenemos que $S \cup T$ no es un subespacio pues por la condición (2) en la proposición 1 debería cumplirse que si $v,w \in S \cup T \implies v+w \in S \cup T$, luego $(0,1) \in S$ y $(1,0) \in T$ pero $(1,0) + (0,1) = (1,1) \notin S \cup T$ se puede observar claramente porque este vector no está en el conjunto graficando en un plano $S$ y $T$.  

Otros ejemplos interesantes de subespacios salen de analizar el espacio vectorial de funciones (visto en [[Espacios Vectoriales]]) $\mathbb{K}^S$. Notemos que en $\mathbb{R}^{[0,1]}$ podemos decir que el conjunto de todas las funciones continuas ([[Continuidad]]) $W = \{f : [0,1] \rightarrow \mathbb{R} / f \text{ continua }\}$ son un subconjunto del mismo, pero ¿Es un subespacio? 
- Veamos que $0(x) = 0$ es el elemento neutro del espacio vectorial y es una función continua por lo tanto $0 \in W$. 
- Si $f \in W$ y $g \in W$ tenemos que $(f+g)(x) = f(x) + g(x)$ por un teorema visto en continuidad la suma de funciones continuas nos da otra función continua, entonces $f+g \in W$. 
- Por último, si $f \in W$ y $\lambda \in \mathbb{R}$ entonces $(\lambda f)(x) = \lambda f(x)$ y sabemos que esta función es continua también, por lo tanto $\lambda f \in W$. 

Tenemos entonces que $W$ si es un subespacio de $\mathbb{R}^{[0,1]}$. 
Podemos comprobar que $\{f: [0,1] \rightarrow \mathbb{R} / f'(x) \text{ exista }\}$ y $\{f:[0,1] \rightarrow \mathbb{R} / \int_0^1 f(x)dx \text{ exista }\}$ son subespacios vectoriales de $\mathbb{R}^{[0,1]}$ también. 


[^1]: Recordemos que esta notación quiere significar que son los subespacios generados por esos vectores entre los símbolos $<>$, es decir son todos los vectores que resultan de multiplicar a estos por cualquier escalar. 