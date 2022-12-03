# El trabajo de una fuerza
En nuestro estudio de la [[Dinámica y leyes De Newton]], nos hemos tomado con lo que llamamos "constantes de movimiento". En [[Energía]] vimos que existen ciertas constantes que no cambian en ciertos tipos de movimiento y que relacionan a la fuerza, la aceleración y la velocidad en una sola ecuación. Lo cual podrémos notar que es muy útil. 

Vimos que en [[Colisiones]] existen situaciones en las cuales dijimos que _"la energía cinética no se conserva y se pierde en calor o sonido, pero lo que llamamos energía mecánica sí se conserva"_ (con esto nos referimos que al calcular la energía final del sistema debemos considerar que debemos sumar la energía perdida en calor para que se conserve), podemos preguntarnos ¿En qué otras situaciones la energía cinética no se conserva? ¿Por qué las energías potenciales relacionan la fuerza con el desplazamiento? (Observe las formulas) ¿Qué significa realmente la energía potencial? 

![[Pasted image 20220424103050.png | 350]]
(1) Cuerpo cayendo considerando abajo como negativo, (2) Cuerpo cayendo coniderando abajo como positivo, (3) Satélite orbitando la tierra, (4) Cuerpo sometido a la fuerza de un resorte.

Notemos que en todas las formulas, para cambiar la energía cinética $T = \frac{1}{2}mv^2$ es necesario cambiar el módulo del vector velocidad, pero como ya vimos esto no siempre ocurre en todos los movimientos. Por ejemplo, en el [[Movimiento Circular]] Uniforme no existe un cambio en el **módulo** de la velocidad pero sí en la dirección.

Es decir, una fuerza resultante puede tener dos componentes, una tangencial al movimiento (que cambia el **módulo de la velocidad**) y una normal al movimiento (que cambia la **dirección de la velocidad**), en la componente normal de la fuerza $F_n$ estan comprendidas todas las fuerzas que son perpendiculares al movimiento del cuerpo (que no afectan al desplazamiento) y la componente tangencial nos da $\frac{F_t}{m} = \frac{dv}{dt}$ por la segunda ley de Newton expresada con el [[Momento Lineal]]. 

Entonces, supongamos un cuerpo que se está moviendo sobre una curva y su fuerza cambia según la posición en la que se encuentre, dividimos el movimiento en trozos muy chicos que llamaremos $ds$ o "**diferencial de desplazamiento**" que representa un cambio en la posición muy chico en un tiempo muy chico. 
![[Pasted image 20220514174833.png]]
Tal que tenemos
$$\frac{dv}{dt} = \frac{dv}{ds} \frac{ds}{dt} = \frac{dv}{ds}v = \frac{d}{ds} \Big(\frac{1}{2}v^2\Big) \implies d \Big(\frac{1}{2}mv^2 \Big) = F_t \cdot ds$$
La última ecuación nos dice que el cambio intantáneo de la energía cinética es igual a la fuerza tangencial al movimiento por un cambio instantáneo en el desplazamiento. Resulta que sí integramos entre dos puntos $P_0$ y $P$ de ambos lados obtenemos un número escalar muy importante al que denominaremos **trabajo**. No sabemos por ahora que es este número ni que significa.

## Trabajo de una fuerza constante en 1D
Para enterder que es el trabajo y de donde sale, empecemos con un ejemplo simple de un cuerpo al que se le está ejerciendo una fuerza $\vec{F}$ en la posición $x_0$ con una velocidad $v_0$, cuya dirección es la misma que la fuerza.
![[Pasted image 20220514175206.png]]
Como solo trabajamos en una dimensión dejaremos de usar vectores por convensión. Sabemos que la aceleración está dada por $a = \frac{F}{m}$ tal que si la integramos obtenemos la ecuación $v(t)$ y al volver a integrar obtenemos $x(t)$. Entonces, si luego despejamos $t$ en la ecuación de velocidad y la reemplazamos en $x(t)$ y manimulamos para dejar al desplazamiento $x_f - x_i$ de un lado, obtenemos
$$x_f - x_0 = \frac{1}{2a} (v_1^2 - v_0^2)$$
Notemos que el termino de la derecha es muy parecida al cambio de la energía cinética $\Delta T = \frac{1}{2} m (v_1^2 - v_0^2)$ entonces pasando $a$ del otro lado y luego multiplicando de ambos lados obtenemos
$$\frac{1}{2}m(v_1^2 - v_0^2) = ma(x_f - x_0)$$
Y si $F = ma$ y $d = x_f - x_0$ entonces

> **Definición de trabajo para fuerzas constantes aplicadas en la misma dirección que el movimiento** $$\Delta T = Fd \equiv W_{ab}$$ Siendo $W$ llamado "el trabajo de la fuerza $F$"

Entonces, nuestro concepto por ahora del trabajo es que es un número que nos representa cuanto "_la fuerza a desplazado al cuerpo_", por así decirlo. Notemos que preguntarnos cuanto trabajo ha hecho la fuerza gravedad en este caso es ridículo ya que el cuerpo se mueve únicamente horizontalmente por lo que no existe relación entre el desplazamiento y la fuerza y el trabajo deberia ser **nulo**.  ¿Y si la fuerza fuera opuesta al movimiento? esto ocurriría cuando la velocidad inicial es opuesta a la fuerza también tal que el cuerpo está **desacelerando**, en este caso el trabajo debería ser **negativo**.

