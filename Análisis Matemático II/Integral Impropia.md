La [[Integral de Riemann]] con la que nosotros siempre trabajamos, hasta ahora esta definida en un intervalo acotado y para una función acotada, pero ahora veremos que ocurre cuando queremos encontrar una integral de este tipo 
$$\int_{a}^{\infty} f(x) dx$$
En este caso lo que queremos preguntar es cual es el área de la función en $[a, \infty)$._¿Como abordamos este tipo de funciones?_ Veamos un ejemplo.
$$\int_0^{\infty} \frac{1}{1+x^2} dx = \fbox{?}$$
Veamos que lo que nos están preguntando es cual es el área de la función en el intervalo $[0, \infty)$. Por ahora, no tenemos definida este tipo de integral, si lo pensamos una manera de resolverlo sería "haciandola acordada", es decir llamar a la parte más grande del intervalo un número $b \in \mathbb{R}$ que se va haciendo *cada vez más grande*. Eventualmente, luego queríamos encontrar que sucede cuando $b \rightarrow \infty$ por lo cual tomamos el [[Límite Infinito de Funciones]] y nos queda
$$\lim_{b \rightarrow \infty} \int_{0}^b \frac{1}{1+x^2} dx$$
Entonces, para encontrar una solución debemos resolver la integral primero, y luego calcular el límite:
$$\lim_{b \rightarrow \infty} \int_{0}^b \frac{1}{1+x^2} dx = \lim_{b \rightarrow \infty} \Big[ \arctan x \Big|_{x=0}^{x=b}\Big]  = \lim_{b \rightarrow \infty} \Big[ \arctan b - \underset{= 0}{\arctan 0} \Big] = \lim_{b \rightarrow \infty} \arctan b = \boxed{\frac{\pi}{2}}$$

---
> #Definición **Integral Impropia (Tipo 1)** 
> Sea $a \in \mathbb{R}$ y sea $f$ una función $[a, \infty) \rightarrow \mathbb{R}$ con la propiedad de ser integrable en el intervalo $[a, b]$, $\forall a < b$ . Se define $$\int_a^{\infty} f(x)dx = \lim_{b \rightarrow \infty} \int_a^b f(x) dx$$ Asumiendo que el límite existe. Analogamente, fijando $b \in \mathbb{R}$ con una función $f: (-\infty, b] \rightarrow \mathbb{R}$ integrable en $[a,b]$, $\forall a<b$. Se define $$\int_{-\infty}^b f(x)dx = \lim_{a \rightarrow - \infty} \int_a^b f(x)dx$$

- Se dice que la integral es **Convergente** si el límite existe y es finito.
- Se dice que la integral es **Divergente** si el límite no existe o existe y no es finito.

De esta manera, podemos resolver la siguiente integral aplicando los métodos anteriores
$$\begin{align}
 \int_0^{\infty} \frac{x}{1+x^2} dx &= \lim_{b \rightarrow \infty}\int_{0}^b \frac{x}{1+x^2}dx  & (1) \\
& = \lim_{b \rightarrow \infty} \frac{1}{2} \int_{0}^b \frac{2x}{1+x^2} dx \quad\quad\;\;  & (2)\\
& = \lim_{b \rightarrow \infty} \frac{1}{2} \ln |x^2 + 1| \Big|_{x=0}^{x=b} \quad \quad  & (3)\\
& = \lim_{b \rightarrow \infty} \Big[ \frac{1}{2}\ln |b^2 + 1| - \frac{1}{2} \ln |1|\Big] & (4)\\
& = \lim_{b \rightarrow \infty} [\frac{1}{2}\ln|b^2 + 1|] = \underset{\text{DIVERGE}}{\boxed{\infty}} & (5) 
\end{align}$$
En (1) usamos la definición de arriba, luego en (2) mult. y div. por 2 para poder aplicar el método de sustitución (visto en [[Métodos Básicos de Integración]]) $u = x^2 + 1 \rightarrow du = 2x dx$. Entonces, en (3) $\int \frac{1}{u}du = \ln |u| + C$ y en (4) simplemente aplicamos la Regla de Barrow (vista en [[Teorema Fundamental del Cálculo]]). Por último en (5) resolvemos el límite teniendo en cuenta que $\lim_{x \rightarrow \infty} \ln |x| = \infty$ . 

