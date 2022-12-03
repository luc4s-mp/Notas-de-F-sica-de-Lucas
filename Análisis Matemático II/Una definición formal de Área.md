# Una definición formal del área
El objetivo de esta #Estructura-matematica nueva es encontrar el área debajo de una curva definida por una función $f: \mathbb{R} \rightarrow \mathbb{R}$ ([[R]]) en el intervalo $[a, b]$ .

Sea $f:[a, b] \rightarrow \mathbb{R}$ una __funcion acotada__. Usaremos el [[Axiomas (Básicos) de los números reales]] Nuestro propósito ahora es definir una de las nociones centrales del curso que es la de __Integral de Riemann__ de $f$ sobre el intervalo $[a, b]$ la que, cuando $f$ es positiva nos dara el area de la region $R(f, a, b)$ delimitada por el grafico de $f$, el eje $x$ y las rectas $x=a$ y $x=b$, esto es, la region de la siguiente figura:

con la definicion que daremos, no para toda $f$ funcion acotada sobre $[a, b]$ existira su integral de Riemann sobre $[a, b]$ por lo que tendremos además que definir la nocion de funcion integrable Riemann sobre $[a, b]$.
Comenzamos con las siguientes definiciones preliminares:

> **Definición 1.3.** Llamaremos partición del intervalo $[a, b]$ a todo conjunto finito ordenado $P=\left\{t_{0}, t_{1}, \ldots, t_{n}\right\}$ tal que $a=t_{0}<t_{1}<t_{2}<\ldots<t_{n}=b$.

Notar que una particion $P=\left\{t_{0}, t_{1}, \ldots, t_{n}\right\}$ del intervalo $[a, b]$ parte al intervalo $[a, b]$ en $n$ subintervalos, a saber los subintervalos $\left[a_{1} t_{1}\right],\left[t_{1}, t_{2}\right], \ldots .\left[t_{n-1}, b\right]$ (de alli el nombre de partición).

> #Definición **(Sumas Superiores e Inferiores)** Si $f:[a, b] \rightarrow \mathbb{R}$ es una funcion acotada y si $P=$ $\left\{t_{0}, t_{1}, \ldots, t_{n}\right\}$ es una particion del intervalo $[a, b]$, definimos la suma inferior $s(f, P)$ mediante $$ s(f, P)=\sum_{i=1}^{n} m_{i}\left(t_{i}-t_{i-1}\right) $$donde $m_{i}=\inf \left\{f(t): L \in\left[t_{i-1}, t_{i}\right]\right\}$.
Definimos tambien la suma superior $S(f, P)$ mediante  $$ S(f, P)=\sum_{i=1}^{n} M_{i}\left(t_{i}-t_{i-1}\right)$$
donde $M_{i}=\sup \left\{f(t): t \in\left[t_{i-1}, t_{i}\right]\right\}$.

Notese que, por ser $f$ acotada en $[a, b]$, lo es tambien en cada subintervalo $\left[t_{i-1}, t_{i}\right]$, luego, para cada $i,\left\{f(t): t \in\left[t_{i}-1, t_{i}\right]\right\}$ es acotado, tanto superiormente como inferiormente y por lo tanto los numeros $m_{i}$ y $M_{i}$ estan bien definidos.

> __Teorema 1.5.__  Sea $f$ una funcion acotada en $[a, b]$ y $P$ y $Q$ particiones de $[a, b]$. Entonces $s(f, P) \leq S(f, Q)$.

Para demostrar este teorema es necesario ver un par más de lemas.

Daremos la demostracion del Teorema 1.5 da clase que viene.
> __Corolario 1.6.__ Si $f$ es una función acotada en $[a, b]$ entonces $\sup \{s(f, P): P$ es particion de $[a, b]\}$ y  inf $\{S(f, Q): Q$ es particion de $[a, b]\}$ existen y vale que $\sup \{s(f, P): P$ es particion de $[a, b]\} \leq \inf \{S(f, Q): Q$ es particion de $[a, b]\}$