Pero, ¿Como expresamos estos últimos dos casos en nuestra ecuación del trabajo? ¿Y que ocurre cuando la fuerza es aplicada en un ángulo? Es decir, si nuestro problema fuera llevado a las dos dimensiones. 

### El trabajo como un producto escalar
Supongamos entonces que tenemos una situación parecida a la anterior pero con la fuerza $\vec{F}$ siendo aplicada en un ángulo $\alpha$ y ahora considerando la fuerza normal $\vec{N}$ y la fuerza peso $\vec{P}$ :
![[Pasted image 20220514182804.png]]
Estamos interasados únicamente en el eje-x, que es la dirección del desplazamiento, entonces
$$F\cos(\alpha) = ma \implies a = \frac{F\cos(\alpha)}{m}$$
Fijemosnos que podemos seguir el mismo proceso que en el ejemplo anterior, ya que en este caso la fuerza sigue siendo constante, para obtener
$$\Delta T = F\cos(\alpha)(x_1 - x_0) \implies \Delta T = F\cos(\alpha)d$$
De esta manera, tenemos una definición nueva de que es el **trabajo**, observemos que si consideramos al desplazamiento como un vector $\vec{s}$ entonces esto último que obtenimos es el **producto escalar** de los vectores $\vec{F}$ y $\vec{s}$ . Notemos que con esta definición podemos ampliar nuestro conocimiento del trabajo (habiamos dicho que es una cantidad que nos representa cuanto una fuerza a desplazado al cuerpo) y responder las preguntas anteriores de porque el trabajo de la fuerza peso es 0.

El signo del trabajo esta dado por el $\cos(\alpha)$, 
- Si $\alpha = 0$ tenemos el caso del ejemplo anterior y **podemos usar la formula simple**. 
- Si $\cos \alpha > 0$  el trabajo es positivo.
- Si $\cos \alpha < 0$  el trabajo es negativo.
- Si $\cos \alpha = 0$ el trabajo es 0.

De esta manera, podemos definir el trabajo como:
> **Definición del trabajo para fuerzas constantes** $$\Delta T = \vec{F} \cdot \vec{s} \equiv W$$ El trabajo dado por una fuerza *constante* es definido como el producto de la componente de la fuerza en dirección del desplazamiento y la magnitud del desplazamiento. 

### El trabajo de fuerzas no constantes
Podemos preguntarnos como podemos calcular al trabajo (que hasta ahora, desde un inicio lo obtuvimos del cambio de la energía cinética) de fuerzas que no son constantes. Como por ejemplo, la de un resorte o en general de cualquier movimiento armónico simple. 

Recordemos en el inicio de la lección cuando teniamos un cuerpo que se movía en una curva con una fuerza **no constante**. Observemos que a lo que llegamos es a exactamente la definición de trabajo que dimos para una fuerza constante. Cuando hablamos de la "fuerza tangencial" es lo mismo que $F_t = F\cos(\alpha)$, siendo $\alpha$ el ángulo entre la fuerza y el desplazamiento. Es decir, al dividir el desplazamiento en tramos muy chicos y encontramos las fuerzas que se aplican en esos momentos, podemos calcular todos los trabajos en estos subintervalos, tal que
$$\Delta T = \sum_i \Delta T_i = \sum_i F_i \cos(\theta_i)ds_i$$
Si tomamos el límite de lo anterior, obtenemos la definición de integral, tal que
$$W_{\text{net}} = \Delta T = \int_{C|P_0}^{P_1} F\cos(\theta)ds = \int_{C|P_0}^{P_1} \vec{F} \cdot d\vec{s}$$
La letra C quiere significar "_a lo largo de la curva c_". Este tipo de integrales se llaman integrales de línea.

De la formula anterior, podemos concluir que el trabajo $W$ realizado por la fuerza $\vec{F}$ entre los puntos $P_0$ y $P_1$ sobre la trayectoria $C$ es **igual a la variación de la energía cinética $\Delta T$ en esos dos puntos**. Con lo cual podemos afirmar que el trabajo *no depende del camino*, sino solo de la posición de los extremos $P_0$ y $P$. Pero para que esto pueda ocurrir es necesario que la fuerza $\vec{F}$ no dependa del tiempo sino solo de la posición, es decir que $\vec{F}$ sea un *campo de fuerzas*.

Para entender a que nos referimos como "campo de fuerza" necesitamos presentar un ejemplo. Tomemos una de las [[Fuerzas Gravitacionales]] de un cuerpo que está orbitando la tierra (tenemos el caso 3 de la tabla), $\vec{F}_g = \frac{GmM}{r^2}\hat{u}_\rho$, veamos que la fuerza depende exclusivamente de la **distancia** a la que se encuentre desde el centro de la tierra. Es decir, cuanto más lejos esté, menor será la fuerza. Cuando hablamos de un **campo** en física decimos que es un plano en el cual a cada punto del espacio se le asigna un escalar o un vector. Si vieramos el campo gravitacional de la tierra sería algo como esto:
![[Pasted image 20220515101837.png]]


> **Definición de trabajo** $$W_{\text{net}} = \int_{C|P_0}^{P_1} \vec{F} \cdot d\vec{s} = \Delta T$$

Las unidades de trabajo son 
$$[W] = [E] = [F][l] = \frac{\text{kg} \cdot \text{m}}{\text{s}^2} \cdot \text{m} = \text{N} \cdot \text{m}$$
Estudiaremos más acerca del trabajo y la energía en [[Ley de la Conservación de la Energía]].




