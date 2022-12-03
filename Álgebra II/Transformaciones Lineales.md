Pasaremos a comprender el objeto de estudio más importante del **algebra lineal** que son las llamadas transformaciones lineales. Que consisten en simplemente, crear una función con [[Espacios Vectoriales]]. 

> #Definición **(Transformaciones Lineales)** Sean $(V, +_V, \cdot_V)$ y $(W, +_W, \cdot_W)$ dos $\mathbb{K}$-[[Espacios Vectoriales]]. Una función $f:V \rightarrow W$ se le llama transformación lineal (u homomorfismo o simplemente morfismo) de V en W si cumple:
> 1. $f(v +_V v') = f(v) + _W f(v')$ 
> 2. $f(\lambda \cdot_V v) = \lambda \cdot_W f(v), \;  \forall \lambda \in K, \forall v \in V$.

Notemos que el ejemplo más simple de transformación lineal es $0: V \rightarrow W$ o también llamada la transformación trivial, que consiste en tomar cualquier vector $v$ del espacio vectorial $V$ y multiplicarlo escalarmente por $0 \in \mathbb{K}$ lo cual nos da el $0_W$ (el cero del espacio vectorial $W$), $0(v) = 0_W$. Sabemos que esta es una transformación lineal porque cumple las dos propiedades: 
- $0(v +_V v') = 0_{\mathbb{K}} \cdot (v +_V v') = 0_{\mathbb{K}} \cdot v +   0_{\mathbb{K}} \cdot v' = 0(v) +_W 0(v')$
- $0(\lambda v) = 0_\mathbb{K} \cdot \lambda \cdot_V v = \lambda \cdot_V 0_\mathbb{K} \cdot v = \lambda \cdot_W 0(v)$  
Luego, está la transformación identidad $I: V \rightarrow V$ que es no hacerle ningún afecto al vector. Es decir $I(v) = v$. 

Si $T: \mathbb{R}^2 \rightarrow \mathbb{R}^2$ y la definimos como $T(x,y) = (1+x,y)$ no es una transformación lineal pues $T((x_1,y_1) + (x_2, y_2)) = T((x_1+x_2, y_1+y_2)) = (x_1+x_2+1, y_1+y_2)$ y que no es igual a $T(x_1, y_1) + T(x_2,y_2) = (x_1+1, y_1) + (x_2+1, y_2) = (x_1+x_2+2, y_1+y_2)$. En general, cuando estamos operando con espacios vectoriales $\mathbb{K}^n$, sumar constantes a las coordenadas ya evita que pueda ser una transformación lineal, al igual que multiplicar las coordenadas entre si como $T(x,y)=xy$ tampoco es una tranformación lineal (TL). _Una forma fácil de comprobar que una función no es una transformación lineal es usando $T(0_V) = 0_W$_, en el ejemplo anterior $T(x, y) = (1+x, y)$ tenemos que $T(0,0) = (1,0) \neq (0,0)$.  

Las transformaciones lineales representan la **estructura de un espacio vectorial**. De hecho las tras propiedades que tienen que cumplir las TL son muy parecidas a las tres propiedades que tiene que cumplir un [[Subespacio Vectorial]]. De esta manera, podemos decir que estamos generando un subespacio en $W$ al agarrar todos los vectores de $V$ y "transformandolos". La siguiente proposición nos dice que podemos agarrar subespacios de un espacio $V$ y usar la tranformación lineal para obtener subespacios de $W$ y viceversa.

> **Proposición 1.** Sea $f: V \rightarrow W$ una transformación lineal. Entonces,
> 1. Si $S$  es un subespacio de $V$, entonces $f(S)$ es un subespacio de $W$. 
> 2. Si $T$ es un subespacio de $W$, entonces $f^{-1}(W)$ es un subespacio de $V$.

Gracias a la definición de transformación lineal es obvio que estas son capaces de preservar combinaciones lineales de un espacio a otro. Es decir, teniendo una base de un subespacio $S \subset V$ que es $\beta = \{v_1, \dots, v_n\}$ nos permite escribir de manera **única** los vectores del subespacio como una comb. lineal por una proposición vista en [[Bases Vectoriales]], tal que si $v \in S$ entonces existen $a_i$'s únicos de manera que $v = \sum_{i=1}^n a_iv_i$. Luego, $f(v) = f\Big(\sum_{i=1}^n a_i v_i\Big) = \sum_{i=1}^n a_if(v_i)$  por la definición de TL. Por la proposición 1 tenemos que los $\{f(v_1), \dots, f(v_n)\}$ generan un subespacio en $W$. 
Esto es útil si nos dan una base de un espacio vectorial de salida $V$ y a donde se dirigen en la imagen de la función, se puede obtener una **transformación única** que cumpla esto. Las siguientes dos proposiciones demuestran lo dicho.

> **Proposición 2.** Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales, V de dimensión ﬁnita. Sea $B = \{v_1 , . . . , v_n \}$una base de V y sean $w_1 , . . . , w_n \in W$ vectores arbitrarios. Entonces existe una única transformación lineal $f : V → W$ tal que $f (v_i) = w_i$ para cada $1 ≤ i ≤ n$.

Se puede generalizar esta proposición para infinitos vectores que sean bases de un espacio vectorial $V$. Algo importante que nos dice esta proposición es que *nos basta con saber a donde van los elementos de una base de $V$ para definir una transformación lineal*.

