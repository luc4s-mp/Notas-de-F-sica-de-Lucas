# Repaso Teórico - Análisis Matemático I
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

> [!DEFINICIÓN]
> (a) Sea una función $f: A \rightarrow B$  y otra función $g: C \rightarrow D$ tal que $B \subset C$. Se define una nueva función, llamada **función compuesta**
$$g \; \mathrm{o} \; f: A \rightarrow D \quad \quad (g \; \mathrm{o} \; f)(x) = g(f(x))$$

> [!DEFINICIÓN]
> (b) Una función $f: A \rightarrow B$ sobreyectiva e inyectiva. Definimos la función **inversa** $f^{-1}: B \rightarrow A$ como aquella función tal que si $f(x) = y$, entonces $f^{-1}(y) = x$ siendo este $x$ único. 

(c) El gráfico de una función inversa $f^{-1}$ es el mismo gráfico que $f$ pero reflejado sobre la función identidad $I(x) = x$. 
(d) Sea $\sin : [-\frac{\pi}{2}, \frac{\pi}{2}] \rightarrow [-1,1]$ y $\cos : [0, \pi] \rightarrow [-1,1]$ dos funciones inyectivas y sobreyectivas, son invertibles. Las funciones $\arcsin : [-1,1] \rightarrow  [-\frac{\pi}{2}, \frac{\pi}{2}]$ y $\arccos : [-1,1] \rightarrow  [0, \pi]$ son sus inversas.

![[Pasted image 20221203151132.png]]
Definimos a estas funciones como
$$(f+g)(x) = f(x) + g(x) \quad \quad (f \cdot g)(x) = f(x)g(x) \quad \Big(\frac{f}{g}\Big)(x) = \frac{f(x)}{g(x)} \; (\text{con } g(x) \neq 0)$$
![[Pasted image 20221203151603.png]](a) Una sucesión es una función definida como $a: \mathbb{N} \rightarrow \mathbb{R}$. 

> [!DEFINICIÓN]
> (b) #Definición  Se dice que una sucesión es **convergente** o tiene límite cuando siendo un $l \in \mathbb{R}$ nuestro límite cumple que para todo $\epsilon > 0$ existe un $N \in \mathbb{N}$ tal que $|a_n - l| < \epsilon$ para todo $n > N$. 

(c) Queremos verificar por definición que
$$\lim_{n \rightarrow \infty} \frac{3n+4}{n} = 3 \iff \forall \epsilon > 0, \exists N \in \mathbb{N} : \Big|\frac{3n+4}{n} - 3\Big| < \epsilon, \forall n > N$$
Buscamos un $N$ tal que cumpla lo de arriba. Analicemos lo que ocurre dentro del módulo:
$$\Bigg|\frac{3n+4}{n} - 3 \Bigg| = \Bigg|\frac{3n+4-3n}{n} \Bigg| = \Bigg|\frac{4}{n}\Bigg| = \frac{4}{n}$$
Luego, por definición sabemos que $\frac{4}{n} < \epsilon$  o de manera equivalente que $n > \frac{4}{\epsilon}$. Entonces, eligiendo cualquier $N > \frac{4}{\epsilon}$ se cumple que todos los términos de la sucesión para $n > N$ cumplen estar dentro de $(3-\epsilon, 3 + \epsilon)$. $\blacksquare$ 
(d) Queremos verificar por definición que 
$$\lim_{n \rightarrow \infty} \sqrt{n+1}-\sqrt{n} = 0 \iff \forall \epsilon > 0, \exists N \in \mathbb{N} : \Big|\sqrt{n+1} - \sqrt{n}\Big| < \epsilon, \forall n > N$$
Analicemos lo que ocurre dentro de el módulo:
$$\Big|\sqrt{n+1}-\sqrt{n}\Big| = \Bigg|\sqrt{n+1}- \sqrt{n} \cdot \frac{\sqrt{n+1}+\sqrt{n}}{\sqrt{n+1}+\sqrt{n}}\Bigg| = \Bigg|\frac{n+1-n}{\sqrt{n+1}+\sqrt{n}} \Bigg| =  \frac{1}{\sqrt{n+1}+\sqrt{n}}$$
Luego, por definición sabemos que $n+1 > n \rightarrow \sqrt{n+1} > \sqrt{n} \rightarrow \sqrt{n+1}+\sqrt{n} > 2\sqrt{n}$ por lo que $\frac{1}{\sqrt{n+1}+\sqrt{n}} < \frac{1}{2\sqrt{n}} \underset{(1)}{<} \epsilon$ entonces nos basta con que ocurra (1) tal que $n > \frac{1}{4\epsilon^2}$. 
Entonces, eligiendo cualquier $N \geq \frac{1}{4\epsilon^2}$ se cumple la definición. $\blacksquare$ 

