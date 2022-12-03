La primera aplicación del axioma de la completitud es un resultado que puede parecer más una forma más natural de expresar matemáticamente que la recta real **no contiene ningún espacio libre**. 

> **Teorema. (Intervalos anillados)** Para cada $n \in \mathbb{N}$, asumamos que nos dan un intervalo cerrado $I_n = [a_n,b_n] = \{x  \in \mathbb{R} : a_n \leq x \leq b_n\}$ (siendo $a_n$ y $b_n$ [[Sucesión]]) Asumamos también que cada $I_n$ también contiene $I_{n+1}$. Entonces, la resultante sucesión anillada de intervalos cerrados$$I_1 \supseteq I_2 \supseteq I_3 \subseteq \cdots$$ nunca tiene intersección nula: eso es $\bigcap_{n=1}^{\infty} I_n \neq \emptyset$. 

## Densidad de $\mathbb{Q}$ en $\mathbb{R}$ 
Resulta que gracias al axioma 13 en cualquier intervalo abierto $(a,b)$ podemos encontrar por lo menos ún número racional, lo cual es obvio. Esta propiedad que tienen los racionales de estar en todos los intervalos de $\mathbb{R}$ se llama **densidad**. 
> #Definición **(Densidad en R)** Un conjunto $A \subset \mathbb{R}$ no vacío, es **denso** en [[R]] si $\forall r, s \in \mathbb{R}$, $r < s$, existe $a \in A$ tal que $r < a < s$. Equivalentemente a decir esto es que cualquier intervalo abierto $(r, s) \subset \mathbb{R}$ tiene intersección no vacía con $A$: $A \cap (r, s) \neq \emptyset$.

> **Teorema.**  $\mathbb{Q}$ es denso en $\mathbb{R}$.

