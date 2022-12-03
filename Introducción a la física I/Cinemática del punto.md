# Cinemática
Para describir el movimiento de una partícula, exploraremos primero que sucede en el caso más simple de todos, el movimiento en línea recta o también llamado **movimiento en una dimensión**. 

## Movimiento en 1D
Una forma de representar el movimiento es a través de una recta, vamos posicionando los distintos momentos en el tiempo $t$ en el que se va encontrando la partícula a medida que este avanza. También podemos reprentar el movimiento en un gráfico posición-tiempo, como si fuera una función a la que normalmente llamamos *función posición* $x(t)$. Supongamos que queremos saber cuanto la partícula se movío en total, entonces agarramos la posición inicial y la final y calculamos lo que denominamos como **desplazamiento**.
$$\Delta x = x_2 - x_1$$

## Rapidez media e instantánea
Si al desplazamiento lo dividimos por el tiempo en el cual se realizó el movimiento obtenemos la **rapidez media** que nos dice a que "velocidad" (en física esta palabra la usamos en otro contexto) se movió la partícula durante todo su movimiento aproximadamente.  Para poder obtenerla necesitamos saber dos puntos $(t_1, x_1)$ y $(t_2, x_2)$:
$$v_{med} = \frac{\Delta x}{\Delta t} \;\;\; \Delta t = t_2 - t_1$$
Sin embargo, ustedes podrán preguntarse ¿Qué sucede si queremos averigar lo que ocurre entre dos puntos intermedios a estos? Podemos usar la misma formula de la rapidez media para cualquier dos momentos en los que sepamos donde se encuentra el objeto ¿Y que ocurre sí queremos averiguar cual es la rapidez en un momento $t$? A este lo llamamos **rapidez instantánea**, para encontrarla debemos saber conceptos del ánalisis matemático, principalmente el concepto de [[Límite finito de Funciones]] y la [[Derivada]].  La rapidez instantanea se define matematicamente como la tasa de cambio intantáneo de la posición (o la derivada):
$$v(t) = \lim_{\Delta t \rightarrow 0} \frac{\Delta x}{\Delta t} = \frac{\mathrm{d}x(t)}{\mathrm{d}t}$$
Podemos armar una función $v(t)$ en la que obtenemos una rapidez instantánea según el tiempo que insertamos en la función. Para representar esta función podemos realizar un gráfico de rapidez-tiempo.

## Aceleración media e instantánea
Sabiendo esto podemos preguntarnos, ¿Qué ocurre cuando tenemos dos rapideces $v_1$ y $v_2$ en dos momentos de tiempo $t_1$ y $t_2$, y hay un cambio en la rapidez (ya sea que aumentó o dismuyó) entre esos dos intantes? Podemos calcular la **aceleración media** para encontrar cuanto fue ese cambio:
$$a_{med} = \frac{\Delta v}{\Delta t} \;\;\; \Delta v = v_2 - v_1$$
Ahora, podemos hacernos la misma pregunta que nos hicimos anteriormente de ¿Qué pasa si queremos calcular la aceleración en un momento de tiempo determinado? Es lo mismo que preguntar ¿Cuál es la tasa de cambio instantáneo de la velocidad en un momento de tiempo $t$? Para resolver esta pregunta debemos utilizar conceptos del análisis matemático otra vez, encontrando el límite en la aceleración media de cuando el instante de tiempo entre dos rapideces $\Delta t$ se hace infinitamente más chico obtenemos la **aceleración instantánea**:
$$a(t) = \lim_{\Delta t \rightarrow 0} \frac{\Delta x}{\Delta t} = \frac{\mathrm{d}v(t)}{\mathrm{d}t} = \frac{\mathrm{d}^2 x(t)}{\mathrm{d} t^2}$$
Al igual que con la rapidez podemos armar una función con todos los valores obtenenidos al derivar la función velocidad. Para representar esta función podemos realizar un gráfico aceleración-tiempo.
A partir de todo esto podemos ver que la derivada de una función es la otra, por lo tanto todas las funciones van a estar relacionadas de alguna manera, y podemos preguntarnos ¿Podemos deducir como se comporta una función a partir de otra o encontrar esa relación entre las funciones en el caso de que la aceleración es constante o la rapidez es constante? Esta pregunta será respondida en [[Ecuaciones Cinemáticas]]. También nos podemos preguntar que ocurre entonces cuando el movimiento ocurre en más de una dimensión, esto lo veremos en [[Movimiento en 2D]].

#Primer-año #Física 