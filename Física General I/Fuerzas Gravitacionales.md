# Fuerzas Gravitacionales
Una propiedad de la naturaleza es el campo gravitacional. La gravitación está catalogada como una de las cuatro fuerzas fundamentales de la naturaleza, la estudiaremos en la [[Mecánica Newtoniana]].
Según indicamos en [[Cinemática en 2D]], los primeros estudios experimentales de caída libre establecieron la importante propiedad de este movimiento de que *todos* los cuerpos, independientemente de sus masas o velocidades iniciales, caían con la misma aceleración constante en el vacío, $g  = 9,81 \text{ m/s}^2$ . 
El hecho de que la aceleración $a = F/m$ permanezca constante cuando se varía $m$ eligiendo cuerpos diferentes en el experimento de la caída libre, indica que si tuvieramos que introducir una propiedad de la materia que conseráramos responsable de la atracción gravitatoria, esta propiedad aumentaría proporcionalmente a la masa inerte. 
Para entender que es lo que describe a las interacciones entre por ejemplo una manzana y la tierra o cualquier otros dos cuerpos, a que _propiedad inherente_ a los cuerpos se debe la fuerza. Por ejemplo, la carga electrica causa las fuerzas eléctricas y es una de dichas propiedades inherente. Es decir, queremos expresar que está _"causando"_ la gravedad.

## Masa gravitatoria vs masa inercial
Resulta que la propiedad de la materia que consideramos se debe la fuerza gravitatoria recibe el nombre de **masa gravitatoria**. Por definición, el cociente entre las masas gravitatorias de los cuerpos A y B está medido por el cociente entre las fuerzas que ejerce la Tierra cuando estan situados en un mismo lugar.  Si se miden dos fuerzas mediante estudios de aceleración y resultan ser $F_A$ y $F_B$ el cociente entre las masas gravitatorias es
$$\frac{M_A}{M_B} = \frac{F_A}{F_B}$$
Notemos que esta es la misma manera de definir la masa inercial, vista en [[Dinámica y leyes De Newton]]. Podemos decir entonces que las masas gravitatorias son en general iguales a las masas ineciales. En la practica cotidiana se suelen llamar  a ambas "masa" a secas, pero no hay que confundirlas, son propiedades diferentes, una es la resistencia a alterar el movimiento y otra la propiedad a la cual se debe la atracción gravitatoria.

## Ley de gravitación universal
> **(Ley de Gravitación Universal)** Dos masas en el espacio interaccionan de tal manera que experimenta cada una una fuerza cuya magnitud es proporcional al producto de sus masas e inversamente proporcional a la distancia al cuadrado, medida de centro a centro de cada masa. Su dirección es de atracción mutua sobre una línea de acción que pasa por el centro de masa. $$F = G \frac{m M}{r^2}$$
![[Pasted image 20220414120552.png]]

Notemos que lo que nos está diciendo esta ley es que dadas dos masas $m_1$ y $m_2$ sobre la recta trazada sobre los puntos que representan los centros de masa (llamada "línea de acción") existen dos fuerzas $F_{12}$ y $F_{21}$ que se aplican cada una en un cuerpo diferente, la relación entre estas fuerzas es $F_{12} = - F_{21}$. Sabemos que las fuerzas son vectores, ahora lo siguiente que tenemos que hacer es elegir un sistema de coordenadas, una vez elegido el origen quedan definidos $\vec{r}_{1}$ y $\vec{r}_2$ que son los vectores posiciones de las masas.
![[Pasted image 20220415084910.png | 400]]
Notemos que $\vec{r}_{12} = \vec{r}_2 - \vec{r}_1$ , en este caso nos conviene elegir un sistema de coordenadas polares ya que normalmente ocurre que los cuerpos están orbitando a la tierra o la tierra está orbitando el sol etc. Sabemos que la fuerza es proporcional al producto de fuerzas $F \propto m_1 m_2$ y que la fuerza es inversamente proporsional al cuadrado de la distancia $F \propto \frac{1}{(\vec{r}_{12})^2}$. Ahora definamos el versor $\hat{r}_{12} = \frac{\vec{r}_{12}}{|\vec{r}_{12}|}$ y el versor $\hat{r}_{21} = \frac{\vec{r}_{21}}{|\vec{r}_{21}|}$. Newton encontró que la proporcionalidad entre la fuerza y las masas estaba definida por una constante $G \simeq 6,67 \times 10^{-11} \quad \text{Nm}^2 / \text{kg}^2$ , llamada **constante de gravitación universal** que se puede determinar con el experimento de Cavendish. La fuerza $\vec{F}_{12}$ entonces nos queda
$$\vec{F}_{12} = - G \frac{m_1 m_2}{r_{12}^2}(\hat{r}_{12})$$
Otra manera bastante útil de realizar esto es utilizar un sistema de coordenadas que tenga su origen en alguna de las dos masas y ahí el versor que usaríamos en expresión es $\hat{u}_{\rho}$ . 
Lo cierto es que esta fuerza para dos masas no tan grandes, como la de dos personas, la gravedad no es perceptible.