![[Pasted image 20221203163300.png]]
Probemos por el absurdo que esto sucede. Sea una sucesión que converge a dos límites distintos $\lim_{n \rightarrow \infty} a_n = l$ y $\lim_{n \rightarrow \infty} a_n = l_0$, entonces:
$$\begin{align}
\lim_{n \rightarrow \infty} a_n = l \iff \forall \epsilon > 0, \exists N \in \mathbb{N}: |a_n - l| < \epsilon \\
\lim_{n \rightarrow \infty} a_n = l_0 \iff  \forall \epsilon_0 > 0, \exists N_0 \in \mathbb{N}: |a_n - l| < \epsilon_0 
\end{align}$$
Por tricotomía, puede ocurrir que $l_0 < l$, $l_0 > l$ o $l_0 = l$. Supongamos $l_0 < l$ y elijamos $\epsilon = \epsilon_0 = \frac{l-l_0}{2}$. Tal que 
$$\begin{align}
|a_n - l| < \frac{l-l_0}{2} \quad \rightarrow \quad -\frac{(l-l_0)}{2} < a_n -l < \frac{l-l_0}{2} \quad \rightarrow \quad l - \frac{l-l_0}{2} < a_n < l + \frac{l-l_0}{2} \\
|a_n - l_0| < \frac{l-l_0}{2} \quad \rightarrow \quad -\frac{(l-l_0)}{2} < a_n -l_0 < \frac{l-l_0}{2} \quad \rightarrow \quad l_0 - \frac{l-l_0}{2} < a_n < l_0 + \frac{l-l_0}{2}
\end{align}$$
Luego, $l - \frac{l-l_0}{2} = \frac{2l-l+l_0}{2} = \frac{l+l_0}{2}$ y $l_0 + \frac{l-l_0}{2} = \frac{2l_0 + l - l_0}{2} = \frac{l_0+l}{2}$ por lo que $\frac{l+l_0}{2} < a_n < \frac{l_0 + l}{2}$ y llegamos a un absurdo, que viene de suponer que $l_0 < l$. Llegamos a un absurdo parecido si consideramos $l_0 > l$, por lo que no queda otra opción que $l_0 = l$. $\blacksquare$

![[Pasted image 20221203170226.png]]
Por hipótesis sabemos que 
$$\begin{align}
\lim_{n \rightarrow \infty} a_n = l \iff \forall \epsilon_1 > 0, \exists N_1 \in \mathbb{N} : |a_n - l| < \epsilon_1  & \quad (1)\\
\lim_{n \rightarrow \infty} b_n = m \iff \forall \epsilon_2 > 0, \exists N_2 \in \mathbb{N} : |b_n - m| < \epsilon_2 & \quad (2)
\end{align}$$
Y queremos llegar a que:
$$\lim_{n \rightarrow \infty} a_n + b_n = l + m \iff \forall \epsilon > 0, \exists N \in \mathbb{N} : |(a_n + b_n) + (l + m)| < \epsilon$$
Si tomamos $N = \mathrm{máx}\{N_1, N_2\}$ entonces este $N$ cumple (1) y (2), y si tomamos $\epsilon_1 = \epsilon_2 = \frac{\epsilon}{2}$  entonces 
$$|(a_n + b_n) + (l+m) | \leq |a_n + l| + |b_n + m| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$$
Y llegamos a lo que queríamos. $\blacksquare$ 

![[Pasted image 20221203174151.png]]
El conjunto $\{a_n | \; n \in \mathbb{N}\}$ es la imagen de la sucesión. Como la sucesión tiene límite se cumple que 
$$\lim_{n \rightarrow \infty} a_n = l \iff \forall \epsilon > 0, \exists N \in \mathbb{N} : |a_n - l| < \epsilon$$
Tomemos un épsilon $\epsilon = 1$ por ejemplo, sabemos que existe un $N \in \mathbb{N}$ tal que, para todo $n > N$, $a_n \in (l- 1, l+1)$.  Entonces, a la imagen la podemos separar en dos $\{a_1, a_2, \dots, a_N\}$ y $\{a_n \; | \; n > N\}$, el primer conjunto obviamente está acotado pues es finito y el segundo está acotado superiormente por $l+1$. Por lo tanto,
$$\underset{\text{está acotado}}{\underbrace{\{a_1, a_2, \dots, a_N\}}} \cup \underset{\text{está acot. sup.}}{\underbrace{\{a_n \; | n > N\}}} = \underset{\text{está acot. sup.}}{\underbrace{\{a_n \; | \; n \in \mathbb{N}\}}}$$
y llegamos a lo que queríamos. $\blacksquare$ 

