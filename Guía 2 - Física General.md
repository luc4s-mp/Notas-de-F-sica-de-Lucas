# Aplicaciones de las leyes de Newton
![[Pasted image 20220402174300.png]]
## Problema 7

## Problema 8 
Sobre una superficie horizontal se fija un extremo del resorte, que tiene longitud natural de $0,5$ m y cuya constante elastica es de $400$  N/m. Al otro extremo se une un cuerpo de 2 kg de masa. Se hace mover el cuerpo de manera que describa una trayectoria circular. 
1. Si el radio de la circunferencia es de 1 m, ¿Cuál es la velocidad del cuerpo?
2. Si se duplica su velocidad ¿Cuál deberá ser el nuevo radio?

### Resolución
**IDENTIFICAR**: Nuestra incognita en el caso (1) es la velocidad que tiene el cuerpo teniendo en cuenta que es un [[Movimiento Circular]] y sabiendo que $R = 1$ m, sabemos que la aceleración está conformada por $\vec{a}(t) = -R\omega^2 (t)\hat{r}(t) + R\gamma(t) \hat{u_v}(t) = \vec{a_n}(t) + \vec{a_t}(t)$, es decir por una aceleración centrípeta y una aceleración tangencial. Observemos que en este caso no existe aceleración tangencial,  por lo que $\gamma (t) = 0$ . Para calcular el módulo de la velocidad es $|\vec{v}| = |R \omega|$  Y sabemos que a su vez el objeto no está fijo a una cuerda sino un resorte y este mismo cambia de longitud. Observemos que en este caso vamos a tener que aplicar la [[Ley de Hooke]], que nos dice que $F_{resorte} = k \Delta l$ siendo $l_0 = 0,5$ m, $l = 1$ m y $k = 400$ N/m. Por último, las fuerzas verticales se cancelan debido a que no existe desplazamiento en el eje y.

**PLANTEAR**: Nuestro diagrama de cuerpo aislado lo vamos a contruir teniendo en cuenta todo lo anterior. Las fuerzas que actuan sobre el cuerpo de masa m son el peso $\vec{P}$  y la fuerza normal $\vec{N}$ de contacto con la superficie horizontal. Sobre el eje-x tenemos la fuerza ejercida por el resorte $\vec{F}$ .  Observemos $\vec{F} = k \Delta l \; \hat{\imath}$, $\vec{N} = N \; \hat{\jmath}$ y $\vec{P} = P \; (-\hat{\jmath})$.  
![[Pasted image 20220402125635.png | 300]]

**EJECUTAR**: Como no existe movimiento en la vertical entonces $\sum F_y = 0$. Por la segunda ley de Newton sabemos que 
$$\vec{R} = \sum \vec{F} = m\vec{a} \;\;\;\; \implies \sum F_x = k \Delta l \; \hat{\imath} = ma_x \hat{\imath} \;\; \sum F_y = N(\hat{\jmath}) + P(-\hat{\jmath}) = (N - P) \; \hat{\jmath} = 0$$
Luego, $N = P$. 
Notemos que $k \Delta l = ma$, puedo despejar la aceración dando $100$ m/s. Luego, yo sé que en un movimiento circular el modulo de la aceleración normal  es igual a $a = |R\omega^2|$ de tal manera que puedo despejar la velocidad angular $100 \text{m/s} = 1 \text{m} \cdot \omega^2$ y nos da $\omega = 10$ rad/s. Por último, como el módulo de la velocidad $v = |R \omega| = l \omega$, entonces $v = 1 \; \text{m} \cdot 10 \;\text{rad/s} = 10 \;\text{m/s}$ . 
_Fin del apartado (a)_ 

