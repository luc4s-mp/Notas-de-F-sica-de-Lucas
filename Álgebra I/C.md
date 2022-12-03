# Números Complejos
En [[R]] vimos que existen algunas ecuaciones simples que no se pueden resolver en los números reales. Vemos que como para un $a \in \mathbb{R}, \; a \cdot a = (-a) \cdot (-a)$, y $a^2 > 0$ para $a>0$, se sigue que si $a \neq 0 \Rightarrow a^2 > 0, \forall \; a \in \mathbb{R}$. Entonces, como $1 > 0$, $-1 < 0$. Por lo tanto, $x^2 = -1$ no tiene soluciones en $\mathbb{R}$. Creemos un sistema númerico nuevo en donde existan soluciones para esta ecuación. 
El problema de resolver $x^2 = -1$ debería recordarnos a nuestro intento de resolver $x^2 =2$ que vimos en [[R]].  Entonces continuemos de la misma manera. Asumamos que existe un conjunto $C$ con las operaciones $+_C$ y $\cdot_C$  que tiene que cumplir con lo siguiente:
1. $\mathbb{R} \subseteq C$ y sus operaciones $+$ y $\cdot$ son intercambiables.
2. $x^2 = -1$ tiene solución en $C$. 
3. Las propiedades conmutativas, asociativas, y distributivas se mantienen en $+_C$ y $\cdot_C$ 
Sea $\Delta$ el elemento de $C$ que cumple $\Delta^2 = -1$. Entonces, por lo que vimos en [[R]], todos los elementos de este nuevo sistema tienen la forma $a +_C (b \cdot_C \Delta)$ para todo $a, b \in \mathbb{R}$. Es más para cada $a, b, c,d \in \mathbb{R}$ 
$$\begin{align}
(a+b\Delta) \cdot_C (c+d\Delta) & = (ac+ \Delta^2bd)+(ad+cd)\Delta \\
& = (ac-bd) + (ad+cb)\Delta, \quad \text{ pues } \Delta^2 = -1
\end{align}$$
Es decir la múltiplicación es una **operación cerrada** (nos da otro elemento del conjunto) en $C$. Podemos ver que lo mismo sucede para la operación suma. 
Dado un conjunto con pares ordenados de números reales $S = \{(a,b) : a,b \in \mathbb{R}\}$. Entonces, para cada elemento de $S$ debe haber un elemento del número sistema, y el nuevo sistema debe contener a $\mathbb{R}$. Definamos una función inyectiva $i$ tal que "mapee"  entre dos elementos de $a,b \in \mathbb{R}$  definida como $i(a,0) = a$ y $i(a,b) = (a,b) \in \mathbb{R}$ para obtener un elemento de este sistema nuevo que queremos crear. Sea $C_1$ un nuevo conjunto tal que
$$C_1 = \{i(a,b):a,b \in \mathbb{R}\}$$
Notemos que si $b=0$ entonces $i(a,0) = a$ o sea que este conjunto contiene a todos los números reales. En este conjunto estan definidas las operaciones $+_{C_1}$ y $\cdot_{C_1}$ tal que
$$\begin{align}
i(a,b) +_{C_1} i(c,d) & = i(a+c,b+d) \\
i(a,b) \cdot_{C_1} i(c,d) & = i(ac-bd, ad+cb) 
\end{align}$$
Ahora, veamos que en este conjunto si existe una solución para $x^2 = -1$. Sea $i(a,b)$ una solución de la ecuación tal que
$$i(a,b) \cdot_{C_1} i(a,b) = i(a^2-b^2, 2ab) = i(-1, 0)$$
Entonces, tiene que ocurrir que $a^2-b^2 = -1$ y que $2ab = 0$ por la definición de la función $i$. Por lo tanto, $a=0$ o $b=0$. Veamos que si $b=0$ nos queda que $a^2 = -1$ lo cual no puede ocurrir para ningún número real, tiene que ocurrir entonces $a =0$. Si $a=0$, nos queda $b^2 =1$ lo cual nos da como solución que $b=-1$ o $b= +1$. Pruebe usted mismo que $(i(0,1))^2 = i(-1,0)$ y $(i(0,-1))^2 = i(-1,0)$.
Podemos ver que si $i(a,b)= i(a,0) + i(0,b)$ y $i(0,b) = i(b,0) \cdot i(0,1)$ entonces nos queda que $i(a,b) = i(a,0) + i(b,0) \cdot i(1,0)$. Luego, $i(a,0) = a$ y $i(b,0) = b$ por lo cual nos queda que todo elemento de $C_1$ puede ser expresado como 
$$i(a,b) = a+b \cdot i(0,1)$$
Llamaremos simplemente a $i(0,1) = i$ o también como la "unidad imaginaria". De esta manera podemos definir a los complejos. 

