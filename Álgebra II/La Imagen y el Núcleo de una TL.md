# La Imagen y el Núcleo de una TL
Como las transformaciones lineales son operaciones entre conjuntos tiene sentido estudiar la validez de las propiedades usuales: inyectividad, suryectividad y biyectividad. 

> [!Tipos de Transformaciones Lineales]
> #Definición Sean $V$ y $W$ dos $\mathbb{K}$ [[Espacios Vectoriales]] y sea $T:V \rightarrow W$ una TL. Se dice que:
> 1. $T$ es un **monomorfismo** si $T$ es inyectiva.
> 2. $T$ es un **epimorfismo** si $T$ es suryectiva.
> 3. $T$ es un **isomorfismo** si $T$ es biyectiva.}
> 
>  #Definición Sea $V$ un $\mathbb{K}$ espacio vectorial y sea $T:V \rightarrow V$ una TL, se llama **endomorfismo** y si además es un isomorfismo se le dice **automorfismo**.

Una observación que podemos observar de la proposición 1 de [[Transformaciones Lineales]] es que como $\{0\} \subset W$ y es subespacio vectorial de este, entonces $f^{-1}({0})$ también debe ser un subespacio a este lo llamamos núcleo.

> [!Núcleo de una transformación lineal]
> #Definición Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales, y sea $T: V \rightarrow W$ una TL. Se llama núcleo de $T$ al conjunto $\mathrm{Nu}(T)= \{v \in V : T(v)=0\} = f^{-1}({0_W})$  

El núcleo se puede usar para determinar si tenemos un **monomorfismo** o no pues si existen otros valores que nos den $0_W$ además de $f(0_V) = 0_W$ entonces no va ser un monomorfismo. 

> [!Proposición 1. inyectividad (mono) es equivalente al núcleo igual a 0]
> Sea $T: V \rightarrow W$ una TL. Entonces, $T$ es un **monoformismo** si y solo si $\mathrm{Nu}(T) = \{0\}$. 

**Demostración.** ($\Rightarrow$) Primero supongamos que $T$ es un monomorfismo.  Queremos probar que $\mathrm{Nu}(T) = \{0\}$. Ya sabemos que $\{0\} \subseteq \mathrm{Nu}(T)$. Para ver la inclusión en la otra dirección, supongamos $v \in \mathrm{Nu}(T)$. Entonces, $T(v) = 0 = T(0)$ pues $T$ es inyectiva ( o monomorfismo). 
($\Leftarrow$) Supongamos que $\mathrm{Nu}(T) = \{0\}$ entonces para probar que es inyectiva veamos que dados $v,w \in V$ entonces $T(v) = T(w) \rightarrow T(v) - T(w) = 0$ lo que nos dice que $v-w \in \mathrm{Nu}(T)$, usando la definición de las TL tenemos $T(v-w) = T(0) \rightarrow v-w = 0 \rightarrow v=w$. $\blacksquare$ 

Otro conjunto importante que es interesante analizar es la **imagen de $f$** que se define como 
> [!Imagen de una TL.]
> Sea $f:V \rightarrow W$ una transformación lineal. Entoncesn definimos $\mathrm{Im}(f) = \{ w \in W : \exists v \in V, f(v) = w\}$ como la _Imagen de $f$_.

que de la proposición 1  vista en [[Transformaciones Lineales]] sabemos que también es un subespacio. 
Como podemos definir una transformación única teniendo elementos de una base de $V$ (por lo que vimos en la proposición 2 de [[Transformaciones Lineales]]). Resulta que no es difícil de deducir que los vectores a los que se dirigen los elementos de la base ordenada $T(a_1v_1 + \dots + a_nv_n) = a_1w_1 + \dots + a_n w_n$ forman una lista de vectores que generan la imagen de $T$. La siguiente proposición demuestra que las TL's mantienen las combinaciones lineales:

> [!Proposición 2.]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales y sea $T: V \rightarrow W$ una transformación lineal. Entonces, si $v_1, \dots, v_n$ es un sistema de generadores de $V$, $T(v_1), \dots, T(v_n)$ es un sistema de generadores de $Im(T)$.