Si la velocidad es el doble $v = 20$ m/s,  y desconocemos el nuevo radio que a su vez representa que tan largo está el resorte entonces planteando la segunda ley nos queda $400 \; \text{N/m} \cdot (l - 0,5 \text{m}) = 2 \; \text{kg} \cdot a$ , despejando $a$ de la ecuación nos queda $a = \frac{400 \;\text{N/m} \cdot (l - 0,5 \text{m})}{2 \text{ kg}}$, luego reemplazamos esto en 
$$\begin{align}
\frac{400 \;\text{N/m} \cdot (l - 0,5 \text{m})}{2 \text{ kg}} = l\omega^2 \implies \omega = \sqrt{\frac{400 \;\text{N/m} \cdot (l - 0,5 \text{m})}{2 \text{ kg} \cdot l}} \\ = \sqrt{\frac{400 \;\text{N/m} \cdot l - 400 \;\text{N/m} \cdot 0,5 \text{m}}{2 \text{ kg} \cdot l}} \\ = \sqrt{ 200 \; \text{rad/s}^2 - \frac{100}{l} \; \text{rad/s}^2} \\ 
\end{align} $$
Finalmente, reemplazamos en la ecuación $v = R \omega$
$$\begin{align}
20 \text{ m/s} = \sqrt{ 200 \; \text{rad/s}^2 - \frac{100}{l} \; \text{rad/s}^2} \cdot l  \\
(20 \text{ m/s})^2 = 200 \; \text{rad/s}^2 \cdot l^2 - \frac{100}{l} \; \text{rad/s}^2 \cdot l^2 \\
400 \text{ m/s} = 200 \; \text{rad/s}^2 \cdot l^2 - 100 \; \text{rad/s}^2 \cdot l \\ 
\end{align}$$
Nos queda una ecuación cuadrática con soluciones $l_1 = 1,69$ m y $l_2 = -1.19$ m. Como por definición el radio de un círculo no puede ser negativo, $l = 1,69$ m. 
_Fin del apartado (b)_

**EVALUAR**: El resultado del apartado (a) es $v = 10 \text{ m/s}$, que tiene unidades correctas, no nos piden el vector sino el módulo de la velocidad así que es correcto dejarlo así. En el apartado (b) obtuvimos que nuestra longitud del resorte para una velocidad $v = 20 \text{ m/s}$ es $l = 1,69 \text{ m}$.

## Problema 11
Un cuerpo está inclinado con coeficientes de rozamiento $\mu_e$  y $\mu_d$: 
1. Indique todas las fuerzas que actuán sobre el cuerpo.
2. Si el ángulo $\theta$ se hace crecer continuamente desde la horizontal, ¿para qué valor de $\theta$ se comenzará a deslizar el cuerpo?
3. Si el cuerpo estuviera moviéndose hacia abajo, ¿para qué ángulo $\theta$ viajaría con la velocidad constante?

### Resolución
**INDENTIFICAR**: En este problema tenemos un caso donde se presentan [[Aplicando las leyes de Newton]] en particular el caso con _fuerzas de rozamiento_. En primer lugar queremos plantear todas las fuerzas que se ejercen sobre el cuerpo, encontraremos que son 3: el peso $\vec{P}$ que apunta verticalmente hacia abajo, luego la normal $\vec{N}$ ya que se encuentra en contacto con una superficie que es perpendicular a la superficie y la fuerza de fricción $\vec{f}$   que va en el sentido opuesto al movimiento. Elegimos un sistema de coordenadas inclinado en un ángulo $\theta$ para seguir el sentido de la aceleración.

**PLANTEAR**: Construimos nuestro diagrama de cuerpo aislado con los datos que obtuvimos anteriormente, observemos que $\vec{P} = mg \cdot \cos(\theta) (\hat{\imath}) + mg \cdot \text{sen} (\theta) (-\hat{\jmath})$,  $\vec{N} = N \hat{\jmath}$  y $\vec{f_e} = \mu_e N(- \hat{\imath})$. Como por ahora estamos suponiendo que el cuerpo está quieto entonces tenemos una fuerza de fricción estática y como estamos intentando encontrar al ángulo máximo posible entonces vamos a usar la fuerza estática máxima, $\vec{f}_{e, \text{máx}} = \mu_e N$.
![[Pasted image 20220402185553.png | 300]]

