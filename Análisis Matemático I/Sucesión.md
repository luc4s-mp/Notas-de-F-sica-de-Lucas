
> #Definición Una **sucesión** de números reales [[R]] es una función de $\mathbb{N}$ en $\mathbb{R}$. Esto es, si llamamos $a$ una sucesión, entonces $a: \mathbb{N} \rightarrow \mathbb{R}$. En general, no utilizamos la notación usual de las funciones $f(x)$ para representar una sucesión, normalmente las denotamos $\{a_n\}_{n \in \mathbb{N}}$ o $\{a_n\}_{n = 1}^{\infty}$ o simplemente $\{a_n\}$. 

Las diferenciamos de las [[Funciones en R]], porque estas tienen la propiedad de tener a los números naturales como dominio, de tal manera que existe un "primer elemento" de la imagen de la sucesión y podemos representarlas como puntos en una gráfica.  
Existen diversas formas de definir una sucesión, nosotros veremos 4:
1. Con una ecuación
2. Listando los primeros términos
3. Con palabras
4. Con [[Definiciones Recursivas]].
La primera de ellas es a través de una ecuación, por ejemplo $a_n = \frac{2^n n!}{n+1}$. Pero también podemos definirla dando los primeros números, por ejemplo $\{b_n\} = \{1,2,4,8,16, \dots\}$ que son las primeras potencias de 2, entones podríamos llegar a pensar $b_n = 2^n$, sin embargo otra posibilidad para esta sucesión perfectamente podría ser $b_n = 2^n + n(n-1)(n-2)(n-3)(n-4)$. Hay que tener mucho cuidado al tener una sucesión definida de esta manera, los primeros terminos nunca nos pueden asegurar que sucesión es. 
Entonces, la convensión es que escribiendo los primeros términos es **muy claro** a lo que nos referimos usamos esto, pero de otra manera usamos ecuaciones.

La tercera forma de definir una sucesión seria con palabras, un ejemplo de esto sería $p_n = \text{ el }n \text{-ésimo primo }$. Esta sucesión esta perfectamente definida y nos conviene definirla de esta manera porque no existe una ecuación que nos de todos los [[Números primos]]. 

La última forma es usando una definición con recurrencia, es decir usar uno de los términos anteriores para definir el siguiente. Por ejemplo la sucesión $a_{n+2} = a_{n+1} + a_n, \; a_0 = 1, \; a_1 = 1$ está perfectamente definida y es conocida como la sucesión de fibonacci.

## El límite de sucesiones
Resulta que las sucesiones, al ser funciones tan simples, muchos de los hechos en el análisis pueden ser reducidos a entender e comportamiento de sucesiones. Es por esto por lo cual nos detendremos a entender como es que estás se comportan para términos muy grandes. 
Empezaremos a responder nuestra primer pregunta central vista en la introducción: _¿Qué significa "acercanos" a un número?_ 

Supongamos la siguiente sucesión $\Big\{\frac{n}{n+1}\Big\}_{n=0}^\infty = \{0,1/2,2/3, 3/4,\cdots\}$ observemos que a medida que vamos encontrando términos cada vez más grandes parece que se "acercan" cada vez más a 1.
![[Pasted image 20220713203929.png]]
En realidad la sucesión nunca va a tomar el valor 1 (porque no existe ningún término que nos pueda dar 1), pero va a "tender" a aproximarse a 1. En general, cuando esto sucede en una sucesión decimos que esta "converge".

> #Definición (**Convergencia de una sucesión**) Una sucesión $\{a_n\}$ converge a un número real $L$ si para cada número positivo $\epsilon$, existe un $N \in \mathbb{N}$ tal que para cualquier $n \geq N$ sucede que $|a_n - L| < \epsilon$. 