**Demostración.** Por definición, $\mathrm{Im}(T) = \{T(v): v \in V\}$. Si $v_1, \dots, v_n$ una lista de vectores que son un sistema de generadores de $V$, existen $a_1, \dots, a_n \in \mathbb{K}$ tales que $v = a_1v_1 + \dots + a_nv_n$. Luego $T(v) = a_1T(v_1) + \dots + a_nT(v_n)$ por lo tanto $T(v) \in <T(v_1), \dots, T(v_n)>$. Esto prueba $\mathrm{Im}(T) \subseteq <f(v_1), \dots, f(v_n)>$, es claro que la vuelta vale también pues  $T(v_i) \in \mathrm{Im}(T)$. Entonces, $\mathrm{Im}(T) = <f(v_1), \dots, f(v_n)>$. $\blacksquare$ 

Supongamos que tenemos la TL; $f: \mathbb{R}^3 \rightarrow \mathbb{R}^3$ tal que $(x,y,z) \mapsto (x-y, -x+y, 2x-2y+z)$. Podemos encontrar un sistema de generadores de la imagen (por la proposición anterior), reemplazando por un sistema de generadores de $V$ (usemos la base canónica): $f(1,0,0) = (1,-1,2)$, $f(0,1,0)= (-1,1,2)$ y $f(0,0,1) = (0,0,1)$. Si usted comprueba usando los métodos vistos en [[Bases Vectoriales]], verá que los vectores son LD, si luego quitamos uno nos queda una base de la imagen $\mathrm{Im}(f) = < (1,-1,2), (0,0,1) >$ . Observemos que a pasar de que agarramos a una base, esta nos llevó a un sistema de generadores que era linealmente dependiente ([[Independencia Lineal]]).

Como consecuencia de esta proposición tenemos que si tenemos una base de $V$ y la mandamos a la función vamos a tener un sistema de generadores de vectores que pueden (o no) ser **linealmente Dependientes**, las transformaciones lineales no mantienen la independencia lineal. De esta manera, como existe la posibilidad de que sean LD, entonces una base de la imagen puede tener la misma dimensión o menor a la del conjunto de salida $V$.

> [!Corolario 2.1]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales y sea $T: V \rightarrow W$ una transformación lineal. Si $V$ es de dimensión finita, entonces $Im(T)$ también lo es y se tiene que $\mathrm{dim(Im}(T)) \leq \dim(V)$.

También se puede deducir que 

> [!Corolario 2.2]
> Si $T:V \rightarrow W$ es un epimorfismo, y $v_1, \dots, v_n$ es un sistema de generadores de $V$, entonces $T(v_1), \dots, T(v_n)$ es un sistema de generadores de $W$.

El ejemplo anterior muestra claramente un ejemplo de estos corolarios, $T$ no mantiene independencia lineal porque $\mathrm{dim(Im}(f)) = 2 \leq \mathrm{dim}(V) = 3$, es decir muestra que **una base de $V$ no nos lleva a una base de $\mathrm{Im}(f)$ sino a un sistema de generadores que puede o no ser LI**. 
Resulta, que para que se mantenga la independencia lineal es necesario que $T$ sea un **monomorfismo** (inyectiva), lo cual tiene sentido porque si no lo fuera $\{v\} \subset V$ es un conjunto LI y $\{f(v)\} = \{0\} \subset W$ no lo es (el vector nulo siempre es linealmente dependiente). 

> [!Proposición 3.]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales y sea $T: V \rightarrow W$ un monomorfismo. Entonces, si $v_1, \dots, v_n$ es una lista de vectores LI de $V$, $T(v_1), \dots, T(v_n)$ también es LI.

**Demostración.** Queremos ver que dado $v_1, \dots, v_n$ es LI, entonces para la combinación lineal $a_1T(v_1) + \dots + a_nT(v_n) = 0$ es solo posible si $a_1= \dots = a_n = 0$. Notemos que $T(a_1v_1) + \dots + T(a_nv_n) = 0 \rightarrow T(a_1v_1 + \dots + a_nv_n) = 0$ por definición de las TL. Luego, como sabemos por hipótesis $T$ es un monomorfismo, por la proposición 1 tenemos que $a_1v_1 + \dots + a_nv_n = 0$ y entonces $a_1 = \dots = a_n = 0$. $\blacksquare$ 