**EJECUTAR**: Notemos que si el cuerpo está en equilibrio entonces 
$$\sum \vec{F}_i = \vec{P} + \vec{N} + \vec{f_e} = 0 \implies \sum F_x = mg \cdot \cos \theta - \mu_e N = 0 \;\; \sum F_y = -mg \cdot \text{sen } \theta + N = 0$$
Luego, $mg \cdot \cos \theta = \mu_e N$ y $N = mg \cdot \text{sen } \theta$ entonces reemplazando una ecuación en la otra obtenemos que 
$$mg \cdot \cos \theta = \mu_e \cdot mg \cdot \text{sen } \theta \implies \mu_e = \frac{\text{sen } \theta}{\cos \theta} \implies \mu_e = \tan \theta \implies \theta = \arctan \mu_e$$
Esta es la solución al apartado (b), es decir este es el ángulo necesario para el cuál el cuerpo se empieza a deslizar. Luego si el cuerpo se estuviera moviendo en una velocidad constante, entonces $a = 0 \; \text{m/s}^2$ usamos las mismas ecuaciones que anteriormente (ya que la formula para la fricción dinámica no cambia en este caso $\vec{f}_d = \mu_d N$ ) nada más que reemplzando $\mu_e$ por $\mu_d$ y obtenemos la misma ecuación $\theta = \arctan \mu_d$. 

**EVALUAR**: Los resultados obtenidos son los siguientes, (a) Las fuerzas que se ejercen son 3, el peso $\vec{P}$, la normal $\vec{N}$ y la fuerza de fricción $\vec{f}$ , (b) $\theta = \arctan \mu_e \; [\text{rad}]$ y (c) $\theta = \arctan \mu_d \; [\text{rad}]$. 

## Problema 16
Un cuerpo de masa $m = 120$ g, apoyado sobre un cono de ángulo $\alpha = 60°$, gira con una frecuencia angular $f = 10$ rpm. Sabiendo que el hilo es inextensible, su longitud es $l = 50$ cm y no existe rozamiento entre el cuerpo y la superficie del cono, calcule:
1. La velocidad tangencial del cuerpo,
2. La tensión del hilo,
3. La velocidad angular necesaria para reducir la reacción del plano a cero.

### Resolución
**IDENTIFICAR**: Nuestra incógnita son $\vec{v}$ , $\vec{T}$  y $\omega$ necesaria para que $\vec{F_c} = 0$. Observemos que el movimiento presentado en el problema es circular uniforme, es decir $\gamma (t) = 0$, por lo cual $|\vec{v}| = v = |R \omega|$ y la aceleración es normal unicamente $|\vec{a_n}| = a_n = a = |R \omega^2|$. Ahora, las fuerzas que están actuando son particularmente 3, la fuerza de contacto $\vec{F_c}$  que es perpendicular a la superficie apoyada (en este caso el cono), el peso $\vec{P}$ y la tensión $\vec{T}$ generada por la cuerda sobre la que está el péndulo. 

**PLANTEAR**: Elegimos un sistema de coordenadas de tal manera que el versor $\hat{\imath}$ apunte hacia el centro del circulo sobre el que rota el cuerpo. Observemos que eligiendo este sistema $\vec{P} = mg (-\hat{\jmath})$, $\vec{F_c} = -F_c \cdot \cos \alpha \hat{\imath} + F_c \cdot \text{sen } \alpha \hat{\jmath}$ y $\vec{T} = T \cdot \text{sen } \alpha (\hat{\imath}) + T \cdot \cos \alpha \hat{\jmath}$   Nos dan la frecuencia, recordemos que la formula para relacionar la frecuencia y la velocida angular es $\omega = 2 \pi \cdot f$ .
![[Pasted image 20220403131928.png | 350]]
**EJECUTAR**: En el apartado (1) nos piden calcular el módulo de la velocidad tangencial, sabemos que $v = R \omega$, en este caso no tenemos ni el radio ni la velocidad angular. Para calcular la velocidad angular la obtenemos de la frecuencia $\omega = 2 \pi \text{ rad} \cdot \frac{10 \text{ rpm}}{60 \text{ s}} = \frac{\pi}{3} \text{ rad/s}$. Luego, para calcular el radio planteamos un tríangulo rectangulo que tiene como hipotenusa el largo del hilo que sostiene al cuerpo $l = 50$ cm y como cateto opuesto al radio, usando la razón trig. seno nos queda $\text{sen } \alpha = \frac{R}{l} \rightarrow \text{sen } 60° = \frac{R}{0,5 \text{ m}} \rightarrow R = 0,5 \text{ m} \cdot \text{sen } 60° = \frac{1}{2} \cdot \frac{\sqrt{3}}{2} = \frac{\sqrt{3}}{4}$. Entonces obtenemos la velocidad $v = \frac{\sqrt{3}}{4} \text{ m}\cdot \frac{\pi}{3} \text{ rad/s} = \frac{\sqrt{3}\pi}{12} \text{ m/s} = \frac{\pi}{4 \sqrt{3}} \text{ m/s}$. 
_Fin del apartado (1)_

