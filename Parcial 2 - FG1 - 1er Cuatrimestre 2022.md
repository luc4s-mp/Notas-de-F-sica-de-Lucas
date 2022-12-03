## Problema 1
Un ascensor de un edificio de 10 pisos viene bajando (sin personas ni carga en su interior) a velocidad constante 1,4 m/s. De repente, cuando va pasando por el quinto piso, sucede un desperfecto con el cable que los sostiene, y se suelta del mismo. A partir del intante en el que suelta del cable el ascensor comienza a caer por el ducto del ascensor de modo tal que la caja exterior del ascensor roza con el interior del ducto. Dicha fuerza de rozamiento es constante y de módulo F.
En el extremo inferior del ducto hay un sistema de reortes de constante equivalente $k$ , que amortigua la caída del ascensor.
Si denotamos $H_1$, la altura desde de la que ocurre el desperfecto hasta la plataforma de resortes (sin comprimir) encuentre la altura $H_2$ alcanzada por el ascensor.

### Solución
Consideremos 5 instantes diferentes:
1. El momento en el que sucede el desperfecto y el ascensor empieza a caer.
2. El momento en el que el ascensor llega entrar en contacto con los resortes.
3. El momento en el que el resorte llega a su máxima comprensión, llamamos $\Delta h$ la distancia que recorrió el ascensor desde el instante 2.
4. El momento en el que el resorte vuelve a su longitud de equilibrio y el ascensor es largado con una fuerza hacia arriba.
5. El momento en el que el ascensor se detiene y llega a la altura $H_2$.
![[Pasted image 20221112130951.png]]
Notemos que hay 2 fuerzas que actúan sobre el ascensor en el instante 1, el peso $\vec{F_g}$ y la fuerza de fricción constante $\vec{F}$ (que sabemos es una fuerza no conservativa) entonces por el teorema de la energía-trabajo:
$$\begin{align}
\int_{H_1}^{0} mg(-\hat{\jmath}) \cdot dy(-\hat{\jmath}) + \int_{H_1}^{0} F\hat{\jmath} \cdot dy (-\hat{\jmath}) & = \frac{1}{2}mv_{1f}^2 - {\frac{1}{2}mv_{10}^2} \\
mgH_1 + FH_1 &= \frac{1}{2}mv_{1f}^2 - {\frac{1}{2}mv_{10}^2} \\
v_{1f} &= \sqrt{2H_1(g + \frac{F}{m}) + v_{10}^2} \\
\end{align}$$
Esto nos ayuda de manera tal que ahora sabemos a que velocidad llega el ascensor a los resortes, planteemos el teorema del trabajo-energía para el instante 2 (teniendo en cuenta que ahora tenemos también la fuerza del resorte):
$$\begin{align}
\int_{0}^{\Delta h} mg(-\hat{\jmath}) \cdot dy(-\hat{\jmath}) + \int_{0}^{\Delta h} F\hat{\jmath} \cdot dy (-\hat{\jmath}) + \int_{0}^{\Delta h} ky\hat{\jmath} \cdot dy(-\hat{\jmath}) & = \underbrace{\frac{1}{2}mv_{2f}^2}_{=0} - \frac{1}{2}mv_{20}^2 \\
mg\Delta h - F\Delta h - \frac{k}{2}(\Delta h)^2 &= - \frac{1}{2}mv_{20}^2  \rightarrow v_{20} = v_{1f} \\
\end{align}$$
Lo único que desconocemos de esta ecuación es $\Delta h$, esta manera si lo despejamos nos queda
$$\Delta h  = \frac{(F-mg-k) \pm \sqrt{(mg-F+k)^2 +2k(\frac{k}{2}+\frac{1}{2}mv_{1f}^2)}}{-k}$$
Luego, podemos encontrar la ecuación para el instante 3 y despejar $v_{3f}$ que no necesariamente es la misma que $v_{1f}$ pues el sistema sigue perdiendo energía por la fricción. 
$$\begin{align}
\int_{\Delta h}^0 mg(-\hat{\jmath}) \cdot dy\hat{\jmath} + \int_{\Delta h}^0 F(-\hat{\jmath}) \cdot dy \hat{\jmath} + \int_{\Delta h}^0 ky\hat{\jmath} \cdot dy\hat{\jmath} & = \frac{1}{2}mv_{3f}^2 - \underbrace{\frac{1}{2}mv_{30}^2}_{=0} \\
-mg\Delta h - F\Delta h + \frac{k}{2}(\Delta h)^2 & =  \frac{1}{2}mv_{3f}^2 \\
v_{3f} & = \sqrt{k(\Delta h)^2-2{\Delta h}(g+\frac{F}{m})}
\end{align}$$
Por último, como ya sabemos esta velocidad que es la misma que la inicial a partir del instante 4 $v_{40} = v_{3f}$ podemos obtener $H_2$.
$$\begin{align}
\int_{0}^{H_2} mg(-\hat{\jmath}) \cdot dy\hat{\jmath} + \int_{0}^{H_2} F(-\hat{\jmath}) \cdot dy \hat{\jmath} & = \underbrace{\frac{1}{2}mv_{4f}^2}_{=0} - \frac{1}{2}mv_{40}^2 \\
-mgH_2 -FH_2 &=- \frac{1}{2}mv_{40}^2  \rightarrow v_{40} = v_{3f}\\
\boxed{H_2} & = \frac{mv_{3f}^2}{2(mg+ F)}
\end{align}$$
## Problema 2
Dos partículas de masas $m_1$ y $m_2$ (con $m_1 = 2m_2$) están ensartadas en dos alambre rígidos y paralelos, separados entre ellos una distancia $d$ . Cada partícula puede deslizar por su alambre sin rozamiento. Además ambas partículas están unidas mediante un resorte de constante $\mathrm{K}$ y longitud natural $\mathrm{L}_0$.
Las partículas son soltadas y abandonadas a sí mismas como se indica en la Figura (1) con $\alpha=45^{\circ}$.
1. Analizando la situación física, explicite qué magnitudes físicas se conservan en este problema. Justifique apropiadamente su respuesta.
Cuando las partículas se encuentren en las posiciones representadas en la Figura 2, calcular:
2.  Los vectores velocidad de cada partícula,
3. El momento angular respecto a un centro de momentos $a$ ubicado sobre una línea paralela a los alambres y que pasa por el centro de masa del sistema, d) El momento de inercia respecto del eje perpendicular al plano de movimiento y que pasa por el CM del sistema, y
4.  La velocidad angular.

