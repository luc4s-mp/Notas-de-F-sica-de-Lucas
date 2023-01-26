# Momento Angular

## Introducción al producto vectorial
Anteriormente, en **Introducción a la física** definimos el producto escalar o producto punto de vectores, en el cual al multiplicar dos vectores $\vec{A}$ y $\vec{B}$ obtenemos que el resultado es un escalar cuya magnitud es $|A||B|\cos \theta$  o bien $\vec{A} \cdot \vec{B} = A_xB_x + A_yB_y + A_z B_z$. Este tipo de producto lo que quiere significar geométricamente es cuanto del vector $\vec{B}$ es _paralelo_ con $\vec{A}$ multiplicado por el módulo de $A$., lo cual por conclusión nos dice cuanto de dos vectores hay en la misma dirección. Ahora definiremos el _producto vectorial_, que nos va a dar como resultado **otro vector**  y se representa con una cruz y no con un punto que nos dice que 
- El módulo está dado por el producto de los módulos y el seno del ángulo comprendido entre ellos (lo cual intuitivamente significa cuan _perpendicular_ un vector está con el otro). 
- La dirección del vector resultante $\vec{C} = \vec{A} \times \vec{B}$ es perpendicular al plano formado por los vectores $\vec{A}$ y $\vec{B}$ .
- El sentido está dado por la **regla de la mano derecha**. Es decir, el sentido es hacia donde apunta el pulgar de la mano derecha al hacer girar el vector $\vec{A}$ sobre $\vec{B}$ . Notemos que $\vec{A} \times \vec{B} = - \vec{B} \times \vec{A}$ , es decir el producto vectorial es anticonmutativo.

### Momento de un vector
Se define al **momento del vector** $\vec{A}$ respecto del punto $O$, denominado centro de momentos, como el producto vectorial
$$\vec{M}_O = \vec{r}_{OA} \times \vec{A}$$
Siendo el vector $\vec{r}_{OA}$ la posición respecto del origen. Usando la definición de producto vectorial 
$$|\vec{M}_{O}| = |\vec{A}||\vec{r}_{OA}|\text{sen } \theta = d|\vec{A}|$$
Con $d$ siendo la distancia al origen con respecto a la **recta de acción** del vector. 
![[Pasted image 20220509154020.png | 250]]
Obervemos que esta operación nos ayuda a encontrar la distancia entre el vector $\vec{A}$ y un punto fijo $O$ y nos da un vector perpendicular a ambos. Notemos que cuanto más lejos esté del origen mayor va a ser el momento del vector.
También podemos hablar del **momento de un par de vectores** 

## Vector velocidad angular y momento angular
Notemos que cuando vimos el [[Momento Lineal]] o también lo llamamos cantidad de movimiento, como lo que mide cuanto el objeto se está moviendo y su capacidad para seguir en ese movimiento. Este tenía el mismo sentido que la velocidad, lo cual nos facilitaba su entendimiento. 
Sin embargo en un [[Movimiento Circular]] vimos que una mejor manera de describirlo es usando el **cambio del ángulo** más que el cambio de la posición. Esto ocurre, porque por ejemplo si observemos que para dos partículas que recorren 2 circunferencias (1 con un radio $R$ más grande que la otra) al mismo tiempo $t$, notemos que las dos partículas no pueden tener la misma **velocidad lineal** ya que una recorrío una mayor trayectoria. Por lo cual es mejor decir que ambas partículas recorrieron el **mismo ángulo** al mismo tiempo y poner a la trayectoria en un segundo plano.
Dijimos que su velocidad angular $\omega$ es positiva cuando estamos yendo en sentido antihorario y es negativa cuando estamos yendo en sentido horario.  _¿Por qué ocurre esto?_ _¿Nos sirve el momento lineal para este tipo de movimiento?_

Vamos a definir al vector velocidad angular $\vec{\omega}$ como un producto vectorial de magnitud $|\vec{\omega}| = \omega = |\vec{v}|/|\vec{r}|$ , cuya dirección es perpendicular al plano del movimiento y cuyo sentido está dado por la regla de la mano derecha.  De manera que
$$\vec{v} = \vec{\omega} \times \vec{r}$$
Veamos que esta definición es muy útil ya que notemos que si la velocidad angular es positiva entonces el cuerpo va a tener una velocidad tal que gire en sentido antihorario y viceversa cuando es negativa.

### Momento angular
Supongamos que tenemos dos cuerpos que se están atrayendo mutuamente, es decir sobre el cuerpo 1 tenemos una fuerza $\vec{F}_1 = m\vec{a}_1$ y sobre el cuerpo 2 una fuerza $\vec{F}_2 = m\vec{a}_2$  entonces por la tercera ley de Newton (vista en [[Dinámica y leyes De Newton]]) sabemos que $F_1 = -F_2$ y por la segunda ley entonces $m_1 \vec{a}_1 + m_2 \vec{a}_2 = 0$. Tomemos un punto fijo $O$ como el origen, y encontremos el momento de ambos vectores $\vec{M}_1 = \vec{r}_{1O} \times \vec{F}_1$  y $\vec{M}_2 = \vec{r}_{2O} \times \vec{F}_2$ , notemos que para que $\vec{F}_1$ y $\vec{F}_2$ estén en una misma recta, los momentos tienen que ser opuestos y de igual magnitud. Sabemos que lo segundo ocurre por las condiciones iniciales y por las propiedades del producto vectorial sabemos que son opuestos. Entonces, para que **ambas fuerzas estén una misma recta** se tiene que cumplir que
$$\vec{r}_{1O} \times \vec{F}_1 + \vec{r}_{2O} \times \vec{F}_2 = 0$$
![[Pasted image 20220524094306.png | 500]]
Obervemos que al igual que del [[Momento Lineal]] deducimos que cuando tenemos dos fuerzas internas en un sistema de dos cuerpos (que se cancelan) están generan que el *"momento lineal se conserve"* ya que $\sum F_i = dP/dt = 0$, de la misma manera podemos ver que en este caso los *momentos de las fuerzas internas se cancelan* por lo cual podríamos llegar a la conclusión de que "algo" nuevo se está conservando.  
Llamaremos a esta nueva cantidad que se conserva **momento angular** $\vec{L}$  que se define como 

