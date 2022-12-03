# Energía y constantes de movimiento
Hasta ahora en Introducción a la física (más concretamente en [[Cinemática del punto]]) vimos como se relacionan la **aceleración**, la **la velocidad** y la **posición**, y a su vez vimos la relación que existe en las **fuerzas** y la **aceleración** de un cuerpo ([[Dinámica y leyes De Newton]]), habiamos concluido que sí existe una fuerza neta no nula aplicada en un cuerpo, debemos tener una aceleración.
Pero observemos que no hay forma de conectar los otros conceptos por ahora, en esta lección aprenderemos como conectar las **fuerzas** aplicadas con la **velocidad** de un cuerpo. Relacionando estos dos conceptos, podemos llegar de una manera más rapida a la función posición. 
Supongamos que tenemos un cuerpo bajo acción de la gravedad cuyas ecuaciones de movimiento en cada componente son 
$$\begin{align}
v_x = v_{0x} \quad & \Rightarrow x(t) = v_{0x} t + x_0 \\
v_y = v_{0y} \quad & \Rightarrow y(t) = v_{0y} t + y_0 \\
v_z = -gt+v_{0z} \quad & \Rightarrow z(t) = -\frac{g}{2}t^2 +v_{0z} t + z_0 \\
\end{align}$$
Sabemos que existe la ecuación $v^2 = v^2_0 - 2g(z-z_0)$ que se obtiene de sacando el módulo del vector veolcidad, y si la reacomodamos como $v^2 + 2gz = v_0^2 + 2gz_0$ fijemosnos que obtenemos una ecuación que nos está diciendo de alguna manera que apesar que **la velocidad cambie, hay una cantidad que se mantiene constante, (que es $v^2 + 2gz$)**, luego si esto lo multiplicamos por $m/2$ (lo cual no afecta a nuestra ecuación ya que establecimos a la masa como una *propiedad de la materia* que no cambia) entonces nos queda 
$$E = \frac{1}{2}mv^2 + mgz = \frac{1}{2}mv_0^2 + mgz_0$$
Donde **E** es una constante que siempre se mantiene igual no importando la velocidad del objeto, este tipo de ecuaciones se llaman **constantes de movimiento** y a esta constante en particular la llamamos **Energía Mecánica del Sistema**. Otra forma de obtener esta ecuación es resolviendola a partir de la ecuación diferencial
$$-g = \frac{d^2z}{dt^2} = \frac{dv_z}{dt} = \frac{dv_z}{dz} \frac{dz}{dt} = \frac{dv_z}{dz}v_z = \frac{d}{dz}\Big(\frac{v_z^2}{2} \Big)$$
Lo que hicimos en el último paso fue aplicar nuestro conocimiento de derivadas, usamos la **regla de la cadena** para decir que la derivada con respecto al cambio en z de $v_z^2/2$ es $v_z$ por la derivada de $dv_z/dz$ . Esta es una técnica que usaremos mucho en el primer curso de *física general*.
Seguimos manipulando la ecuación nos quedó
$$-g = \frac{d}{dz}\Big(\frac{v_z^2}{2} \Big) \implies \frac{d}{dz} (-gz) = \frac{d}{dz}\Big(\frac{v_z^2}{2} \Big) \implies \frac{d}{dz} \Big( \frac{1}{2}v_x + gz \Big) = 0$$
Por último, multiplicamos por la masa $m$ y nos queda
$$\frac{d}{dz} \Big( \frac{1}{2}mv_z + mgz \Big) = 0$$
Sabemos que si la derivada de una función es 0, entonces **debe ser una constante**, es por esto de donde viene el nombre constante de movimiento. Si la derivada de el cambio de la posición nos da 0, entonces es una constante que se mantiene igual en todo el movimiento.

Este proceso lo podemos replicar para otros cuerpos con otras fuerzas siendo aplicadas, entonces obtendríamos una ecuación de la energía diferente pero no cambiaría mucho.
![[Pasted image 20220424103050.png | 400]]
Al primer término de esta fórmula siempre lo llamamos **energía cinética** $T$ y al segundo **energía potencial** $V$ y a la suma total de ambas la llamamos **energía mecánica** $E$, ya veremos porque en [[Trabajo]].



