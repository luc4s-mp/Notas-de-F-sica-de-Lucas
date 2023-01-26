# Momento Lineal
Conocimos a una partícula sometida en muchas fuerzas en [[Dinámica y leyes De Newton]] . En esta nota siempre tratamos que los cuerpos que trabajamos eran partículas (es decir no ocupan ningún volumen o área, también se los puede pensar como un **punto matemático**, sin dimensiones). Sin embargo, la mayoría del tiempo tratamos con cuerpos grandes que tienen una estructura. 
Los métodos utilizados en [[Aplicando las leyes de Newton]] fallan cuando intentamos analizar sistemas como asteroides en los cuales su masa cambia constantemente. Los cohetes aceleraran hacia adelante tirando parte de su propia masa, no es obvio como podemos aplicar $\vec{F} = M\vec{a}$ a tal sistema. 
En esta nota generalizaremos los conceptos para sistemas de más de una partícula. La segunda ley de Newton nos dice
$$ \vec{F} = m \vec{a}$$
Pero, en realidad esta no fue la verdadera forma en la que la escribió Newton, él la expreso de la siguiente manera
$$\vec{F} = \frac{d}{dt} \Big(m\vec{v} \Big)$$
No le dio nombre al vector $m\vec{v}$ pero nosotros si lo haremos, es comúnmente llamado **momento lineal** $\vec{p}$, o **cantidad de movimiento** de un cuerpo. Entonces,
$$\vec{F} = \frac{d \vec{p}}{dt}$$
Esta forma es preferible de $\vec{F} = m\vec{a}$ porque nos ayuda a generalizar el comportamiento de sistemas complejos, porque resulta que el momento lineal termina siendo más fundamental que la masa o la velocidad por separado. 

## Muchas partículas en un sistema
### Sistema de dos partículas
Consideremos un sistema **aislado** (es decir, un conjunto de 2 o más cuerpos en los cuales las únicas fuerzas que existen son internas), por ejemplo, dos masas $m_1$ y $m_2$ unidas por un resorte sin masa.
![[Pasted image 20220424140501.png | 400]]
Sabemos que $\vec{F}_{21} = - \vec{F}_{12}$  y sabemos entonces que si analizamos el movimiento del sistema en su conjunto (sumando la función del movimiento del cuerpo 1 $\vec{F}_{12} = m\vec{a}_2$ con la del cuerpo 2 $\vec{F}_{21} = m\vec{a}_2$):
$$m\vec{a}_1 + m\vec{a}_2 = 0 \rightarrow \frac{d}{dt}\Big(m\vec{v}_1 + m\vec{v}_2 \Big) = 0 \rightarrow \frac{d}{dt} (\vec{p_1} + \vec{p_2}) = 0$$
Estamos en un caso en el cual el momento lineal es igual a una constante que se **conserva en todo el movimiento de los cuerpos** y que por lo tanto dado que $\vec{P} = \vec{p}_1 + \vec{p}_2$ , entonces $d\vec{P}/dt = 0$. 
A las fuerzas $\vec{F}_{12}$ y $\vec{F}_{21}$ las llamamos **fuerzas internas del sistema** pues estas se cancelan cuando hablamos del sistema en conjunto. Es claro que existen otras fuerzas que están influenciando a ambos cuerpos (suponiendo que ambos cuerpos están en la superficie de la tierra) existen la fuerza normal y peso sobre cada cuerpo, las cuales al incluirlas en nuestras ecuaciones no se cancelan como las fuerzas internas, este tipo de fuerzas se dicen **fuerzas externas del sistema**.

> Cuando hablamos de que el momento se "conserva", decimos que el momento lineal es una constante y que se mantiene igual en todo tiempo del movimiento. 

