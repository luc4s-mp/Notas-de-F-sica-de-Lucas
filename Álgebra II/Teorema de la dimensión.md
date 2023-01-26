# Teorema de la dimensión
Ya entendimos bastante respecto a las [[Transformaciones Lineales]] en relación con dos subespacios muy importantes que son [[La Imagen y el Núcleo de una TL]]. Aprendimos que cuando $\mathrm{Nu}(T) = \{0\}$ la transformación es un monomorfismo (es decir, inyectiva). 

Notemos que realizando un análisis de la dimensión de los subespacios núcleo, imagen y el espacio de salida $V$, podemos entender bastante sobre la transformación. En el corolario 2.1 de [[La Imagen y el Núcleo de una TL]] concluimos que $\dim V \geq \dim (\mathrm{Im}(T))$, pero luego en el corolario 3.1 concluimos que cuando $T$ es un monomorfismo tenemos que $\dim V = \dim (\mathrm{Im}(T))$. Por lo tanto, tenemos que la dimensión de la imagen y el espacio de salida son iguales cuando $\mathrm{Nu}(T) = \{0\}$ pero a su vez esto quiere significar que la dimensión del núcleo es 0. Mientras que generalmente cuando la dimensión del núcleo puede ser más grande tenemos que $\dim V \geq \dim (\mathrm{Im}(T))$. Puede usted mismo notar que la dimensión de estos tres espacios se encuentran relacionadas entre sí, y encontrar esa relación nos puede llevar a obtener resultados muy interesantes. 

Ahora estamos listos para demostrar el teorema de la dimensión.

> [!Teorema de la dimensión.]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales, $V$ de dimensión finita, y sea $T: V \rightarrow W$ una transformación lineal. Entonces,
> $$\dim V = \dim(\mathrm{Nu}(T)) + \dim(\mathrm{Im}(T))$$

**Demostración.** Sean $n = \dim V$ y $r = \dim (\mathrm{Nu}(T))$. Si $r=n$, entonces $T \equiv 0$ pues $\dim(\mathrm{Im}(T)) = 0$. Si $r=0$, entonces $T$ es un monomofismo y ya probamos que en este caso $\dim(Im(T)) = n = \dim V$ y el teorema vale. 
Supongamos ahora que $0 < r < n$. Sea $\{v_1, \dots, v_n\}$ una base de $\mathrm{Nu}(T)$, como el núcleo es un subespacio de $V$, entonces $\{v_1, \dots, v_n\}$ es LI en $V$ y se puede extender a una base por la proposición 4 en [[Bases Vectoriales]]. Sean $v_{r+1}, \dots, v_n$ en $V$ tales que $\{v_1, \dots, v_r, v_{r+1}, \dots, v_n\}$ es una base de $V$, se tiene que por la proposición 2 en [[La Imagen y el Núcleo de una TL]]: 
$$\mathrm{Im}(T) = < T(v_1), \dots, T(v_r), T(v_{r+1}), \dots, T(v_{n})>$$
y como $T(v_i) = 0, \; 1 \leq i \leq r$ tenemos que $\mathrm{Im}(T) = <T(v_{r+1}), \dots, T(v_n)>$. Nos faltaría ver que el sistema de generadores de la imagen planteado, es linealmente independiente. 
Sean $\alpha_{r+1}, \dots, \alpha_n \in \mathbb{K}$ tales que $\sum_{i=r+1}^n \alpha_i T(v_i)= 0$. Entonces, $T\Big(\sum_{i={r+1}}^n \alpha_iv_i\Big) = 0$ por la 2da propiedad de las [[Transformaciones Lineales]]. Luego, $\sum_{i=r+1}^n \alpha_iv_i \in \mathrm{Nu}(T)$. Y como $\{v_1, \dots, v_r\}$ es una base del núcleo tenemos que 
$$\sum_{i= r+1}^n \alpha_i v_i = \sum_{i=1}^r \alpha_i v_i \iff \sum_{i= r+1}^n (-\alpha_i) v_i + \sum_{i=1}^r \alpha_i v_i = 0$$
Como $\{v_{r+1}, \dots, v_n\}$ es un conjunto LI en $V$ y $\{v_1, \dots, v_r\}$ también lo es tenemos que $\{v_1, \dots, v_n\}$ es LI, por lo tanto $\alpha_i = 0$ para cada $1 \leq i \leq n$. Luego, $\{T(v_{r+1}), \dots, T(v_n)\}$ es LI. Entonces, tenemos que $\mathrm{Im}(T) =n - r = \dim V - \dim (\mathrm{Nu}(T))$. $\blacksquare$ 

