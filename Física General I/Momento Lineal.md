# Momento Lineal
Conocimos a una particula sometida en muchas fuerzas en [[Dinámica y leyes De Newton]] . En esta nota siempre tratamos que los cuerpos que trabajamos eran partículas (es decir no ocupan ningún volumen o área, también se los puede pensar como un **punto matemático**, sin dimensiones). Sin embargo, la mayoría del tiempo tratamos con cuerpos grandes que tienen una estructura. 
Los métodos utilizados en [[Aplicando las leyes de Newton]] fallan cuando intentmos generalizar sistemas cuando tenemos más de una partícula interctuando entre sí, por ejemplo en el sistema solar, las orbitas de los planetas no se ven afectadas únicamente por la [[Fuerzas Gravitacionales]] que le hace el sol, sino también por las fuerzas que le hacen otros planetas que están cerca suyo, entender como actua el sistema solar en su conjunto es más dificil en este caso.
En esta nota generalizaremos los conceptos para sistemas de más de una partícula. La segunda ley de Newton nos dice
$$ \vec{F} = m \vec{a}$$
Pero, en realidad esta no fue la verdadera forma en la que la escribió newton, él la expreso de la siguiente manera
$$\vec{F} = \frac{d}{dt} \Big(m\vec{v} \Big)$$
Él no le dió nombre a este vector $m\vec{v}$ pero nosotros si lo haremos, es comunmente llamado **momento lineal** $\vec{p}$, o **cantidad de movimiento** de un cuerpo. Entonces,
$$\vec{F} = \frac{d \vec{p}}{dt}$$
Esta forma es preferible de $\vec{F} = m\vec{a}$ porque nos ayuda a generalizar el comprotamiento de sistemas complejos, porque resulta que el momento lineal termina siendo más fundamental que la masa o la velocidad por separado. 

## Impulso
Supongamos que reescribimos la ecuación anterior de la siguiente manera
$$\begin{align}
\vec{F}_{net} = \frac{\lim_{t \rightarrow t_f}\vec{P}(t) - \vec{P}(t_f)}{\lim_{t \rightarrow t_f}t-t_f} \quad \rightarrow \quad (\lim_{t \rightarrow t_f}t-t_f)\vec{F}_{net} = {\lim_{t \rightarrow t_f}\vec{P}(t) - \vec{P}(t_f)} \quad \rightarrow \quad dt\vec{F}_{net} = d\vec{P}\\
\int_{t_i}^{t_f} d \vec{p} = \int_{t_i}^{t_f} \vec{F}_{net}\cdot dt \quad \rightarrow \quad \vec{p}_f - \vec{p}_i = \Delta \vec{p} = \int_{t_i}^{t_f} \vec{F}_{net}\cdot dt \\
\end{align}$$
Observemos que dependiendo de cuanta fuerza apliquemos en un cierto período de tiempo muy corto, mayor o menor va a ser el cambio en momento. Una mayor fuerza aplicada en un período de tiempo corto implica un gran cambio en momento (es decir el cuerpo va a cambiar su velocidad rapidamente por una más grande o más chica), al mismo tiempo que una fuerza chica aplicada en un período de tiempo largo también indica un gran cambio de momento. Sabiendo esto podemos entender porque otra forma de llamarlo es la **cantidad de movimiento**, porque representa _cuanto movimiento es generado por fuerza aplicada en un cierto período de tiempo infinitesimalmente pequeño._
Un ejemplo muy visual del cambio en momento es en un choque de autos. El auto que choca pasa de tener una velocidad muy grande a volverse 0 en un intervalo de tiempo muy chico, lo cual implica que la fuerza generada sobre el conductor va a ser muy grande. Justamente las bosas de aire están  diseñadas para frenar más lentamente la velocidad del conductor (lo que implica un cambio de momento menor) y así que la fuerza generada sobre el conductor sea menor.
El cambio de momento en un cierto tiempo normalmente es llamado *impulso*.