### Solución
1. Empecemos notando que podemos calcular el centro de masa $\vec{r}_{\mathrm{CM}}$ desde un origen a afuera del sistema (consideramos nuestro sistema como las 2 partículas).
$$
\begin{aligned}
\vec{r}_{CM} &=\frac{m_1 \vec{r}_1+m_2 \vec{r}_2}{m_1+m_2} \\
&=\frac{2 m_2(d \hat{\jmath})+m_2(d \hat{\imath})}{2 m_2+m_2} \\
&=\frac{m_2}{3 m_2}(2 d \hat{\jmath}+d \hat{\imath}) \\
&=\frac{2}{3} d \hat{\jmath}+\frac{d}{3} \hat{\imath}
\end{aligned}
$$
Esto tiene sentido pues nos dice que estamos más cerca de la masa 2 (que es más grande). Una vez que sabemos donde está el centro de masa potemos colocar su centro de momentos ahí. De esta manera, podemos resolver los ecuaciones de fuerzas y torques.
$$\begin{aligned} 
\sum_{i=1}^n F_i &= \underset{= \; 0}{\underbrace{\vec{F}_{21}+\vec{F}_{12}}} +\underset{= \; 0}{\underbrace{\vec{N}_1+\vec{F}_1}}+\underset{= \; 0}{\underbrace{\vec{N}_2+\vec{P}_2}}=0 \Rightarrow a_{CM}=0 \\
\sum_{i=1}^n \vec{r}_i \times \vec{F}_i &= \vec{r}_1 \times \vec{F}_{21}+\vec{r}_2 \times \vec{F}_{12}+\vec{r}_1 \times \vec{P}_1+\vec{r}_2 \times \vec{P}_2+\vec{r}_1 \times \vec{N}_1 +\vec{r}_2 \times \vec{N}_2= I \vec{\gamma} \end{aligned}$$
De estas ecuaciones podemos concluir que el momento lineal se conserva pues 
$$\frac{d\vec{p}}{dt} = \sum_{i=1}^n \vec{F}_i = 0$$
la aceleración del centro de masa es 0, por lo tanto este se está moviendo en velocidad constante o está en reposo. 
Luego, veremos que el momento angular no se conserva porque si bien los torques de $\vec{r}_1 \times \vec{P}_1 + \vec{r}_1 \times \vec{N}_1 + \vec{r_1} \times \vec{F_{21,y} = 0$ y $\vec{r}_2 \times \vec{P}_2 + \vec{r}_2 \times \vec{N}_2 + \vec{r_2} + \vec{r_2} \times \vec{F}_{12,y} = 0$ se cancelan mutuamente (no existe movimiento alrededor del eje-y), tenemos que $\vec{r}_1 \times \vec{F}_{21,x} +\vec{r}_2 \times \vec{F}_{12,x} \neq 0$ (aunque las magnitudes de las fuerzas sean las mismas $\vec{r}_1$ y $\vec{r}_2$ tienen valores diferentes). Entonces,
$$\frac{d\vec{L}}{dt} = vec{r}_1 \times \vec{F}_{21,x}+\vec{r}_2 \times \vec{F}_{12,x}$$
Por último, la energía sí se conserva pues todas las fuerzas que realizan trabajo son conservativas.

2. Las velocidades se pueden calcular usando la conservación del momento lineal:
$$\begin{align} \vec{p_{inicial} = \vec{p_{final}}
\end{align}$$