En el apartado (2), nos piden la tensión del hilo ahora es necesario usar las leyes de Newton, ($P = mg = 0,12 kg \cdot 9,8 \text{ m/s}^2 = 1,18 \text{ N}$) sabemos que
$$m\vec{a} = \sum \vec{F}_i = \vec{F_c} + \vec{T} + \vec{P} \rightarrow \;\;\; \begin{align} 
\sum F_x = T \cdot \text{sen } 60° - F_c \cdot \cos 60° = ma \\ 
\sum F_y = T \cdot \cos 60° + F_c \cdot \text{sen } 60° - 1,18 \text{ N} = 0
\end{align}$$
Sademos que $\sum F_y = 0$ ya que el cuerpo no se desplaza verticalmente sino horizontalmente. Observemos que tenemos un sistema de ecuaciones con 2 incógnitas que podemos resolver, sabiendo que la aceleración normal es $a = R \omega^2 = \frac{\pi}{4 \sqrt{3}} \text{ m} \cdot \Big(\frac{\pi}{3} \text{rad/s} \Big)^2 = \frac{\pi^3}{36 \sqrt{3}} \text{ m/s}^2$ y esto por la masa nos da una resultante de $\frac{\pi^3}{300 \sqrt{3}} \text{ N}$.    
$$
\left\{\begin{array}{l}
\frac{\sqrt{3}}{2} T-\frac{1}{2} F_{C}=0,06 \mathrm{~N} \\
\frac{1}{2} T+\frac{\sqrt{3}}{2} F_{C}=1,18 \mathrm{~N}
\end{array}\right.
$$
Resolvemos por sustitución
$$
\begin{aligned}
-\frac{1}{2} F_{c} &=0,06 \mathrm{~N}-\frac{\sqrt{3}}{2} T \\
F_{c} &=-0_{1} 12 \mathrm{~N}+\sqrt{3} T
\end{aligned}
$$
Esto la reemplezamos en
$$
\begin{aligned}
\frac{1}{2} T+\frac{\sqrt{3}}{2}(-0,12 N+\sqrt{3} T) &=1,18 N \\
\frac{1}{2} T - 0,10 N + \frac{3}{2} T &=0,10 N+\frac{3}{2} T=1,18 N \\
2 T &=1,18 N+0,10 \mathrm{~N} \\
2 T &=1,28 \mathrm{~N} \\
T &=0,64 \mathrm{~N}
\end{aligned}
$$
_Fin del apartado (2)_

En el apartado (3), nos piden la velocidad angular necesaria para que el cuerpo ya no esté en contacto con el cono y $F_c = 0 \text{ N}$. Entonces, sabiendo además que la aceleración normal, dada una velocidad angular, es igual a $a = R \omega^2$  y que la tensión la calculamos con la ecuación $\frac{1}{2} T+\frac{\sqrt{3}}{2} (0 \text{ N})=1,18 \mathrm{~N}$ tiene que ocurrir que 
$$0 \;\mathrm{N} = m(R \omega^2) - \frac{\sqrt{3}}{2}T \rightarrow \;\; 0 = 0,12 \text{ kg} \cdot \frac{\sqrt{3}}{4} \text{ m} \cdot \omega^2 - \frac{\sqrt{3}}{2}(2,36 \text{ N}) \rightarrow \;\; \omega = 6,27 \text{ m/s}$$
_Fin del apartado (3)_