# Fuerzas conservativas y no conservativas
Gracias a nuestra definición nueva del [[Trabajo]], podemos definir de manera más concreta que es la [[Energía]].

Supongamos un cuerpo en el que se aplican distintas fuerzas de las que vimos anteriormente y analizamos el trabajo entre dos puntos $Q_0$ y $Q$:
$$\begin{align} 
 W = &  \int_{C|Q_0}^Q \vec{P} \cdot d\vec{s} + \int_{C|Q_0}^Q \vec{N} \cdot d\vec{s} + \int_{C|Q_0}^Q \vec{f} \cdot d\vec{s} + \int_{C|Q_0}^Q \vec{K} \cdot d\vec{s} + \\ & \int_{C|Q_0}^Q \vec{F}_{\text{otras}} \cdot d\vec{s} = \int_{C|Q_0}^Q m\vec{a} \cdot d\vec{s}
\end{align}$$
Analicemos primero el trabajo de la fuerza peso (Caso 1 de la tabla):
$$\begin{align} 
\int_{C|Q_0}^{Q_1} \vec{P} \cdot d\vec{s} = \int_{C|Q_0}^{Q_1} mg(-\hat{\jmath}) \cdot (dx \hat{\imath} + dy\hat{\jmath}) =_1 & \int_{C|Q_0}^{Q_1} -mg \hat{\jmath} \cdot dx \hat{\imath} + \int_{C|Q_0}^{Q_1} -mg \hat{\jmath} \cdot dy \hat{\jmath} \\
=_2 & \; 0 - \int_{C|Q_0}^{Q_1} mg dy \\
=_3 & \; -mgy_1 + mgy_0
\end{align}$$
En (1) lo que hicimos fue separar la integral en dos partes usando la propiedad de la suma, luego en (2) resolvimos el producto escalar ($\hat{\imath} \cdot \hat{\jmath} = 0$ ya que son perpendiculares y $\hat{\jmath} \cdot \hat{\jmath} = 1$ porque son paralelos) y por último en (3) resolvimos la integral usando el segundo [[Teorema Fundamental del Cálculo]] (siendo $Q_0 = x_0 \hat{\imath} + y_0\hat{\jmath}$ y $Q_1 = x_f \hat{\imath} + y_f \hat{\jmath}$ ) para obtener que $W_P = -mgh$ siendo $h = y_f - y_0$, notemos que este resultado es muy parecido a la **energía potencial gravitatoria**. Notemos además que al cancelarse la primera integral, entendemos que la energía potencial gravitatoria depende _únicamente del eje $y$_. 

Ahora analicemos un cuerpo sometido a una fuerza de un resorte (Caso 4 de la tabla):
$$\begin{align}
\int_{C|Q_0}^{Q_1} \vec{K} \cdot d\vec{s} = \int_{C|Q_0}^{Q_1} -k(x-x_0)\hat{\imath} \cdot (dx \hat{\imath} + dy\hat{\jmath}) = & \int_{C|Q_0}^{Q_1} -k(x-x_0) \hat{\imath} \cdot dx \hat{\imath} + \int_{C|Q_0}^{Q_1} -k(x-x_0) \hat{\imath} \cdot dy \hat{\jmath} \\
= & \int_{C|Q_0}^{Q_1} -k(x-x_0) dx (\hat{\imath} \cdot  \hat{\imath}) + \int_{C|Q_0}^{Q_1} -k(x-x_0) dy (\hat{\imath} \cdot  \hat{\jmath}) \\
= & -k\int_{C|Q_0}^{Q_1}(x-x_0) dx + 0\\
= & -\frac{k}{2}(x_f-x_0)^2 + \frac{k}{2}(x_0-x_0)^2 \\
= & - \frac{k}{2}(x_f-x_0)^2
\end{align}$$
De vuelta, notemos que el termino que obtuvimos es parecido a la **energía potecial** a la que habiamos calculado anteriormente en este caso. 
Veamos que ambas fuerzas **dependen de las coordenadas y no del tiempo** y como vimos anteriormente cuando tenemos fuerzas de este tipo podemos decir que el trabajo no depende del camino y escribir al trabajo como $W = \Delta T$ (como la variación de la energía cinética), pero ahora además podemos escribir al trabajo como la variación de una función escalar $V(x,y,z)$ tal que el trabajo de la fuerza entre el camino de los puntos $P_0$ y $P$ es
$$W = \int^{P}_{P_0} \vec{F}\cdot d\vec{s} = -[V(x,y,z)-V(x_0,y_0, z_0)]$$
Entonces, podemos encontrar una **función para la energía potencial** $V(x,y,z)$, en todos los casos en los que el trabajo no dependa del camino, es decir podemos encontrar el trabajo encontrando esta función y evaluandola en los extremos del camino sin necesidad de saber que ocurrió en el medio de la trayectoria. Al tipo de fuerzas con las cuales esto ocurre se llaman **fuerzas conservativas**. Y podemos armar un campo con cada ellas llamado **campo conservativo**.