Intentemos entender que es lo que nos dice esta definición. En el siguiente dibujo se ilustran los primeros términos de la sucesión que dimos de ejemplo $a_n = \frac{n}{n+1}$, supongamos que yo agarro un intervalo tal que $(2/3, 3/2)$.  
![[Pasted image 20220713211005.png]]
Notemos que el intervalo no toma el término $a_1$, este queda afuera del mismo. Sin embargo, todos los términos a partir del $a_2$ si entran en el intervalo. Luego, veamos que pasa si tomamos un intervalo $(4/5, 6/5)$, en este caso no entrarían los términos $a_1, a_2$ y $a_3$ pero si todos a partir del término $a_4$. 

A todos estos términos que caen dentro de un intervalo abierto que elegimos cerca de 1 los vamos a llamar la "cola" de términos de $a_n$. Queremos que esta cola de términos se mantenga adentro del intervalo que elegimos cerca de nuestro número L al que queremos ver que converge la sucesión (en este caso 1). Ahora, quiero que esto sea verdad para **cualquier** intervalo abierto que tomemos alrededor de $1$, lo cual tiene sentido pues no importa que intervalo tomemos siempre tiene que existir una "cola" de términos para la cual todos los términos que sigan caigan adentro del mismo intervalo y no salgan. 

Estamos muy cerca de definir formalmente el concepto de "acercarse" a un número. Cuando decimos que "nos acercamos 1" nos referimos a que no importa que intervalo abierto tomemos cerca de 1, va a existir un primer término que sea miembro de la cola y a partir de ahí todos los términos que sigan caigan en ese intervalo.

Para formalizar esto vamos a llamar a la distancia desde nuestro $L$ a los bordes del intervalo abierto que tomamos $\epsilon$ (epsilon). Notemos que este número tiene que ser positivo ya que es una distancia. Luego el intervalo entonces queda definido como $(L-\epsilon, L+\epsilon)$ y quiero a partir de un $N \in \mathbb{N}$ determinado todos los $a_n$ pertenecen al intervalo, o sea $L-\epsilon < a_n < L+\epsilon$ para $n > N$ . Luego,  restando $L$ en la desigualdad, $-\epsilon < a_n - L < \epsilon \rightarrow |a_n - L| < \epsilon$ y llegamos a la definición de arriba.

A este número $L$ lo llamamos el **límite de la sucesión** y si es un número finito decimos que la sucesión **converge**. Normalmente lo denotamos
$$\lim_{n \rightarrow \infty} a_n = L$$
y se lee "el límite de la sucesión cuando $n$ tiende a infinito es $L$".

Resulta obvio ver que una sucesión no puede converger a dos límites distintos, entonces se dice que es único.

> **Teorema 1. (Unicidad del Límite de Sucesiones)** Dada una sucesión $a_n$ en el que existe un $L \in \mathbb{R}$ tal que $\lim_{n \rightarrow \infty} a_n = l$ , $l$ es único.

**Demostración.** Supongamos por el absurdo que existe $l_0 \neq l$ y que se cumple $\lim_{n \rightarrow \infty} a_n = l$ y un $\lim_{n \rightarrow \infty} a_n = l_0$. Como $l_{0} \neq l$ podemos asumir que $l<l_{0}$. Elegimos entonces $\epsilon_{0}=\left(l_{0}-l\right) / 2>0$. Para este $\epsilon_{0}$ tiene que existir $N \in \mathbb{N}$ tal que $\left|a_{n}-l\right|<\epsilon_{0}$ para cada $n>N$, pues $\left\{a_{n}\right\}$ converge a $l$.
Por otro lado, para el mismo $\epsilon_{0}$ tiene que existir $M \in \mathbb{N}$ tal que $\left|a_{n}-l_{0}\right|<\epsilon_{0}$ para cada $n>M$, pues $\left\{a_{n}\right\}$ converge a $l_{0}$.
Tomemos ahora algún $j>\max \{N, M\}$ (esto lo hacemos porque queremos que $j$ sea mayor a ambos, entonces tomamos el más grande de los dos). Para este $j$ se cumple que $l-\epsilon_{0}<a_{j}<l+\epsilon_{0} \quad$ y $\quad l_{0}-\epsilon_{0}<a_{j}<l_{0}+\epsilon_{0}$.
Por un lado $a_{j}<l+\epsilon_{0}=l+\frac{l_{0}-l}{2}=\frac{l_{0}+l}{2}$.
Por otro lado $a_{j}>l_{0}-\epsilon_{0}=l_{0}-\frac{l_{0}-l}{2}=\frac{l_{0}+l}{2}$.
Entonces nos queda que $\frac{l_0 + l}{2} < a_j < \frac{l_0  + l}{2}$ pero esto es un absurdo. La contradicción se generó por suponer que $l_0 \neq l$, entonces $l_0 = l$. $\blacksquare$    

