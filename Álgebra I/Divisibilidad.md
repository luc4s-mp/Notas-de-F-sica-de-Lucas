# Divisibilidad
Los números enteros $\mathbb{Z}$ tienen un problema en la ecuación $a = bx$ para unos $a,b \in \mathbb{Z}$, resulta que no tiene soluciones para todos los $a, b$ que elijamos. Esto es porque en los enteros no existen los inversos multiplicativos, es decir ecuaciones como $2x = 1$ no se pueden resolver pues no existe el inverso multiplicativo de 2 en los enteros (que en los reales sería $x = \frac{1}{2}$).

Nuestro lugar de inicio es el llamado el **algoritmo de la división** que nos habla de cuando podemos dividir en los números enteros [[Z]]. 

## Algoritmo de la división
> **Teorema. (Algoritmo de la división)** Sean $a, b \in \mathbb{Z}, b > 0$ entonces $\exists q \in \mathbb{Z}$ y $r \in \mathbb{Z}$ tales que $$a = bq + r \;\; \text{ con } \;\; 0 \leq r < |b|$$Estos números $q$ (el cociente) y $r$ (el resto) son únicos.

El objetivo de presentar este teorema no es resolver una división inicialmete, sino de demostrar que cualquier par de números enteros se puede escribir como la multiplicación de uno de ellos por otro al que llamamos cociente y luego sumado a uno al que llamamos resto. Por ahora, esto nada tiene que ver con la división, pero eventualmente lo hará. 

