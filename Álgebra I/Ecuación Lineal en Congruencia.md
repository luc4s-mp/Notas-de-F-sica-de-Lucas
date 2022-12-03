# Ecuaciones lineales en Congruencia
Nos topamos nuevamente con la cuestión de dividir los enteros modulares, es decir de resolver la ecuación $[a][x] = [b]$ en un específico $\mathbb{Z}_n$. En [[Enteros Modulares]] vimos como resolver algunas ecuaciones como $[5][x] = [4]$ en $\mathbb{Z}_6$, y concluimos que para poder resolver esta ecuación es necesario que exista el inverso de $[a]$ en $\mathbb{Z}_n$ y a su vez esto ocurre cuando $(a,n) = 1$. Queremos generalizar esto en una **ecuación lineal en congruencia** $ax \equiv b \; (n)$. 

Notemos que si la ecuación tiene solución entonces se tiene que cumplir $n|ax-b$, lo cual para un $y \in \mathbb{Z}$ significa $ny = ax -b$ o también $n(-y) + ax = b$. Entonces, esta es una combinación lineal (vista en [[Máximo Común Divisor]]) que vimos que podemos escribirla solo si $(n,a)|b$. Por lo tanto, $x$ es una solución de la congruencia lineal si y solo si hay un entero $y$ tal que $x$ y $y$ forman una combinación lineal $ax+ny = b$.

> **Teorema.** Dados $a, b \in \mathbb{Z}$ ([[Z]]), $n \in \mathbb{Z}$ y sea $d=(a,n)$. Podemos encontrar un $x \in \mathbb{Z}$ que resuelva  $$ax \equiv b \; (n)$$ si y solo si $d|b$. Si d divide a b, y si $x_0$ es una solución particular, entonces la solución general es dada por $x = x_0 + \frac{nt}{d}$ para todo $t \in \mathbb{Z}$. 

**Demostración.**
- ($\Rightarrow$) $ax \equiv b \; (n)$ tiene solución en $x_0 \in \mathbb{Z} \implies ax_0 - b = nq_1, \; q_1 \in \mathbb{Z}$. Como $(a, n)|a \implies (a, n)| ax_0; \; (a, n)| nq_1 \implies (a, n)|b$.
- ($\Leftarrow$) $(a, n)|b$. Supongamos primero $a \perp n$ (es decir son coprimos como vimos en [[Números primos]])$\implies \exists s,t \in \mathbb{Z}$ tal que $1 = sa + tn \underbrace{\implies}_{\text{mult. por b}} b = (bs)a + (bt)n \implies (bs)a - b = -btn$ 
  $\implies n|(-bt)n \implies n|(bs)a - b \implies (bs)\cdot a \equiv b \; (n)$. Luego, $x_0 = bs$ es una solución de la ecuación, luego si  $x_1 \in \mathbb{Z}$ es la siguiente solución de la ecuación lineal en congruencia: $ax_0 - ax_1 \equiv b - b \; (n) \equiv 0 (n) \implies a(x_0 - x_1) \equiv 0 \; (n) \implies n| a(x_0 - x_1)$ pero $(a, n) = 1 \implies n| (x_0 - x_1) \implies x_0 - x_1 = nq, \; q \in \mathbb{Z} \implies x_1 = x_0 + n(-q), \; -q \in \mathbb{Z}$.
  Por otro lado, los nros $x_0 + kn, \; k \in \mathbb{Z}$ son soluciones de la ecuación. El conjunto de soluciones está dado por 
  $$\{z \in \mathbb{Z}: \; z = x_0 + kn, \; k \in \mathbb{Z}, x_0 \text{ solución particular.}\}$$
  Si ahora suponemos que $d = (a,n) > 1$ y $d|b$. Sean $s, t \in \mathbb{Z}$ tales que 
  $$\begin{align}
  d  & = sa + tn \\
  1 & = s \big(\frac{a}{d} \big) + t \big(\frac{n}{d} \big) \\
  b & = bs \big(\frac{a}{d} \big) + bt \big(\frac{n}{d} \big) \\
  b & = sa \big(\frac{b}{d} \big) + nt \big(\frac{b}{d} \big)
  \end{align}
