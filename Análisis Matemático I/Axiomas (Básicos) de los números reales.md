Nos planteamos las siguientes preguntas, de manera ingenua: ¿Por qué
$$
x^3+1=(x+1)\left(x^2-x+1\right)
$$
se cumple para cualquier número $x$ ?
¿Por qué el resultado de sumar dos números no cambia si se cambia el orden al sumarlos?
El tema que nos ocupa es, en general y de manera informal, cuándo debemos esperarnos en dar una respuesta explicada o, por el contrario, nos conformamos con responder simplemente "Porque sí". La última posibilidad la aceptaríamos solo para propiedades muy básicas. Pero, ¿cuáles serían las propiedades básicas? Para poder probar proposiciones necesitamos una base de la cual partir de la cual podamos decir "a partir de esto que yo asumo que es verdadero obtenego todo el resto", a estas propiedades las llamamos "axiomas".

Podemos definir a todos los números reales como aquellos números que cumplen una cierta cantidad de propiedades o "axiomas"[^1]. Dados tres números $a, b, c \in \mathbb R$ se cumple que:

> **Propiedades de la suma**
> - (P1) Asociatividad: $(a+b)+c = a+(b+c)$
> - (P2) Existencia y unicidad del elemento neutro: $a+0 = 0+a = a$ 
> - (P3) Existencia y unicidad del opuesto: $a+(-a)=(-a)+a$
> - (P4) Conmutatividad: $a+b = b+a$

> **Propiedades de la múltiplicación**
> - (P5) Asociatividad: $(a \cdot b) \cdot c = a \cdot (b \cdot c)$
> -  (P6) Existencia y unicidad del elemento neutro: $a \cdot 1 = 1 \cdot a = a$
> - (P7) Existencia y unicidad del inverso: $a \cdot a^{-1} = a^{-1} \cdot a$
> - (P8) Conmutatividad: $a \cdot b = b \cdot a$

**Propiedades que relacionan las operaciones suma y producto**
- (P9) Propiedad distributiva: $a \cdot (b + c) = a \cdot b + a \cdot c$ 

En general a todos los conjuntos números que cumplen las 9 propiedades de arriba se los llama **cuerpo**.

> **Proposición**
> 1.  $-(-a)=a$ para todo $a \in \mathbb{R}$.
> 2.  $\left(a^{-1}\right)^{-1}=a$ para todo $a \in \mathbb{R}, a \neq 0$.
> 3.  $a \cdot 0=0$ para todo $a \in \mathbb{R}$.
> 4. Si $a \neq 0$ y $a \cdot b=a \cdot c$ entonces $b=c$.
> 5.  Si $a \cdot b=0$ entonces $a=0$ o $b=0$.
> 6.  $-(a \cdot b)=(-a) \cdot b=a \cdot(-b)$ para todo $a, b \in \mathbb{R}$.
> 7. $(-a) \cdot(-b)=a \cdot b$ para todo $a, b \in \mathbb{R}$.

**Demostración.**
- Inciso (1). Sabemos que $(-a)+a=0$ por P3. Además, aplicando P3 a $(-a)$, tenemos que $(-a)+(-(-a))=0$. Ahora, según P3, hay un único opuesto para $(-a)$, por lo tanto $a=(-(-a))$.
- Inciso (2). Sabemos que $(a^{-1}) \cdot a = 1$ por P7. Además, aplicando P7 a $(a^{-1})$, tenemos que $(a^{-1}) \cdot (a^{-1})^{-1} = 1$. Ahora, según P7, hay un único opuesto para $(a^{-1})$, por lo tanto $a = (a^{-1})^{-1}$.
- Inciso (3). Sabemos que $0=0+0$ por P2. Entonces, por P9 $a \cdot 0=a \cdot(0+0)=a \cdot 0+a \cdot 0$. Luego.
$$
\begin{aligned}
(-a \cdot 0+a \cdot 0) &=(-a \cdot 0+a \cdot 0)+a \cdot 0 \quad \leftarrow\mathrm{P} 1 \\
0 &=0+a \cdot 0 \quad \quad \leftarrow \text { usamos P3 } \\
0 &=a \cdot 0 \quad \leftarrow \text { usamos } \mathrm{P} 2
\end{aligned}
$$
Luego, $0=a \cdot 0$. Listo!
- Inciso (4). Si $a \neq 0$ y $a \cdot b=a \cdot c$, entonces
$$
\begin{aligned}
a^{-1} \cdot a \cdot b &=a^{-1} \cdot a \cdot c \\
\left(a^{-1} \cdot a\right) \cdot b &=\left(a^{-1} \cdot a\right) \cdot c \leftarrow  \mathrm{P5} \\
1 \cdot b &=1 \cdot c \quad \leftarrow \text { usamos } \mathrm{P} 7 \\
b &=c \quad \leftarrow \text { usamos P6,  Listo! }
\end{aligned}
$$
- Inciso (5). Supongamos que $a \cdot b=0$.
	Primero, si $a=0$, Listo! por inciso (3).
	Ahora, si $a \neq 0$, entonces
