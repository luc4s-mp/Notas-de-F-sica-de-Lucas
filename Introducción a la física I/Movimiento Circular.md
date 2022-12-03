# Movimiento Circular
El movimiento circular es un caso particular de la [[Cinemática en 2D]] en el cual la trayectoria es una circunferencia, o parte de ella, esto es, para todo instante en el intervalo de interes, las coordenadas del movil cumplen
$$(x(t) - x_0)^2 + (y(t) - y_0)^2 = R^2$$
Si para describir el movimiento se elige un sistema de coordenadas cuyo origen coincida con el centro de la circunferencia, entonces $x_0 = 0$, $y_0 = 0$ y la trayectoria es descripta en coordenadas cartesianas por la ecuacion
$$x^2(t) + y^2(t) = R^2$$
Pasaremos a estudiar este tipo de movimientos circulares (lo que están centrados en el origen).

## El vector posición, velocidad y aceleración
El vector posición ([[Vectores]]) de una partícula que realiza un movimiento circular puede expresarse en funcion del radio del círculo, que es una constante, y el angulo $\theta(t)$, que forma dicho vector con el eje $x$,
$$\vec{r}(t) = R[\; \cos(\theta(t))\hat{\imath} + \text{sen}(\theta(t)) \hat{\jmath} \;] \implies |\vec{r}(t)|$$
La función $\theta(t)$ se llama **posición o movimiento angular** que representa el cambio del ángulo del vector posición con respecto al tiempo.  Derivando $\vec{r}(t)$ obtenemos el vector velocidad del cuerpo,
$$\vec{v}(t) = R \Big[ -\text{sen}(\theta(t)) \frac{\mathrm{d}\theta}{\mathrm{d}t} \hat{\imath} + \cos(\theta(t))\frac{\mathrm{d}\theta}{\mathrm{d}t}\hat{\jmath}\Big] = R \frac{\mathrm{d} \theta}{\mathrm{d}t} [-\text{sen}(\theta(t))\hat{\imath} + \cos(\theta(t))\hat{\jmath}]$$
La [[Derivada]] del movimiento angular $\theta(t)$, se llama velocidad angular y se denota
$$\omega(t) = \frac{\mathrm{d}\theta(t)}{\mathrm{d}t}$$
Entonces
$$\vec{v}(t) = R\omega(t) \; [-\text{sen}(\theta(t))\hat{\imath} + \cos(\theta(t))\hat{\jmath}]  \implies |\vec{v}(t)| = R|\omega(t)|$$

----

Derivando luego el vector velocidad obtenemos el vector acelerción
$$\vec{a}(t) = R \frac{\mathrm{d}\omega}{\mathrm{d}t} [- \text{sen} (\theta(t)) \hat{\imath} + \cos(\theta(t)) \hat{\jmath}] + R \omega \Big[-\cos(\theta(t))\cdot \frac{\mathrm{d}\theta}{\mathrm{d}t}\hat{\imath} - \text{sen}(\theta(t)) \cdot \frac{\mathrm{d}\theta}{\mathrm{d}t} \hat{\jmath}\Big]$$
$$\vec{a}(t) = R \frac{\mathrm{d}\omega}{\mathrm{d}t} [- \text{sen} (\theta(t)) \hat{\imath} + \cos(\theta(t)) \hat{\jmath}] + R \omega^2 [-\cos(\theta(t)) \hat{\imath} - \text{sen}(\theta(t))  \hat{\jmath}]$$
La derivada con repecto al tiempo de la velocidad angular la vamos a llamar aceleración angular y se denota
$$\gamma(t) = \frac{\mathrm{d}\omega(t)}{\mathrm{d}t}$$
Entonces el vector aceleración nos queda definido como
$$\vec{a}(t) = -R\omega^2(t) \; [\cos (\theta(t)) \hat{\imath} + \text{sen} (\theta(t)) \hat{\jmath}] + R \gamma(t) [- \text{sen} (\theta(t)) \hat{\imath} + \cos(\theta(t)) \hat{\jmath}]$$
Si realizamos el producto escalar entre el vector posición, ecuación (1), y el vector velocidad, ecuación (4), vemos que
$$\vec{r}(t) \cdot \vec{v}(t) = \big(R[\cos(\theta(t)) \hat{\imath} + \text{sen}(\theta(t)) \hat{\jmath}]\big) \cdot \big(R\omega[-\text{sen}(\theta(t)) \hat{\imath} + \cos(\theta(t)) \hat{\jmath}]\big)$$
Recordemos que al multiplicar $\hat{\imath} \cdot \hat{\jmath}$ y $\hat{\jmath} \cdot \hat{\imath}$ nos da 0 porque estos ortogonales entre sí, por lo que
$$\vec{r}(t) \cdot \vec{v}(t) = R^2 \omega [-\cos(\theta (t))\text{sen}(\theta(t)) + \text{sen}(\theta(t))\cos(\theta(t))] = 0$$
Sabemos que lo visto en la última ecuación da 0 porque se cancela lo que esta entre corchetes. Entonces, si el producto escalar entre el vector posición y el vector velocidad da 0 eso quiere significar que son ortogonales en todo instante, $\vec{r}(t) \perp \vec{v}(t)$. 

