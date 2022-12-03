# Movimiento Relativo
Puede ser aplicado tanto a [[Cinemática del punto]] como a [[Cinemática en 2D]]. Es muy posible que para describir el movimiento de un dado cuerpo, dos personas que lo observan utilicen dos sistemas de coordenadas diferentes. Como si esto fuera poco, las personas pueden estar en distintos lugares, y además moviendose a distintas velocidades. El **movimiento relativo** estudia como diversos marcos de referencia ven el movimiento de un objeto.

## Cambio de Coordenadas 
Supongamos que tenemos dos marcos de referencia denominados A y B. Las coordenadas del punto P del plano serán $(x_{PA}, y_{PA})$ y $(x_{PB}, y_{PB})$, respectivamente. 
El origen del sistema B, visto desde el sistema A, está determinado por el vector posición $\vec{r}_{BA}$ mientras que el origen del sistema A respecto del sistema B está dado por $\vec{r}_{AB}$. Sademos que $\vec{r}_{BA} = -\vec{r}_{AB}$,
$$\vec{r}_{PA} = \vec{r}_{PB} - \vec{r}_{AB} \;\;\;;\;\;\; \vec{r}_{PB} = \vec{r}_{PA} - \vec{r}_{BA}$$
En la imagen 1 se muestran dos posibles sistemas de coordenadas y sus vectores representando un punto.
![[Pasted image 20220130084005.png | 350x350]]

La posición del punto podría cambiar con el tiempo si está en movimiento o también podrían moverse el sistema de referencia, es decir dicha figura se podría pensarse como una fotografía en un instante en particular. La película completa sería la sucesion de fotografías para distintos valores del tiempo, por lo cual podríamos armar funciones vectoriales dependientes del tiempo que cumplan
$$\vec{r}_{PA} (t) = \vec{r}_{PB} (t) - \vec{r}_{AB} (t) \;\;\;;\;\;\; \vec{r}_{PB} (t) = \vec{r}_{PA} (t) - \vec{r}_{BA} (t)$$
Estas ecuaciones, que relacionan coordenadas de un punto respecto a dos sistemas de coordenadas se denominan *transformaciones de coordenadas*.

Supongamos primero que los sistemas A y B no se mueven uno respecto del otro. Entonces las relaciones son:
$$\vec{r}_{PA} (t) = \vec{r}_{PB} (t) - \vec{r}_{AB} \;\;\;;\;\;\; \vec{r}_{PB} (t) = \vec{r}_{PA} (t) - \vec{r}_{BA}$$
La velocidad del cuerpo vistas desde cada uno de los sistemas se obtiene derivando el vector posición con respecto del tiempo:
$$\vec{v}_{PB} = \frac{\mathrm{d}\vec{r}_{PB}(t)}{\mathrm{d}t} = \frac{\mathrm{d}}{\mathrm{d}t} (\vec{r}_{PA} (t) - \vec{r}_{BA}) = \frac{\mathrm{d}\vec{r}_{PA} (t)}{\mathrm{d}t} = \vec{v}_{PA}$$
Entonces, podemos concluir que en este caso para ambos sistemas de referencia, el objeto va a la misma velocidad. 

Supongamos ahora que los sistemas están en movimiento uno respecto del otro. 
$$\vec{v}_{PB} = \frac{\mathrm{d}\vec{r}_{PB}(t)}{\mathrm{d}t} = \frac{\mathrm{d}}{\mathrm{d}t} (\vec{r}_{PA} (t) - \vec{r}_{BA} (t)) \;\;\;\text{ y }\;\;\; \vec{v}_{PA} = \frac{\mathrm{d}\vec{r}_{PA}(t)}{\mathrm{d}t} = \frac{\mathrm{d}}{\mathrm{d}t} (\vec{r}_{PB} (t) - \vec{r}_{AB} (t))$$
es decir
$$\vec{v}_{PA} (t) = \vec{v}_{PB} (t) - \vec{v}_{AB} \;\;\;;\;\;\; \vec{v}_{PB} (t) = \vec{v}_{PA} (t) - \vec{v}_{BA}$$

Las transformaciones de coordenadas que asumen que la velocidad relativa entre ambos sistemas es constante, por lo tanto $\vec{r}_{BA} (t) = \vec{v}_{BA} t + \vec{r}_{AB} (0)$ con lo cual la relación entre las coordenadas del cuerpo descriptas por los dos sistemas puede obtenerse sustituyendo esta expresión en la ecuación (2)
$$\vec{r}_{PA} = \vec{r}_{PB} - \vec{v}_{BA} t - \vec{r}_{AB} (0)$$
se denominan *transformaciones de Galileo* y juegan un rol importante para el estudio de la [[Dinámica]].

#Primer-año #Física 