Dada una sucesión podemos encontrar donde converge "probando valores" dentro de la misma y luego comprobar que el límite es ese usando la definición de convergencia. Por ejemplo, supongamos que tenemos $a_n = \frac{4n+3}{5n}$ probando valores observaremos que la sucesión parece acercarse a $4/5$, demostremos que este es el límite usando la definición.
Busacamos un valor $N \in \mathbb{N}$ que dado nuestra definición de "cerca" $\epsilon> 0$ cumpla que todos los $a_n$'s con $n > N$ estén en $\frac{4}{5} - \epsilon < \frac{4n+3}{5n} < \frac{4}{5} + \epsilon \rightarrow |\frac{4n+3}{5n} - \frac{4}{5}|< \epsilon$. Luego,
$$\Big|\frac{4n+3}{5n} - \frac{4}{5}\Big| = \Big|\frac{4n+3-4n}{5n} \Big| = \frac{3}{5n} < \epsilon \rightarrow n > \frac{5}{3\epsilon}$$
Eligiendo entonces $N > \frac{5}{3\epsilon}$ podemos encontrar siempre un $N$ para todo $\epsilon$ por lo cual $4/5$ es el límite y es único por la proposición anterior. 
Notemos que encontrar límites de sucesiones por definición puede ser muy difícil cuando estas se hacen más complicadas. 

Observemos una cosa, si reescribimos la sucesión anterior como $\frac{4 + 3/n}{5}$ podemos demostrar de manera lógica que $\lim_{n \rightarrow \infty} 1/n = 0$ [^1] tal que los valores de $3/n$ se harían cada vez más chicos hasta también converger a 0 tal que nos queda $\frac{4+0}{5} = \frac{4}{5}$ que es el límite. Esto nos da un incapíe para desarrollar un método nuevo para encontrar límites de sucesiones más complicadas usando el hecho de que la sucesión $\frac{1}{n}$ tiende a 0.
Pero antes, relacionemos los conceptos viston en [[Axioma del supremo y el ínfimo]] sabiendo que la imagen de una sucesión está en los reales.

## Sucesiones Acotadas

> #Definición de sucesión *acotada inferiormente* y *acotada superiormente*
> - Diremos que una sucesión está **acotada superiormente** si existe $C \in \mathbb{R}$ tal que $a_n \leq C$ para todo $n \in \mathbb{N}$. 
> - Diremos que una sucesión está **acotada inferiormente** si existe $c \in \mathbb{R}$ tal que $a_n \geq c$ para todo $n \in \mathbb{N}$. 
> - Diremos que una sucesión está **acotada** si es acotada superiormente e inferiormente.

>**Teorema 2 (Relación entre convergencia de una sucesión y una sucesión acotada).** Si una sucesión $\{a_n\}$ es una sucesión convergente entonces está acotada.

**Demostración.** Llamaremos $l$ al límite de $\{a_n\}$. Entonces utilizamos la definición de convergencia de $\{a_n\}$ para $\epsilon = 1$.
$$|a_n - l| < 1, \; \forall n > N \;\;\;\;\; \iff \;\;\;\;\; l - 1 < a_n < l + 1, \; \forall n > N$$
Es decir, el conjunto $\{a_n: n > N\}$ está acotado superiormente por $l + 1$ e inferiormente por $l - 1$. Por otro lado, el conjunto de los primero $a_n$'s, $\{a_1, a_2, a_3, \cdots, a_N\}$ es finito y alcanza su máximo y mínimo. Luego tenemos el conjunto imagen:
$$\underbrace{\{a_n : n \in \mathbb{N}\}}_{\text{ imagen de la función}} = \underbrace{\{a_1, a_2, \cdots, a_N\}}_{\text{ está acotada}} \cup \underbrace{\{a_n : n > N\}}_{\text{está acotada}}$$
Lo cuál comprueba que la sucesión está acotada. $\blacksquare$