Notemos  que $\vec{r_d}(t)$ que determina la dirección del vector posición y el siguiente vector $\vec{u_v}(t) = -\text{sen}(\theta(t)) \hat{\imath} + \cos(\theta(t))\hat{\jmath}$ que determina la dirección del vector velocidad, son ortogales ya que $\vec{r}(t) \cdot \vec{u_v}(t) = 0$ como vimos antes al multiplicar el vector posición y velocidad anteriormente. Si comprobamos tienen todas las caracteristicas que cumple una [[Base Vectorial]]. También, estos vectores son **normales**, es decir tienen una magnitud de 1. Entonces, al ser **ortonormales** los vamos a pasar a llamar *versores*.

Observemos entonces que el vector aceleración, resulta descompuesto en dos tipos de aceleraciones diferentes, **la aceleración normal** (que va en dirección del versor posición, pero en sentido opuesto al centro de la circunferencia) y la **aceleración tangencial** (que va en dirrección del versor velocidad, y con su mismo sentido). 

---

$$\vec{a}(t) = -R\omega^2 (t)\hat{r}(t) + R\gamma(t) \hat{u_v}(t) = \vec{a_n}(t) + \vec{a_t}(t)$$
En la imagen 1 se muestran todos los vectores que intervienen en el movimiento circular.
![[Pasted image 20220126103728.png| 300x300]]

## Movimiento Circular Uniforme
En este tipo de movimiento no existe aceleración angular $\gamma(t) = 0$, pero sí hay velocidad angular constante $\omega(t) = \omega_0$. Lo cual nos deja con las siguientes ecuaciones,
$$\omega(t) = \omega_0 
 \begin{cases}
 \gamma(t) & = \frac{\mathrm{d}\omega}{\mathrm{d}t} = 0\\
 \theta(t) & = \int \omega \mathrm{d}t = \omega_0t + \theta_0
 \end{cases}$$
En este caso, el vector posición será
$$\vec{r}(t) = R[\cos(\omega_0t) \hat{\imath} + \text{sen}(w_0t)\hat{\jmath}]$$
Luego, el vector velocidad es
$$\vec{v}(t) = \frac{\mathrm{d}\vec{r}}{\mathrm{d}t} = R\omega_0 [-\text{sen}(\omega_0t)\hat{\imath} + \cos(\omega_0t)\hat{\jmath}$$
El modulo de la velocidad constante lo obtenemos usando $|\vec{v}(t)| = R|\omega_0|$. Finalmente calculamos la aceleración,
$$\vec{a}(t) = \frac{\mathrm{d}\vec{v}}{\mathrm{d}t} = -R\omega^2_0 [\cos(\omega_0t) \hat{\imath} + \text{sen}(\omega_0 t) \hat{\jmath}] = -R \omega_0^2 \hat{r}(t)$$

----

Como la aceleración angular es nula, entonces no existe la aceleración tangencial. El vector aceleración coincide con el vector aceleración normal,
$$\vec{a}(t) = \vec{a_n}(t) = R\omega_0^2 \hat{r}(t)$$
En este caso, el vector velocidad y lel vector aceleración son ortogonales entre sí.  

Entonces, al no haber aceleración tangencial, esto es, en el sentido de la velocidad, el módulo de la velocidad permanece constante, pero cambia su dirección y sentido debido a la presencia de una aceleración normal no nula.

## Movimiento Circular en coordenadas polares
Notemos que una forma más sencilla de representar el movimiento circular es utilizando [[Coordenadas Polares]]. En este caso trae simplicidad en la descripcion usar un sistema de coordenadas polares, centrado en el círculo, ya que la ecuacion (3), qué define un movimiento circular, en coordenadas polares toma la simple forma 
$$\rho = R$$
Es decir, $\rho$ es una constante, solo necesitamos de la función $\theta(t)$ para describir completamente el movimiento. Para calcular la velocidad debemos derivar el vector posición respecto al tiempo. Hasta ahora habíamos derivado vectores cuyas componentes estan escritas en coordenadas cartesianas, donde los versores son constantes y por lo tanto su derivada respecto al tiempo es cero.
![[Pasted image 20220127201253.png]]
En este caso, las derivadas de los versores dan vectores del módulo $|\omega(t)|$. Entonces en el caso del movimiento circular el vector velocidad es 
$$\vec{v}(t) = \frac{\mathrm{d}\vec{r}(t)}{\mathrm{d}t} = R \frac{\mathrm{d}\hat{u}_\rho (t)}{\mathrm{d}t} = R\omega(t)\hat{u}_\theta (t)$$
Podemos realizar el mismo proceso para el vector aceleración y obtenemos una ecuación parecida a (11).

#Primer-año #Física 