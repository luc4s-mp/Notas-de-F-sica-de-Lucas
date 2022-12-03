.# Cinemática en 2D
En este caso ampliaremos nuestros conocimientos de [[Cinemática del punto]] a 2D, en nuestro estudia de la [[Mecánica Newtoniana]]. 
Cuando tenemos un objeto que se mueve en 2 dimensiones, existe un cambio importante. No sucede los mismo cuando cambiamos de 2D a 3D, en escencia ocurre algo parecido, pero cuando pasamos de 1D a 2D si hay un cambio trascendental.
Principalmente porque el movimiento empieza a ser descripto utilizando [[Vectores]].  Tanto la velocidad como la aceleración se comportan como vectores, los cuales en nuestro estudio de la física va a ser definido un vector aquel que posee tres elementos: una magnitud, una dirección y un sentido. 

## ¿Por qué usamos vectores para describir la posición?
Imaginemos la siguiente situación: usted está en un bosque perdido y a partir de un punto, que vamos a llamar origen con $t = 0$, nos movemos en una dirección con un ángulo $\alpha$ de magnitud de 3 km. Luego, a partir del punto en el que nos encontramos, nos volvemos a mover otros 4 km en un ángulo $\beta$. Ahora, observemos los dos movimientos trazados en la Imagen 1 ¿Sería lo mismo hacer el recorrido en azul de 5 km que hacer el de 3 km y luego el de 4km?
![[Pasted image 20220125092335.png| 350x300]]
La respuesta clara es que sí, es lo mismo. Esto sucede gracias a las propiedades de los vectores al sumarlos, para ver más ir a [[Vectores]]. Vemos que es muy util utilizar vectores para describir el cambio de posición.
A su vez, como tenemos dos dimensiones, podemos hablar por separado del movimiento en cada una de ellas. Es decir, podemos separar el movimiento de arriba en dos funciones $x(t)$ y $y(t)$ y hablar del movimiento por separado en cada una de ellas y al fin de cuentas es como si tuvieramos dos movimientos rectilineos. Pero en general podemos hablar de la función posición $\vec{r}(t)$ que es una función vectorial definida de la siguiente manera:
$$\vec{r}(t) = x(t) \hat{\imath} + y(t) \hat{\jmath}$$
A esta misma función, podemos aplicarle el mismo proceso que hicimos en [[Cinemática del punto]] para obtener el vector velocidad y el vector aceleración.
$$\vec{v}(t) = \frac{\mathrm{d} \vec{r}(t)}{\mathrm{d} t} = \frac{\mathrm{d}x(t)}{\mathrm{d}t} \hat{\imath} + \frac{\mathrm{d}y(t)}{\mathrm{d}t} \hat{\jmath} \;\;\;\space\;\;\; \vec{a}(t) = \frac{\mathrm{d} \vec{v}(t)}{\mathrm{d} t} = \frac{\mathrm{d}v_x(t)}{\mathrm{d}t} \hat{\imath} + \frac{\mathrm{d}v_y(t)}{\mathrm{d}t} \hat{\jmath}$$

### Aceleración constante y velocidad  constante en movimiento en 2D
En este caso, tenemos que definir si el objeto se está moviendo en aceleración constante o velocidad constante en $x(t)$ o $y(t)$.  Podemos usar las mismas ecuaciones vistas en [[Ecuaciones Cinemáticas]], pero ahora tenemos que tener en cuenta que estamos tratando con vectores. 
Supongamos que se nos da el vector de velocidad inicial $\vec{v_0}$ (su magnitud) y nos dicen que la partícula mantiene la misma velocidad durante todo el movimiento ¿Cómo se va a ver la función posición en este caso? Primero veamos que la función velocidad se va a ver así:
$$\vec{v}(t) = v_0 \cdot \cos (\theta) \hat{\imath} +  v_0 \cdot \text{sen} (\theta) \hat{\jmath}$$
Esto ocurre porque tenemos que descomponer el vector de velocidad incial en sus componentes horizontales y verticales para poder usarlo. Entonces, ahora para encontrar la función del vector posición debemos integrar:
$$\vec{r}(t) = [v_0 \cdot \cos (\theta)t + x_0] \hat{\imath} +  [v_0 \cdot \text{sen} (\theta)t + y_0] \hat{\jmath}$$

## Movimiento parabólico
Analizaremos un caso particular de movimiento en el plano que es de gran interes. Estudiaremos la cinemática de un cuerpo bajo la acción de la atracción gravitatoria de la Tierra. Todos los cuerpos ubicados en las proximidades de la superficie de la Tierra experimentan la misma aceleración, que denominaremos con la letra $g$. Esta aceleración apunta en la dirección vertical hacia la Tierra. Su valor aproximadamente $9,78 \; m/s^2$ en el ecuador y $9,83 \; m/s^2$ en los polos. En los pocos casos en que sea necesario reemplazar g por su valor numerico en esta sección, usaremos una aproximación más grosera, $g \simeq 10 \; m/s^2$.
Entonces el vector aceleración será:
$$\vec{a}(t) = -g \hat{\jmath}$$
Considerando el instante incial del movimiento como $t = 0 \; s$ y sabemos que el objeto fue lanzado a una velocidad $\vec{v_0}$ a una altura inical $y_0 = h$, entonces los vectores posición y velocidad para el instante $t = 0 \; s$ son,
$$\vec{r}(0) = h \; \hat{\jmath}  \;\;\;\space\;\;\; \vec{v}(0) = v_0 \;\cos(\alpha) \; \hat{\imath} + v_0 \;\text{sen}(\alpha) \;\hat{\jmath}$$
Ahora para obtener la función del vector velocidad integramos
$$\vec{v}(t) = \int \vec{a} \; \mathrm{d}t = - \int g \; \hat{\jmath} \; \mathrm{d}t = -gt \; \hat{\jmath} + \vec{C}$$
Veamos que $\vec{C}$ es el vector de la velocidad inicial:
$$\vec{v}(t) = -gt \; \hat{\jmath} + \vec{C} = -gt \; \hat{\jmath} + v_0 \;\cos(\alpha) \; \hat{\imath} + v_0 \;\text{sen}(\alpha) \;\hat{\jmath}$$
Entonces el vector velocidad del cuerpo es
$$\vec{v}(t) = v_0 \;\cos(\alpha) \; \hat{\imath} + (-gt + v_0 \;\text{sen}(\alpha)) \;\hat{\jmath}$$
Ahora volvemos a integrar para obtener la función del vector posición:
$$\vec{r}(t) = \int \vec{v} \; \mathrm{d}t = [v_0 \;\cos(\alpha)]t \; \hat{\imath} + \Big[-\frac{1}{2}gt^2 + v_0 \;\text{sen}(\alpha)t\Big] \;\hat{\jmath} + \vec{D}$$
El vector posición $\vec{D}$ representa el vector posición en el intante inicial, el cual ya definimos como $\vec{D} = h \; \hat{\jmath}$, entonces:
$$\vec{r}(t) = [v_0 \;\cos(\alpha)t] \; \hat{\imath} + \Big[-\frac{1}{2}gt^2 + v_0 \;\text{sen}(\alpha)t + h\Big] \;\hat{\jmath}$$


#Primer-año #Física 