---

Esto nos lleva a poder demostrar la siguiente proposición:

> **Proposición 3. (Álgebra de Límites)** Sean $\{a_n\}$ y $\{b_n\}$ sucesiones convergentes a $l$ y $m$ respectivamente. Entonces se cumple que:
> 1. $\lim_{n \rightarrow \infty} a_n + b_n = l + m$
> 2. $\lim_{n \rightarrow \infty} a_n \cdot b_n = l \cdot m$
> 3. Si $m \neq 0$, existe $N \in \mathbb{N}$ tal que $a_n/b_n$ está definida para todo $n > N$ y $\lim_{n \rightarrow \infty} \frac{a_n}{b_n} = \frac{l}{m}$.

**Demostración.** Vamos primero 1. Sabemos que
$$
\begin{aligned}
&\forall \varepsilon_1>0 \exists N_1 \text { tal que }\left(n \geq N_1 \Rightarrow\left|a_n-\ell\right|<\varepsilon_1\right) . & (1)\\
&\forall \varepsilon_2>0 \exists N_2 \text { tal que }\left(n \geq N_2 \Rightarrow\left|a_n-m\right|<\varepsilon_2\right) . & (2)
\end{aligned}
$$
Queremos que ver que
$$
\forall \varepsilon>0 \exists N \text { tal que }\left(n \geq N \Rightarrow\left|a_n+b_n-(\ell+m)\right|<\varepsilon\right) .
$$
O sea, dado $\varepsilon>0$, buscamos $N$ que haga cumplir esa implicación. Planteamos
$$
\begin{aligned}
\left|a_n+b_n-(\ell+m)\right| &=\left|a_n+b_n-\ell-m\right|=\left|a_n-\ell+b_n-m\right| \\
& \leq\left|a_n-\ell\right|+\left|b_n-m\right|<\varepsilon_1+\varepsilon_2
\end{aligned}
$$
La última desigualdad se cumpla si $n>N_1$ y $n>N_2$ (o sea, si $n>\operatorname{máx}\left\{N_1, N_2\right\}$ ). Luego, tomando
$$
\varepsilon_1=\varepsilon_2=\frac{\varepsilon}{2} \quad \text { y } \quad N=\operatorname{máx}\left\{N_1, N_2\right\}
$$
resulta que si $n>N$, entonces
$$
\left|a_n+b_n-(\ell+m)\right|<\varepsilon,
$$
como queríamos. *Sigamos entonces con 2*, como hipótesis tenemos que ocurre (1) y (2), queremos que ver que
$$
\forall \varepsilon>0 \quad \exists N \text { tal que }\left(n \geq N \Rightarrow\left|a_n b_n-\ell m\right|<\varepsilon\right) .
$$
O sea, dado $\varepsilon>0$, buscamos $N$ que haga cumplir esa implicación. Debemos encontrar una expresión equivalente a $a_n b_n-\ell m$, que involucre las expresiones $a_n-\ell_1$ y $a_n-\ell_2$ de las hipótesis, para poder usarlas. Planteamos
$$
\begin{aligned}
\left|a_n b_n-\ell m\right| &=\left|a_n b_n-\ell b_n+\ell b_n-\ell m\right|=\left|\left(a_n-\ell\right) b_n+\ell\left(b_n-m\right)\right| \\
& \leq\left|a_n-\ell\right|\left|b_n\right|+|\ell|\left|b_n-m\right| \leq\left|a_n-\ell\right| C+|\ell|\left|b_n-m\right|
\end{aligned}
$$
con $C>0$ (en la última desigualdad hemos usado la proposición anterior: Como $b_n$ tiene límite, entonces está acotada).
Luego, por (2) y (3), si $n>N_1$ y $n>N_2$ se cumple que
$$
\left|a_n b_n-\ell m\right|<C \varepsilon_1+|\ell| \varepsilon_2
$$
La última desigualdad vale si $n>N_1$ y $n>N_2$ (o sea, si $n>\operatorname{máx}\left\{N_1, N_2\right\}$ ).
Del $\varepsilon$ que nos dieron, destinamos la mitad al primer sumando de $C \varepsilon_1+|\ell| \varepsilon_2$ y la mitad al segundo. Así,
$$
C \varepsilon_1=\frac{\varepsilon}{2} \quad \text { y } \quad|\ell| \varepsilon_2=\frac{\varepsilon}{2} .
$$
Luego, tomando
$$
\varepsilon_1=\frac{\varepsilon}{2 C}, \quad \varepsilon_2=\frac{\varepsilon}{2|\ell|} \quad \text { y } \quad N=\operatorname{máx}\left\{N_1, N_2\right\}
$$
resulta que si $n>N$, entonces
$$
\left|a_n b_n-\ell m\right|<C \frac{\varepsilon}{2 C}+|\ell| \frac{\varepsilon}{2|\ell|}=\varepsilon,
$$
como queríamos. _Por último, veamos 3,_ notemos que es suficiente probar que $\lim_{n \rightarrow \infty} \frac{1}{b_n} = \frac{1}{m}$ (com $m \neq 0$) pues como ya demostramos (2), $\lim \frac{a_n}{b_n} = \lim a_n \cdot \lim 1/b_n= l \cdot 1/m = l/m$. Queremos ver entonces que existe un $N \in \mathbb{N}$ tal que para todo $n > N$ :
$$\Big|\frac{1}{b_n} - \frac{1}{m}\Big| < \epsilon$$
Comencemos notando que $\Big| \frac{1}{b_n} - \frac{1}{m} \Big| = \Big| \frac{b_n - m}{b_n \cdot m} \Big| = \frac{|b_n - m|}{|b_n||m|}$  . Ahora, como $\lim _{n \rightarrow \infty} b_n=m$, para "epsilon" $\frac{|m|}{2}>0$, existe $N_1 \in \mathbb{N}$ tal que $\left|b_n-m\right|<\frac{|m|}{2}$ para todo $n>N_1$. $\mathrm{Al}$ mismo tiempo notemos que si $n>N_1$
$$
|m|=\left|m-b_n+b_n\right| \leq\left|m-b_n\right|+\left|b_n\right|<\frac{|m|}{2}+\left|b_n\right| .
$$
Entonces $|m|-\frac{|m|}{2}<\left|b_n\right|$, esto es $\frac{|m|}{2}<\left|b_n\right|$. Lo cual implica que
$$
\frac{1}{\left|b_n\right|}<\frac{2}{|m|}, \quad \text { para todo } n>N_1 .
$$
Sea $\epsilon>0$. Como $\lim _{n \rightarrow \infty} b_n=m$, para $\frac{|m|^2}{2} \cdot \epsilon>0$, existe $N_2 \in \mathbb{N}$ tal que $\quad\left|b_n-m\right|<\frac{|m|^2}{2} \cdot \epsilon \quad$ para cada $n>N_2$. Finalmente, para el epsilon dado, $\epsilon>0$, elegimos $N=\max \left\{N_1, N_2\right\}$. Entonces, si $n>N$ se cumple que
$$
\left|\frac{1}{b_n}-\frac{1}{m}\right|=\frac{\left|b_n-m\right|}{\left|b_n\right| \cdot|m|}<\frac{|m|^2}{2} \cdot \epsilon \cdot \frac{2}{|m|} \cdot \frac{1}{|m|}=\epsilon .
$$
Lo que termina de probar (3). $\blacksquare$ 