## Monomorfismos, Epimorfismos e Isomorfismos
Como las tranformaciones lineales son operaciones entre conjuntos tiene sentido estudiar la validez de las propiedades usuales: inyectividad, suryectividad y biyectividad. 

> #Definición **(-ismos 1)** Sean $V$ y $W$ dos $\mathbb{K}$ espacios vectoriales y sea $f:V \rightarrow W$ una TL. Se dice que:
> 1. $f$ es un **monomorfismo** si $f$ es inyectiva.
> 2. $f$ es un **epimorfismo** si $f$ es suryectiva.
> 3. $f$ es un **isomorfismo** si $f$ es biyectiva.

> #Definición **(-ismos 2)** Sea $V$ un $\mathbb{K}$ espacio vectorial y sea $f:V \rightarrow V$ una TL, se llama **endomorfismo** y si además es un isomorfismo se le dice **automorfismo**.

Una observación que podemos observar de la proposición 1 es que como $\{0\} \subset W$ y es subespacio vectorial de este, entonces $f^{-1}({0})$ también debe ser un subespacio a este lo llamamos núcleo.

> #Definición **(Núcleo de una TL)** Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales, y sea $f: V \rightarrow W$ una TL. Se llama núcleo de $f$ al conjunto $\mathrm{Nu}(f)= \{v \in V : f(v)=0\} = f^{-1}({0_W})$  

El núcleo se puede usar para determinar si tenemos un **monoformismo** o no pues si existen otros valores que nos den $0_W$ además de $f(0_V) = 0_W$ entonces no va ser un monoformismo. 

> **Proposición 3.** Sea $f: V \rightarrow W$ una TL. Entonces, $f$ es un **monoformismo** si y solo si $\mathrm{Nu}(f) = \{0\}$. 

Otro conjunto importante que es interesante analizar es la **imagen de $f$** que se define como $\mathrm{Im}(f) = \{ w \in W : \exists v \in V, f(v) = w\}$ que de la proposición 1 sabemos que también es un subespacio. 
Como podemos definir una transformación única teniendo elementos de una base de $V$, podemos de manera inversa obtener un sistema de generadores de la imagen de $f$ teniendo un sistema de generadores de $V$ tal que demostramos la siguiente proposición:

> **Proposición 4.** Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales y sea $f: V \rightarrow W$ una transformación lineal. Entonces, si $\{v_i: i \in I\}$ es un sistema de generadores de $V$, $\{f(v_i): i \in I\}$ es un sistema de generadores de $Im(f)$.

Supongamos que tenemos la TL; $f: \mathbb{R}^3 \rightarrow \mathbb{R}^3$ tal que $(x,y,z) \mapsto (x-y, -x+y, 2x-2y+z)$. Podemos encontrar un sistema de generadores de la imagen (por la proposición anterior), reemplazando por un sistema de generadores de $V$ (usemos la base canónica): $f(1,0,0) = (1,-1,2)$, $f(0,1,0)= (-1,1,2)$ y $f(0,0,1) = (0,0,1)$. Si usted comprueba usando los métodos vistos en [[Bases Vectoriales]], verá que los vectores son LD, si luego quitamos uno nos queda una base de la imagen $\mathrm{Im}(f) = \langle (1,-1,2), (0,0,1) \rangle$ .

Como consecuencia de esta proposición tenemos que si tenemos una base de $V$ y la mandamos a la función vamos a tener un sistema de generadores de vectores que pueden (o no) ser **linealmente Dependientes**, las transformaciones lineales no mantienen la independencia lineal. De esta manera, como existe la posibilidad de que sean LD, entonces una base de la imagen puede tener la misma dimensión o menor a la del conjunto de salida $V$.

> **Colorario 4.1.** Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales y sea $f: V \rightarrow W$ una transformación lineal. Si $V$ es de dimensión finita, entonces $Im(f)$ también lo es y se tiene que $\mathrm{dim(Im}(f)) \leq \mathrm{dim}(V)$.

> **Colorario 4.2** Si $f:V \rightarrow W$ es un epimorfismo, y $\{v_i : i \in I\}$ es un sistema de generadores de $V$, entonces $\{f(v_i) : i \in I\}$ es un sistema de generadores de $W$.

El ejemplo anterior muestra claramente un ejemplo de estos colorarios, $f$ no es un epimorfismo porque $\mathrm{dim(Im}(f)) = 2 \leq \mathrm{dim}(V) = 3$ y nos muestra que **una base de $V$ no nos lleva a una base de $\mathrm{Im}(f)$ sino a un sistema de generadores que puede o no ser LI**. 
Resulta, que para que se mantenga la independencia lineal es necesario que $f$ sea un **monomorfismo** (inyectiva), lo cual tiene sentido porque si lo es entonces $f(v) = 0_W$, $v=0_V$ y es el único valor que lo cumple, de otra manera si $\{v\} \subset V$ es un conjunto LI y $\{f(v)\} = \{0\} \subset W$ no lo es (el vector nulo siempre es linealmente dependiente). 

> **Proposición 5.** Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales y sea $f: V \rightarrow W$ un monomorfismo. Entonces, si $\{v_i : i \in I\}$ es un conjunto LI de $V$, $\{f(v_i) i \in I\}$ también es LI.

Como consecuancia,

> **Colorario 5.1** Sea $f: V \rightarrow W$ un monomorfismo