![[Pasted image 20221203181601.png]]
Por hipótesis tenemos que
$$\begin{align}
\lim_{n \rightarrow \infty} a_n = l \iff \forall \epsilon_1 > 0, \exists N_1 \in \mathbb{N} : |a_n - l| < \epsilon_1  & \quad (1)\\
\lim_{n \rightarrow \infty} b_n = m \iff \forall \epsilon_2 > 0, \exists N_2 \in \mathbb{N} : |b_n - m| < \epsilon_2 & \quad (2)
\end{align}$$
Y queremos llegar a que 
$$\lim_{n \rightarrow \infty} a_n \cdot b_n = l \cdot m \iff \forall \epsilon > 0, \exists N \in \mathbb{N} : |a_nb_n - l\cdot m| < \epsilon$$
Si elegimos $N = \mathrm{máx} \{N_1, N_2\}$ entonces se cumple (1) y (2). Luego, observemos que
$$|a_nb_n -lm| = |a_nb_n +b_nl - b_nl - lm| = |b_n(a_n - l) +l(b_n-m)|$$
Nos ayudaría poder "acotar" la sucesión $b_n$ de alguna manera, sabemos por el ejercicio (12) que toda sucesión con límite está acotada superiormente, entonces existe un $C \in \mathbb{R}$ tal que $|b_n| \leq C$ para todo $n \in \mathbb{N}$. Entonces, tomando $\epsilon_1 = \frac{\epsilon}{2C}$ y $\epsilon_2 = \frac{\epsilon}{2|l|}$ nos queda que
$$|b_n(a_n-l) + l(b_n-m)| \leq |b_n||a_n-l| + |l||b_n-m| < C \cdot \frac{\epsilon}{2C} + |l| \cdot \frac{\epsilon}{2|l|} = \epsilon$$
Y llegamos a lo que queríamos. $\blacksquare$ 

![[Pasted image 20221203202715.png]]
(a) **(Lema del Sándwich)** Sean dos sucesiones con límites ambos a $l$, llamadas $b_n$ y $c_n$, y una tercera sucesión $a_n$. Si se cumple que $b_n \leq a_n \leq c_n$ entonces $a_n$ también tiene límite a $l$.
**Demostración.** Sabemos por hipótesis que
$$\begin{align}
\lim_{n \rightarrow \infty} c_n = l \iff \forall \epsilon > 0, \exists N_1 \in \mathbb{N}: |c_n - l| < \epsilon, \forall n > N_1 \\
\lim_{n \rightarrow \infty} b_n = l \iff \forall \epsilon > 0, \exists N_2 \in \mathbb{N}: |b_n - l| < \epsilon, \forall n > N_2
\end{align}$$
Y queremos llegar a que 
$$\lim_{n \rightarrow \infty} a_n = l \iff \forall \epsilon > 0, \exists N \in \mathbb{N}: |a_n - l| < \epsilon, \forall n> N$$
Sabiendo que $b_n \leq a_n \leq c_n$. Elijamos el mismo $\epsilon$ para $b_n$ y $c_n$  y el mayor de $N_1$ y $N_2$ tal que ambas desigualdades se cumplan $N = \mathrm{máx}\{N_1, N_2\}$. Ahora, podemos reescribir las desigualdades como: $l-\epsilon < c_n < l + \epsilon$ y $l-\epsilon < b_n < l+\epsilon$. Entonces, 
$$l-\epsilon < b_n \leq a_n \leq c_n < l + \epsilon \quad \implies \quad l-\epsilon < a_n < l+\epsilon \quad \implies \quad |a_n - l | < \epsilon$$
Y llegamos a lo que queríamos. $\blacksquare$ 
(b) Queremos probar que 
$$\lim_{n \rightarrow \infty} \frac{10^n}{n!} = 0$$
Usemos el lema del Sándwich, nos gustaría poder acotar nuestra sucesión por otras dos que también tiendan a 0. Una de los candidatos obvios es la sucesión $b_n = 0$ y la segunda se puede encontrar razonando como crece la función. Si el límite tiende a 0 entonces el factorial crece más rápido que $10^n$ a partir de un punto, intentemos separarlo en partes e ir acotando cada una de ellas:
$$0 \leq \underset{C}{\underbrace{\frac{10 \cdot 10 \cdots 10}{1\cdot 2 \cdots 10}}} \cdot \underset{\leq 1}{\underbrace{\frac{10}{11}}} \cdot \underset{\leq 1}{\underbrace{\frac{10}{12}}} \cdots \frac{10}{n-1} \cdot \frac{10}{n} \leq C \cdot 1 \cdot \frac{10}{n}$$
Luego, $\lim_{n \rightarrow \infty} C\frac{10}{n} = 0$ por lo cual por el lema del Sandwitch tenemos que $\lim_{n \rightarrow \infty} \frac{10^n}{n!} = 0$. 