Usando este teorema se puede concluir que cuando una transformación lineal es un monomorfismo es un epimormismo y a su vez es un isomorfismo.

> [!Corolario 1.1]
> Sean $V$ y $W$ dos $\mathbb{K}$ espacios vectoriales de dimensión $n$, y $T: V \rightarrow W$ una transformación lineal. Son equivalentes:
> 1. $T$ es un monomorfismo.
> 2. $T$ es un epimorfismo.
> 3. $T$ es un isomorfismo.

Notemos que el teorema solo vale para transformaciones lineales de dimensión finita. No funciona para espacios vectoriales infinitos. Por ejemplo $T: \mathbb{K}[x] \rightarrow \mathbb{K}[x], \; T(P) = P'$ es un epimorfismo pues si $Q = \sum_{i=0}^n a_ix^i \in \mathbb{K}[x]$ entonces $T\Big(\sum_{i=1}^{n+1} \frac{a_i}{i} x^i\Big) = Q$, pero no es un monomorfismo pues los vectores contantes se dirigen todos al $0$ por lo tanto la dimensión del núcleo es 1.

A partir del Teorema de la dimensión se puede demostrar:

> [!Proposición 2.]
> **(NEF)** Sean $V$ y $W$ son dos $\mathbb{K}$-espacios vectoriales finitos, tenemos que:
> 1. Si $\dim V > \dim W$ no existe transformación lineal tal que vaya de $V$ a $W$ que sea un monomorfismo.
> 2. Si $\dim V < \dim W$ no existe una transformación lineal tal que vaya de $V$ a $W$ que sea un epimorfismo. 

**Demostración.** Sea $T : V \rightarrow W$ una transformación lineal.
1. Como, $\dim(\mathrm{Nu}(T)) = \dim V - \dim (\mathrm{Im}(T)) \geq \dim V - \dim W > 0$. Entonces no puede ser inyectiva (monomorfismo), a su vez esto quiere significar, que por el corolario 2.1, no puede existir un ismorfismo.
2.  Como, $\dim (\mathrm{Im}(T)) = \dim V - \dim (\mathrm{Nu}(T)) \leq \dim V < \dim W$. Entonces como $\dim (\mathrm{Im}(T)) < \dim W$ esto significa que no puede ser sobreyectiva (epimorfismo), a su vez esto quiere significar por el corolario 2.1 que no puede existir un isomorfismo. $\blacksquare$ 

Esta proposición nos da mucha información útil, con simplemente analizar la dimensión de los espacios vectoriales de salida y de llegada, ya podemos encontrar si _puede existir o no un isomorfismo_, sin embargo que $\dim V = \dim W$ **no me indica necesariamente que la transformación sea un isomorfismo**. Por ejemplo, $T(x,y,z) = (x,y,0)$ no es un isomorfismo a pesar de que la dimensión del conjunto de llegada sea el mismo que el de salida.  