$$
\begin{aligned}
a^{-1} \cdot a \cdot b &=a^{-1} \cdot 0 \\
\left(a^{-1} \cdot a\right) \cdot b &=a^{-1} \cdot 0 \quad \leftarrow \text { P5 } \\
1 \cdot b &=0 \quad \leftarrow \text { usamos P7 e inciso (3) } \\
b &=0 \quad \leftarrow \text { usamos P6, Listo! }
\end{aligned}
$$
- Inciso (6)

## Propiedades de Ordenación
Las tres propiedades básicas de los números que faltan por enunciar hacen referencia a las desigualdades. Aunque las desigualdades se presentan pocas veces en las matemáticas elementales, desempeñan un papel destacado en el análsis matemático. Los números $a \in \mathbb{R}$ que satisfacen $a > 0$, se llaman **positivos**, mientras que los números $a$ que satisfacen $a < 0$, se llaman **negativos**. Mientras que la positividad puede definirse así en términos de $<$, es posible invertir el proceso $a < b$ quiera significar que $a - b$ es positivo.  Dado $P = \{a \in \mathbb R : a > 0\}$ el conjunto de todos los números positivos:

> **Propiedades de $P$** 
> - (P10) Ley de tricotomía: Si $a \in \mathbb R$, entonces se cumple alguna de las siguientes condiciones, $a \in \mathbb P$, $a = 0$ o $-a \in P$
> - (P11) *La suma es cerrada en $\mathbb P$*, es decir $a + b \in P$
> - (P12) *El producto cerrado en $\mathbb P$*, es decir $a \cdot b \in P$

P10 es una propiedad muy importante en los números, podemos concluir algunas proposiciones de ella, tal como:
- $a > b$ se cumple que $a - b \in P$
- $a < b$ se cumple que $b > a$. 
- $a \geq b$ se cumple que $a > b$ o $a = b$.
- $a \leq b$ se cumple que $a < b$ o $a = b$.

El hecho de que sea $-a > 0$ si $a < 0$ es la base de un concepto que va a desempeñar un papel muy importante en el análisis. 
Una afirmación que los alumnos de matemática elemental se han cansado de repetir es el hecho de que **menos por menos es más**, ¿Cómo podemos demostrar esoto usando nuestras propiedades que definimos de los números? Queremos ver entonces que si $a < 0$ y $b < 0$ entonces $ab >0$. Tenemos que $-a \in {P}$ y $-b \in {P}$, en consecuencia por la P12 (multiplicación es cerrada), $(-a)(-b) = ab \in {P}$. Y llegamos a lo queríamos.   La demostración de que si $a>0$ y $b>0$ entonces $ab>0$ es más sencilla todavía.
Otro resultado que es muy común que los estudiantes repitan sin saber es que _al multiplicar por un número negativo en una desigualdad esta "se da vuelta"_, probemos esto también. Queremos ver entonces que dado $a<b$ y $c < 0$ tenemos que $ac > ab$, primero veamos que $a-b \in {P}$ y $-c \in P$ entonces por P12 $(-c)(b-a)= -(cb)-(-(ca))= ca-cb \in P$ por último esto significa que $ca - cb > 0 \rightarrow ca > cb$ que es lo que queríamos probar.
Teniendo estas dos últimas proposiciones en cuenta podemos resolver inecuaciones como 
$$\frac{-2x+8}{x-2} > 0$$
Para resolverla concideramos los casos en los que $-2x+8>0$ y $x-2 > 0$ ó $-2x+8 < 0$ y $x-2 <0$ por la proposición que nos dice que si $a >0$ y $b>0$ ó $a < 0$ y $b < 0$ entonces $ab>0$. Para el primer caso tenemos que $x<4$ y $x>2$ ó $4<x<2$ y para el segundo tenemos que $x>4$ y $x<2$, es obvio que no existe un número que cumpla esto entonces las soluciones de esta inecuación son $\{x \in \mathbb{R} : 2<x<4\}$. 

