# Coordenadas Polares
El [[Movimiento Circular]] lo expresamos en su mayoria en coordenadas #cartecianas, pero una manera más sencilla de expresarla sería usando las coordenadas #polares . En donde, #Definición para representar un punto con coordenadas cartecianas $P = (x_p^2, y_p^2)$ usamos la distancia del mismo al origen, normalmente denominada $\rho$ ($\rho_p = \sqrt{x_p^2 + y_p^2}$), y el ángulo que forma el segmento de la distancia $\overline{OP}$, normalmente llamado $\theta$. Así, el punto expresado en coordenadas polares nos quedaría $P = (\rho, \theta)$.
Si quisieramos pasar de coordenadas cartecianas a polares usaríamos las ecuaciones $\rho_p = \sqrt{x_p^2 + y_p^2}$ y $\tan(\theta_p) = \frac{y_p}{x_p} \implies \theta_p = \arctan\Big(\frac{y_p}{x_p} \Big)$. Por otro lado si quisieramos pasar de coordenadas polares a coordenadas cartecianas, entonces usariamos las formulas $x_p = \rho_p \cos(\theta_p)$ y $y_p = \rho_p \text{sen}(\theta_p)$. 

## Funciones de Movimiento 
Para describir el movimiento de un cuerpo en dos dimenciones que se ve en [[Cinemática en 2D]], al igual que podemos crear funciones que representen el movimiento horizontal $x(t)$ y vertical $y(t)$ según el tiempo, podemos hacer lo mismo en coordenadas polares. Hablando de cambio de la magnitud del vector según el tiempo $\rho(t)$ y el cambio del ángulo según el tiempo $\theta(t)$. 

### Los versores $\hat{u}_\rho$ y $\hat{u}_\theta$ en coordenadas polares
Los versores $\hat{\imath}$ y $\hat{\jmath}$ son los versores ([[Base Vectorial]] Ortonormal) en las direcciones de crecimiento de coordenadas $x$ e $y$, respectivamente, podemos definir versores en las direcciones de crecimiento de las coordenadas $\rho$ y $\theta$. 
Es necesario obtener la expresión de los versores $\hat{u}_\rho$ y $\hat{u}_\theta$  en un sistema de coordenadas cartecianas para poder pasar de un sistema al otro:

Supongamos que tenemos un punto $R$ representado en el sistema polar y que su vector posición es $\vec{r}$. Para obtener $\hat{u}_\rho$ usamos que $\rho = |\vec{r}|$, por lo tanto
$$\hat{u}_\rho = \frac{\vec{r}}{|\vec{r}|} = \frac{x \hat{\imath} + y \hat{\jmath}}{|\vec{r}|} = \frac{\rho \cos(\theta)\hat{\imath} + \rho \text{sen}(\theta) \hat{\jmath}}{\rho} = \cos(\theta)\hat{\imath} + \text{sen}(\theta) \hat{\jmath}$$
Luego, para calcular la formula del versor $\hat{u}_\theta$ podemos usar el hecho que son ortogonales con $\hat{u}_\rho$:
$$\hat{u}_\rho \cdot \hat{u}_\theta = \cos(\theta) \cdot \hat{u}_{\theta,x} + \text{sen}(\theta) \cdot \hat{u}_{\theta,y} \;\;\;;\;\;\; \hat{u}_{\theta, x}^2 + \hat{u}_{\theta, y}^2 = 1$$
La solución a estas dos ecuaciones es $\hat{u}_{\theta, x} = \pm \text{sen}(\theta)$; y $\hat{u}_{\theta, y} = \mp \cos(\theta)$, lo cual tiene sentido ya que este versor define dos sentidos, horario y antihorario. Por convensión solemos definir al ángulo $\theta$ a partir del eje $x$ en sentido antihorario, así de las dos soluciones nos quedamos con
$$\hat{u}_{\theta} = -\text{sen}(\theta) \hat{\imath} + \cos(\theta) \hat{\jmath}$$
![[Pasted image 20220127120038.png]]
En la imagen 1 se muestram dos puntos A y B, y sus versores $\hat{u}_\rho$ y $\hat{u}_\theta$

#Primer-año #Matemática 