Usando transformaciones lineales, se puede expresar de una nueva manera la demostración del teorema 1 en [[Cantidad de soluciones de un SEL]]. Supongamos que $a_{ij} \in \mathbb{K}$ para $i = 1, \dots, m$ y $j = 1, \dots, n$. Consideremos el siguiente sistema homogéneo de $m$ ecuaciones y $n$ incógnitas:
$$\sum_{i=1}^n a_{1i}x_i = 0 \quad \cdots \quad \sum_{i=1}^n a_{mi}x_i = 0$$ Podemos definir $T : \mathbb{K}^n \rightarrow \mathbb{K}^m, \; T(x_1, \dots, x_n) = \Big(\sum_{i=1}^n a_{1i}x_i, \dots, \sum_{i=1}^n a_{mi}x_i\Big)$ como una transformación lineal (se puede probar que lo es muy fácilmente). Queremos saber cuando el sistema tiene más de una solución que no sea la trivial, es decir todas las soluciones tales que $T(x_1, \dots, x_n) = (0,0, \dots, 0)$. O sea queremos encontrar el núcleo de la transformación cuando $\mathrm{Nu}(T) \neq \{0\}$, pero esto a su vez quiere significar que la función no es inyectiva. Por lo tanto, por la proposición 2 $n > m$ (hay más incógnitas que ecuaciones). De esta manera, demostrarmos el teorema 1 usando transformaciones lineales.
También podemos probar que para un sistema no homogéneo pueden no existir soluciones cuando tenemos más incógnitas que ecuaciones, pues esto significaría que podemos armar una transformación lineal $\mathbb{K}^n \rightarrow \mathbb{K}^m$ no es suryectiva (epimorfismo) cuando $n < m$. 

Muchos de los teoremas que vimos anteriormente se pueden demostrar usando transformaciones lineales. 

## Proyectores
Un tipo de transformaciones lineales muy interesantes son los **proyectores**, se utilizan en múltiples ocasiones. 

> [!Proyectores]
> #Definición Sea $V$ un $\mathbb{K}$-espacio vectorial. Una transformación lineal $\mathrm{P} : V \rightarrow V$ si $P \circ P = P$, es decir son aquellas TL's tales que si las aplico dos veces sobre sí misma dan el mismo resultado que si las hubiera aplicado una vez.

La definición de proyector formaliza y generaliza la idea de una _"proyección gráfica"_. Es decir, en ciertas ocasiones, es necesario obtener que tanto de un vector esta paralelo a una línea o un plano. Por ejemplo en física, para obtener que tanto de una velocidad esta "tangencial" a la trayectoria de una partícula. La siguiente imagen muestra una forma de aplicar una proyección sobre una línea:
![[Pasted image 20230116174446.png| 200]]
Es claro que está función es una transformación lineal y se entiende de donde viene la definición de proyección que dice que todo elemento en la imagen, al aplicar $P$ otra vez obtenemos el mismo vector, pues la proyección gráfica de un vector que esta sobre la línea es sí mismo. 

> [!Proposición 3.]
> Sea $V$ un $K$-espacio vectorial, y sea $P: V \rightarrow V$ una transformación lineal. Entonces $P$ es un proyector si y sólo si $P(v)=v$ para cada $v \in \operatorname{Im}(P)$.

**Demostración.** $(\Rightarrow)$ Supongamos que $P$ un proyector. Sea $x \in \operatorname{Im}(f)$. Entonces existe $v \in V$ tal que $x=P(v)$. Luego, $P(x)=P(P(v))=P \circ P(v)=P(x)=x$.
($\Leftarrow$) Sea $v \in V$. Entonces $P(v) \in \mathrm{Im} (f)$ y por hipótesis, $P(P(v))=P(v)$, es decir, $P \circ P(v)=$ $P(v)$. Como esto vale para cada $v \in V$, resulta que $P \circ P=P$. $\blacksquare$

Un ejemplo claro de un proyector es por ejemplo $P: \mathbb{R}^3 \rightarrow \mathbb{R}^3, \;P(x,y,z) = (x,y,0)$ que "aplasta" o "proyecta" todos los vectores del espacio de 3D en el plano $xy$. 
![[Pasted image 20230116181504.png| 250]]
Notemos que el núcleo de esta transformación es $\mathrm{Nu}(P) = <(0,0,1)>$, es decir el eje $z$, y la imagen de la transformación es $\mathrm{Im}(P) = <(1,0,0), (0,1,0)>$, que es todo el plano $xy$. Entonces, se puede probar que usando la suma directa vista en [[Suma de subespacios]]:  

