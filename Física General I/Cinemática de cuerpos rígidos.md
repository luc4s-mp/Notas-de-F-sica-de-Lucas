# Cinemática de Cuerpos Rígidos
Hasta ahora hemos estudiado exhaustivamente la interacción de dos cuerpos de masas puntuales. Nos podemos preguntar ¿Qué sucede cuando tenemos más de dos cuerpos? ¿Cómo estudiamos sus interacciones? También, podemos preguntarnos ¿Cómo podemos hacer rotar los tipos de cuerpos que por ahora estudiamos (representados por un punto)? la respuesta a la pregunta anterior es evidentemente que no podemos. Necesitamos ampliar nuestra comprensión del cuerpo.

> **Definición de Cuerpo Rígido**
> Entendemos por cuerpo rígido a un cuerpo cuyos puntos mantienen invariable la distancia entre sí, sin importar las fuerzas que estén aplicadas. Se dice en lenguaje común que estos cuerpos *no son deformables*.

Un cuerpo rígido es entonces, un montón de puntos de masa muy chica y densidad muy chica que se encuentran a la misma distancia y que están unidos a tráves de fuerzas de interacción (que por ahora desconocemos totalmente que las ocasiona), imaginemos que somos físicos del siglo 18 que no sabemos de la existencia de átomos o de fuerzas electromagnéticas, entonces estás fuerzas de interacción entre los puntos de una masa muy chica se relacionan usando la *tercera ley de Newton* (vista en [[Dinámica y leyes De Newton]]) y por lo tanto se cancelan al calcular la sumatoria de las fuerzas del sistema.
Los cuerpos rígidos son un concepto teórico, es decir no pueden existir en el mundo real, todo objeto tiende a deformarse en sierta medida cuando se les aplica una fuerza.

## Centro de Masa
Supongamos ahora que cada pequeño punto que forma el cuerpo tienen una distancia tan chica entre ellos que es indistinguible y los puntos ocupan el espacio de manera continua. La siguiente imagen muestra (representado por un conjunto de celdas) como se organizarían los puntos en este tipo de cuerpo, al cual llamaremos **cuerpo rígido continuo**.

![[Pasted image 20220527105803.png | 250]]
Cada uno de estos puntos tiene un vector posición $\vec{r}_i$ y ocupa un volumen $\delta V_i$  y una masa $\delta m_i$. Sí el volumen es suficientemente pequeño, pero no demasiado pequeño para no despresiarlo, esa masa será proporsional al mismo.  La constante de proporsionalidad es la **densidad** $\rho_i$ de la celda i-ésima, de manera que 
$$\rho_i = \frac{\delta m_i}{\delta V_i} \implies \delta m_i = \rho_i \delta V_i \quad (1)$$
Podemos tomar el límite de la expresión anterior (1) para cuando las partículas son cada vez más chicas y ocupan menos volumen (es decir $\delta V_i \rightarrow 0$) y así obtener la densidad del cuerpo. Notemos que $\delta m_i$ y $\delta V_i$ *no son diferenciales* sino más bien cantidades que pueden ser tan chicas como queramos hasta cierto punto, para escalas de las moléculas y átomos esta relación pierde el sentido y deja de ser correcto la relación establecida anteriormente. A este tipo de valores $\delta V$ que se vuelven pequeños, pero no tan pequeños se suelen llamar "diferenciales físicos". Por lo cual decimos que para problemas fuera del domino molecular, se le asocia $\delta V$ el diferencial matemático $dV = dx \cdot \hat{\imath} + dy \cdot \hat{\jmath} + dz \cdot \hat{k}$ entonces
$$\rho(x,y,z) = \frac{dm}{dV} \implies dm= \rho dV$$
Veamos que la densidad es un cociente diferencial, pero noes derivada porque no exite ninguna función (por ahora) tal que $m$ dependa del volumen $m(V)$. Esta si existe y la podemos usar para obtener la masa total 
$$M = \lim_{\delta V_i \rightarrow 0} \sum_{i=1}^n \delta m_i =  \lim_{\delta V_i \rightarrow 0} \sum_{i=1}^n \rho_i \delta V_i = \int \rho dV$$
Entonces, de acuerdo a la definición de centro de masa
$$\vec{r}_{CM} = \frac{\sum^{N}_{i=1} \vec{r}_i \delta m_i}{M} = \frac{\lim_{\delta V_i \rightarrow 0} \sum^{N}_{i=1} \vec{r}_i \delta m_i}{M} = \frac{\int \rho \vec{r} dV}{M}$$
> **Posición del Centro de Masa de un Cuerpo Rígido** $$\vec{r}_{CM} = \frac{\int \rho \vec{r}dV}{\int \rho dV}$$ Para poder definir el centro de masa necesitamos antes definir un origen de coordenadas para el cual están definidos los vectores posición de los puntos $\vec{r}$. A su vez se puede separar en las componenentes $$x_{CM} = \frac{\int x \rho dV}{M} \quad y_{CM} = \frac{\int y \rho dV}{M} \quad z_{CM} = \frac{\int z \rho dV}{M}$$