## Valores Absolutos
> #Definición **(Valor Absoluto)** Para todo número $a$ definimos el **valor absoluto** $|a|$ dea $a$ como sigue: $$|a| = \begin{cases}
a, & a \geq 0 \\
-a, & a \leq 0
\end{cases}$$

En general, el método más directo para afrontar problemas con valor absoluto requiere de la consideración por separado de distintos casos, puesto que ya para empezar los valores absolutos han sido definidos por casos.

> **Teorema. (Desigualdad Triangular)** $\forall a, b \in \mathbb{R}$ se tiene que $$ |a+b| \leq |a| + |b|$$

**Demostración**. Vamos a considerar cuatro casos: (1) $a \geq 0, \quad b \geq 0$; (2) $a \geq 0, \quad b \leq 0$; (3) $a \leq 0, \quad b \geq 0$; y (4) $a \leq 0, b \leq 0$.
En el caso (1) tenemos también $a+b \geq 0$ y el teorema es evidente; en efecto,
$$
|a+b|=a+b=|a|+|b|,
$$
de modo que en este caso se cumple la igualdad.
En el caso (4) se tiene $a+b \leq 0$ y de nuevo se cumple la igualdad:
$$
|a+b|=-(a+b)=-a+(-b)=|a|+|b| .
$$
En el caso (2), cuando $a \geq 0$ y $b \leq 0$, debemos demostrar que
$$
|a+b| \leq a-b .
$$
Este caso puede dividirse, por lo tanto, en dos subcasos. Si $a+b \geq 0$, entonces tenemos que demostrar que $a+b \leq a-b$, es decir, $b \leq-b$
lo cual se cumple ciertamente puesto que $b$ es negativo $\mathrm{y}-b$ positivo. Por otra parte, si $a+b \leq 0$ debemos demostrar que $-a-b \leq a-b$ , es decir, $-a \leq a$ lo cual es verdad puesto que $a$ es positivo y $-a$ negativo.

Nótese finalmente que el caso (3) puede despacharse sin ningún trabajo adicional aplicando el caso (2) con $a$ y $b$ intercambiados. $\blacksquare$ 

Otra propiedad interesante que se puede demostrar de los valores absolutos es que dados $x,y \in \mathbb{R}$ tenemos que $|xy| = |x||y|$.

Veamos por ejemplo:
$$|x-2| < 8 \implies \begin{cases}
x-2 < 8 & \text{ si } x-2 > 0 \\
-(x-2) < 8 & \text{ si } x-2 < 0 \\
\end{cases} \implies \begin{cases}
x < 10 & \text{ si } x > 2 \\
x > -6 & \text{ si } x < 2 \\
\end{cases}$$
Luego, tenemos que $-6 < x < 10$ son soluciones a esta inecuación. Si lo pensamos geométricamente el módulo de $|x-a|$ representa la **distancia a un punto**, ahora observando el ejemplo anterior, lo que estamos pidiendo son todos los puntos de la recta real cuya distancia desde $2$ sea menor a $8$. 

Para el desarrollo de futuras notas va a ser fundamental que entendamos que significa que un número este "cerca" de otro. Una definición razonable es que dado un número $\epsilon \in \mathbb{R}, \empsilon > 0$ muy chico decimos que un número $x$ está cerca de $x_0$ cuando la _"distancia"_ entre estos dos números es menor a $\epsilon$, es decir cuando $x$ cumple la inecuación $|x-x_0| < \epsilon$.