Sin embargo, existen fuerzas que dependen de las coordenadas pero en ellas el trabajo si depende del camino (por lo tanto no se puede obtener una función de la energía potencial) entonces estas fuerzas se llaman **fuerzas no conservativas**. Un ejemplo de una fuerza no conservativa es la fricción, supongamos un auto con frenos bloqueados que se derrapa por el pavimento con una velocidad (y energía cinética) decreciente(s), la energía cinética no se puede recuperar de ninguna manera, por lo tanto la energía mecánica **no se conserva** (con esto nos referimos a que a simple vista no se conserva, pero como veremos en la ley de conservación la energía siempre se debe ir a algún lado) y no existe función de energía potencial para la fuerza de fricción.

Podemos ver la importancia entonces del trabajo, nos relaciona la **energía cinética** con la **energía potencial**. 

# Ley de la Conservación de la energía
En [[Trabajo]] empezamos manipulando una serie de formulas que ya sabíamos y nos topamos con que  el trabajo de la fuerza resultante es igual a la variación de la energía cinética en el punto inicial y final del movimiento ( $W_{\text{net}} = \Delta T$) otra forma de llegar a este resultado es calculando la integral la última integral del cuerpo anterior  $\int m\vec{a} \cdot d\vec{s}$. Sabiendo esto y calculando el trabajo de cada fuerza veremos que $W_{\text{net}} = (-\Delta V_P) + (-\Delta V_K) + (-\Delta V_{\text{otros}})$ entonces $W_{\text{net}} = -\Delta V_{\text{total}}$   

Luego, dijimos que siempre que tengamos fuerzas que dependen de las coordenadas (fuerzas conservativas) vamos a poder encontrar una función de la energía potencial $V(x,y,z)$ tal que $W = -\Delta V$. Entonces, si queremos analizar la variación de la energía mecánica debe ocurrir que $\Delta E = 0$  para que esta se **conserve**, y esto ocurre para los casos tratos ya que
$$\Delta E = \Delta T + \Delta V \implies \Delta E = W  - W = 0  \implies E_i = E_f \quad (\text{también } \Delta T = -\Delta V)$$
> **Ley de la Conservación de la Energía Mecánica**
> La energía mecánica $E$ se conserva si y solo sí existen fuerzas conservativas aplicadas a un cuerpo de masa puntal,  su energía cinética aumenta o disiminuye "a expensas" de la energía potencial $\Delta T = -\Delta V$.

Observemos que esta ley no corresponde con la noción general de energía que siempre nos dieron que es "la energía no se crea, ni se destruye, solo se transforma", esta frase viene del hecho que si bien la energía mecánica no se conserve (es decir tenemos una fuerza no conservativa actuando) la energía perdida debe ir a algún lugar, ya sea calor, sonido, deformaciones del material, la energía se debe manifestar de otra manera, _no se puede destruir o crear energía de la nada_ siempre tiene que venir o ir a algún lugar.

Los casos anteriores fueron bastante convenientes, ya que las fuerzas dependian únicamente de una coordenada. Pero, ¿Qué ocurre cuando dependen de más una coordenada? Y podemos preguntarnos también, ¿Cómo obtenemos las funciones de las fuerzas usando la función de la energía potencial dado?

## Relacionando Conceptos de Trabajo - Energía - Fuerzas cons. y no cons.
En [[Trabajo]], vimos que 
$$W = \int_{P_1}^{P_2} F(x,y,z)du = -[V(x_2,y_2,z_2)-V(x_1,y_1,z_1)]$$
Notemos que $V(x,y,z)$ es una primitiva de la función $F(x,y,z)$ es decir
$$F(u) = -\frac{dV}{du}$$
Entonces, si tenemos la función potencial $V$ veamos que podemos obtener la función de la fuerza conservativa $\vec{F}_c$:
$$-dV(x,y,z) = \vec{F_c} \cdot d\vec{s} = (F_{cx} \hat{\imath} + F_{cy}\hat{\jmath} + F_{cz}\hat{k})\cdot (dx \hat{\imath}+ dy \hat{\jmath} + dz\hat{k})$$
Entonces, $F_{cx}dx + F_{cy}dy + F_{cz}dz = -dV(x,y,z)$ y si quisieramos despejar $F_{cx}$ por ejemplo podriamos considerar como fijas las coordenadas $y$ y $z$ de manera tal que el segundo y el tercer término no afectan en nada. Pasando el incremento $dx$  dividiendo y tomando límite obtenemos una [[Derivada Parcial]]:
$$F_{cx} = - \frac{\partial V(x,y,z)}{\partial x}$$
Y así se puede hacer lo mismo con las otras coordenadas $y$ y $z$. Notemos entonces que
$$\vec{F_c} = \frac{\partial V(x,y,z)}{\partial x}\hat{\imath} - \frac{\partial V(x,y,z)}{\partial y} \hat{\jmath} - \frac{\partial V(x,y,z)}{\partial z}\hat{k}$$
Para este tipo de funciones vectoriales en las que sus componentes cartecianas se pueden escribir como las derivadas parciales de una función escalar lo llamamos _gradiente_ (lo simbolizamos con un signo "nabla" $\nabla$ ) entonces
> **Fórmula para encontrar Fuerzas Conservativas que dependen de más de una coordenada**$$\vec{F_c} = -\nabla V(x,y,z)$$