### Sistemas de muchas partículas
Generalicemos ahora algunas propiedades de los sistemas físicos. Es importante saber de que hablamos cuando decimos "sistema". Somos libres de poner las fronteras de nuestro sistema donde queramos, pero una vez hayamos hecho la elección, debemos ser consistentes con las partículas que son incluidas al sistema y las que no están incluidas.
Supongamos que tenemos un sistema de partículas en el que ellas interactúan entre sí e interactúan con el exterior. Para generalizarlo, supongamos que tengo $N$ partículas de masas $m_1, m_2, \dots, m_N$. La posición de la partícula $j$ es $\vec{r}_j$ medido desde un origen O, la fuerza neta que se ejerce sobre la partícula es $\vec{F}_j$ y su momento es $\vec{p}_j = m_j\dot{\vec{{r}_j}}$. La fuerza neta de la partícula $j$ puede ser dividida en dos términos:
$$\vec{F_j} = \vec{F_j}^{int} + \vec{F_j}^{ext}$$
donde $\vec{F_j}^{int}$ es la suma de todas las **fuerzas internas** generadas por la interacción entre las partículas y $\vec{F_j}^{ext}$ es la suma de todas las **fuerzas externas** que actúan sobre la partícula. Luego, la ecuación anterior puede ser reescrita como $\frac{d\vec{p_j}}{dt}= \vec{F}_{j}^{int} + \vec{F}_j^{ext}$ y si ahora sumamos cada una de estas ecuaciones para cada partícula $j=1, \dots, N$ tenemos que
$$\sum_{j=1}^N \vec{F}_j^{int} + \sum_{j=1}^N \vec{F}_j^{ext} = \sum_{j=1}^N \frac{d\vec{p}_j}{dt} \quad \quad (1)$$
Luego, gracias a la tercera ley de newton (vista en [[Dinámica y leyes De Newton]]), las fuerzas de interacción entre dos partículas son siempre iguales y opuestas así que su suma debe ser 0. Se sigue que las fuerzas internas se cancelan en pares así que la suma de todas las fuerzas da 0.
$$\sum_{j=1}^N \vec{F}_j^{int} = 0$$
El segundo término de (1) se puede simplificar llamando a $\vec{F}_{ext} = \sum_{j=1}^N \vec{F}_j^{ext}$ la fuerza total externa del sistema y a $\sum_{j=1}^N \frac{d\vec{p}_j}{dt} = \frac{d\vec{P}}{dt}$. Tal que podemos reescribir (1) como 
$$\vec{F}_{ext} = \frac{d\vec{P}}{dt}$$
Veamos un ejemplo que ilustre porque esto es útil, hasta ahora lo único que hicimos fue definir conceptos nuevos. 

---
### Ejemplo. Las Boleadoras.
Las Boleadoras son un instrumento usado por los gauchos para cazar animales como ganado, aves y otros. Consiste en tres bolas de piedra o de hierro conectadas por cintas. El gaucho gira la boleadora en el aire y la arroja al animal. ¿Qué podemos decir de su movimiento?
![[Pasted image 20221209205008.png]]
Tenemos 3 masas $m_1$, $m_2$ y $m_3$, y la cuerda. Entonces, las únicas fuerzas externas que existen son el peso de cada masa. Tal que, el momento total obedece la simple ecuación:
$$\frac{d\vec{P}}{dt} = \vec{F}_{ext} = \vec{F_1}^{ext} + \vec{F_2}^{ext} + \vec{F_3}^{ext} = m_1 g + m_2g + m_3g = (m_1+m_2 + m_3)g = Mg$$
donde $M$ es la masa total. La ecuación representa un primer paso muy importante en encontrar la trayectoria detallada. La ecuación es idéntica si tuviéramos una única masa $M$ con momento $\vec{P}$. De esta manera, entender el movimiento de cada bola por separado puede ser muy difícil, pero se puede entender el sistema como un todo y obtener información relevante. 

---

## Centro de Masa
De acuerdo a la ecuación $\vec{F}_{ext} = \frac{d\vec{P}}{dt}$, tenemos que este resultado es idéntico a $\mathbf{F} = M\mathbf{\ddot{R}}$ [^1] donde $M$ es la masa total del sistema y $\vec{R}$ es un vector a definir. Como $\mathbf{P} = \sum_{j=1}^N m_j \dot{\mathbf{r}}_j$ nos queda que con las dos ecuaciones mencionadas anteriormente:
$$M\ddot{\mathbf{R}} = \frac{d\mathbf{P}}{dt} = \sum_{j=1}^N m_j \ddot{\mathbf{r}}_j$$
Lo cual es verdad si
$$\vec{R} = \frac{1}{M} \sum_{j=1}^N m_j \vec{r}_j$$
Tal que $\vec{R}$ es un vector desde el origen a un punto que llamamos **centro de masa**. El movimiento del centro de masa de un sistema parece comportarse como si toda la masa estuviera concentrada ahí y todas las fuerzas externas actuaran en ese punto. En [[Aplicando las leyes de Newton]] creamos un proceso para tratar problemas desde la perspectiva de que cada cuerpo que tratamos en el problema es un punto, ahora se puede ver que esto no está tan desacertado. 