__Prueba.__ Por el Teorema 1.5. cualquier suma superior de $f$ es una cota superior del conjunto de de todas las sumas inferiores de $f$, entonces el conjunto de todas las sumas inferiores esta acotado superiormente y claramente es no vacio, por lo tanto existe el sup $\{s(f, P): P$ es particion de $[a, b]\}$. Mas aun, como, para cualquier particion $Q, S(f, Q)$ es una cota superior del conjunto $\{s(f, P): P$ es particion de $[a, b]\}$, deberemos tener que
$$
\sup \{s(f, P): P \text { es particion de }[a, b]\} \leq S(f, Q)
$$
Podemos aplicar el mismo proceso para el conjunto $\{S(f,Q) : Q$ es una partcición de $[a,b]\}$  y obtendremos que
$$s(f, P) \leq \inf\{S(f,Q) : Q \text{ es una partición de } [a, b] \}$$
Uniendo las desigualdades y mirando en las extremos concluimos
$$\sup \{s(f, P): P \text { es particion de }[a, b]\} \leq \inf\{S(f,Q) : Q \text{ es una partición de } [a, b] \} \quad \blacksquare$$
Más adelante en la definición de función integrable veremos que en realidad esta desigualdad resulta ser una igualdad para este tipo de funciones.

## Analizando el área debajo de una función
Escencialmente, las sumas superiores e inferiores, representan una aproximación del área debajo de una función acotada. Cada sumando $m_i(t_i - t_{i-1})$ de las sumas inferiores si lo analizamos es un pequeño rectangulo con base $(t_i - t_{i-1})$ y de altura $m_i$ y al sumar todos estos rectangulos obtenemos una aproximación del área. Notaremos que en el caso de las sumas inferiores, nuestra estimación va a estar **por debajo del valor real del área** $s(f,P) \leq Área(R(f,a,b))$ para cualquier $P$ y en las sumas superiores vamos a tener una estimación **por arriba del valor real del área** entonces $S(f,P) \geq Área(R(f,a,b))$ .

A medida que la partición $P$ tenga más elementos, mejor será la aproximación para ambos casos. Fijemosnos que el conjunto de tanto sumas superiores como sumas inferiores **tienden** a un número en particular (el área) por lo tanto podemos aplicar la definición de [[Límite Finito de Sucesiones]] . Entonces, si yo creo una sucesión de particiones $\{P_n\}_{n \in \mathbb{N}}$ y luego creo otra más a partir de esta con las sumas superiores, va a suceder que $\lim_{n \rightarrow \infty} S(f, P_n) = Area(R(f,a,b))$ , como sabemos que la sucesión de sumas superiores está acotada inferiormente, entonces
$$Area(R(f,a,b)) = \inf\{S(f,P) : P \text{ es una partición de } [a, b] \}$$
Y podemos aplicar el mismo proceso para las sumas inferiores y obtener que
$$Area(R(f,a,b)) = \sup \{s(f, P): P \text { es particion de }[a, b]\}$$
Por lo tanto, 
$$\sup \{s(f, P): P \text { es particion de }[a, b]\} = \inf \{S(f, P): P \text { es particion de }[a, b]\}$$
Las funciones aquellas en la que la igualdad vale podemos llamarlas "funciones razonables para calcular su área" o directamente "**funciones integrables**".

>  **Definición 1.7.** Sea $f : [a, b] \rightarrow \mathbb{R}$ una función (no necesariamente positiva). Diremos que $f$ es integrable en $[a,b]$ si y solo si $f$ es acotada y además  $$\sup \{s(f, P): P \text { es particion de }[a, b]\} = \inf \{S(f, Q): Q \text { es particion de }[a, b]\}$$

> **Definición 1.8.** Si $f$ es integrable definimos la integral de $f$ sobre el intervalo $[a, b]$ como el valor común entre el supremo e infimo, esto es, $$\int_a^b f(x) dx = \sup \{s(f, P): P \text { es particion de }[a, b]\} = \inf \{S(f, Q): Q \text { es particion de }[a, b]\}$$

Sin embargo, en la práctica, aplicar esta definición de integrabilidad resulta un poco tedioso, para esto existen dos criterios de integrabilidad que se pueden usar (cualquiera de los dos) para demostrar que una función es integrable.