Gracias a esta proposición podemos encontrar el límite al que convergen sucesiones más complejas como $a_n = \frac{3n^3 + 1 + 7n^2}{4n^3 - 8n + 63}$, que contrarlas por definición sería muy complejo, pero usando la proposición:
$$\lim_{n \rightarrow \infty} \frac{3n^3 + 1 + 7n^2}{4n^3 - 8n + 63} = \lim \frac{n^3(3+\frac{1}{n^3} + \frac{7}{n})}{n^3(4-\frac{8}{n^2} + \frac{63}{n^3})} \underset{(3)}{=} \frac{\lim 3+\frac{1}{n^3} + \frac{7}{n}}{\lim 4-\frac{8}{n^2} + \frac{63}{n^3}} \underset{(1)}{=} \frac{\lim 3 + \lim \frac{1}{n^3} + 7\lim \frac{1}{n}}{\lim 4 - 8\lim \frac{1}{n^2} + 63\lim \frac{1}{n^3}}$$
Notemos que pudimos aplicas la proposición pues **sabemos que cada uno de los límites existen por separado**, $\lim 1/n = 0$, $\lim 1/n^2 = 0$ y $\lim 1/n^3 = 0$.  Tal que obtenemos que el límite es $4/3$. No siempre podemos aplicar este método, pues es importante que los límites de las sucesiones por separado existan, de otro modo si se aplica se llegan a absurdos como $0/0$ o $\infty \times 0$ , más sobre esto en [[Indeterminaciones del límite]]. 

