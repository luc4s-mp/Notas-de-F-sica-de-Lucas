![[Pasted image 20221202095039.png]]
(a) Las nueve propiedades de un cuerpo son
1. **Propiedad Conmutativa.** Si $a,b \in \mathbb{R}$se cumple $a+b = b+a$ y $ab = ba$.
2. **Propiedad Asociativa.** Si $a,b \in \mathbb{R}$ se cumple $a+ (b+c) = (a+b) + c$ y $a(bc) = (ab)c$.
3. **Propiedad del Neutro de la suma.** Si $a \in \mathbb{R}$ existe un número $0 \in \mathbb{R}$ tal que $a+0 = a$. 
4. **Propiedad del opuesto de la suma.** Si $a \in \mathbb{R}$ existe un número $-a \in \mathbb{R}$ tal que $a+(-a) = 0$.
5. **Propiedad del Neutro de la multiplicación.** Si $a \in \mathbb{R}$ existe un número $1 \in \mathbb{R}$ tal que cumpla $a \cdot 1 = a$.
6. **Propiedad del inverso multiplicativo.** Si $a \in \mathbb{R}$ existe un número $a^{-1} \in \mathbb{R}$ tal que $a \cdot (a^{-1})$.
7. **Propiedad Distributiva.** Si $a,b,c \in \mathbb{R}$ se cumple que $a \cdot (b+c) = a \cdot b + a \cdot c$.

(b) Queremos demostrar que $a \cdot 0 = 0$. Veamos que por la propiedad (4) se cumple que existe un número $-(a \cdot 0) \in \mathbb{R}$ tal que $a \cdot 0  + (- (a \cdot 0)) = 0$ . Luego, $0 = 0 + 0$ por la propiedad (3) por lo que $a \cdot (0 + 0) + (-(a \cdot 0)) = 0$ y por la propiedad (7) tenemos que $a \cdot 0 + \underset{= \; 0}{\underbrace{a \cdot 0 + (-a \cdot 0)}} = 0$ y nos queda $a \cdot 0 = 0$. $\blacksquare$
Queremos demostrar que $a \cdot (-b) = -(a \cdot b)$. Notemos que $b + (-b) = 0$  por la propiedad (4) por lo que $a \cdot (b + (-b)) = a \cdot 0$ que ya vimos que $a \cdot 0 = 0$. Usando esto y la propiedad (7) nos queda que $a \cdot b + a \cdot (-b) = 0$ y luego por la propiedad uniforme de la igualdad podemos sumar de ambos lados por $-(a \cdot b)$ tal que nos quede $\underset{=\;0}{\underbrace{(a \cdot b) + (-(a \cdot b))}} + (a \cdot (-b)) = -(a \cdot b)$ por lo tanto $a \cdot (-b) = -(a \cdot b)$. $\blacksquare$

![[Pasted image 20221202102640.png]]
(a) Las 4 propiedades son: sean $a, b, c \in \mathbb{R}$ 
1. **(Propiedad de Tricotomía)** Pueden ocurrir 3 situaciones: $a < b$, $a=b$ o $a > b$. 
2. **(Propiedad de transitividad)** Si $a < b$ y $b<c$ entonces $a<c$
3. **(Propiedad de la Cerradura)** Si $a < b$ entonces $a+c < b+c$ y con $c >0$ se cumple $ac < bc$.

(b) Queremos probar que $1 > 0$. Notemos que pueden haber 3 situaciones por la propiedad de orden (1), $1 > 0$, $1 < 0$ y $1 = 0$. Es obvio que $1 \neq 0$, para probar que $1 > 0$ supongamos por el absurdo que $1 < 0$. Si $1 < 0$ entonces podemos usar la propiedad de orden (3) tal que $1 + (-1) < 0 + (-1)$. Pero luego tenemos que $0 < -1$ nos están diciendo entonces que $-1$ es un número positivo, por lo que podemos usar la propiedad de orden (3) de nuevo en $1 < 0$ tal que $(-1) \cdot 1 < (-1) \cdot 0$ pero luego por la segunda propiedad prbada en el ejercicio 1(b) tenemos que -(1 \cdot 1) < 0$ y por la propiedad (5) $1 \cdot 1 = 1$ por lo que $-1 < 0$ y llegamos a un absurdo porque antes habiamos obtenido que $0 < -1$. Por lo que no queda otra opción que $1 > 0$. $\blacksquare$