> #Definición A partir de lo visto en [[Conjuntos]] podemos definir a los **números complejos** como un conjunto $\mathbb{C} = \{a+bi : a,b \in \mathbb{R}\}$ donde $i$ es llamada "unidad imaginaria" tal que resuelve la ecuación $i^2=-1$. El número real $a$ es llamado "parte real" y de denota $a = \mathrm{Re}(z)$ donde $z \in \mathbb{C}$  y el número real $b$ es llamado "parte imaginaria" y se denota $b= \mathrm{Im}(z)$.  
- $(\cdot): (i, i) \rightarrow -1$ (definición del producto de $i$ por $i$)
- $(\cdot): (0, i) \rightarrow 0$ (0 es el neutro $\mathbb{R}$)
- $(+): (0,i) \rightarrow i$ (0 es el neutro)
- $(\cdot): (1,i) \rightarrow i$ (1 queremos que siga siendo identidad del producto)
- $b \in \mathbb{R}, \; (\cdot):(b, i) \rightarrow bi$
La asignación del producto de $b$ e $i$, $b \in \mathbb{R}$ no produce que $bi \in \mathbb{R}$. 
- $a,\; b \in \mathbb{R}, \; (+): (a, bi) \rightarrow a+bi$


## El cuerpo de los números complejos
$(\mathbb{C}, +, \cdot)$ es un cuerpo (vimos la definición en [[Enteros Modulares]]). Esto es verdadero debido a que la operación $+$ es conmutativa y es asociativa, la operacpues lo es sobre los números reales. Además $0 = 0 + 0 \cdot i \mathbb{C}$ es el elemento neutro para la suma, y el opuesto aditivo de $z = a + bi$ sería $-z = -a -bi$.
También se puede comprobar que en $\mathbb{C}$ la operación $\cdot$ es conmutativa y asociativa. El elemento $1 = 1 + 0i$, es el elemento neutro o identidad del producto y para todo $z = a + bi$ se tiene que existe 
$$z^{-1} = \frac{a}{a^2 + b^2} - \frac{b}{a^2 + b^2} \cdot i \in \mathbb{C}$$
que es el inverso multiplicativo de $z$. Se puede verificar con facilidad $z \cdot z^{-1} = 1$.
No existe forma de comprobar que $\mathbb{C}$ se pueda definir para que se extendienda el orden de $\mathbb{R}$ con todas sus propiedades. Esto es porque, por ejemplo (propiedad de tricotromía vista en [[R]]) $i \nless 0$, ni $i \ngtr 0$, ni $i \neq 0$.

---

## Definiciones
Si $z \in \mathbb{Z} \implies z = a+bi, \; a,b \in \mathbb{R}$:
1. $a$ se denomina **parte real** y $b$ se denomina **parte imaginaria** de $z$, $a = Re(z)$ y $b = Im(z)$.
2. La forma de ordenar $Re(z) + Im(z)i$ de ordenar los números se llama **forma binomial**.
3. Se denomina **conjugado de z** al nro complejo $\bar{z} = a-bi$.
4. Se denomina **valor absoluto o módulo** de $z$ al número real:
	$$|z| = \sqrt{a^2 + b^2}$$
Observaciones: $|z|= 0$ si y sólo si $z = 0$, y $|z| = \sqrt{z \cdot \bar{z}}$ y $z^{-1} = \frac{\bar{z}}{|z|^2}$.

---

### Propiedades
> Sean $z, w \in \mathbb{C}$. Entonces se cumple que
> 1. $\bar{\bar{z}} = z$
> 2. $\overline{(z+w)} = \bar{z} + \bar{w}$
> 3. $\overline{(z \cdot w)} = \bar{z} \cdot \bar{w}$
> 4. $|zw| = |z| \cdot |w|$
> 5. $z = \bar{z}$
> 6. $z + \bar{z} = 2Re(z)$ y $z - \bar{z} = 2Im(z)$
> 7. $|Re(z)| \leq |z|$ y $|Im(z)| \leq |z|$ 
> 8. $|z+w| \leq |z|+|w|$
> 9. $||z|-|w|| \leq |z-w|$


---

Existen otras formas de escribir un número complejo como la [[Forma Trigonométrica o polar de C]].


#Matemática #Primer-año 