Observe como las funciones son parecidas, pero una converge y la otra no, lo cual nos hace preguntarnos _¿Existe una forma de predecir si una función tiene área convergente?_ pues a veces encontrar la integral y resolver el límite se puede hacer muy complicado para funciones más dificiles y nos sirve mucho saber de antemano si la función es convergente o no para no perder nuestro tiempo en calcularla.
Primero, para responer esta pregunta analicemos que sucede con las áreas de $\int_1^{\infty} \frac{1}{t} dt$ y $\int_1^{\infty} \frac{1}{t^2}dt$. 
$$\int_1^{\infty} \frac{1}{t^2}dt = \lim_{b \rightarrow \infty} \int_1^b \frac{1}{t^2} dt = \lim_{b \rightarrow \infty} \int_1^b t^{-2}dt = \lim_{b \rightarrow \infty} -\frac{1}{t} \Bigg|_{x=1}^{x=b}= \lim_{b \rightarrow \infty} -\frac{1}{b}+1 = \boxed{1}$$
Pero en cambio,
$$\int^\infty_1 \frac{1}{t}dt = \lim_{b \rightarrow \infty} \int_1^b \frac{1}{t} dt = \lim_{b \rightarrow \infty} \ln(t)\Bigg|_{x=1}^{x=b} = \lim_{b \rightarrow \infty} \ln(b) -1 = \underset{\text{DIVERGE}}{\boxed{\infty}}$$
![[Pasted image 20221013095734.png]]
Observe como el área debajo de $1/x^2$ se va "atachando" mucho más rápido que $1/x$. Más adelante vamos a aprender a usar esto para encontrar si una función tiene área convergente. 

---
Ahora que podemos calcular áreas en intervalos no acotados, una nueva pregunta puede surgir al lector _¿Puedo calcular el área debajo de toda mi función?_ Resulta que en ocasiones si podemos, definamos un nuevo tipo de integral impropia:
> #Definición **Integrales Impropias (Tipo 2)** Supongamos $f : \mathbb{R} \rightarrow \mathbb{R}$ una función integrable en $[a,b]$, $\forall a > b$. Y sea un $c \in \mathbb{R}$ fijo, definimos $$\int_{-\infty}^{\infty} f(x)dx = \lim_{a \rightarrow -\infty} \int_a^c f(x)dx + \lim_{b \rightarrow \infty} \int_c^b f(x)dx$$Asumiendo que ambos límites existen y son finitos.

Usted podría llegar a pensar que una mejor definición para esta integral podría ser $\int_{-\infty}^{\infty}f(x)dx = \lim_{R \rightarrow \infty} \int_{-R}^R \int f(x)dx$. El siguiente ejemplo nos mostrará porque esta definición no nos sirve para resolver la integral.
Calculemos el área de $\int_{-\infty}^{\infty}xdx$. Es tentador pensar que como al separar esta integral en 2: $\int_{-\infty}^{\infty}xdx = \int_{-\infty}^{0}xdx + \int_{0}^{\infty}xdx$ por ejemplo de esta manera, la primera integral es negativa y la segunda es positiva, entonces por simetría $\int_{-\infty}^{\infty}xdx = 0$. O también si calculamos la integral usando nuestra "definición erronea" obtenemos:
$$\int_{-\infty}^{\infty}xdx = \lim_{R \rightarrow \infty} \int_{-R}^R xdx = \lim_{R \rightarrow \infty} \frac{x^2}{2}\Bigg|_{x = -R}^{x=R} = \lim_{R \rightarrow \infty} \frac{R^2}{2} - \frac{R^2}{2} = 0$$
Pero si tomaramos por ejemplo la siguiente integral tendría que valer lo mismo pero no lo hace:
$$\int_{-\infty}^{\infty}xdx = \lim_{R \rightarrow \infty} \int_{-R+1}^{R+1} xdx = \lim_{R \rightarrow \infty} \frac{x^2}{2}\Bigg|_{x = -R+1}^{x=R+1} = \lim_{R \rightarrow \infty} \frac{(R+1)^2}{2} - \frac{(1-R)^2}{2} = \infty$$
Lo cual nos muestra que la definición no es la forma correcta de resolver el problema. 
Volviendo a nuestra definición original, no estamos analizando si los límites de ambas integrales existen. **Si al menos uno de los dos límites no existe o tiende a infinito entonces la integral impropia de tipo 2 diverge**. 
$$\int_{0}^{\infty}xdx = \lim_{b \rightarrow \infty} \int_0^b xdx = \lim_{b \rightarrow \infty} \frac{b^2}{2} = \infty$$
Entonces, como ya una de las dos integrales diverge, la integral $\int_{-\infty}^{\infty}xdx$ diverge también.

---
Veamos que existen otras áreas que nos puede interesar encontrar son por ejemplo $\int_0^1 \frac{1}{x} dx$, es decir de funciones que tienen al infinito en un punto, para esto definimos:
 > #Definición  **Integrales Impropias (Tipo 3)** Sea $f: (a,b] \rightarrow \mathbb{R}$ una función con la propiedad de ser integrable en $[c,b]$ para todo $c \in (a,b)$. Se define $$\int_a^b f(x)dx = \lim_{c \rightarrow a^+} \int_c^b f(x)dx$$Analogamente, si $f : [a,b) \rightarrow \mathbb{R}$ una función 

Para esto calculemos el área entonces de $\int_0^1 \frac{1}{x}dx$ 
$$\int_0^1 \frac{1}{x}dx = \lim_{c \rightarrow 0^+} \int_c^1 \frac{1}{x}dx = $$

