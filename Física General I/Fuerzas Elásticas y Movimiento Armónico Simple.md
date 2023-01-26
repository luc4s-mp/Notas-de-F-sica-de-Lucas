# Fuerzas Elásticas
En nuestro estudio de la [[Mecánica Newtoniana]], muchos tipos de movimiento se repiten una y otra vez: la vibración de un cristal de cuarzo en un reloj de pulso, la péndola oscilante de un reloj con pedestal, las vibraciones sonoras producidas por un clarinete o un tubo de órgano y el movimiento periódico de los pistones de un motor de combustión. A esta clase de movimiento le llamamos movimiento periódico u oscilación, y será el tema del presente capítulo. Su comprensión será indispensable para nuestro estudio posterior de las ondas, el sonido, la corriente alterna y la luz.

## Movimiento Oscilatorio
El caso más simple de movimiento oscilatorio es cuando tenemos un cuerpo de masa $m$ que está unido a un resorte de masa despreciable que tiene un largo $l_0$ que es la posición relajada o inicial del resorte. Gracias a la [[Ley de Hooke]] sabemos que el resorte si se estira o se comprime genera una fuerza de restitución sobre el cuerpo.
 ![[Pasted image 20220417094757.png | 300]]
 ![[Pasted image 20220417094832.png | 300]]
 Lo más sencillo es elegir nuestro sistema de coordenadas **en la posición de equilibrio**. Siempre que el resorte es estirado o comprimido tiende a volver a su posición inicial, si desplazamos el cuerpo hacia la derecha hasta $x = A$ y lo soltamos, la fuerza total y la aceleración son a la izquierda. La velocidad va aumentando hasta llegar a la posición de equilibrio. Luego, el cuerpo se sigue moviendo hacia la izquierda pero su velocidad cada vez es menor ya que ahora tenemos otra fuerza (que resurta de comprimir el resorte) que apunta a la derecha, evidentemente la velocidad se vuelve 0 y pasa luego a aumentar de nuevo en la dirección de la derecha. De esta manera el movimiento se repite indefinidamente a no ser que una fuerza externa actue.
 
 Veamos las siguientes definiciones:
>[!AMPLITUD]
>**Amplitud**: denotada normalmente como $A$ es la magnitud máxima del desplazamiento con respecto del equilibrio, es decir, el valor máximo de $|x|$ y siempre es positiva. 

> [!PERÍODO]
> **Período**: denotada normalmente como $T$, es el tiempo que tarda un ciclo.

> [!FRECUENCIA]
> **Frecuencia**: $f$, es el número de ciclos en la unidad de tiempo. En el SI se miden usando Hertz o $s^{-1}$ . 

La relación que existe entre la frecuencia y el periódo es: $f = \frac{1}{T}$.
 
> **Frecuencia angular**: $\omega$, es $2 \pi$ veces la frecuencia, $\omega = 2 \pi f$ . 

 Ya habiamos definido anteriormente a la frecuencia angular como **velocidad angular** en [[Movimiento Circular]], escencialemente son lo mismo y tienen las mismas unidades.
 Notemos que solo exite movimiento horizontal en el cuerpo, entonces $$F_y = 0 \quad , \quad F_z = 0 \quad y \quad F_x = -kx$$
De manera generica, si el cuerpo se encuentra en posición $x_i$ la fuerza es 
$$\vec{F} = -k(x_i)\hat{\imath}$$
El signo menos indica que la aceleración siempre va a tener el sentido opuesto al desplazamiento. 
Usemos la segunda ley de newton y la definición de aceleración como $a_x = \frac{\mathrm{d}^2 x}{\mathrm{d}t^2}$ para definir la ecuación de movimiento del sistema:
$$m\frac{\mathrm{d}^2 x}{\mathrm{d}t^2} = -kx \implies \frac{\mathrm{d}^2 x}{\mathrm{d}t^2} = - \frac{k}{m}x \implies \frac{\mathrm{d}^2 x}{\mathrm{d}t^2} + \frac{k}{m}x = 0$$
La ecuación obtenida anteriormente, es una ecuación diferencial. Entonces, debemos encontrar una ecuación en la que la derivada segunda sea igual a $-k/m$ por la función misma. 
Mediante un experimento de poner a rotar una pelota en movimiento circular uniforme si proyectamos la sombra de la pelota sobre una pared veremos que el movimiento de la sombre es un movimiento armónico simple. Lo que nos hace concluir que *el movimiento armónico simple es la proyección del movimiento circular uniforme sobre un diámetro*. 
![[Pasted image 20220418231212.png]]