## Tiro Vertical a gran altura
Supongamos ahora que tenemos un cuerpo de masa $m$ bajo la acción de la fuerza gravitatoria de la Tierra. En primer lugar haremos la suposición que estamos en un marco de referencia no inercial y la Tierra no se está moviendo. Elegimos un sistema de coordenadas con origen en el centro de la tierra. 
![[Pasted image 20220415100752.png]]
Entonces, 
$$\vec{F} = -G \frac{M_T m}{R_T^2} \hat{u}_{\rho}$$
Donde $M_T$  y $R_T$ son la masa y el radio de la tierra, podemos estimar ($R_T = 6371 \text{ km}$) usando el peso de una persona en la Tierra que $M_T \simeq 6 \times 10^{24} \text{ kg}$ . 
Sabiendo que $\vec{F} = m \vec{a}$ representa la fuerza resultante que causa el movimiento y $$ma \hat{u}_{\rho} = -G \frac{M_T m}{R_T^2} \hat{u}_{\rho} \implies a = G \frac{M_T m}{R_T^2} \implies \frac{\mathrm{d}^2 r}{\mathrm{d}t^2} = G \frac{M_T m}{R_T^2}$$  
Fijemosnos que buscamos de alguna manera describir el movimiento del cuerpo, es decir queremos encontrar $r(t)$, fijemosnos que lo que nos quedó al último es una ecuación diferencial es decir tenemos que aplicar
$$\frac{\mathrm{d}^2 r}{\mathrm{d}t^2} = \frac{\mathrm{d} v}{\mathrm{d}t} = \frac{\mathrm{d}v}{\mathrm{d}r} \cdot \frac{\mathrm{d}r}{\mathrm{d}t} = \frac{\mathrm{d}}{\mathrm{d}r} \Big(\frac{1}{2}v^2 \Big)$$
Fijemosnos que podemos reemplazar $-\frac{1}{r^2}$ por $\frac{\mathrm{d}}{\mathrm{d}r} \big( \frac{1}{r} \big)$ y 
$$\frac{\mathrm{d}}{\mathrm{d}r} \Big(\frac{1}{2}v^2 \Big) - \frac{\mathrm{d}}{\mathrm{d}r} \Big(\frac{GM_T}{r} \Big) = 0$$
Es decir,
$$\frac{\mathrm{d}}{\mathrm{d}r} \Big(\frac{1}{2}v^2 - \frac{GM_T}{r} \Big) = 0$$
Interpretemos lo que nos quiere decir esto, tenemos que una derivada nos da 0, entonces como conclusión podemos sacar que estamos derivando por una _constante_, fijemosnos que esta constante tendría que cumplir que para dada cualquier velocidad del cuerpo $v$ esto se mantiene constante, es lo que llamamos una **Constante de Movimiento**, en este caso sí multiplicamos por la masa se llama **Energía Mecánica**. 
$$E = \frac{1}{2}mv^2 - \frac{GmM_T}{r}$$
El primer término es la **Energía Cinética** y el segundo la **Energía Potencial Gravitatoria**. Si despejamos $v$ de la ecuación anterior nos queda una función que es la velocidad respecto a la posición,
$$v(r) = \pm \sqrt{\frac{2E}{m} + \frac{2GM_T}{r}}$$
Como $v = \frac{\mathrm{d}r}{\mathrm{d}t}$ , podemos reescrbir la función en términos del diferencial de la posición y luego pasar toda la raíz dividiendo obtenieno y luego integrando obtenemos una expresión explícita de la función del movimiento. Podemos obtener cierta información sobre el movimiento a partir de la expresión de la energía.
Supongamos que nos preguntan **el radio máximo** para el cual el proyectil puede llegar al ser lanzado veticalmente. Nos dan entonces la posición inicial $r_0$ y la velocidad inicial $v_0$, usando la ecuación anterior de $v(r)$ y sabiendo que la energía es la misma en todo momento reemplazamos:
$$\begin{align}
v(r) & = \pm \sqrt{\frac{2 \Big(\frac{1}{2}mv_0^2 - \frac{GmM_T}{r_0} \Big)}{m} + \frac{2GM_T}{r}} \\
& = \pm \sqrt{\frac{mv_0^2 - \frac{2GmM_T}{r_0}}{m} + \frac{2GM_T}{r}} \\
& = \pm \sqrt{v_0^2 - \frac{2GM_T}{r_0} + \frac{2GM_T}{r}} \\
& = \pm \sqrt{v_0^2  - 2GM_T \Big(\frac{1}{r_0} - \frac{1}{r}} \Big) \\
\end{align}$$
Notemos que para que para que la velocidad dentro de la raíz cuadrada no sea negativa tiene que ocurrir que
$$2GM_T\Big(\frac{1}{r_0} - \frac{1}{r} \Big) > v_0^2$$
es decir, si
$$\frac{1}{r} < \frac{1}{r_0} - \frac{v_0^2}{2GM_T}$$
el radio máximo al cual el proyectil puede llegar al ser lanzado verticalmente es
$$r_{\text{máx}} = \frac{1}{\frac{1}{r_0} - \frac{v_0^2}{2GM_T}}$$