Como consecuencia

> [!Corolario 3.1]
> Sea $T: V \rightarrow W$ un monomorfismo y $B = v_1, \dots, v_n$ una base ordenada de $V$, entonces $B_T = T(v_1), \dots, T(v_n)$ es una base ordenada de $\mathrm{Im}(T)$. En particular, $\dim(\mathrm{Im}(T)) = \dim V$.

Como un isomorfismo es a la vez un monomorfismo y un epimorfismo (que significa que $\dim W = \dim (\mathrm{Im}(T))$) entonces se deduce:

> [!Corolario 3.2]
> Sea $T: V \rightarrow W$ un isomorfismo. Entonces, para toda base $B$ de $V$, $f(B)$ es una base de $W$. En particular, $\dim V = \dim W$.

Las proposiciones 1, 2 y 3 se pueden generalizar para espacios vectoriales de dimensión infinita considerando al sistema de generadores como $\{v_i: i \in I\}$, siendo $I$ el conjunto de índices. 

## Composición de Transformaciones Lineales
Se puede demostrar que la composición de transformaciones lineales es una transformación lineal:
> [!Proposición 4. Composición de Tl's]
> Sean $V, W$ y $Z K$-espacios vectoriales. Sean $f: V \rightarrow W y g: W \rightarrow Z$ trungformtaciones lineales. Fintonces $g \circ f: V \rightarrow Z$ es una transformación linat.

**Demostración.** Sean $v, v^{\prime} \in V$. Entonces
$$
\begin{align} g \circ f\left(v+v^{\prime}\right)=g\left(f\left(v+v^{\prime}\right)\right)=g\left(f(v)+f\left(v^{\prime}\right)\right)& =g(f(v))+g\left(f\left(v^{\prime}\right)\right) \\ &=g \circ f(v)+g \circ f\left(v^{\prime}\right) \end{align}
$$
Análogamente, si $\lambda \in K$ y $v \in V$, se tiene que
$$
g \circ f(\lambda \cdot v)=g(f(\lambda \cdot v))=g(\lambda \cdot f(v))=\lambda \cdot g(f(v))=\lambda \cdot(g \circ f(v)) . \quad \blacksquare
$$
Finalmente, analizamos las propiedades de la función inversa de una transformación lineal biyectiva (es decir, un isomorfismo).

> [!Proposición 5. La tl inversa]
>  Sean $V$ y W dos $\mathbb{K}$-espacios vectoriales y sea $f: V \rightarrow W$ una transformación lineal. Si $f$ es un isomorfismo, entonces $f^{-1}: W \rightarrow V$ es una transformación lineal (que resulta ser un isomorfismo).

**Demostración.** Sean $w, w^{\prime} \in W$. Como $f$ es un isomorfismo, existen únicos $v ; v^{\prime} \in V$ tales que $w=f(v)$  y $w^{\prime}=f\left(v'\right)$. Entonces:
$$
f^{-1}\left(w+w^{\prime}\right)=f^{-1}\left(f(v)+f\left(v^{\prime}\right)\right)=f^{-1}\left(f\left(v+v^{\prime}\right)\right)=v+v^{\prime}=f^{-1}(w)+f^{-1}\left(w^{\prime}\right) .
$$
Dadas $w \in W$ y  $\lambda \in \mathbb{K}$, existe un único $v \in V$ tal que $w=f(v)$. Entonces
$$
f^{-1}(\lambda \cdot w)=f^{-1}(\lambda \cdot f(v))=f^{-1}(f(\lambda \cdot v))=\lambda \cdot v=\lambda \cdot\left(f^{-1}(w)\right) .
$$
Luego. $f^{-1}$ es una transformación lineal. Es claro que es biyectiva. $\blacksquare$ 