Notemos que con este tipo de cuerpos podemos ampliar la cantidad de movimientos que podemos describir. Con [[Cinemática del punto]] y [[Cinemática en 2D]] podemos describir el movimiento que hace una pelota de tenis cuando la tiro en el aire con una velocidad incial. Pero nosotros concideramos a la pelota como un punto, nunca consideramos la *rotación* de la pelota.
Podemos dividir el movimiento de los cuerpos en dos partes:
- La **traslación** del cuerpo generando una trayectoria en el espacio que puede ser explicada usando principios parecidos a los vistos anteriormente
- La **rotación** del cuerpo, en el que cada punto del cuerpo rígido está girando sobre un mismo eje.
Analicemos primero el segundo tipo de movimiento que es el que menos entendemos.

## Rotación y traslación de cuerpos rígidos
### Rotación Pura
En una rotación pura el eje sobre el que está girando el cuerpo está fijo. Cada punto en el cuerpo rígido está describiendo un [[Movimiento Circular]], pero veamos que no todos tienen la misma velocidad en un mismo angulo $\theta$. Sabemos por lo que vimos anteriormente que $v = r\omega$ siendo $r$ la distancia al centro, por lo cual *cuanto más lejos esté del eje un punto del cuerpo rígido, mayor va a ser su velocidad lineal $v$* . Es por esto por lo cual no nos sirve describir el movimiento del cuerpo usando los principios que entendimos de la mecanica traslacional, como la trayectoria, la velocidad lineal, el momento lineal, etc. 