![[Pasted image 20221202104418.png]]
(a) Sea $x \in \mathbb{R}$ definimos al **valor absoluto** de $x$ a 
$$|x| = \begin{cases}
x & x \geq 0 \\
-x & x < 0
\end{cases}$$
(b) Para demostrar que $|x+y| \leq |x| + |y|$ consideremos los 4 casos:
$$\begin{align}
x \geq 0 \text{ y } y \geq 0  &  \quad (1)\\
x < 0 \text{ y } y \geq 0 & \quad (2) \\
x \geq 0 \text{ y } y < 0 & \quad (3) \\
x < 0 \text{ y } y < 0 &  \quad (4) \\
\end{align}$$
- Consideremos el caso (1) es obvio que entonces $|x+y| = x+y = |x| + |y|$, luego llegamos a lo que queríamos. 
- En el caso (2) $|x| + |y| = -x + y = y-x$ queríamos demostrar entonces que $|x+y| \leq y-x$. Lo cual se puede dividir en dos subcasos:
	- $x+y \geq 0$, entonces $x+y \leq y-x$. Nos basta probar que $x \leq -x$ lo cual es verdad pues $x < 0$ y $-x > 0$. 
	- $x+y \leq 0$, entonces $-x-y \leq y-x$. Nos basta probar que $-y \leq y$ lo cual es verdad pues $y>0$ y $-y < 0$.
- En el caso (3) $|x| + |y| = x-y$ de vuelta para probar $|x+y| \leq x-y$ podemos dividirlo en dos subcasos:
	- $x+y \geq 0$, entonces $x+y \leq x-y$. Nos basta probar que $y \leq -y$ lo cual es verdad pues $y < 0$ y $-y > 0$. 
	- $x+y \leq 0$, entonces $-x-y \leq x-y$. Nos basta probar que $-x \leq x$ lo cual es verdad pues $x>0$ y $-x < 0$.
- Por último, el caso (4) es obvio pues $|x+y| = -x-y = |x| + |y|$. $\blacksquare$

![[Pasted image 20221202110505.png]]
(a) Si $A \subset \mathbb{R}$. Decimos que este conjunto está **acotado superiormente** si existe un número $M \in \mathbb{R}$ (llamado **cota superior**) tal que para todo $a \in A$ tenemos que $a \leq M$. Por otro lado, por el [[Axioma del supremo y el ínfimo]] sabemos que todo conjunto acotado superiormente tiene **supremo** que se define como la *menor cota superior*. Decimos que $\alpha = \sup A$ si:
- $\alpha$ es una cota superior.
- Sea $M$ una cota superior, $\alpha \leq M$.

(b) Probemos esto por el absurdo. Supongamos que existe una cota superior $M$ de $\mathbb{R}$, entonces tiene supremo que le llamamos $\alpha = \sup \mathbb{R}$ por lo que cumple que $\alpha \geq r$ para todo $r \in \mathbb{R}$ pero luego sabemos que $M \in \mathbb{R}$ (por definición de la cota) por lo tanto $M \leq \alpha \leq r$ por lo que se genera un absurdo, $\alpha$ no puede ser el supremo. Y $\mathbb{R}$ no está acotado superiormente. $\blacksquare$

(c) **Propiedad del supremo.** Sea $A \subset \mathbb{R}$ tenemos que si existe una cota superior $M \in \mathbb{R}$ entonces existe un supremo del conjunto $A$. 

(d) Queremos probar que $\sup [0,6) = 6$. Es obvio que $6$ es una cota superior, entonces el conjunto $[0, 6)$ tiene supremo. Sabemos que $0 \geq x < 6$ entonces $0 < 6-x$, luego por la propiedad arquimediana existe un $n_0 \in \mathbb{N}$ tal que $0 < \frac{1}{n_0} < 6-x$. Podemos reordenar esto, $x < 6- \frac{1}{n_0} < 6$ por último por el lema útil sabemos que $6-\frac{1}{n_0} \in [0,6)$ entonces $6$ es el supremo del conjunto. 