**Demostración.** La demostración se puede dividir en dos partes: la existencia de los números $q$ y $r$, y la únicidad de esos números.
- **Existencia:** 
	- **Caso 1:** Sea $a \geq 0$  y $b > 0$. El caso $a = 0$ es trivial pues obviamente $q=0$ y $r=0$ tal que $0 = 0b + 0$.  Entonces, tomemos directamente $a>0$. Sea $S = \{n : n \cdot b > a, \; n \in \mathbb{N}\}$. Obviamente $S \subseteq \mathbb{N}$ y sabemos que el conjunto no está vacío, pues $a+1 \in S$ por $a+1 > a$ y como $b > 0 \rightarrow (a+1)b > a$. En consecuencia, $S$ tiene primer elemento por el principio de buena ordenación (visto en [[Principio de la inducción fuerte]]), llamemos a este primer elemento $n_1$. Ahora, notemos que todos los $q$ que buscamos entan antes de $n_1$ , por lo cual  $n_1 \cdot b > a$, pero $(n_1 -1) \cdot b \leq a$.  Hay dos subcasos, dependiendo que parte de $\leq$ se cumpla.
		- **Subcaso 1:** Si $(n_1 - 1)b = a$ entonces podemos elegir a $q = n_1 - 1$ como un posible cociente y $r=0$ como un posible resto.
		- **Subcaso 2:** Si $(n_1 - 1)b < a$, entonces tomemos $q = n_1 - 1$ y  $qb < a < (q+1)b$ luego $qb < a < qb+b$ si por hipótesis $r = a-qb \rightarrow r = a - (n_1 -1)b$ nos queda que $0 < r < b$.
		Como conclusión de ambos casos encontramos unos posibles $q$ y $r$ tal que  $0 \leq r < b$ como queriamos.
	- **Caso 2**: Sea $a > 0$ y $b < 0$. dividimos $a$ por $-b$; así existen $q'$ y $0 \leq r \leq -b = |b|$ tales que $a = q'(-b) + r$. Reescribiendo $a = (-q)b+r$.
	- **Caso 3:** Sea $a < 0$ y $b > 0$. Sea $a = -c, \; c \in \mathbb{N}$ . Como $c > 0$ tenemos el caso 1 por lo cual existen un $q'$ y un $r'$ . Entonces, $-a = q'b + r'$, es decir $a = -q'b-r'$. Si $r'=0$ elegimos $q = q'$ y $r=r'=0$ . Si $0 < r'<b$, es decir si $-b < -r < 0$ sumamos b para obtener $0< -r'+b < b$ y en $a = (-q'-1)b + (b-r')$. Elegimos entonces $q = -q'-1$ y $r=b-r'$.
	- **Caso 4**: Sea $a<0$ y $b < 0$. como $-b>0$ dividimos $-a$ por $-b$; así existen $q^{\prime}$ y $0 \leq r^{\prime}<-b$ tales que $-a=q^{\prime}(-b)+r^{\prime}$, es decir $a=q^{\prime} b-r^{\prime}$. Si $r^{\prime}=0$ elegimos $q=q^{\prime}$ y $r=r^{\prime}=0$. Si $0<r^{\prime}<-b$, tenemos que $a=q^{\prime} b-r^{\prime}$ con $b<-r^{\prime}<0$. Sumando y restando $b$ resulta que $a=q^{\prime} b+b-b-r^{\prime}=\left(q^{\prime}+1\right) b+\left(-b-r^{\prime}\right)$ con $0<-b-r^{\prime}<-b=|b|$. Luego elegimos $q=q^{\prime}+1$ y $r=-b-r^{\prime}$.
- **Unicidad:** Por último, supongamos que $a=q b+r=q^{\prime} b+r^{\prime}$ con $0 \leq r, r^{\prime}<b$. Entonces $\left(q-q^{\prime}\right) b=r^{\prime}-r$, es decir $r^{\prime}-r$ es un múltiplo de $b$. Como $0 \leq r^{\prime}<b$ y $0 \leq r<b$, tenemos que $0 \geq-r>-b$ y luego que $-b<r^{\prime}-r<b$. Siendo 0 el único múltiplo de $b$ en estas condiciones resulta que $r^{\prime}-r=0$, es decir $r^{\prime}=r$ y luego, dado que $b \neq 0$, resulta también que $q^{\prime}=q$.  $\blacksquare$ 

Entonces, por el algoritmo de división podemos decir que existe la división en los números enteros cuando $r=0$. Es decir, tenemos que $a=bq$ para algún $q \in \mathbb{Z}$. 

> #Definición Si $a, b \in \mathbb{Z}$, $b \neq 0$, decimos que **a divide a b** ($a|b$) si existe un $c \in \mathbb{Z}$ tal que $a = b \cdot c$. Hablar de divisibilidad es útil unicamente para [[Z]].

También se puede decir que **b es un múltiplo de a** o que **a es un divisor de b**. Para expresar que $a$ no divide a $b$, escribimos $a \nmid b$. 
Decimos que los divisores de $6$ son $\pm 6, \pm 3, \pm 2, \pm 1$. Podemos hablar de un conjunto que contega todos estos números.

> **Definición.** Sea $\mathrm{Div}(n)$ el conjunto de divisores de un entero $n$, es decir $\mathrm{Div}(n) = \{d \in \mathbb{Z}: d|n\}$ 

Tenemos entonces que
- $\{1,-1,n,-n\} \subseteq \mathrm{Div}(n)$ 
- $\mathrm{Div}(1) = \{1,-1\}$
- $\mathrm{Div}(0) = \mathbb{Z}$ 
- Si $a \in \mathrm{Div}(n) \iff -a \in \mathrm{Div}(n)$
Para denotar únicamente los divisores positivos de un número usamos $\mathrm{Div}_+(n)$. 

> **Lema.** Sean $a, b, c \in \mathbb{Z}$. Entonces,
> 1. $1|a$ y si $a \neq 0 \implies a|a$
> 2. Si $a \neq 0, \;\; b \neq 0, \;\; a|b$ y $b|c \implies a|c$.
> 3. Si $a,  b\neq  0, a|b$ y $b|a$, entonces o $a=b$ o $a = - b$.
> 4. Si $a \neq 0, \;\; a|(b+c)$ y $a|b \implies a|c$.
> 5. Si $a \neq 0, \; a|b$ y $a|c \implies a|b+c$ y $a|b-c$
> 6. Si $a \neq 0, a|b \implies a|bc$. 
> 7. Si $a \neq 0$ y $c|a \implies |c| \leq |a|$. 

**Demostración**.
1. $a = 1 \cdot a \implies 1|a$ y $a|a$
2. $a|b \implies \exists s \in \mathbb{Z}: b = a \cdot s$
	$b|c \implies \exists t \in \mathbb{Z}: c = b \cdot t$
	$c = (a \cdot s)\cdot t = a \cdot (st) \implies a|c$
3. Si $a|b \implies \exists q \in \mathbb{Z} : b = aq$ y luego $b|a \implies \exists k \in \mathbb{Z} : a = kb$. Entonces si reemplazamos una ecuación en la otra $b= (kb)q \implies b = (kq)b \implies kq = 1$. Por lo cual tenemos dos casos $k=1$ y $q=1$ o $k=-1$ y $q=-1$.
4. $a|b \implies \exists s \in \mathbb{Z}: b = a \cdot s$
	$a|(b+c) \implies \exists t \in \mathbb{Z}: b+c = a \cdot t$
	$b +c = a \cdot t \Rightarrow (a \cdot s) + c  = a \cdot t \Rightarrow c =  a \cdot t - a \cdot s \Rightarrow c = a(t-s) \implies a|c$
5. $a|b \implies \exists s \in \mathbb{Z}: b = a \cdot s$
	$a|c \implies \exists t \in \mathbb{Z}: c = a \cdot t$
	$b+c = a \cdot s + a \cdot t = a(s + t) \implies a|b+c$
	$b-c = a \cdot s - a \cdot t = a(s - t) \implies a|b-c$
6. Si $a|b \implies \exists q \in \mathbb{Z} : b = qa$ y si multiplicamos de ambos lados del igual por $c \in \mathbb{Z}$ tenemos que $b \cdot c = qa\cdot c \rightarrow bc = (qc)a \implies a|bc$. 
7. Si $c|a \implies \exists q \in \mathbb{Z} : a = cq$, luego $|a| = |q| \cdot |c| \geq |c|$ ya que $|q| \geq 1$. $\blacksquare$  

> **Teorema.** Si $c \in \mathbb{Z}$ divide a $a_1,a_2, \cdots, a_k \in \mathbb{Z}$ entonces $c$ divide a $a_1u_1 + a_2u_2 + \cdots + a_k u_k$ para todos los enteros $u_1, u_2, \cdots, u_k$.

Este teorema nos presenta un tipo de ecuación matemática que utilizaremos mucho en esta parte de la aritmética que son las **combinaciones lineales** en donde se combina la multiplicación y la suma de muchas variables en un polinomio de grado 1. El teorema sale como conclusión de las propiedades (5) y (6) del lema.
En particular usaremos más el siguiente colorario en vez del teorema.
> **Colorario.** Si $c$ divide $a$ y $b$, entonces $c|au+bv$ para todos los enteros $u$ y $v$.

---

### Descripción del algoritmo de la división
Queremos calcular q y r donde q es el cociente y r es el resto de la división de $a$ por $b \neq 0$.
- Si $a \geq 0$ y $b > 0$:
	- Tomar $q = 0, \; r = a$
	- Mientras que $r \geq d$, reemplazar
		- $k \leftarrow k+1$
		- $r  \leftarrow r-d$
- Si $a \geq 0$ y $b< 0$:
	- Aplicar el algoritmo a $a$ y $-d$
	- Dar como respuesta $(-q, r)$
- Si $a < 0$ y $b > 0$:
	- Aplicar el algoritmo a $-a$ y $b$.
	- Si $r = 0$, dar como respuesta $(-q, 0)$
	- Si no, dar como respuesta $(-q-1, d-r)$
- Si $a < 0$ y $b > 0$:
	- Aplicar el algoritmo a $-a$ y $b$.
	- Si $r = 0$, dar como respuesta $(-q, 0)$
	- Si no, dar como respuesta $(q+1, -r-d)$
Una de las aplicaciones más útiles del algoritmo de la división es para encontrar el [[Máximo Común Divisor]].