$$
$a \big( s \cdot \frac{b}{d} \big) - b =  - nt \big(\frac{b}{d} \big) \implies n \Big| \big( s \cdot \frac{b}{d} \big) \cdot a - b \implies \big( s \cdot \frac{b}{d} \big) \cdot a \equiv b \; (n)$
Luego $x_0 = s \cdot \frac{b}{(a,n)}$ es una solución particular de la ecuación lineal. Luego, como $\frac{n}{(a, n)}$ y $\frac{a}{(a,n)}$ son coprimos, y por lo hecho arriba sabemos que todas las soluciones son de la forma $x_0 + k \frac{n}{(a, n)}, \; k \in \mathbb{Z}$. $\blacksquare$ 

> **Colorario.** Si $mcd(a,n) = 1$ luego las soluciones $x$ de la ecuación lineal en congruencia $ax \equiv b \; (n)$ forman una misma clase de congruencia $[x]$ en $\mathbb{Z}_n$. 

Podemos usar un método parecido a como hicimos la demostración para encontrar las soluciones de una ecuación lineal. Para ecuaciones simples como por ejemplo: $7x \equiv 3 \; (12)$ (cuya ecuación equivalente es $[7][x] = [3]$ en $\mathbb{Z}_{12}$) podemos encontrar el inverso de 7 a ojo, (sabemos que existe pues $(7,12)=1$) veamos que $[x] = [9]$ pues $7 \cdot 9 \equiv 63 \equiv 3 \; (12)$, entonces las diversas soluciones están dadas por $x = 9 + 12k, \forall k \in \mathbb{Z}$ (que son justamente los elementos de la clase de congruencia $[9]_{12}$). 
Pero a medida que el módulo crece o $[a]$ es más grande se vuelve cada vez más complicado encontrar a ojo $[x]$ como solución a esto aparece el siguiente lema.

> **Lema.** Sea $m,a,b,n \in \mathbb{Z}, m|a, m|b, m|n$ , y sea $a' = a/m$, $b' = b/m$ y $n' = n/m$; entonces $$ax \equiv b \; (n) \iff a'x \equiv b' \; (n')$$Si $(a,n) = 1$, entonces basta con dividir $a' = a/m$ y $b' = b/m$ y tenemos que $$ax \equiv b \; (n) \iff a'x \equiv b' \; (n)$$

**Demostración.** Salen como consecuencia de la propisición "reducción de módulos" vista en [[Congruencia de Enteros]]. $\blacksquare$ 

 ---
## Resolución completa de la ecuación de congruencia $ax \equiv b \; (n)$
1. Antes de empezar reemplazo a $a$ por $r_n(a)$ (el resto de dividir $a$ por $n$) y $c$ por $r_n(c)$. Así de entrada se tienen que los coeficientes de la ecuación de congruencia son los más simples posibles.
2. ¿Tiene solución la ecuación?
	- (no) si $(a, n)  \nmid b$.  
	- (sí) si $(a,n) \mid b$.
3. Uso el lema: 
	$$a'x \equiv c' \; (n'), \;\; \text{ con } a' = \frac{a}{(a,n)}, \; c' = \frac{c}{(a,n)}, \; n' = \frac{n}{(a,n)}$$
4. Si tenemos la situación $a' \perp n'$ entonces se simplificaron todos los factores comunes entre $a'$ y $c'$. Esto simplifica la busqueda de una solución particular.
5. Se encuentra una solución particular $x_0$ de forma tal que esté en $0 \leq x_0 < n'$. Esto lo podemos hacer convirtiendo nuestra ecuación como una combinación lineal $a'x_1 + n'y_1 = 1$ (tomando como si fuera una combinación lineal del [[Máximo Común Divisor]]), encontramos a "ojo" $x_1$ y $y_1$, o usando el algoritmo de euclides extendido, luego multiplicamos por $c'$ de ambos lados, tal que $a'c'x_1 + c'n'y_0 = c'$. Por último movemos un poco los valores para obtener $a'(n'x_1) \equiv c' \; (n') \implies x_0 = n'x_1$.
6. Por último, se construye 
	$$S = \{x \in \mathbb{Z}: x_0 + nk\}$$
	si $a \perp n$. De otra forma:
	$$S = \{x \in \mathbb{Z}: x_0 + \frac{n}{(a,n)}k\}$$

---

