## La Fuerza Normal
Si un cuerpo está en contacto con una superficie, la fuerza en el cuerpo generada por la superficie puede separarse en dos componentes, una perpendicular a la superficie y una tangencial a la superficie. La componente perpendicular es llamada fuerza **normal** y la tangencial es la **fricción**.
El origen de la fuerza normal nace de un análisis de lo que ocurre de manera molecular en un cuerpo. Cuando ponemos un libro sobre una mesa, las moléculas del libro ejercen fuerzas hacia abajo sobre las moléculas de la mesa. La parte superior de la mesa se hunde hasta que la repulsión de las moléculas de la mesa se balancea con la fuerza aplicada sobre el libro. Para ilustrar esto mejor, si usted tiene una superficie hecha de gelatina, notará que al colocar el libro este se hunde en la misma, esto ocurre por lo que mencionamos y ocurre en todas las superficies, nada más que **en cuanto más rígida es la misma menor es la depresión que genera el libro**.
Hay que tener mucho cuidado al darle un valor a la fuerza normal, a diferencia de otras fuerzas como las [[Fuerzas Gravitacionales]] y las [[Fuerzas Elásticas y Movimiento Armónico Simple]] a estas no se las puede definir concretamente en una formula, fluctúan mucho dependiendo el contacto que tiene el objeto con la superficie. Por ejemplo, si usted está parado entonces la magnitud de la fuerza normal es igual a la magnitud de su peso, en cambio si empieza a caminar, la fuerza normal va cambiando de valor porque el contacto con la superficie ya no es el mismo. 

## La Fuerza de Fricción
La fricción es una fuerza que _se opone al movimiento relativo del cuerpo en contacto_. En el desarrollo de instrumentos mecánicos la fricción se ve como un problema, pero en general nuestra vida cotidiana no podría existir sin fricción: no podríamos caminar ni conducir autos. 

La fricción aparece cuando un cuerpo se mueve, o intenta moverse, sobre una superficie de otro cuerpo. La magnitud de la fricción varia de manera complicada dependiendo de la naturaleza de las superficies y su velocidad relativa. De hecho, lo único que podemos decir de la fricción es que se ***opone al movimiento que puede ocurrir en su ausencia***. Por ejemplo, si empujamos un libro usando fuerzas chicas, puede que al principio el libro no se mueva porque la fuerza de fricción se le opone al movimiento y mantiene el libro en reposo. Si vamos haciendo crecer la fuerza que aplicamos puede que el libro siga en reposo y la fuerza de fricción crezca para oponerse a la fuerza que estamos haciendo. Sin embargo, la fuerza no puede crecer hasta el infinito. Si empujamos al libro usando la fuerza suficiente, entonces este se va a empezar a mover. Una vez que el libro está moviéndose, la fuerza de fricción parece mantenerse constante. 

Ya que la fuerza normal y la fuerza de fricción vienen del mismo lado tiene sentido que el límite de la fuerza de fricción sea proporcional a la normal $f \propto N$. La constante de proporcionalidad se llama **coeficiente de fricción**  $\mu$ (mu) y existe una para cada superficie, inclusive podemos diferenciar entre la constante proporcionalidad **estática** (para cuerpos que no están en movimiento) y la **cinética** (para cuerpos que se mueven), los cuales suelen ser muy parecidos. 

Para resumir, definimos a  $f$ que se comporta como:
1. Para cuerpos que no tienen movimiento (fricción estática) tenemos que $0 \leq f \leq \mu_e N$.  $\vec{f}$ se opone al movimiento que ocurriría en su ausencia y cuando se aplica una fuerza de magnitud $F$ que no es mayor a $\mu_e N$ entonces $f = F$.
2. Para cuerpos que tienen movimiento (fricción cinética), tenemos que $f = \mu_c N$ y $\vec{f}$ es opuesta a la velocidad relativa del cuerpo. 

Podemos graficar el comportamiento de $f$ como:
![[Pasted image 20221208211926.png]]

### Ejemplo. Un bloque en un plano inclinado con fricción
Un bloque de masa $m$ descansa sobre un plano inclinado de ángulo $\theta$. El coeficiente de fricción estática es $\mu_e$. Encuentre el valor de $\theta$ para el cual el bloque empieza a deslizar, y la aceleración horizontal $\ddot{x}$ en la que se desliza.   
![[Pasted image 20221208212813.png]]
En la ausencia de fricción, el bloque hubiera deslizado por el plano, es por esto que $\vec{f}$ apunta hacia arriba. Con las coordinadas mostradas tenemos por la segunda ley de Newton que $$\begin{align}
m \ddot{x} & = W \mathrm{sen} \; \theta - f \\
m \ddot{y} & = N - W \cos \theta = 0\\ 
\end{align}$$
Notemos que el valor máximo que puede tener la fricción estática es $f = \mu_e N$ y en ese caso $\ddot{x} = 0$, en este caso se encuentra el ángulo máximo que buscamos:
$$\begin{align}
W \mathrm{sen} \; \theta_{\text{máx}} &= \mu_e N\\
W \cos \theta_{\text{máx}} &= N 
\end{align}$$
De esta manera, reemplazando una ecuación en otra tenemos que $$W \mathrm{sen} \; \theta_{\text{máx}} = \mu_e (W \cos \theta_{\text{máx}}) \quad \rightarrow \quad \mu_e = \frac{\mathrm{sen} \; \theta_{\text{máx}}}{\cos \theta_{\text{máx}}} = \tan \theta_{\text{máx}} \quad \rightarrow \quad \theta_{\text{máx}} = \arctan \mu_e$$
Entonces, si hacemos aumentar el ángulo del bloque desde cero, la fuerza de fricción crece en magnitud desde $0$ a como máximo $\mu_e N$, antes de llegar a esta situación extrema su módulo está dado por 
$$f = Mg\; \mathrm{sen} \; \theta  \quad \theta < \theta_{\text{máx}}$$
Una vez que el bloque está acelerando, la aceleración está dada por
$$\ddot{x} = g(\mathrm{sen} \; \theta - \mu_c \cos \theta)$$