>[!DEFINICIÓN]
>**Ecuación del momento angular** $$\vec{L} = \vec{r} \times \vec{p} = \vec{r} \times m\vec{v}$$![[Pasted image 20220509171004.png | 300]]

Esta definición la obtenemos sabiendo que al derivar con respecto al tiempo a los momentos angulares de cada cuerpo, obtenemos los momentos de los vectores fuerzas interiores entre los cuerpos del sistema. Por ejemplo tomemos los momentos angulares de la situación de dos cuerpos que hablamos anteriormente:
$$\frac{d}{dt}(\vec{r}_{1O} \times m_1 \vec{v}_1 + \vec{r}_{2O} \times m_2 \vec{v}_2) =_! \vec{r}_{1O} \times \vec{F}_1 + \vec{r}_{2O} \times \vec{F}_2 + \vec{v}_1 \times m_1 \vec{v}_1 + \vec{v}_1 \times m_1 \vec{v}_1$$
En (!) lo que hicimos fue aplicar la formula de derivada del producto y luego tener en cuenta que $dr/dt = v$. Veamos que $\vec{v} \times m \vec{v} = 0$ ya que estamos multiplicando dos vectores paralelos, por lo tanto obtenemos lo que queríamos. 

>**Ley de la conservación del momento angular** $$\frac{d\vec{L}}{dt} = \frac{d}{dt}\Big(\sum_{i=1}^n \vec{r}_{iO} \times \vec{P}_i \Big) = \sum_{i=1}^n \vec{r}_{iO} \times \vec{F}_i = 0 \rightarrow \vec{L} = cte$$
>Esta ley está definida para $n$ cuerpos en un sistema. Para poder aplicar esta ley es necesario definir un punto fijo de origen $O$ al que llamamos *centro de momentos*.
 
Ahora, en un movimiento circular el radio siempre se mantiene constante y $\vec{r}$ y $\vec{p}$ son siempre perpendiculares entre sí tiene la consecuencia de que $L$ es $mvr$ tal que $\vec{L} = mvr \;\hat{k}$ .   Lo cual tiene el mismo sentido que la velocidad angular.

## Torque
En [[Momento Lineal]] dimos una nueva definición de la segunda ley de Newton como $\vec{F} = d\vec{p}/dt$ , es decir un cambio instantaneo en el momento lineal en un intervalo muy chico de tiempo implica que exite una fuerza que está haciendo que cambie ese movimiento. Notemos que lo que obtuvimos de la **ley de la conservación del momento angular** es que al derivar el momento angular obtenemos un momento de vector fuerza resultante:
$$\frac{d\vec{L}}{dt} = \vec{r} \times \vec{F} \equiv \vec{\tau}$$
Siendo $\vec{\tau}$   lo que llamamos **torque**. De esta manera, la [[Mecánica Newtoniana]] la podemos dividir en dos partes la **mecánica traslacional** que estudia el movimiento de objetos que van en línea recta y la **mecánica rotacional** que estudia los objetos en lo que la trayectoria es una circunferencia. En sí podemos comparar ambas teniendo en cuenta que sus principios funcionan de manera parecida. 

El **torque** lo poderiamos de definir como *la capacidad de rotar de un objeto sobre un punto fijo* y se comporta de manera parecida a la fuerza que hace que cambie el movimiento lineal o traslacional del sistema. Por ejemplo, en [[Colisiones]] vimos que ocurría cuando dos cuerpos sufren de un "choque inelástico" que a pesar que se pierda energía cinética el momento lineal se conserva ya que no existen fuerzas externas. Supongamos ahora un disco B que está rotando con un momento angular y sobre este choca otro A que no tiene momento angular (es decir está quieto) entonces ocurre (en este caso espacial) que ambos siguen rotando pero a una velocidad más chica, (el disco A gana momento angular y B lo pierde) ¡Pero el momento angular del sistema no a cambiado! es decir que este también **se conserva** cuando ocurre que **el torque del sistema es igual a 0**, al igual que cuando el momento lineal se conservaba si las fuerzas externas del sistema son iguales a 0. 
**(Para entender de manera completa este ejemplo es necesario hablar de cuerpos rígidos, [[Cinemática de cuerpos rígidos]],  y no cuerpos representados por un punto matemático)**

Ahora, al igual que cuando existian fuerzas exteriores en un sistema el momento lineal ya no se conserva, *lo mismo ocurre con el momento angular*. Cuando existen **torques** exteriores al sistema el momento angular  **no se conserva**.  Notemos que no todas las fuerzas exteriores van a ser torques exteriores, si las fuerzas son paralelas al radio entonces el torque vale 0 y no influyen a hacer que el momento angular no se conserve.