Sabemos que podemos agrupar a las fuerzas aplicadas a un cuerpo en dos conjuntos: las fuerzas conservativas $\vec{F_c}$ y no conservativas $\vec{F}_{nc}$ tal que el trabajo de todas las fuerzas aplicadas de una masa puntal que se desplaza en la curva $C$ desde el punto $Q_1$ al punto $Q_2$ será
$$W  = W_{F_c} + W_{F_{nc}} \implies_{(1)} \quad \Delta T= -\Delta V + W_{F_{nc}} \implies W_{F_{nc}} = \Delta T + \Delta V = \Delta E$$
En (1) lo que hicimos fue reemplazar sabiendo que el trabajo de todas las fuerzas aplicadas es igual a la variación de la energía cinética $W = \Delta T$ y que $W_{F_n} = -\Delta V$. 

> **Fórmula para la energía cuando existen Fuerzas no conservativas** $$\Delta E = W_{F_{nc}}$$

### Analizando diagramas de energía potencial de un cuerpo en movimiento unidimensinal
Cuando una partícula se mueve en línea recta bajo la acción de una fuerza conservativa, podemos entender mejor los posibles movimientos examinando la gráfica de la función de energía potencial $V(x)$.
Estas gráficas son muy útiles ya que podemos entender muchos datos del movimiento sin necesidad de requerir del tiempo en el que ocurrió. Demos un ejemplo, supongamos un cuerpo al que se le ejerce una fuerza $F_x = -kx$ (fuerza de un resorte, [[Ley de Hooke]]) que oscila en un intervalo $[-A, A]$. Su gráfica de energía potencial $V(x) = \frac{k}{2}x^2$ (obtenida integrando la función de la fuerza del resorte) se vería:
![[Pasted image 20220518103640.png | 300]]
De esta gráfica podemos obtener los siguientes datos:
- Los **valores para los cuales la energía vale**: es decir, para un valor fuera del intervalo $[-A, A]$ no podríamos obtener su energía, porque para que fuera posible la *energía cinética debería ser negativa y eso no es posible*. 
- La **energía cinética** (en el gráfico se representa con la letra $K$) en cada punto: ya que sabemos que $K = E - U$  entonces podemos simplemente restar al valor de la energía menos el valor de la energía potencial en ese punto y obtenemos la energía cinética.
- La **fuerza aplicada** al cuerpo en cada punto: sabemos que $\vec{F}(x) = -dV/dx$  por lo tanto la pendiente de la recta tangente en cada punto es la fuerza que se aplica en ese momento, recordemos que el signo de la fuerza es opuesto al valor de la energía potencial (entonces cuando la pendiente es positiva, la fuerza es negativa y viceversa). 
- Los **puntos de equilibrio del cuerpo**: observemos que en el punto $x=0$ la pendiente de la recta tangente es 0 por lo tanto $F = 0$ y no existe energía potencial (pero sí cinética, de hecho en este punto se llega a su más alto valor), es por esto que este tipo de puntos se llaman "punto de equilibrio". En particular, este es un **punto de equilibrio estable** ya que si trazaramos todas las fuerzas en cada punto (teniendo en cuenta que es la derivada y que tienen el signo opuesto), veamos que al principio entre -A y O las rectas tangentes tienen una pendiente negativa por lo que las fuerzas van a ser positivas, también observemos que a medida que estamos cerca de O las pendientes van tendiendo a hacerse 0 por lo cual las fuerzas son cada vez más chicas a medida que nos acercamos a O; ocurre lo opuesto entre O y A. Es como si las fuerzas tendieran a hacer que las partículas se acerquen a ese punto, tal cual ocurre en el movimiento armónico simple. Entonces, podemos afirmar que *siempre que haya un mínimo va a haber un punto de equilibrio estable*. Cuando existe un _máximo_ en la función obtenemos que hay un **punto de equilibrio iniestable** porque las fuerzas tienden a hacer que la partícula se aleje de ese punto. 