Veamos que para estos casos nos combine expresar el movimiento en *ángulos* ya que si bien la velocidad lineal cambia según en el punto que elijamos la **velocidad angular** $\omega$ no cambia (en el caso de que no exista aceleración angular). Acá también entra en juego los beneficios de usar el [[Momento Angular y Torque]]. 
Vimos anteriormente en [[Momento Angular y Torque]] que podemos expresar al vector velocidad como el producto vectorial $\vec{v} = \vec{\omega} \times \vec{r}$ . Observese que el vector $\vec{r}$ puede ser vector posición de cualquier punto $O'$ del eje de rotación. Siendo $\vec{r}' = \overline{O'O} + \vec{r}$ , tenemos $\omega \times \vec{r}' = \omega \times \overline{O'O} + \omega \times \vec{r} = \vec{v}$ .
![[Pasted image 20220529124442.png]]
Si ahora tenemos en cuenta que el objeto tiene una **aceración angular** $\vec{\gamma}$ nos queda que la aceración traslacional tiene dos componentes: una aceleración tangencial y una normal al movimiento. De manera que
$$\vec{a} =_! \frac{d\vec{\omega}}{dt} \times \vec{r} + \vec{\omega} \times \frac{d\vec{r}}{dt} =_{!!} \vec{\gamma} \times \vec{r} + \vec{\omega} \times (\vec{\omega} \times \vec{r})$$

En (!) lo que hicimos fue aplicar la derivada del producto de funciones y luego en (!!) reemplazamos $d\vec{w}/dt = \vec{\gamma}$ y $d\vec{r}/dt = \vec{v} = \vec{\omega} \times \vec{r}$ . Veamos que el primer termino representa la componente tangencial al movimiento (tiene la mismaa dirección que la velocidad ya que $\vec{\gamma} \parallel \vec{\omega}$) y el segundo es la componenete de la aceleración normal.

### Traslación Pura
En este tipo de movimiento todos los puntos del rígido se mueven a la misma velocidad, tal que $\vec{v}(\vec{r}) = \vec{v_0}$. Es decir, existe un *campo vectorial* de velocidades en los que a cada punto del cuerpo rígido se la asigna una velocidad $\vec{v_0}$.

### Roto-traslación
Si al movimiento de rotación le superponemos ahora un movimiento de traslación caracterizado por una velocidad $\vec{v}_0$ (es decir el cuerpo esta rotando y trasladandose al mismo tiempo, como la pelota de tenis), la velocidad de cada punto del rígido será 
$$\vec v = \vec\omega \times \vec{r} + \vec{v_0}$$
![[Pasted image 20220529173152.png]]
> **Ecuación que describe el movimiento general de un cuerpo rígido** $$\vec{v} = \vec{\omega} \times \vec{r} + \vec{v_0}$$ Siendo $\vec{v_0}$ representante del movimiento traslatorio del rígido y $\vec{\omega} \times \vec{r}$  representa la velocidad generada por el movimiento rotatorio del rígido.

Observese que este estado más general de movimiento de un cuerpo rígido está definido por dos vectores característicos $v_0$ y $\omega$, que si los conocemos (tres funciones de tiempo para $v_0$ y tres para $\omega$) tendremos determinada la velocidad de cada punto en función del tiempo, y por lo tanto, conoceremos la posición del cuerpo rígido en cada instante.

Notemos lo útil que es esta ecuación que nos describe perfectamente el movimiento de "infinitos" puntos. La cual va a seguir funcionando *sin importar el origen de coordenadas o el eje que elijamos* (este último siendo paralelo al eje original). 

Hemos visto que en todo sistema de partículas el **centro de masa** es un punto notable a tener en cuenta. Ya vimos como calcular el centro de masa de un rígido, y como sabemos que podemos elegir cualquier eje de rotación mientras que sea paralelo al original, podemos elegir uno que pase por el centro de masa del cuerpo. La expresión de la velocidad entonces será 
$$\vec{v}(\vec{r}) = \vec{\omega} \times \vec{r} +  \vec{v}_{CM}$$
> **Ayuda para resolver ejercicios:** "La clave para estudiar el movimiento de un cuerpo rígido es superponer su movimiento de traslación del centro de masa con el movimiento de rotación con el eje en su centro de masa"

Cuando hablamos de "superponer" nos referimos a que es preferible diferenciar ambos movimientos, en vez de estudiarlos como uno. Por ejemplo, como haciamos en tiro parabólico, que estudiabamos el movimiento horizontal que era MRU y el vertical que era MRUV. 

#### Velocidad y Aceleración relativa, y Centro Instantáneo
Ahora que sabemos que un cuerpo rígido tiene permitido rotar y trasladarse al mismo tiempo podemos describir mejor lo visto anteriormente usando los conceptos del  [[Movimiento Relativo]]. Supongamos que tenemos un cuerpo que se mueve de manera tal que los puntos A y B se trasladan con los vectores $\vec{r}_{A}$ y $\vec{r}_{B}$, tal que luego los vectores $|\vec{r}_{AB}| = |\vec{r}_{BA}|$ por la propiedad general de un rígido.
![[Pasted image 20220611200555.png| 250]]

Si ahora medimos un cambio infinitamente pequeño en la posición en un cambio infinitamente pequeño en el tiempo, obtenemos los vectores velocidad de A y B.
![[Pasted image 20220611201054.png | 200]]
Fijemosnos que podemos encontrar la velocidad relativa de B en función de A, ya que sabemos su vector posición respecto a A. Sabemos que en una roto-traslación la velocidad del punto A está definida por $\vec{v}_A = \vec{v}_0 + \omega \times \vec{r}_A$ y para la velocidad en el punto B es $\vec{v}_B = \vec{v}_0 + \omega \times \vec{r}_B$ , entonces restando ambas ecuaciones nos queda $\vec{v}_B - \vec{v}_A = \omega \times (\vec{r}_A - \vec{r}_B)$ veamos que $\vec{r}_{BA} = \vec{r}_A - \vec{r}_B$ y nos queda 
$$\vec{v}_B = \vec{v}_A + \vec{\omega} \times \vec{r}_{BA}$$
De esta manera, podemos escribir la velocidad relativa del punto en función con cualquier otro. Es bastante útil entonces usar el centro de masa como punto de referencia para obtener la velocidad relativa del resto de los puntos. 

### Rodadura
Consideremos ahora una rueda que está sobre el suelo (la fricción se despresia) y empieza a rodar. A este tipos de movimientos que describen los puntos situados sobre el perímetro de una rueda que rueda *sin deslizar* sobre una superficie plana los llamamos rodadura.

Usemos la ayuda para resolver problemas vista arriba y veamos ambos movimientos como separados y combinemoslos:
![[Pasted image 20220529200501.png | 500]]
Es muy útil usar el centro de masa como origen de coordenadas del sistema, ya que podemos establecer la relación $v_{CM} = R \omega$ siempre y cuando la rueda no este "*deslizando*" por el suelo, para explicar a que nos referimos con esto es mejor usar un ejemplo: supongamos un automóvil de "arrancones" (es decir, que comienza a acelerar sus ruedas muy rápido en un intervalo muy corto de tiempo) comienza a moverse, los neumáticos traseros están girando con gran rapidez mientras que el vehículo casi no se mueve, así que $R \omega$ es mayor que $v_{CM}$. Si el conductor aplica los frenos con demasiada fuerza y el coche derrapa, los neumáticos casi no girarán y $R \omega$ será menor que $v_{CM}$.
![[Pasted image 20220530105224.png]]

Comprobemos que podemos escribir la velocidad del centro de masa $v_{CM} = R \omega$ matemáticamente, la velocidad del punto de contacto A sería:
$$\vec{v}_{A} = \vec{\omega} \times \vec{r}_{A} + \vec{v}_0$$
Pero sabemos que $\vec{v}_A = 0$, con lo cual 
$$\vec{v}_0 = - \vec{\omega} \times \vec{r}_A$$
Veamos que obtuvimos una ecuación que relaciona el movimiento traslatorio con el movimiento de rotación $v_0 = R \omega$. Pero no era particularmente a lo que queriamos llegar, supongamos ahora que yo elijo un eje paralelo a este que tenga como origen el punto de contacto A en un tiempo dado de manera que lo llamaremos *eje instantaneo* (donde la velocidad de este eje es 0 por lo tanto $\vec{v}_{0, A} = 0$), entonces la velocidad del centro de masa (ubicado en el punto O) queda 
$$\vec{v}_{CM} = \vec{\omega} \times \vec{r}_{CM} = \vec{\omega} \times (-\vec{r}_A) = -\vec{\omega} \times \vec{r}_A = \vec{v}_0$$
Y obtenemos a lo que queríamos llegar, que $v_{CM} = R \omega$.