## Muchas particulas en un sistema
### Sistema de dos partículas
Consideremos un sistema **aislado** (es decir, un conjunto de 2 o más cuerpos en los cuales las únicas fuerzas que existen son internas), por ejemplo, dos masas $m_1$ y $m_2$ unidas por un resorte sin masa.
![[Pasted image 20220424140501.png | 400]]
Sabemos que $\vec{F}_{21} = - \vec{F}_{12}$ sabemos entonces que si analizamos el movimiento del sistema en su conjunto (sumando la función del movimiento del cuerpo 1 $\vec{F}_{12} = m\vec{a}_2$ con la del cuerpo 2 $\vec{F}_{21} = m\vec{a}_2$):
$$m\vec{a}_1 + m\vec{a}_2 = 0 \rightarrow \frac{d}{dt}\Big(m\vec{v}_1 + m\vec{v}_2 \Big) = 0 \rightarrow \frac{d}{dt} (\vec{p_1} + \vec{p_2}) = 0$$
Estamos en un caso en el cual el momento lineal es igual a una constante que se **conserva en todo el movimiento de los cuerpos** y que por lo tanto dado que $\vec{P} = \vec{p}_1 + \vec{p}_2$ , entonces $d\vec{P}/dt = 0$. 
A las fuerzas $\vec{F}_{12}$ y $\vec{F}_{21}$ las llamamos **fuerzas internas del sistema** pues estas se cancelan cuando hablamos del sistema en conjunto. Es claro que existen otras fuerzas que están influenciando a ambos cuerpos (suponiendo que ambos cuerpos están en la superficie de la tierra) existen la fuerza normal y peso sobre cada cuerpo, las cuales al incluirlas en nuestras ecuaciones no se cancelan como las fuerzas internas, este tipo de fuerzas se dicen **fuerzas externas del sistema**.
> Cuando hablamos de que el momento se "conserva", decimos que el momento lineal es una constante y que se mantiene igual en todo tiempo del movimiento. 

### Sistemas de muchas partículas
Generalicemos ahora algunas propiedades de los sistemas físicos. Es importante saber de que hablamos cuando decimos "sistema". Somos libres de poner las fronteras de nuestro sistema donde queramos, pero una vez hayamos hecho la elección, debemos ser consistentes con las partículas que son incluidas al sistema y las que no están incluidas.
Supongamos que tenemos un sistema de partículas en el que ellas interactuan entre sí e interactuan con el exterior. Para generalizarlo, supongamos que tengo $N$ partículas de masas $m_1, m_2, \dots, m_N$. La posición de la partícula $j$ es $\vec{r}_j$ medido desde un origen O, la fuerza neta que se ejerce sobre la partícula es $\vec{F}_j$ y su momento es $\vec{p}_j = m_j\dot{\vec{{r}_j}}$. La fuerza neta de la partícula $j$ puede ser dividida en dos términos:
$$\vec{F_j} = \vec{F_j}^{int} + \vec{F_j}^{ext}$$
donde $\vec{F_j}^{int}$ es la suma de todas las fuerza interna generadas por la interacción entre las partículas y $\vec{F_j}^{ext}$ es la suma de todas las fuerzas externas que actuan sobre la partícula. Luego, la ecuación anterior puede ser reescrita como $\frac{d\vec{p_j}}{dt}= \vec{F}_{j}^{int} + \vec{F}_j^{ext}$ y si ahora sumanos cada una de estas ecuaciones para cada particula $j=1, \dots, N$ tenemos que
$$\sum_{j=1}^N \vec{F}_j^{int} + \sum_{j=1}^N \vec{F}_j^{ext} = \sum_{j=1}^N \frac{d\vec{p}_j}{dt}$$
Luego, gracias a la tercera ley de newton (vista en [[Dinámica y leyes De Newton]]) 