A menudo, un problema puede ser simplificado eligiendo el sistema de coordenadas correcto. _El sistema de coordenadas con origen en el centro de masa es particularmente útil_. 
Considere el caso del sistema $x$, $y$, $z$, hay dos partículas localizadas en $\vec{r}_1$ y $\vec{r}_2$ y su centro de masa está en
![[Pasted image 20221209205059.png]]
$$\vec{R}_{CM} = \frac{m_1 \vec{r}_1 + m_2 \vec{r}_2}{m_1 + m_2}$$
Podemos entonces crear un nuevo sistema en las coordenadas $x'$, $y'$ y $z'$ con el origen en el centro de masa. Las coordenadas desde el centro de masa de las dos masas son $\vec{r'}_1 = \vec{r}_1 - \vec{R}$ y $\vec{r'}_2 = \vec{r}_2 - \vec{R}$. 
![[Pasted image 20221209211545.png]]
Este sistema no tiene fuerzas externas o sus fuerzas externas suman 0, pues como $\vec{R} = 0$ entonces $\ddot{\mathbf{R}} = 0$ y nos queda que $\vec{F}_{ext} = 0$, tal que el movimiento del centro de masa es trivial, se mueve uniformemente. Es más, $m_1 \vec{r'}_1 + m_2 \vec{r'}_2 = 0$ por lo cual, si sabemos el movimiento de una partícula, el movimiento de la otra ya queda determinado. 

## Conservación del Momento Lineal
>[!LEY DE CONSERVACIÓN DEL MOMENTO LINEAL]
>Cuando tenemos que no existen fuerzas externas o estas se anulan $\vec{F}_{ext} = 0$, entonces decimos que el momento lineal **se conserva** pues $d\vec{P}/dt = 0$ y por un corolario del [[Teorema del Valor Medio]] tenemos que $\vec{P}(t)$ es una función constante.

Esta ley se sigue directamente de la Tercera Ley de Newton, vista en [[Dinámica y leyes De Newton]], tal que la ley de conservación parece ser una consecuencia natural de la mecánica newtoniana. 
En algunas situaciones podemos aplicar la conservación del momento lineal por **continuidad de** $\vec{P}(t)$ pues como $\vec{P} = m\vec{v}$ y la velocidad $\vec{v}(t)$ tiene que ser una **función continua** (por lo visto en [[Cinemática del punto]]) entonces $\vec{P}(t)$ también lo es. Entonces, podemos decir que si sabemos que la función está cerca de un valor $P$ si tomamos un intervalo de tiempo infinitesimalmente pequeño si la función va estar muy cerca de $P$ con una diferencia prácticamente indistinguible. 

## Impulso
Supongamos que reescribimos la ecuación $\vec{F} = \frac{d\vec{P}}{dt}$ de la siguiente manera
$$\begin{align}
\vec{F}_{net} = \frac{\lim_{t \rightarrow t_f}\vec{P}(t) - \vec{P}(t_f)}{\lim_{t \rightarrow t_f}t-t_f} \quad \rightarrow \quad (\lim_{t \rightarrow t_f}t-t_f)\vec{F}_{net} = {\lim_{t \rightarrow t_f}\vec{P}(t) - \vec{P}(t_f)} \quad \rightarrow \quad dt\vec{F}_{net} = d\vec{P}\\
\int_{t_i}^{t_f} d \vec{p} = \int_{t_i}^{t_f} \vec{F}_{net}\cdot dt \quad \rightarrow \quad \vec{p}_f - \vec{p}_i = \Delta \vec{p} = \int_{t_i}^{t_f} \vec{F}_{net}\cdot dt \\
\end{align}$$
Observemos que dependiendo de cuanta fuerza apliquemos en un cierto período de tiempo muy corto, mayor o menor va a ser el cambio en momento. Una mayor fuerza aplicada en un período de tiempo corto implica un gran cambio en momento (es decir el cuerpo va a cambiar su velocidad rápidamente por una más grande o más chica), al mismo tiempo que una fuerza chica aplicada en un período de tiempo largo también indica un gran cambio de momento. Sabiendo esto podemos entender porque otra forma de llamarlo es la **cantidad de movimiento**, porque representa _cuanto movimiento es generado por fuerza aplicada en un cierto período de tiempo infinitesimalmente pequeño._

Un ejemplo muy visual del impulso es en un choque de autos. El auto que choca pasa de tener una velocidad muy grande a volverse 0 en un intervalo de tiempo muy chico, lo cual implica que la fuerza generada sobre el conductor va a ser muy grande. Justamente las bosas de aire están  diseñadas para frenar más lentamente la velocidad del conductor (lo que implica un cambio de momento menor) y así que la fuerza generada sobre el conductor sea menor.
El cambio de momento en un cierto tiempo normalmente es llamado *impulso*.

---
### Ejemplo. Picando una pelota de caucho.
Una pelota de caucho de masa $0.2$ kg cae al piso. La pelota choca con una velocidad de $8$ m/s y vuelve con aproximadamente la misma velocidad. Fotografías de alta velocidad muestran que la pelota está en contacto con el piso por $\Delta t = 10^{-3} \; s$ ¿Qué podemos decir sobre la fuerza ejercida por el piso en la pelota?
![[Pasted image 20221210105614.png]]
El momento de la pelota justo antes de que choque con el piso es de $\vec{P}_a = -1.6 \; kg \cdot m/s \; \hat{\mathbf{k}}$ y su momento $10^{-3} \; s$ después es $\vec{P}_b = +1.6 \; kg \cdot m/s \; \hat{\mathbf{k}}$. Usando $\int_{t_a}^{t_b} \vec{F}dt = \vec{P}_b - \vec{P}_a$ tenemos que $\int_{t_a}^{t_b} \vec{F}dt = 1.6 \; \hat{\mathbf{k}} - (-1.6 \hat{\mathbf{k}}) = 3.2 \; kg \cdot m/s \; \hat{\mathbf{k}}$. Notemos que la fuerza $\vec{F}$ es una fuerza que varía con el tiempo, por el Teorema del Valor Medio para integrales visto en [[Teorema Fundamental del Cálculo]], existe una fuerza promedio $\vec{F}_{pr}$ tal que
$$\vec{F}_{pr}\Delta t = \int_{t_a}^{t_b+\Delta t}\vec{F}dt$$
![[Pasted image 20221210105646.png]]
Como $\Delta t = 10^{-3} \; s$ 
$$\vec{F}_{pr} = \frac{3,2 \; kg \cdot m/s}{10^{-3} \; s} = 3200 \; N \; \hat{k}$$
Pero usted notará que hay un fallo en el cálculo de la fuerza, que es que asumimos que $\vec{F}_{piso}$ (la fuerza producida por el piso) es la única, cuando en realidad es obvio que existe el peso también como otra fuerza que también causa impulso. Veamos entonces:
$$\vec{F} = \vec{F}_{piso} - Mg \;\hat{\mathbf{k}} \quad \rightarrow \quad \int_0^{10^{-3}} \vec{F} dt = \int_0^{10^{-3}} \vec{F}_{piso}dt - \int_{0}^{10^{-3}} Mg \; \hat{\mathbf{k}}\; dt = 3.2 \; kg \cdot m/s \; \hat{\mathbf{k}}$$
Tal que ahora si calculamos el impulso del peso obtenemos que
$$- \int_0^{10^{-3}} Mg \; dt \; \hat{\mathbf{k}} = -Mg \int_0^{10^{-3}}dt \; \hat{\mathbf{k}} = -(0.2)(9.8)(10^{-3}) \; kg \cdot m/s \; \hat{\mathbf{k}} = -1.96 \cdot 10^{-3} \; kg \cdot m/s \; \hat{\mathbf{k}}$$
Esto es menos que un milésimo del impulso total, por lo cual podemos directamente evitarlo. El peso puede cambiar el momento de la pelota si se aplica en largos intervalos de tiempo, pero en cortos como en este caso su efecto es casi nulo comparado a lo grande que es la fuerza de contacto con el piso. 


[^1]: A veces utilizaremos la letra **negrita** para referirnos a cantidades vectoriales para no confundir los dos puntos. 

