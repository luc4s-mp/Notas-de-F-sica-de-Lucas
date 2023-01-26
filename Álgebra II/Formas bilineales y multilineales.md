Si bien las [[Transformaciones Lineales]] son un tipo de funciones muy interesante entre [[Espacios Vectoriales]], no son las únicas. Existen otros tipos de funciones muy interesantes que valen la pena estudiar que no son transformaciones lineales. Por ejemplo, $f: \mathbb{R}^2 \rightarrow \mathbb{R}, \; f(x,y) = xy$ no es una transformación lineal. Sin embargo, si fijamos una de sus variables, por ejemplo $x \in \mathbb{R}$ , tenemos que $f(y) = xy$ si es una transformación lineal. Podemos generalizar esto último y hablar de todas las funciones $f: V \rightarrow \mathbb{K}$ con $V$ un $\mathbb{K}$-espacio vectorial finito, y veamos que $f_{w}(\vec{v}) = \vec{v} \cdot \vec{w}$[^1] con $\vec{w} \in V$ fijo y donde $\cdot$ es un [[Producto Interno]]  en $V$[^2],  es una transformación lineal especial llamada **forma lineal**. 

Entonces, se puede probar que una función es una **forma lineal** si el producto en $V$ esta definido de forma tal que se cumple  $\vec{v}, \vec{u} \in V, \; f_w(\vec{v} + \vec{u})$$= (\vec{v} + \vec{u}) \cdot \vec{w}$ $= \vec{v} \cdot \vec{w} + \vec{u} \cdot \vec{w} = f_w(\vec{v}) + f_w(\vec{u})$  y $\lambda \in \mathbb{K}, \vec{v} \in V, \; f_w(\lambda\vec{v}) = (\lambda\vec{v}) \cdot \vec{w} = \lambda(\vec{v} \cdot \vec{w})$ $= \lambda f_w(\vec{v})$ . Para acortar este proceso de demostrar que una función es una forma lineal, basta con demostrar $f(\lambda \vec{v} + \vec{w}) = \lambda f(\vec{v}) + f(\vec{w})$ pues eligiendo $\lambda = 1$ tenemos la primer propiedad y luego eligiendo $\vec{w} = 0$ tenemos la segunda. Ahora, notemos que la función $f_w(\vec{v}) = \vec{v} \cdot \vec{w}$ tiene a $\vec{w}$ fijo, pero si aparte podemos definir $f_{v}(\vec{w}) = \vec{v} \cdot \vec{w}$ con $\vec{v}$ fijo y esta también cumple ser una forma lineal. Entonces decimos que podemos simplemente definir $f(\vec{v}, \vec{w}) = \vec{v} \cdot \vec{w}$ que fijando un vector o el otro es una forma lineal, a esta la llamamos **forma bilineal**.  

> [!Forma Binomial]
> #Definición Sean $V$ y $W$ dos $\mathbb{K}$ espacios vectoriales. Una _forma bilineal_ de $V$ en $W$ es una función $F: V \times W \rightarrow \mathbb{K}$  si:
> 1. $F( v_1 + v_2, w) = F(v_1, w) + F(v_2, w)$ 
> 2. $F(v, w_1 + w_2) =  F(v, w_1) + F(v, w_2)$ 
> 3. $F(\lambda v, w) = \lambda F(v,w) = F(v, \lambda w)$
> Con $w, w_1, w_2 \in W, \; v, v_1, v_2 \in V$ y $\lambda \in \mathbb{K}$

Notemos como construimos el concepto de forma bilineal usando transformaciones lineales. Esto nos permite entender a las formas bilineales gracias a que ya entendemos a las TL's. El siguiente ejemplo muestra la intima relación entre ambos tipos de funciones.