> **Teorema 1.10 (primer criterio de integrabilidad).** Sea $f : [a, b] \rightarrow \mathbb{R}$ una función acotada. Si existen $l \in \mathbb{R}$ y una sucesión de particiones $\{P_n\}_{n \in \mathbb{N}}$ de $[a, b]$ tales que $\lim_{n \rightarrow \infty} s(f,P_n) = \lim_{n \rightarrow \infty} S(f, P_n) = l$, entonces $f$ es integrable y $\int_a^b f(x)dx = l$.  

**Prueba.** Sea 
$$A = \{s(f,P) : P \text{ es una partición de } [a,b]\} \quad \text{ y } \quad B = \{S(f,P) : P \text{ es una partición de } [a,b]\}$$
Ahora, para cada $n$ tenemos que $s(f, P_n) \leq \sup(A)$ y $\inf(B) \leq S(f, P_n)$. También, por el colorario 1.6, $\sup(A) \leq \inf(B)$. Luego, $s(f, P_n) \leq \sup(A) \leq \inf(B) \leq S(f, P_n)$ si calculamos el límite de los extremos
$$l = \lim_{n \rightarrow \infty} s(f, P_n) \leq \sup(A) \leq \inf (B) \leq \lim_{n \rightarrow \infty} S(f, P_n) = l$$
entonces $l \leq \sup(A) \leq \inf(B) \leq l$ lo que implica $\sup A = \inf B = l \quad \blacksquare$ .

> **Teorema 1.11. (segundo criterio de integrabilidad).** Sea $f: [a, b] \rightarrow \mathbb{R}$ una función acotada. Entonces $f$ es integrable en $[a, b]$ si y solo si para todo $\epsilon > 0$  existe una partición $P$ de $[a, b]$ tal que $S(f, P) - s(f, P) < \epsilon$ . 

**Prueba.** ($\Rightarrow$) Supongamos que $f$ es integrable en $[a, b]$. Entonces,
$$\sup \{s(f,P) : P \text{ es partición de } [a, b] \} = \inf \{S(f, Q) : Q \text{ es una partción de } [a, b]\}$$
Sea $l$ el valor común del ínfimo y el supremo y sea $\epsilon > 0$. Entonces, $l - \frac{\epsilon}{2} < \sup \{s(f,P) : P \text{ es partición de } [a, b] \}$  
Luego, como $\sup \{s(f,P) : P \text{ es partición de } [a, b] \}$ es la menor de las cotas superiores entonces $l - \frac{\epsilon}{2}$ no es una cota superior del conjunto $\{s(f,P) : P \text{ es partición de } [a, b] \}$ . Entonces existe una partición $P_{\epsilon}$ de $[a, b]$ tal que 
$$l - \frac{\epsilon}{2} < s(f, P_{\epsilon})$$
Por otro lado, sabemos que $l + \frac{\epsilon}{2} > \inf \{S(f, Q) : Q \text{ es una partción de } [a, b]\}$ . Luego, como el infimo es la mayor de todas las cotas inferiores $l + \frac{\epsilon}{2}$ no es una cota inferior de $\{S(f, Q) : Q \text{ es una partción de } [a, b]\}$ . Entonces existe una partición $Q_{\epsilon}$ de $[a, b]$ tal que
$$l + \frac{\epsilon}{2} > S(f, Q_\epsilon)$$
Sea la partición $P = P_\epsilon \cup Q_\epsilon$ .  Y por el lema 1.9. yo se qué $s(f, P) \geq s(f, P_\epsilon)$ y $S(f, P) \leq S(f, Q_\epsilon)$ , entonces
$$s(f, P) \geq s(f, P_\epsilon) > l - \frac{\epsilon}{2} \quad \quad S(f, P) \leq S(f, Q_\epsilon) < l + \frac{\epsilon}{2}$$
Si entonces, restamos una sobre la otra obtenemos que
$$S(f,P) - s(f, P ) < l + \frac{\epsilon}{2} - \Big(l + \frac{\epsilon}{2} \Big) = \epsilon \quad \square$$
($\Leftarrow$) P