![[Pasted image 20221204103551.png]]

> [!DEFINICIÓN]
> (a) Decimos que una sucesión **diverge al infinito** cuando $$\forall M > 0, \exists N \in \mathbb{N} : a_n > M, \forall n > N$$

(b) Queremos probar que $\lim_{n \rightarrow \infty} \frac{n^3 + n}{n+1} = \infty$ por definición:
$$\lim_{n \rightarrow \infty} \frac{n^3 + n}{n+1} = \infty \iff \forall M > 0, \exists N \in \mathbb{N} : \frac{n^3 +n}{n+1} > M, \forall n > N$$
Teniendo un número muy grande $M > 0$ queremos encontrar un $N$ tal que la sucesión para todo término mayor que $a_N$ supere a $M$. Observemos que
$$\frac{n^3 + n}{n+1} = \frac{n^3}{n+1} + \frac{n}{n+1}$$
Notemos que $1 > \frac{n}{n+1}$ y $1 > \frac{1}{n+1}$ entonces:
$$n^3 \cdot 1 + 1 >\frac{n^3}{n+1} + \frac{n}{n+1} > M$$
Por lo que nos basta con que $n^3 + 1 > M \rightarrow n > \sqrt[3]{M-1}$, tal que eligiendo $N \geq \sqrt[3]{M-1}$ se cumple lo que queríamos. $\blacksquare$ 

![[Pasted image 20221204111613.png]]
Queremos probar que si $\lim_{n \rightarrow \infty} a_n = \infty$ y $\lim_{n \rightarrow \infty} b_n = \infty$ entonces $\lim_{n \rightarrow \infty} a_n b_n = \infty$. 
Sabemos por hipótesis que 
$$\begin{align}
\lim_{n \rightarrow \infty} a_n = \infty \iff \forall M_1 > 0, \exists N_1 \in \mathbb{N} : a_n > M_1, \forall n > N_1 \\
\lim_{n \rightarrow \infty} b_n = \infty \iff \forall M_2 > 0, \exists N_2 \in \mathbb{N} : b_n > M_2, \forall n > N_2 \\ 
\end{align}$$
Y queremos llegar a que
$$\lim_{n \rightarrow \infty} a_n b_n = \infty \iff \forall M> 0, \exists N \in \mathbb{N} : a_n b_n > M, \forall n > N$$
Veamos que $a_n b_n > M_1 M_2$ entonces eligiendo $M_1 = M_2 = \sqrt{M}$ se cumple que $a_nb_n > \sqrt{M}\sqrt{M} = M$. Para cada uno de estos $M$'s hay en su respuesta un $N_{1, \sqrt{M}}$ y $N_{2, \sqrt{M}}$ y eligiendo $N = \mathrm{máx} \{N_{1, \sqrt{M}}, N_{2, \sqrt{M}}\}$ obtenemos lo que queríamos. 

![[Pasted image 20221204113601.png]]
**(Teorema de la Convergencia Monótona)** Queremos probar que si $\{a_n\}$ una sucesión acotada superiormente ($\exists C \in \mathbb{R}, \; a_n < C, \forall n \in \mathbb{N}$) y creciente ($a_n \leq a_{n+1}, \; \forall n \in \mathbb{N}$) es convergente a un límite $l$, es decir
$$\lim_{n \rightarrow \infty} a_n = l \iff \forall \epsilon > 0, \exists N : |a_n - l| < \epsilon, \forall n > N$$
Como la sucesión está acotada superiormente entonces su imagen tiene supremo, veamos que $\sup\{a_n \; | \; n \in \mathbb{N}\} = l$. Tomemos ahora un $\epsilon > 0$, entonces por el lema útil debería existir un $a_N$ tal que $l- \epsilon < a_N < l$ y como la sucesión es creciente para todo $n> N$, se cumple que $l - \epsilon < a_n < l < l + \epsilon$. Tal que entonces $|a_n - l| < \epsilon, \forall n > N$ pero notemos que esta es la definición de convergencia. $\blacksquare$ 

