# Transformaciones Lineales
Pasaremos a comprender el objeto de estudio más importante del **algebra lineal** que son las llamadas transformaciones lineales. Que consisten en simplemente, crear una función con [[Espacios Vectoriales]]. 

> [!Transformaciones Lineales]
> #Definición  Sean $(V, +_V, \cdot_V)$ y $(W, +_W, \cdot_W)$ dos $\mathbb{K}$-[[Espacios Vectoriales]]. Una función $f:V \rightarrow W$ se le llama transformación lineal (u homomorfismo o simplemente morfismo) de V en W si cumple:
> 1. $f(v +_V v') = f(v) + _W f(v')$ 
> 2. $f(\lambda \cdot_V v) = \lambda \cdot_W f(v), \;  \forall \lambda \in K, \forall v \in V$.

Notemos que el ejemplo más simple de transformación lineal es $0: V \rightarrow W$ o también llamada la transformación trivial, que consiste en tomar cualquier vector $v$ del espacio vectorial $V$ y multiplicarlo escalarmente por $0 \in \mathbb{K}$ lo cual nos da el $0_W$ (el cero del espacio vectorial $W$), $0(v) = 0_W$. Sabemos que esta es una transformación lineal porque cumple las dos propiedades: 
- $0(v +_V v') = 0_{\mathbb{K}} \cdot (v +_V v') = 0_{\mathbb{K}} \cdot v +   0_{\mathbb{K}} \cdot v' = 0(v) +_W 0(v')$
- $0(\lambda v) = 0_\mathbb{K} \cdot \lambda \cdot_V v = \lambda \cdot_V 0_\mathbb{K} \cdot v = \lambda \cdot_W 0(v)$  
Luego, está la transformación identidad $I: V \rightarrow V$ que es no hacerle ningún afecto al vector. Es decir $I(v) = v$. 

Si $T: \mathbb{R}^2 \rightarrow \mathbb{R}^2$ y la definimos como $T(x,y) = (1+x,y)$ no es una transformación lineal pues $T((x_1,y_1) + (x_2, y_2)) = T((x_1+x_2, y_1+y_2)) = (x_1+x_2+1, y_1+y_2)$ y que no es igual a $T(x_1, y_1) + T(x_2,y_2) = (x_1+1, y_1) + (x_2+1, y_2) = (x_1+x_2+2, y_1+y_2)$. En general, cuando estamos operando con espacios vectoriales $\mathbb{K}^n$, sumar constantes a las coordenadas ya evita que pueda ser una transformación lineal, al igual que multiplicar las coordenadas entre si como $T(x,y)=xy$ tampoco es una transformación lineal (TL). _Una forma fácil de comprobar que una función no es una transformación lineal es usando $T(0_V) = 0_W$_, en el ejemplo anterior $T(x, y) = (1+x, y)$ tenemos que $T(0,0) = (1,0) \neq (0,0)$.  

Otros ejemplos de transformaciones lineales pueden ser la diferenciación $D: \mathbb{K}[x] \rightarrow \mathbb{K}[x]$ siendo $\mathbb{K}$ un subcuerpo de los complejos, tal que $D(p) = p'$. Podemos probar que lo es pues $(f+g)' = f' + g'$ y $(\lambda f)' = \lambda f'$. También, la integración (con limites definidos), por ejemplo $T: \mathbb{K}[x] \rightarrow \mathbb{K}, \; T(p) = \int_0^1 p(x)dx$ es una transformación lineal pues $\int (f+g)(x) dx = \int f(x)dx + \int g(x)dx$ y $\int\lambda f(x)dx = \lambda \int f(x)dx$ por propiedades vistas en [[Una definición formal de Área]]. 

