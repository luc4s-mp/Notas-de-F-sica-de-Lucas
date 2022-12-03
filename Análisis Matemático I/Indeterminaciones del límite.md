Supongamos que tenemos dos sucesiones ([[Sucesión]]) digamos $a_n = n$ y $b_n = n^2$ ambas son [[Sucesiones Divergentes]], sin embargo $\lim n/n^2 = \lim 1/n = 0$ a pesar de que estamos dividiendo dos sucesiones que se hacen cada vez más grandes. El factor escencial que entra en juego para que el límite en este caso converja, es el hecho de que $b_n$ crece **mucho más rápido que $a_n$**. Esto hace que la división siempre parezca acercarse a 0, de ahí el límite. Fijemosnos que usar la propiedad del límite (vista en [[Sucesión]]) en este caso que me dice "el límite  de la división es la división de los límites" estaría mal en este caso porque terminariamos concluyendo que 
$$\lim \frac{a_n}{b_n} = \frac{\lim a_n}{\lim b_n} = \frac{\infty}{\infty}$$
Lo cual estaría mal porque la propsición nos dice que para que el límite de la división sea la división de los límites **ambos límites deben converger** lo cual no ocurre en este caso. Los casos absurdos como $\frac{\infty}{\infty}$ que nacen de aplicar mal las propiedades del límite se dicen **indeterminaciones**. Cuando llegamos a una indeterminación esto quiere significar que algo hicimos mal proque llegamos a un caso ridículo. Algunas otras indeterminaciones conocidas son 
$$\frac{0}{0} \quad \frac{\infty}{\infty} \quad \infty - \infty \quad 0 \times \infty \quad 1^{\infty} \quad 0^0 \quad \infty^0$$
Es importante recalcar que las indeterminaciones son **notaciones** para casos particulares del límite, cuando decimos que un límite tiene la indeterminación $\infty/\infty$ lo que queremos decir es que tenemos dos límites de sucesiones que tienden al infinito, pero puede haber una de estas sucesiones (en concreto la del denominador) que crezca más rápido que la otra y en este caso el límite converge. 
Para notas más avanzadas veremos que es útil saber que tipo de indeterminación tenemos.

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