**Ejemplo 1.** Sean $f, g : V \rightarrow \mathbb{K}$ dos transformaciones lineales, tenemos que $F(v,w) = f(v)g(w)$ es una forma binomial. Esto pues 
- $F(\lambda v_1 + v_2, w) = f(\lambda v_1 + v_2)g(w) = (\lambda f(v_1) + f(v_2)) g(w)$ $= \lambda f(v_1)g(w) + f(v_2)g(w) = \lambda F(v_1, w) + F(v_2, w)$. Donde en la segunda igualdad usamos que $f$ es una TL.
- $F(v, \lambda w_1 + w_2) = f(v)g(\lambda w_1 + w_2) = f(v)(\lambda g(w_1) + g(w_2) =$ $\lambda f(v)g(w_1) + f(v)g(w_2) = \lambda F(v,w_1) + F(v, w_2)$ . Donde en la segunda igualdad usamos que $g$ es una TL.

Empecemos con nuestro desarrollo de definir el determinante. El determinante es un escalar en un cuerpo $\mathbb{K}$ que se le asigna a una matriz, este va a resultar muy útil para darnos cierta información de la matriz y de la transformación lineal que representa. Entender las formas bilineales son un paso a definir el determinante. 

**Ejemplo 2.** Supongamos que tenemos la forma bilineal $F: \mathbb{R}^2 \times \mathbb{R}^2 \rightarrow \mathbb{R}$, notemos lo siguiente
$$\begin{align} F((a,b),(c,d)) & = F((a,0) + (0,b), (c,d)) = F((a, 0) + (0,b), (c,0) + (0,d)) \\ 
& = a \cdot F((1,0), (c,0)+ (0,d) + b \cdot F((0,1),(c,0)+(0,d)) \\ &= ac \cdot F((1,0),(1,0) + ad \cdot F((1,0),(0,1)) + bc \cdot F((0,1),(1,0)) \\ & \quad + bd \cdot F((0,1),(0,1)) \end{align}$$
Usando las propiedades de las formas bilineales. Notemos que entonces la función queda determinada por $F((1,0),(1,0)), \; F((0,1),(1,0)), \; F((1,0), (0,1))$ y $F((0,1),(0,1))$. Existe isomorfismo entre $\mathbb{R}^2 \times \mathbb{R}^2$ a $M_{2 \times 2}(\mathbb{R})$ por lo tanto tenemos que de cierta manera, podemos llegar a concluir que al igual que representamos una transformación lineal usando matrices podemos hacer lo mismo con las formas bilineales.

## Matriz de una forma bilineal
Supongamos que dada la matriz $A = \begin{pmatrix} 1 & -3 & 2 \\ 0 & 4 & -1\end{pmatrix}$ queremos encontrar una forma bilineal $F: \mathbb{R}^2 \times \mathbb{R}^3 \rightarrow \mathbb{R}$, $F(v, w) = v^t \cdot A \cdot w$ tal que esté expresada solo en las coordenadas de $\mathbb{R}^2$ y $\mathbb{R}^3$, $v = (x_1, x_2)$ y $w = (y_1, y_2, y_3)$, o lo que es lo mismo $v = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$ y $w = \begin{pmatrix} y_1 \\ y_2 \\ y_3 \end{pmatrix}$ . Notemos que $F$ si es una forma bilineal y lo puede comprobar usando las propiedades de la definición. 
Veamos también que $v^t \cdot A \cdot w$ tiene sentido pues $v^t$ es una matriz $1 \times 2$, $A$ es una matriz $2 \times 3$ y $w$ es una matriz $3 \times 1$, entonces tenemos permitida la multiplicación de matrices (vista en [[Operaciones con Matrices]]). 
Luego,
$$\begin{pmatrix} x_1 & x_2\end{pmatrix} \cdot \begin{pmatrix} 1 & -3 & 2 \\ 0 & 4 & -1\end{pmatrix} \cdot \begin{pmatrix} y_1 \\ y_2 \\ y_3 \end{pmatrix} = x_1y_1 -3x_1y_2 + 2x_1y_3 +4x_2y_2 - x_2y_3$$
Y listo, tenemos definida $F((x_1,x_2), (y_1, y_2, y_3)) = x_1y_1 -3x_1y_2 + 2x_1y_3 +4x_2y_2 - x_2y_3$ como nuestra forma binomial. 

Una pregunta que nos podemos hacer es _¿Al igual que puedo obtener de cualquier matriz una forma binomial correspondiente, puedo obtener de una forma binomial una matriz?_ Resulta que si podemos, lo cual motiva la siguiente definición

> [!Matriz de una forma bilineal]
> #Definición Sea $F: V \times V \rightarrow \mathbb{K}$ una forma binomial, y sea $B = v_1, \dots, v_n$ una base de $V$. Definamos $([F]_{B})_{ij} = (F(v_i, v_j)) \in M_{n \times n}(\mathbb{K})$ es la _matriz de $F$ en la base $B$._

De esta manera, se puede comprobar en el ejemplo anterior que $A$ es la matriz de la forma binomial $F$ usando la base canónica. 

Podemos probar entonces lo siguiente
> [!Proposición 1.]
> Sea $V$ un $\mathbb{K}$-espacio vectorial de dimensión finita y sea $B = v_1, \dots, v_n$ es una base ordenada de $V$. Sea $F: V \times V \rightarrow \mathbb{K}$ una forma bilineal. Entonces, para cada $v,w \in V$, $$F(v,w) = (v)^t_B[F]_{B}(w)_{B}$$
> 

**Demostración.** Probemos que de ambos lados obtenemos lo mismo. Teniendo $v = \sum_{i=1}^n \alpha_iv_i$ y $w = \sum_{i=1}^n \beta_iv_i$ expresados en la base $B$.
$$F(v,w) = F\Big(\sum_{i=1}^n \alpha_i v_i, \sum_{j=1}^n \beta_jv_j\Big) = \sum_{i=1}^n \alpha_i F\Big(v_i, \sum_{j=1}^n\beta_j v_j\Big) = \sum_{i=1}^n \alpha_i \Big(\sum_{j=1}^n \beta_j F(v_i,v_j)\Big)$$
Luego,
$$\begin{align} (v)_{B}^t [F]_B (w)_B & = \begin{pmatrix} \alpha_1 & \alpha_2 & \cdots & \alpha_n \end{pmatrix} \cdot 
[F]_{B} \cdot 
\begin{pmatrix} \beta_1 \\ \beta_2 \\ \vdots \\ \beta_n\end{pmatrix} = \sum_{i=1}^n \alpha_i \left( [F]_B \cdot \begin{pmatrix} \beta_1 \\ \beta_2 \\ \vdots \\ \beta_n \end{pmatrix}\right)_{i1}  \\ & = \sum_{i=1}^n \alpha_i\Big( \sum_{j=1}^n \beta_j F(v_i, v_j)\Big) \quad \blacksquare \end{align} $$
Algo muy importante de notar al observar a las formas bilineales, es que la mayoría parecen **polinomios**. 

Volveremos a las formas bilineales para cuando queremos generalizar el [[Producto Interno]] de un espacio vectorial. 

## Funciones Multilineales
Nos vamos a concentrar de ahora en adelante en definir el **determinante**. Una de las aplicaciones más útiles del determinante, es la capacidad de decirnos si una matriz es invertible o no y a la vez nos dice si la transformación lineal que representa es un isomorfismo o no (por lo visto en [[Matrices de Transformaciones Lineales]]).  Entonces, buscamos definir una función que nos lleve de varios vectores (que se pueden ordenar en una matriz) a un escalar que nos diga si los vectores columna (o filas) son linealmente independientes, en ese caso el determinante es distinto de 0.

**Ejemplo 3.** Primero veamos como definir un determinante de $2 \times 2$. Para esto, ya vimos en el ejemplo 2 que en una forma bilineal $F: \mathbb{R}^2 \times \mathbb{R}^2 \rightarrow \mathbb{R}$ tenemos que está determinada por $F((1,0),(1,0)), \; F((0,1),(1,0)), \; F((1,0), (0,1))$ y $F((0,1),(0,1))$. 
Tenemos que claramente la primera lista de vectores y la cuarta son dos vectores linealmente dependientes, entonces queríamos que $F((0,1), (0,1)) = 0$ y $F((1,0), (1,0)) = 0$. Por lo tanto, podemos definir al determinante como "una forma bilineal  tal que al evaluarla en vectores iguales nos da 0". Sabiendo que $F$ es una función de este tipo veamos ahora que dado $v ,w \in \mathbb{R}^2$ tenemos que
$$\begin{align} 0 & = F(v+w, v+w) = \underset{=0}{\underbrace{F(v,v)}} + F(w,v) + F(v,w) + \underset{=0}{ \underbrace{F(w,w)}} \\ 
0 & = F(v,w) + F(w,v) \\
\boxed{F(v,w)} & = - F(w,v)
\end{align}$$
Luego, $F((1,0),(0,1)) = -F((0,1), (1,0))$ y tenemos entonces que nuestra función buscada es $F((a,b),(c,d)) = (ad - bc)F((1,0),(0,1))$. 

Sin embargo, el determinante puede calcularse para cualquier matriz cuadrada (para encontrar si estas son invertibles), entonces tenemos que definir el concepto de función multilineal. 
> [!Función multilineal]
> #Definición  Sea $V$ un $\mathbb{K}$-espacio vectorial, y una función $F: \prod_{i=1}^n V \rightarrow \mathbb{K}$  se dice _multilineal_ si cumple la propiedad de ser una _forma lineal_ en cada entrada. Es decir, fijando $n-1$ valores y dejando $v_i$ libre, si se cumplen $F(v_1 + v, \dots, cv_i +v_j, \dots, v_n) = cF(v_1, \dots, v_i, \dots, v_n) + F(v_1, \dots, v_j, \dots, v_n)$  para cada $i = 1, \dots, n$ con $v_j \in V$ y $c \in \mathbb{K}$. 

A una función multilineal "tal que al que al evaluarla en listas con dos vectores iguales nos da 0" la llamamos **función alternada**.
> [!Función Alternada]
> Una _función multilineal_ $F: \prod_{i=1}^n V \rightarrow \mathbb{K}$ se dice _alternada_ si se cumple que al evaluarla en una lista de $n$ vectores en los que 2 son iguales nos da 0. Es decir, para $v_1, \dots, v_i, \dots, v_j, \dots, v_n$, una lista de vectores con $v_i = v_j$, $F(v_1, \dots, v_n) = 0$.

Ya sabemos que podemos crear un isomorfismo entre $\mathbb{K}^n$ y $V$ (gracias a la proposición 1 en [[Matrices de Transformaciones Lineales]]) usando una base de finita $V$ y luego existe otro claro isomorfismo entre $\mathbb{K}^n \times \cdots \times \mathbb{K}^n$ y $M_{n \times n} (\mathbb{K})$. Por lo tanto, a cada función multilineal alternada $F: \prod_{i=1}^n V \rightarrow \mathbb{K}$ le asignamos (gracias a los isomorfismos) a una función $F: M_{n \times n}(\mathbb{K}) \rightarrow \mathbb{K}$, por lo tanto trabajemos simplemente con estas funciones.

Gracias a estas dos definiciones, estamos listos para definir el determinante de una matriz $2\times 2$ : 
> [!Determinante 2x2]
> #Definición La función bilineal alternada $\det_2: M_{2 \times 2}(\mathbb{K}) \rightarrow \mathbb{K}$ tal que $\det_2(Id_2) = 1$ se llama _determinante de orden 2_. 

Tal que
$$\det \begin{pmatrix} a & b \\ c & d\end{pmatrix} = (ad-cb) \cdot \underset{= 1}{\underbrace{\det \begin{pmatrix} 1 & 0 \\ 0 & 1\end{pmatrix}}}$$
 
> [!Proposición 1.]
> Una matriz $A \in M_{2 \times 2}(\mathbb{K})$ es invertible si y sólo si su determinante es distinto de 0. 

**Demostración.** ($\Rightarrow$) Supongamos que $A = \begin{pmatrix}a & b \\ c & d \end{pmatrix}$ es invertible si y solo si $T_A(x) = Ax$ entonces $\mathrm{Im}(T_A) = \mathbb{K}^2$ (es decir es un epimorfismo, visto en [[La Imagen y el Núcleo de una TL]]). Lo que a su vez quiere significar que el rango de la matriz $A$ es 2, es decir tanto las filas como las columnas forman una base en $\mathbb{K}^2$. Entonces, $(a,b), (c,d)$ queremos probar que es una lista de vectores LI. Luego $\exists \lambda_1, \lambda_2 \in \mathbb{K}$ tal que 
$$\lambda_1(a,b) + \lambda_2(c,d) = 0 \implies \begin{cases} \lambda_1a + \lambda_2c = 0 \\ \lambda_1b + \lambda_2 d = 0\end{cases}$$
Podemos dividir la solución del sistema en 2 casos: (1) si $a \neq 0$ y (2) si $a = 0$. 
1. Si $a \neq 0$, supongamos que $\lambda_2 \neq 0$ y que por lo tanto podemos despejar de la primera ecuación $\lambda_1 = - \frac{\lambda_2 c}{a}$ y reemplazarlo en la segunda tal que $- \frac{\lambda_2 c}{a}b + \lambda_2 d = 0 \rightarrow \lambda_2 \Big(\frac{-cb}{a} + d\Big) = 0 \rightarrow \frac{\lambda_2}{a} (ad - cb) = 0 \rightarrow ab-cd = 0$ . Lo cual es lo opuesto a lo que queríamos probar, por lo tanto cuando $\lambda_2 =0 = \lambda_1$ entonces $ab-cd \neq 0$. 
2. Si $a = 0$, veamos que nos queda $\lambda_2 c = 0$. Si $c = 0$, entonces el $\mathrm{rg}(A) \leq 1$ lo cual es un absurdo, así que este caso no puede pasar. Si $c \neq 0$, entonces $\lambda_2 = 0$ y nos queda únicamente $\lambda_1 b = 0$. Por último si $\lambda_1 \neq 0$ nos queda que $b= 0$ y $ab-bc = 0$. Lo cual es lo opuesto a lo que queríamos demostrar, por lo tanto cuando $\lambda_1 = \lambda_2 = 0$ entonces $ad-cb \neq 0$. 
($\Leftarrow$) Suponiendo que $\det(A) = ad-cb \neq 0$ entonces (por lo desarrollado anteriormente) tenemos que $(a,b), (c,d)$ son LI. Luego, tenemos que generan un base y que el rango de la matriz $A$ es 2, por lo tanto es invertible. $\blacksquare$




[^1]: Notemos que para algunos espacios vectoriales, específicamente para las matrices, es necesario definir $f({v}) = {v}^t \cdot {w}$ para poder hacer la multiplicación de matrices.  
[^2]:  No es necesario entender esto ahora mismo, solo piénselo como un producto ya definido que multiplica los elementos del espacio vectorial entre sí, por ejemplo la multiplicación de matrices en el espacio vectorial $M_{m \times n}(\mathbb{K})$ ó el conocido "producto escalar" definido para $\mathbb{R}^3$ y $\mathbb{R}^2$. 