También, una transformación lineal muy importante es la de [[Matrices]]. Si $T: \mathbb{K}^n \rightarrow \mathbb{K}^m, T(v) = Av$ con $A \in M_{m \times n}(\mathbb{K})$ es una transformación lineal.  Y lo puede probar usted mismo, usando que la suma de matrices esta definida como $(A+B)_{ij} = (A)_{ij} + (B)_{ij}$, la multiplicación por escalar esta definida como $(\lambda   A)_{ij} = \lambda (A)_{ij}$. 

Las transformaciones lineales representan la **estructura de un espacio vectorial**. De hecho las tras propiedades que tienen que cumplir las TL son muy parecidas a las tres propiedades que tiene que cumplir un [[Subespacio Vectorial]]. De esta manera, podemos decir que estamos generando un subespacio en $W$ al agarrar todos los vectores de $V$ y "transformándolos". La siguiente proposición nos dice que podemos agarrar subespacios de un espacio $V$ y usar la transformación lineal para obtener subespacios de $W$ y viceversa.

> [!Proposición 1. las tl's mantienen los subespacios]
> Sea $f: V \rightarrow W$ una transformación lineal. Entonces,
> 1. Si $S$  es un subespacio de $V$, entonces $f(S)$ es un subespacio de $W$. 
> 2. Si $T$ es un subespacio de $W$, entonces $f^{-1}(W)$ es un subespacio de $V$.

**Demostración.** 
1. Sea $S \subseteq V$ un subespacio y consideremos $f(S) = \{w \in W / \exists s \in S, f(s) = w\}$. Probemos por la proposición 1 de [[Subespacios]] que es un subespacio de $W$.
		1. $0_W \in f(S)$, puesto que $f(0_V) = 0_W$ y $0_V \in S$. 
		2. Sean $w, w' \in f(S)$. Entonces existen $s, s' \in S$ tales que $f(s)= w$ y $f(s') = w'$ tal que $w+w' = f(s) + f(s') = f(s+s')$. Por lo tanto, $w+w' \in f(S)$.
		3. Sean $\lambda \in \mathbb{K}$ y $w \in f(S)$. Existe $s \in S$ tal que $w = f(s)$ luego $\lambda w = \lambda f(s) = f(\lambda s)$
2. Sea $T$ un subespacio de $W$ y consideremos $f^{-1}(T) = \{v \in V / f(v) \in T\}$. Probemos por la proposición 1 de [[Subespacios]] que es un subespacio de $V$. 
	1. $0_V \in f^{-1}(T)$ puesto que $f(0_V) = 0_W \in T$. 
	2. Sean $v,v' \in f^{-1}(T)$. Entonces $f(v)$, $f(v') \in T$ y, por lo tanto $f(v+v') = f(v) + f(v') \in T$. Luego $v+v' \in f^{-1}(T)$.
	3. Sean $\lambda \in \mathbb{K}$ y $v \in f^{-1}(T)$. Entonces $f(v) \in T$ por lo tanto $\lambda f(v) = f(\lambda v) \in T$. Luego $\lambda v \in f^{-1}(T)$. $\blacksquare$ 

Gracias a la definición de transformación lineal es obvio que estas son capaces de preservar combinaciones lineales de un espacio a otro. Es decir, teniendo una base de un subespacio $S \subset V$ que es $\beta = \{v_1, \dots, v_n\}$ nos permite escribir de manera **única** los vectores del subespacio como una comb. lineal por una proposición (Criterio de la Base) vista en [[Bases Vectoriales]], tal que si $v \in S$ entonces existen $a_i$'s únicos de manera que $v = \sum_{i=1}^n a_iv_i$. Luego, $f(v) = f\Big(\sum_{i=1}^n a_i v_i\Big) = \sum_{i=1}^n a_if(v_i)$  por la definición de TL. Por la proposición 1 tenemos que los $\{f(v_1), \dots, f(v_n)\}$ generan un subespacio en $W$. 
Esto es útil si nos dan una base de un espacio vectorial de salida $V$ y a donde se dirigen en la imagen de la función, se puede obtener una **transformación única** que cumpla esto. Las siguientes dos proposiciones demuestran lo dicho.

> [!Proposición 2. TL's y bases del dominio]
> Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales, V de dimensión ﬁnita. Sea $B = v_1 , . . . , v_n$ una base ordenada de V y sean $w_1 , . . . , w_n \in W$ vectores arbitrarios. Entonces existe una única transformación lineal $T: V → W$ tal que $T (v_i) = w_i$ para cada $1 ≤ i ≤ n$.

**Demostración.** Primero probemos la existencia de la TL con la propiedad deseada. Definamos $T: V \rightarrow W$ por $T(c_1 v_1 + \cdots + c_nv_n) = c_1w_1 + \cdots + c_n w_n$ donde $c_1, \dots, c_n$ son elementos arbitrarios de $\mathbb{K}$. Como $\{v_1, \dots, v_n\}$ es una base de $V$, y cada elemento de $v \in V$ se puede escribir como una combinación lineal de estos, y $w_1, \dots, w_n \in W$ entonces la función esta bien definida. Veamos ahora que es una transformación lineal. Si $u,v \in V$ con $u = a_1v_1 + \dots + a_nv_n$ y $v= c_1v_1 + \dots +c_nv_n$. Entonces 
$$\begin{align} T(u+v) &= T((a_1+c_1)v_1 + \dots + (a_n+c_n)v_n) \\
&= (a_1+c_1)w_1 + \dots +(a_n+c_n)w_n \\
& = (a_1w_1 + \dots + a_n w_n) + (c_1v_1 + \dots +c_n v_n) \\
&= T(u) + T(v)
\end{align}$$
Probar que para un $\lambda \in \mathbb{K}$ y $v \in V$, $T(\lambda v) = \lambda T(v)$ es aún más sencillo.
Luego, la transformación lineal es **única** pues si $T(v_j) = w_j$ para todo $1 \leq j \leq n$. Sean $c_1, \dots, c_n \in \mathbb{K}$ fijos. La 2da propiedad de $T$ implica que $T(c_jv_j) = c_jw_j$ para todo $1 \leq j \leq n$. La 1era propiedad de $T$ implica $T(c_1 v_1 + \dots + c_n v_n) = c_1 w_1 + \dots + c_nw_n$. Como $\{v_1, \dots, v_n\}$ es una base en $V$ esto implica que existen coeficientes **únicos** $c_1, \dots, c_n \in \mathbb{K}$ para cada $v \in V$, esto significa que $T$ está únicamente determinada en $V$. $\blacksquare$ 

Se puede generalizar esta proposición para infinitos vectores que sean bases de un espacio vectorial $V$. Algo importante que nos dice esta proposición es que *nos basta con saber a donde van los elementos de una base de $V$ para definir una transformación lineal*.

## El conjunto de todas las TL
Fijados dos $\mathbb{K}$-espacios vectoriales $V$ y $W$, tiene sentido considerar el conjunto de todas las transformaciones lineales de $V$ en $W$. 

> [!Espacios vectoriales de Transformaciones Lineales]
> #Definición Sean $V$ y $W$ dos $\mathbb{K}$-espacios vectoriales. Definimos $$\text{Hom}_{\mathbb{K}}(V,W) = \{f: V \rightarrow W / f \text{ es una transformación lineal } \}$$
> Otra forma de escribirlo es $\mathcal{L}(V,W)$.

>[!Adición y multiplicación escalar en el conjunto de todas las TL]
>Dadas $f,g \in \mathrm{Hom}(V,W)$ se define $f+g$ como $(f+g)(x) = f(x) + g(x)$ , $\forall x \in V$. Y el producto $\lambda f$ como $(\lambda f)(x) = \lambda f(x)$. 

Se puede probar que $f+g$ y $\lambda f$ son efectivamente transformaciones lineales y pertenecen a $\mathrm{Hom}(V,W)$. Luego, se puede probar que $\mathrm{Hom}(V,W)$ es un espacio vectorial. 

 