## Sucesiones crecientes y decrecientes
Diremos que $\{a_n\}$ es **creciente** si $a_n \leq a_{n+1}$ para todo $n \in \mathbb{N}$, por otro lado llamaremos a una sucesión **decreciente** si $a_n \geq a_{n+1}$ para todo $n \in \mathbb{N}$. También podemos hablar de estrictamente creciente (si $a_n < a_{n+1}$ para todo n) y estrictamente decreciente (si $a_n > a_{n+1}$ para todo n).

> **Teorema. (Teorema de la convergencia monótona)** Sea $\{a_n\}$ una sucesión. 
> 1.  Si $\{a_n\}$ es ==creciente== y ==acotada superiormente==, entonces es convergente. 
> 2.  Si $\{a_n\}$ es ==decreciente== y ==acotada inferiormente==, entonces convergente.


**Demostración.** Consideremos el conjunto $A = a_n : n \in \mathbb{N}$ como la imagen de la sucesión. Tenemos que $A \neq \emptyset$, además que está acotada superiormente, entonces existe un $C$ tal que $a_n < C$ para todo $n \in \mathbb{N}$. Esto nos dice que $A$ es acotado superiormente, pues $C$ es una cota superior de $A$, por el [[Axioma del supremo y el ínfimo]], por lo cual $\alpha = \sup(A)$.
Queremos ver que $\lim_{n \rightarrow \infty} a_n = \alpha$.
Tomemos $\epsilon > 0$, entonces $\alpha - \epsilon < \alpha$. Por el [[Axioma del supremo y el ínfimo]] debe existir $a_N \in A$ tal que $\alpha - \epsilon < a_N < \alpha$. Además si $n > N$, y como la sucesión es creciente , se cumple que $a_N \leq a_n$.  A su vez, tenemos que $a_n \leq \alpha$. Por lo tanto
$$\alpha - \epsilon < a_N \leq a_n \leq \alpha < \alpha + \epsilon$$
A partir de esto obtenemos que $|a_n - \alpha| < \epsilon$ para todo $n > N$. Lo cual es la definición de límite, por lo cual prueba (1) que $\lim_{n \rightarrow \infty} a_n = \alpha$.
Para probar (2) podemos usar la misma lógica. $\blacksquare$

Para encontrar que una sucesión diverge debemos primero definir el concepto de [[Subsucesión]].

[^1]: Se puede demostrar usando la propiedad arquimediana, tenemos que  $|\frac{1}{n} - 0 | < \epsilon$  siemrpe existe un $N$ tal que $\frac{1}{N} < \frac{1}{n} < \epsilon$ para todo $n > N$.