> [!Proposición 4.]
> Sea $V$ un $K$-espacio vectorial y sea $P: V \rightarrow V$ un proyector. Entonces $\mathrm{Nu}(P) \oplus \operatorname{Im}(P)=V$.

**Demostración.** En primer lugar, veamos que $\operatorname{Nu}(P) \cap \operatorname{Im}(P)=\{0\}$. Sea $x \in \operatorname{Nu}(P) \cap \operatorname{Im}(P)$. Como $x \in \operatorname{Im}(P)$, por la proposición anterior, $P(x)=x$. Pero $x \in \mathrm{Nu}(P)$, de donde $P(x)=0$. Luego, $x=0$.
Veamos ahora que $\operatorname{Nu}(P) + \operatorname{Im}(P)=V$. Sea $x \in V$. Entonces $x = (x - P(x)) - P(x)$ y se tiene que $P(x-P(x))=P(x)- P\circ P(x)=P(x)-P(x)=0$, con lo que $x-P(x) \in \operatorname{Nu}(P)$ y $P(x) \in \operatorname{Im}(f)$. $\blacksquare$ 

Luego, se puede pensar de manera inversa. Si yo tengo dos subespacios $U$ y $W$ de $V$ tal que uno es complemento del otro, es decir $U \oplus W = V$, entonces yo puedo encontrar un proyector tal que $\mathrm{Nu}(P) = U$ y $\mathrm{Im}(P) = W$, y es más resulta que este proyector es **único**.

>[!Proposición 5.]
>Sea un $K$-espacio vectorial, y sean $U$ y $W$ subespacios de $V$ tales que. $U \oplus W=V$. Entonces exisle un único proyector $P: V \rightarrow V$ tal que $\operatorname{Nu}(f)=U, \operatorname{Im}(f)=W$.

**Demostración.** Como $V=U \oplus W$, para cada $v \in V$, existen únicos $u \in U$ y $w \in W$ tales que $v=u+w$ (por la proposición 3 en [[Suma de subespacios]]). Entonces, si $P: V \rightarrow V$ es un proyector tal que $\mathrm{Nu}(P)=U, \operatorname{Im}(P)=W$, se tiene que $P(v)=P(v+w)=P(u)+P(w)=0+w=w$, donde la penúltima igualdad es consecuencia de que $P$ es un proyector y $w \in \operatorname{Im}(P)$ (ver Proposición 5).
Consideremos entonces la función $P: V \rightarrow V$ definida por
$$
P(v)=w \quad \text { si } v=u+w \text { con } u \in U, w \in W
$$
Observamos que $P$ es una transformación lineal:
- Si $v, v^{\prime} \in V$ tales que $v=u+w, v^{\prime}=u^{\prime}+w^{\prime}$, con $u, u^{\prime} \in U$ y $w, w^{\prime} \in W$, entonces $v+v^{\prime}=\left(u+u^{\prime}\right)+\left(w+w^{\prime}\right)$ con $u+u^{\prime} \in U$ y $w+w^{\prime} \in W$ (puesto que $U$ y $W$ son subespacios de $V$) por lo tanto, $P\left(v+v^{\prime}\right)=w+w^{\prime}=P(v)+P\left(v^{\prime}\right)$
- Si $\lambda \in \mathbb{K}$ y $v \in V, v=u+w$ con $u \in U, w \in W$, entonces $\lambda v=(\lambda  u)+(\lambda w)$ con $\lambda . u \in U$, $\lambda . w \in W$. Luego, $P(\lambda, v)=\lambda v=\lambda . P(v)$.
Además, $P$ es un proyector: pues si $v \in V$ y $v = u+w$, entonces $P(P(v)) = P(P(u)+P(w)) = P(0 + w) = P(w) = w = P(v)$. Es claro que $\mathrm{Im}(P) = W$ pero comprobemos $\mathrm{Nu}(P) = U$, si $v = u+w$ con $u \in U$ entonces $P(v) = P(u) + P(w) = 0 + w$ tal que $P(u) = 0$ por lo tanto $u \in \mathrm{Nu}(P)$.  $\blacksquare$ 