## Peso
El peso es la fuerza gravitacional hecha por la tierra a un cuerpo. A la superficie de la tierra, el peso de masa $m$ es
$$\vec{P} = -G\frac{M_Tm}{R_T^2}\hat{r} = m\vec{g}$$
Nuestra definición de peso es precisa. De acuerdo a esta definición el peso de un cuerpo _no es afectado por su movimiento_. Pero existe otra definición, más comúnmente reconocida en la cual el peso es la magnitud de una fuerza sobre un cuerpo que debe ser ejercida por su entorno para mantener al cuerpo bajo la influencia de la gravedad. El siguiente ejemplo muestra la diferencia entre las dos definiciones

### Ejemplo. Tortuga en un Ascensor 
Una tortuga de masa $M$ se encuentra sobre un ascensor que está acelerando hacia arriba a una aceleración $a$. Encuentre $N$ que es la fuerza ejercida sobre la tortuga por el suelo del ascensor. 
Las fuerzas actuando sobre la tortuga claramente son la normal $\vec{N}$ y el peso $\vec{W} = M\vec{g}$, como todo ocurre sobre un eje $y$ podemos expresar todas las fuerzas en una única ecuación:
$$N - Mg = Ma \quad \rightarrow \quad N = M(g+a)$$
Este caso demuestra nuestra dos definiciones de peso. En el caso del peso definido por la ley de gravitación, es el peso de la tortuga $Mg$, que es independiente del movimiento. Por otro lado, nuestra otra definición nos dice que el peso es la fuerza ejercida por el elevador en la tortuga, entonces si midiéramos la fuerza que se le ejerce a la tortuga sería $N = M(g+a)$. Lo que esta definición nos dice es que el peso de la tortuga incrementa cuando el ascensor acelera hacia arriba (porque $a$ es cada vez más grande) y decrece si el ascensor acelera hacia abajo. Si el ascensor cae en caída libre, entonces $a = -g$ y tenemos que $N = 0$ es decir que la tortuga se eleva del piso y empieza a "flotar" dentro del ascensor. 

Esto es lo que los astronautas utilizan para simular la "gravedad cero" que hay en el espacio, se suben a un avión y hacen que el mismo empiece a caer por su propio peso, generando que el peso de los astronautas "sea nulo". Sin embargo, nuestra otra definición nos dice que el peso de los astronautas es siempre el mismo, nunca cambia, lo que hicimos en realidad fue que el entorno nos modificara nuestra medición del peso.

En general utilizaremos la definición formal de peso, $\vec{P} = M\vec{g}$.

---