![[Pasted image 20221204115344.png]]
(a) Sea $a_n$ decimos que $b_j : \mathbb{N} \rightarrow \mathbb{R}$ es una **subsucesión** de $a_n$ si existe otra función $n_j: \mathbb{N} \rightarrow \mathbb{N}$ tal que $n_j$ sea **estrictamente creciente** y $a_{n_j} = b_j$.  

(b) Un criterio que obtenemos como corolario del **Teorema de Bolzano-Weierstrass** nos dice que una sucesión diverge si existen dos subsucesiones de la misma que convergen a dos límites distintos. Veamos que si tomamos $n_j = 2j$ y $m_j = 2j+1$ tal que $a_{2j} = 1$ y $a_{2j+1} = -1$ dos subsucesiones, estas convergen a límites distintos y por lo tanto la sucesión $a_n$ diverge. 

![[Pasted image 20221204120953.png]]
Por hipótesis, sabemos que $\{a_n\} \rightarrow l$ por lo que:
$$\lim a_n = l \iff \forall \epsilon > 0, \exists N : |a_n -l| < \epsilon, \forall n > N$$
Y queremos probar que dada una función $n_j : \mathbb{N} \rightarrow \mathbb{N}$ es cierto que
$$\lim a_{n_j} = l \iff \forall \epsilon > 0, \exists N : |a_{n_j} - l| < \epsilon, \forall j > j_0$$
Debe existir un ${j_0}$ tal que $n_{j_0} > N$ entonces, como la función est. creciente se cumple que  $n_j > n_{j_0}$  para todo $j > j_0$ por lo tanto $|a_{n_j} - l|< \epsilon$ se cumple para todo $j > j_0$. $\blacksquare$ 

![[Pasted image 20221204125440.png]]

> [!DEFINICIÓN]
> (a) Decimos que una función tiene límite $l$ en $a$ (denotado $\lim_{x \rightarrow a} f(x) = l$) cuando para todo $\epsilon > o$, existe un $\delta > 0$ tal que se cumple $|f(x) - l| < \epsilon$ para todo $x$ en $0 < |x-a| < \delta$. 

(b) Verifiquemos por definición que $\lim_{x \rightarrow 0} 4x\sin x = 0$. Por definición se puede expresar como
$$\lim_{x \rightarrow 0} 4x \sin x = 0  \iff \forall \epsilon > 0, \exists \delta > 0 : |4x\sin x| < \epsilon, \forall x \in \mathbb{R} : 0 < |x| < \delta$$
Notemos que $|\sin x| \leq 1$ y $|4x| = 4|x|$ por lo tanto $|4x\sin x| = 4|x||\sin x| \leq 4|x|$. Luego por definición sabemos que nos dan un $\epsilon$ y en respuesta queremos encontrar un $\delta$. Entonces, $4|x| < \epsilon \rightarrow |x| < \epsilon/4$ entonces si tomamos $\delta = \epsilon/4$ tenemos que se cumple la definición. 

![[Pasted image 20221204131817.png]]
Decimos que el límite es una propiedad "local" pues agarrando un intervalo abierto alrededor de un valor $a$, si decimos que tiene límite en $l$, esto nos dice que todos los valores de $f(x)$ con $x$ "cercano" a $a$ van a estar cerca de $l$. Más precisamente:

Si $f(x)$ y $g(x)$ coinciden en un intervalo **abierto** alrededor de $a$ (posiblemente no en $a$), entonces 
$$\lim_{x \rightarrow a} f(x) = \lim_{x \rightarrow a} g(x)$$

![[Pasted image 20221204134541.png]]
Podemos definir al **límite lateral por la izquierda de $a$** como $\forall \epsilon > 0, \exists \delta > 0 : |f(x) - l| < \epsilon$ para todo $x$ que cumple $0 < a-x< \delta$.
Luego, el **límite lateral por derecha de $a$** se define como $\forall \epsilon > 0, \exists \delta > 0 : |f(x) - l| < \epsilon$ para todo $x$ que cumple $0 < x-a < \delta$.  

![[Pasted image 20221204134938.png]]
(a) 