![[Pasted image 20221203092758.png]]
(a) Decimos que $m \in \mathbb{R}$ es una **cota inferior** del conjunto $A$ si para todo $a \in A$ ocurre que $m \leq a$. 
Decimos que $\beta \in \mathbb{R}$ es un **ínfimo o la mayor cota inferior** del conjunto $A$ si:
- $\beta$ es una cota inferior.
- Si $m$ es otra cota inferior se cumple que $\beta \geq m$.

(b) Sea $A \subset \mathbb{R}$ no vacío acotado inferiormente, queremos demostrar que tiene ínfimo. Creemos el conjunto $-A = \{-a | a \in A\}$ que contiene todos los opuestos de los valores de A, este es no vacío también pues A es no vacío. El conjunto $-A$ está acotado superiormente pues si $m$ es una cota inferior de $A$ tenemos que $-m$ va a ser una cota superior de $-A$. Luego, por la propiedad del supremo existe el $\sup (-A)$. Nos faltaría probar que 
$$\inf (A) = -\sup(-A)$$
Como existe $\alpha = \sup(-A)$ entonces $\alpha \geq -a$ para todo $a \in A$, luego multiplicando por -1 de ambos lados $-\alpha \leq a$ tal que tenemos que $-\alpha$ es una cota inferior de $A$. Siguiendo si $-m$ es una cota superior de $-A$ se cumple que $-m \geq \alpha$, entonces $m \leq -\alpha$ y como $-\alpha$ es una cota inferior de $A$, $m$ es una cota inferior. Como podemos hacer esto con todas las cotas superiores de $-A$ tenemos que $\inf(A) = -\alpha = - \sup(-A)$. $\blacksquare$

(c) Queremos probar que $\mathbb{N}$ no está acotado superiormente. Empecemos suponiendo que sí lo está, en ese caso existe un supremo $\alpha = \sup \mathbb{N}$ 
luego como $\alpha$ es una cota superior, entonces $\alpha \geq n$ para todo $n \in \mathbb{N}$. Pero luego, $\alpha \geq n+1$ también se cumple, entonces $\alpha -1 \geq n$ tal que $\alpha -1$ es una cota superior, pero acá llegamos a un absurdo pues $\alpha$ es la menor cota superior. $\blacksquare$

(d) **Propiedad Arquimediana.** Queremos probar que para todo $\epsilon > 0$ existe un $n \in \mathbb{N}$ tal que $\frac{1}{n} < \epsilon$. Podemos obtener esto como un colorario de la proposición anterior. Si $\frac{1}{\epsilon} > 0$ entonces como los números naturales no están acotados superiormente $\frac{1}{\epsilon}$ no es una cota superior por lo que debe existir un número natural que supere este número $n > \frac{1}{\epsilon} \rightarrow \frac{1}{n} < \epsilon$. $\blacksquare$

(e) Decimos que un conjunto $A$ es **denso en $\mathbb{R}$** cuando dado un intervalo $(a,b)$ de los reales existe un $x \in A$ que a su vez $x \in (a,b)$. O de otra manera, dados $a < b$ existe un $x \in A$ tal que $a<x<b$.

![[Pasted image 20221203104148.png]]
(a) Una función $f:A \rightarrow B$ es **inyectiva** cuando para todo $a,b \in A$, si $f(a) = f(b)$ se cumple que $a=b$.
(b) la **imagen** de la función $f:A \rightarrow B$ es un subconjunto de $B$ tal que $\mathrm{Im}(f)=\{f(t): t \in A\}$. 
(c) Una función $f:A \rightarrow B$ es **sobreyectiva** cuando la $\mathrm{Im}(f) =B$. 

![[Pasted image 20221203105521.png]]
(a) Una función $f: A \rightarrow B$  y otra función $g: C \rightarrow D$ tal que $B \subset C$. Se define una nueva función
$$g \; \mathrm{o} \; f: A \rightarrow D \quad \quad (g \; \mathrm{o} \; f)(x) = g(f(x))$$

(b) Una función $f: A \rightarrow B$ sobreyectiva e inyectiva. Definimos la función $f^{-1}: B \rightarrow A$ como aquella función $f()