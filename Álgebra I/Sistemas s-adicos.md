# Sistemas de númeración
El sistema de númeración que utilizamos desde que (según parece) Fibonacci lo introdujo en el mundo occidental, en el **sistema decimal indo-arábigo**, que es un sistema que funciona por posiciones de los dígitos, donde otra importancia del número 0 radica en que hay una posición vacía. 

Así, cuando escribimos el número seis mil setecientos nueve, 6709, nos referimos al número compuesto por 6 unidades de 1000, 7 unidades de 100, 0 unidades de 10 y 9 unidades, o sea el número
$$6709 = 6 \cdot 10^3 + 7 \cdot 10^2 + 0 \cdot 10 + 9$$
Generalizandolo, el número natural $a = r_n r_{n-1} \cdots r_1 r_0$ simboliza entonces el número:
$$a= r_n \cdot 10^n + r_{n-1} \cdot 10^{n-1} + \cdots + r_1 \cdot 10 + r_0$$
Supongamos que queremos plantear un sistema mejor, incluso capaz más conveniente para representar números naturales [[N]]. La lista de digitos $a_4a_3a_2a_1$ representa al número $a_4 \cdot 4 + a_3 \cdot 3 + a_2 \cdot 2 + a_1$. Así $2301$ representa $2 \cdot 4 + 3 \cdot 3 + 1 =$ dieciocho que escrito en notación decimal sería $18$.  Pero también $3200$ y $600$ representan 18. Esto no es útil, un mismo número tiene multiples representaciones.

Entonces, para que cada número tenga una única representación le agregamos la resricción $0 \leq r_i < 10$ o sea los digitos deben ser del 0 al 9. Podemos ver a los digitos entonces como **restos** al dividir por 10. Por lo tanto
$$a = 10q_0 + r_0, \quad 0 \leq r_0 < 9$$
Donde $r_0$ es el primer digito,  $a-r_0$ es divisible por $10$ y $(a-r_0)/10 = q_0$. Si dividimos a $q_0$ por 10, tenemos que $q_0 = 10q_1 + r_1$ donde $r_1$ es el segundo digito del número, entonces:
$$\begin{align} 
a & = 10q_0 + r_0 \\
 & = 10(10q_1 + r_1) + r_0 \\
 & = 10^2 q_1 + 10^1 r_1 + 10^0r_0
\end{align}$$
Y seguimos de esta manera las divisiones sucesivas hasta que eventualmente $q_i < 10$ y ya no podamos seguir dividiendo. El resultado va a ser nuestra representación inicial de $a$. Al representar un número en sistema decimal, para aclarar que estamos usando una base 10, escribimos $(a)_{10}$ . 
Nos podemos hacer la siguiente pregunta _¿Cómo representamos en otras bases?_ 

Para representar números en **binario**, por ejemplo, seguimos el mismo proceso que con la base 10, realizamos divisiones sucesivas por 2 hasta llegar a que $q_i < 2$ y entonces nos detenemos. 

> **Teorema. (Desarrollo en base b)** Sea $d \in \mathbb{N}$ con $d \geq 2$. Todo número $a \in \mathbb{N}_0$ admite un desarrollo en base $d$ de la forma $$a = r_n \cdot d^n + r_{n-1} \cdot d^{n-1} + \cdots + r_1 \cdot d + r_0$$ con $0 \leq r_i < d$ para $0 \leq i \leq n$ y $r_n \neq 0$ si $a \neq 0$. Además dicho desarrollo, con las exisgencias $0 \leq r_i < d$ impuestas para los simbolos es único.

**Demostración.** 
- **Existencia del desarrollo en base $d$ :** La idea intuitiva es ir dividiendo iteradamente el número a y los sucesivos cocientes por $d$. Para formalizar la prueba se puede hacer por inducción en $a \in \mathbb{N}_{0}:$
	- Para $a=0$, se tiene $0=(0)_{d}$, es decir estamos en el único caso en que todos los dígitos son cero.
	- $a \geq 1$ :
	La hipótesis inductiva es que todo número natural o cero menor que $a$ admite un desarrollo en base $d$. Queremos probar que entonces $a$ admite también un desarrollo en base $d$.
	Usando el algoritmo de división, dividimos a por $d$, y obtenemos un cociente $k$ que satisface $0 \leq k<a$ y un resto $r_{0}$ que satisface $0 \leq r_{0}<d$ : Por hipótesis inductiva, al ser $0 \leq k<a, k$ admite un desarrollo en base $d$ que notamos por conveniencia en la forma:
	$$
k=r_{n} \cdot d^{n-1}+\cdots+r_{2} \cdot d+r_{1} \quad \text { con } 0 \leq r_{n}, \ldots, r_{1}<d
	$$
	Entonces
$$
\begin{aligned}
a &=k \cdot d+r_{0} \\
&=\left(r_{n} \cdot d^{n-1}+\cdots+r_{2} \cdot d+r_{1}\right) \cdot d+r_{0} \\
&=r_{n} \cdot d^{n}+\cdots+r_{1} \cdot d+r_{0}
\end{aligned}
$$
donde $0 \leq r_{i}<d$ para $0 \leq i \leq n$ como se quiere.
Así, todo $a \in \mathbb{N}$ admite un desarrollo en base $d$.
- **Unicidad:** Es una consecuencia de la unicidad del resto y del cociente en el algoritmo de división: $r_{0}$ es el resto de la división de a por $d$ y por lo tanto es único, $r_{1}$ es el resto de la división de $\left(a-r_{0}\right) / d$ por $d$ y es único también, etc... Como antes, podemos formalizar esto por inducción en $a \in \mathbb{N}_{0}$.
	- Para $a=0$, el único desarrollo es claramente $0=(0)_{d}$.
	- Para $a \geq 1$, supongamos que
$$
a=r_{n} \cdot d^{n}+\cdots+r_{1} \cdot d+r_{0}=s_{m} \cdot d^{m}+\cdots+s_{1} \cdot d+s_{0}
$$
	con $0 \leq r_{i}, s_{j}<d$ para $0 \leq i \leq n, 0 \leq j \leq m$ y $r_{n} \neq 0, s_{m} \neq 0$.
	Ahora bien, está claro que $r_{d}(a)=r_{0}=s_{0}$, y además, el cociente de dividir a por $d$ (que es único) es
$$
k=r_{n} \cdot d^{n-1}+\cdots+r_{1}=s_{m} \cdot d^{m-1}+\cdots+s_{1} .
$$
	Por hipótesis inductiva, el desarrollo en base $d$ del cociente $k$ es único, luego $n=m$ y $r_{i}=s_{i}, 1 \leq i \leq n$.

Así concluimos que para todo $a \in \mathbb{N}_{0}$, el desarrollo en base $d$ de $a$ es único. $\blacksquare$ 