Notemos que si realizamos el experimento reflejando la sombra sobre el eje-x, la sombra de la pelota se va a mover a medida que la componente en x del vector posición cambie, por lo tanto siendo $A$ la longitud del vector tenemos que la componente es $x = A \cos \theta$  (esta es una posible solución a nuestra ecuación, vamos a ver porque). 
Luego, sabiendo que la aceleración del [[Movimiento Circular]] uniforme siempre apunta hacia el centro y se mantiene constante, con el MAS (movimiento armónico simple) ocurre algo parecido. Notemos que la formula para la aceleración va a nacer de la proyección del movimiento circular en el eje-x, es decir la comp. del eje x de del vector aceleración (en MCU, sabiendo que $a = R\omega^2$) es $a_x = -\omega^2A \cos \theta$ .
Entonces veamos que la última formula obtenida cumple todas las condiciones necesarias para la solución de la ecuación diferencial que estabamos buscando, suponiendo que $\omega = \sqrt{\frac{k}{m}}$ . Esta solución es correcta ya que
$$ \begin{align}
0 = \frac{\mathrm{d}^2 x}{\mathrm{d}t^2} + \frac{k}{m}x = & -\omega^2A \cos \theta + \frac{k}{m} A \cos \theta \\
& = A \Bigg[\Big(-\omega^2 + \frac{k}{m} \Big) \text{cos } \theta \Bigg] \\
& = A \Bigg[\Big(-\Big( \sqrt{\frac{k}{m}} \Big)^2 + \frac{k}{m} \Big) \text{cos } \theta \Bigg]
\end{align}$$
Ahora, como el movimiento circular es uniforme, entonces $\theta(t) = \omega t$.

Pero esta es solo una posible solución, podemos preguntarnos _¿Qué solución obtenemos cuando en vez de reflejar el movimiento circular sobre el eje-x, lo hacemos sobre el eje-y?_
La solución que obtenemos es muy parecida $y = B \text{sen } (\omega t)$ que también cumple todas las propiedades necesarias, veamos que si sumamos ambas soluciones (es decir formamos una combinación lineal de ambas) esto también es una solución: $$x(t) = A \text{sen } (\omega t) + B \cos (\omega t)$$Anteriormente, cuando teniamos las soluciones por separado podiamos ver claramente que $A$ y $B$ eran las amplitudes del MAS, sin embargo en esta ultima solución ya no cumplen eso. Para tener una solución completa necesitamos definir $A$ y $B$, y para esto necesitamos de información adicional dada en los problemas. 
Supongamos ahora por un momento que en el movimiento circular que estamos proyectando tiene un vector posición inicial $\vec{r}_0$ con un ángulo de $\phi_0$  y el radio es $R = x_m$. Las componentes de este vector van a ser $\vec{r}_0 = x_m \cos (\phi_0) \hat{\imath} + x_m \text{sen } (\phi_0) \hat{\jmath}$  ahora elegimos convenientemente $A = x_m \text{cos } \phi_0$ y $B = x_m \text{sen } \phi_0$ (podemos cambiar el orden de esto, tendremos una solución que no diferirá mucho):
$$x(t) = x_m \cos (\phi_0)\text{sen} (\omega t) + x_m \text{sen} (\phi_0) \cos(\omega t)$$
Podemos aplicar la propiedad trigonométrica de la suma de ángulos de la función seno:
$$x(t) = x_m \text{sen}(\omega t + \phi_0)$$
La constante $\phi_0$ en la ecuación se llama **desface** o **ángulo de fase**, que nos indica en que punto del ciclo se encontraba el cuerpo cuando $t = 0$. Resulta evidente que
$$x_m = \sqrt{A^2 + B^2} \quad \text{y} \quad \tan (\phi_0) = \frac{B}{A}$$
Obtenegamos ahora la velocidad $v_x$ y $a_x$ en función del tiempo para un oscilador armónico derivando:
$$\begin{align}
v_x & = \frac{dx}{dt} =  \omega x_m \cos (\omega t + \phi_0) \\
a_x & = \frac{dv_x}{dt} = - \omega^2 x_m  \text{sen} (\omega t + \phi_0)
\end{align}$$
Sabemos que $x(0) = x_0 = x_m \text{sen}(\phi_0)$ y $v_x(0) = v_0 = \omega x_m \cos(\phi_0)$ que constituyen un sistema de ecuaciones con dos incógnitas, resolvemos obteniendo
$$x_m = \sqrt{x_0^2 + \Big(\frac{v_0}{\omega}\Big)^2} \quad \text{y} \quad \tan (\phi_0) = \frac{\omega x_0}{v_0}$$
Analizemos por último la **frecuencia angular** (en MAS) o velocidad angular (en MCU) $\omega$ sabiendo que $\omega t' + \phi_0  = \alpha$  y que como la función seno es periódica, existe un tiempo $T$ en el que tarda en dar una vuelta (el **periódo**) o $2 \pi$ en el que $\omega(t' + T) + \phi_0 = \alpha + 2 \pi$, entonces $\omega t' + \phi_0 + \omega T = \alpha + \omega T = \alpha + 2 \pi \implies \omega T = 2 \pi \implies T = \frac{2 \pi}{\omega}$ . Y sabiendo que la frecuencia angular está determinada por $k$ y $m$ :
$$T = \frac{2 \pi}{\omega} = 2 \pi \sqrt{\frac{m}{k}}$$



 