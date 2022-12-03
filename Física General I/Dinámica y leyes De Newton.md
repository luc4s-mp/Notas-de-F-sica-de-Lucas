# Leyes de Newton - Dinámica
En Fisíca General empezaremos con nuestro estudio de la **dinámica**, que es una parte de la [[Mecánica Newtoniana]] que estudia la **razón** sobre la cual se producen los movimientos, algo que en [[Cinemática del punto]] evitabamos, solo nos preocupabamos por intentar predecirlos.

---
## Problema Inicial - Persiguiendo aliens
Aliens se han inflintrado en una estación de policía espacial intergaláctica, robaron un transbordador espacial y ahora están huyendo. Dos naves espaciales fueron las encargadas de pereguirlos: la nave A, dirigida por la comandante Abril y la nave B, dirigida por  el comandante Bruno. Para capturar el transbordador, los comandantes deben saber si este está acelerando o yendo a una velocidad constante. Por simplicidad, vamos a asumir que tanto A, B y el transbordador se mueven en línea recta. 

Usando sus métodos de detección del movimiento de la luz, la comandante Abril hace un sistema de coordenadas con su nave como origen y mide la distancia con el transbordador espacial en diversos tiempos, modelando la función $x_A(t)$. A partir de está función de movimiento calcula la función velocidad sabiendo que $v_A(t) = \dot{x}_A(t)$[^1]  y luego la aceleración por $a_A(t) = \ddot{x}_A(t)$.
![[Pasted image 20220910132649.png]]

Los resultados, muestran que el transbordador tiene una aceleración constante. Abril calcula cual sería esta aceleración. Sin embargo, cuando el comandante Bruno reptite el mismo proceso le da una aceleración distinta a la medida por Abril ¿Por qué puede suceder esto?

---

Nuestro objetivo en esta nota es entender las leyes de Newton del movimiento. Estas leyes son simples de escribir y no son matemáticamente complejas. Combinan definiciones, observaciones de la naturaleza, conceptos intuitivos, que son el resultado de cientos de años de desarrollo por físicos. Newton nomás las formalizó, pero estas ideas se vinieron formando desde los antiguos griegos. 

Empecemos realizando un experimento simple. Desgraciadamente, "experimentos simples de mecánica" pueden ser dificiles de llevar a cabo porque el movimiento en nuestro día a día está influenciado por varias "entidades" como la gravedad, la fricción o el aire. Para entender las leyes debemos pensar como eliminar los efectos de estas y estudiar los "sistemas aislados"[^2] , es lo más recomendable primero para poder entender cuales son las propiedades básicas del movimiento. La forma más obvia de generar estas condiciones es irnos al espacio, lo cual es un poco difícil de lograr a no ser que seas Elon Musk. Otra manera de generar estas condiciones es usar un "linear air track" que aproxima las condiciones ideales pero solo en una dimensión (no esta claro que podamos entender el movimiento en 3 dimensiones de estudiar el movimiento en 1 dimensión, pero resultara que si podemos). 
![[Pasted image 20220910122224.png| 400]]
Cuando se enciende el aparato, el "corredor" o rider flota sobre el air track sobre una fina capa de aire. De esta manera, podemos hablar de que la fricción sobre el corredor es practicamente nula, y la gravedad sobre el mismo también se vuelve nula (pues al estar flotando quiere significar que el empuje que le hace el aire contraresta el empuje de la gravedad). Entonces, hemos eliminado estas entidades que nos impedían ver claramente como se comportan cuerpos ante el movimiento. 
Ahora, observemos como se comporta el corredor. Supongamos que colocamos el corredor cuidadosamente para que permanezca en reposo. Va a observar que efectivamente el corredor se mantiene en reposo, _al menos hasta que alguna corriente de aire aparezca o alguien lo mueva_. Lo siguiente que hacemos es empujar ligeramente al corredor y dejar que este se mueva libremente. El movimiento del corredor no parece que vaya a parar y este se está moviendo a una velocidad constante, es decir que esta idea de que "los cuerpos tienden a detenerse" es erronea. Si detenemos la corriente de aire que mantiene al corredor flotando, entonces eventualmente este se detendría por la "fricción" que le haría la superficie. 

Podemos concluir entonces, que para que el movimiento de un cuerpo se detenga es necesario que una entididad exterior (que la mayoría de las veces en la vida cotidiana es la fricción del aire o la superficie) intervenga, de lo contrario **el cuerpo tiende a seguirse moviendo con velocidad constante**.  Esto es lo mismo que observó Galileo hace 400 años y llamó a esta propiedad de los cuerpos "inercia" que luego Newton la escribió como su primera ley de movimiento.

## Primera Ley - Inercia
> Todo cuerpo persevera en su estado de reposo o movimiento uniforme y rectilíneo a no ser que sea obligado a cambiar su estado por fuerzas impresas sobre él.

El reposo no tiene nada de particular respecto del movimiento rectilíneo uniforme (MRU), visto en [[Cinemática del punto]]. Los cuerpos tienden indistintamente a cualquiera de estos dos estados, según cuál sea la situación inicial: si por alguna razón un cuerpo está en MRU (velocidad constante) y no se aplica ninguna fuerza, seguirá con MRU; mientras que si estaba en reposo, seguirá en reposo (a menos que algo exterior lo cambie). Entonces, no hace falta ejercer una fuerza ”para que las cosas se muevan”, sino más bien, para que cambien su estado de movimiento. 

Para que la primera ley tenga sentido es necesario medir el movimiento respecto de un **sistema de coordenadas** (como hizo la comandante Abril). Esto es siempre lo primero que hay que hacer al abordar un problema de Dinámica: **elegir un sistema de coordenadas**. La comandante Abril, eligió un sistema de coordenadas fijo en su nave espacial, pero en realidad _somos libres de elegir el sistema de coordenas que queramos y obtendremos los mismos resultados_[^3].

## Segunda Ley 
> El cambio de movimiento es directamente proporcional a la fuerza motriz impresa y ocurre según la línea recta a lo largo de la cual aquella fuerza se imprime.

Veamos ahora que ocurre cuando al corredor este ya no está "aislado" de entidades exteriores. Supongamos que empujamos al corredor con una banda elástica, el mismo empieza a moverse. Si movemos nuestra mano de tal manera que el estiramiento de la bandita elástica sea constante, veremos que el corredor se mueve de una manera muy simple, su velocidad aumenta con el tiempo de manera uniforme. Tiene una _aceleración constante_. 
![[Pasted image 20220915185009.png]]
Pero luego, si cambiamos el corredor por uno más grande que el anterior y le aplicamos el mismo empuje con la bandita, observaremos que este también tendrá un cambio en su velocidad, pero este será _menor_ que en el caso anterior. Parece ser que la aceleración no depende únicamente de lo que le hagamos al cuerpo, sino también de algo más, una propiedad de los cuerpos a la que llamamos **masa inercial**.

### Masa inercial
Vamos a usar nuestro experimento de la banda elástica para _definir_ a que nos referimos con masa. Empezaremos dicendo arbitrariamente del primer corredor al que le realizamos el experimento tiene una masa $m_1$. Definimos a $m_1$ como una unidad de masa. Entonces, podemos definir a la masa de un segundo corredor (más grande o más chico) como $m_2 \equiv m_1 \frac{a_1}{a_2}$ , donde $a_1$ es la aceleración que tiene el cuerpo 1 y $a_2$ es la aceleración que tiene el cuerpo 2. Podemos repetir este proceso varias veces con la cantidad de cuerpos que queramos, tal que podemos definir la masa de cualquier cuerpo. 
Nos podemos preguntar _¿Podría yo entonces definir propiedades aleatorias del cuerpo como por ejemplo $Z_2 \equiv Z_1(a_1/a_2)^2$?_ La respuesta es sí pero veremos que la propiedad Z, a diferencia de la masa, no es útil en nada.

Si repetimos este experimento cambiando las aceleraciónes que les producimos a los cuerpos, las masas de los cuerpos no cambian, se mantienen constantes. La masa definida de esta manera **termina siendo independiente de la aceleración que tenga el cuerpo, tal que es una propiedad inherente del mismo**. Obviamente, el valor númerico de la masa depende de que determinemos como una unidad de masa. En el sistema MKS se mide con $kg$ kilogramos, mientras que en el CGS se mide en $g$ gramos.

Nuestra definición de la masa es un ejemplo de lo que se suele llamar _definición operacional_. Con _operacional_ nos referimos a que la definición se saca a través de experimentos que realizamos y no en terminos de conceptos abstractos o matemáticos, como por ejemplo otra definición que podemos dar de masa es "la masa inercial es la resistencia de los cuerpos al cambio del movimiento". 

### Fuerzas
Una definición abstracta que se suele dar de fuerza _"es toda acción que se le puede aplicar a un cuerpo"_. Sin embargo, podemos definirlas operacionalmente. Cuando aplicamos una "fuerza" sobre un corredor en el experimento anterior representada por "el empuje que hace la banda elástica", la masa medida acelera con una razón $a$. Luego, si aplicamos dos fuerzas iguales sobre dos bandas elásticas que están unidas al cuerpo, desde el mismo lado, encontraremos que la aceleración generada es de $2a$, y si aplicamos las fuerzas en lados opuestos, la aceleración es cero. Esto nos hace concluir que las fuerzas tienen un **sentido** y que se suman algebraicamente para obtener la aceleración. 
Dependiendo la fuerza que apliquemos, tendremos una aceleración diferente. De nuestra definición de masa, la fuerza produce $F \times (1/m)$ unidades de aceleración cuando actua sobre una masa $m$. Entonces, la aceleración producida por la fuerza $F$ es $a=F/m$ (o en un orden más familiar). La unidad general de las fuerzas en el MKS es $[N] = \frac{kg \cdot m}{s^2}$ Newtons. 
Es natural asumir que para el movimiento en 3 dimensiones, las fuerzas se comportan como **vectores**. La suma vectorial de todas las fuerzas que actuan sobre un cuerpo nos da la aceración del cuerpo, esta se conoce como la **segunda ley de Newton**: 
$$\sum_{i}^N \vec{F_i} = m\vec{a}$$
Siendo que se aplican $N$ fuerzas sobre el cuerpo. 
Es importante recalcar que las aceleraciones **no siempre son causadas por fuerzas**  pues para que haya una fuerza es necesaria una interacción entre cuerpos. También que si un cuerpo, que no está aislado, está en reposo **no quiere significar que no tiene fuerzas actuando** solo que estás fuerzas al sumarlas vectorialmente dan 0.
De esta ley podemos predecir el movimiento de cualquier cuerpo sabiendo que fuerzas actuan sobre él, como veremos en [[Aplicando las leyes de Newton]].

### Sistemas inerciales y sistemas no inerciales
Para nosotros poder medir el movimiento del rider es necesario verlo desde un sistema de coordenadas que se "mueve uniformemente" alrededor del rider, es decir o bien no se mueve o lo hace con velocidad constante, tales sistemas se llaman **sistemas inerciales**.  
No todos los sistemas de coordenadas son inerciales. Por ejemplo supongamos que el rider se mueve con velocidad constante, visto de un sistema de coordenadas que está acelerando con respecto al air track, la velocidad del corredor parecería _cambiar con respecto al tiempo_ pero esto es imposible. En este caso ya no valdrían las leyes de Newton pues, como vimos en la segunda ley las aceleraciones aparecen en consecuencia de una fuerza, pero no hay fuerzas actuando sobre el corredor, entonces la sumatoria de fuerzas nos quedaría $\sum_{i=1}^N  \vec{F}_i = 0 = m\vec{a}$ lo cual es imposible.
Podríamos decir que una consecuencia de la primera ley de Newton es que siempre se puede encontrar un sistema de coordenadas en donde el cuerpo se mueve uniformemente. 

> Existen sistemas de referencia (los sistemas inerciales) en los cuales se cumple que todo cuerpo persevera en su estado de reposo o movimiento uniforme y rectilíneo a no ser que sea obligado a cambiar su estado por fuerzas impresas sobre él.

## Tercera Ley - Acción-Reacción
> Con toda acción ocurre siempre una reacción igual y contraria: quiere decir que las acciones mutuas de dos cuerpos siempre son iguales y dirigidas en sentido opuesto.

La tercera del de Newton nos dice que **siempre** las fuerzas vienen en pares que son iguales en magnitud pero opuestas en sentido: si el cuerpo $b$ le ejerce una fuerza $\vec{F}_a$ al cuerpo $a$, entonces el cuerpo $a$ le debe hacer una fuerza $\vec{F}_b$ al cuerpo $b$, tal que $\vec{F}_a = -\vec{F}_b$. _Nunca hay una fuerza sin su pareja_. Veremos luego en [[Momento Lineal]] que esta ley nos dirige diretamente a una de las 3 leyes de conservación[^4] que veremos en Física General I, que es la ley de conservación del momento lineal. 
Notemos que las fuerzas pares actuan en **cuerpos diferentes**, es decir que cuando hacemos las sumatoria de fuerzas para el cuerpo $a$ ponemos solo $F_b$ y no $F_a$, un error muy común es pensar que las fuerzas "se cancelan" (y por lo tanto el cuerpo no tiene una aceleración) lo cual es un error.

---
## Resolución del problema inicial
La segunda ley de Newton $\vec{F} = m\vec{a}$ se mantiene solo en sistemas inerciales. El concepto de sistemas inerciales parece raro y arbitrario, pero la realidad es que no hay nada de arbitrario en este concepto y el problema nos ayuda a entender porque. 

Resulta que Abril calcula la aceleración del trasbordador espacial como $a_A = 1000  \; \text{m/s}^2$. Ella llega a la conclusión que el motor del trasbordador está haciendo una fuerza para causar que este se mueva, entonces podemos escribir:
$$\begin{align}
F_A & = M_sa_A \\
& = 1000 \; [\mathrm{m/s}^2] \times M_s \;[\mathrm{kg}]
\end{align}$$
Siendo $M_s$ la masa del trasbordador.
Mientras que Bruno sigue el mismo procedimiento que Abril y calcula la aceleración como $950 \; \mathrm{m/s}^2$. El desacuerdo es serio porque entonces obtenemos que la fuerza $F_A$ tiene dos valores diferentes, y esto es imposible, al menos uno de los valores debe ser erroneo. 

Afortunadamente, Abril y Bruno son físicos y saben que la segunda ley de Newton solo funciona para sistemas inerciales pero ¿Cómo pueden saber si su nave es un sistema inercial? La comandante Abril se le ocurre la idea de hacer un experimento al que ella denomina "prueba del alfajor", que consiste en que cuidadosamente dejar un alfajor en el vacío desde su nave, al hacer esto observa que este flota al frente suyo sin movimiento, lo cual le hace concluir que su nave es un sistema inercial. El argumento es el siguiente: mientras Abril sostenga el alfajor, este debe tener la misma velocidad instantanea y aceleración que la nave, pero en el momento en que ella lo suelta, ya no actuan fuerzas sobre el alfajor y representa un cuerpo aislado. Si la nave espacial estuviera acelerando entonces el alfajor parecería tener una aceleración relativa "igual y opuesta" en la perspectiva de la nave. Como esto no ocurre, entonces la nave no está acelerando. 

La medición de Abril debe ser correcta pues ella está en un sistema inercial. Pero, ¿Qué podemos decir de las mediciones de Bruno? Para responder esta pregunta, miremos la relación entre $x_A$ y $x_B$. 
![[Pasted image 20220915195853.png]]
Donde $X(t)$ es la posición relativa entre las naves (recordemos [[Movimiento Relativo]]). 
$$x_A(t) = x_B(t) + X(t)$$
Derivando 2 veces con respecto al tiempo tenemos:
$$\ddot{x}_A(t) = \ddot{x}_B(t) + \ddot{X}(t) \quad (1)$$
Como el sistema de la nave $A$ es inercial, entonces se tiene que cumplir $F_{\text{verdadera}} = M_s \ddot{x}_A$. La fuerza aparente que mide el sistema $B$ es $F_{\text{B, aparente}} = M_s \ddot{x}_B$. Usando los resultados de la ecuación (1) tenemos $F_{\text{B, aparente}} = M_s \ddot{x}_A - M_s \ddot{X}$. Entonces, Bruno puede medir la fuerza real solo si $\ddot{X}= 0$, es decir, si la nave B no se está acelerando con respecto de la nave A. Bruno sospecha que capaz este no es el caso y realiza la "prueba del alfajor". La prueba revela que el alfajor no se mantiene en reposo o velocidad constante, por lo tanto Bruno está en un sistema no inercial. Una revisión en la nave revela que uno de los motores quedó prendido accidentalmente, causando una aceleración de $50 \; \mathrm{m/s}^2$. Una vez que Bruno apaga el motor y vuelve a hacer las mismas mediciones, obtiene que efectivamente la aceleración del trasbordador es $1000 \; \mathrm{m/s}^2$. 
Y en todo el tiempo en el que se tardaron en realizar estas mediciones, el trasbordador espacial ya estaba en la concha de la lora. 

---
Como resultado de trabajar en sistemas no inerciales aparecen lo que suele llamar "fuerzas ficticias" que no existen realmente (recuerde de que a pesar que las llamamos "fuerzas" no lo son, pues no existe una interacción con ningún cuerpo que la cause). La fuerza ficticia en el ejemplo anterior que surge de que Bruno no está en un sistema inercial es de $F_{ficticia} = M_s (50 \; \mathrm{m/s}^2)$ y que por lo calculado anteriormente $F_{\text{verdadera}} = F_{\text{B,aparente}} + F_{\text{ficticia}} = M_s (950 \; \mathrm{m/s}^2) + M_s (50 \mathrm{m/s}^2) = M_s(1000 \; \mathrm{m/s}^2)$.  
Otro ejemplo de estas fuerzas ficticias que suelen aparecer es la **fuerza centrífuga** que lo vemos en [[Fuerzas Elásticas y Movimiento Armónico Simple]].


[^1]: El punto simboliza "la derivada con respecto al tiempo", es decir $v_A(t) = dx_A(t)/dt$. Esta notación empezó a ser utilizada por Newton. 
[^2]: Llamamos a un sistema aislado a aquellos cuerpo a los cuales no afectan "fuerzas externas" como la gravedad o la fricción, solo las que se producen entre sí.
[^3]: Sin embargo, hay algunos sistemas que son más convenientes de usar que otros.
[^4]: En general, hay 6 leyes importantes que usted tiene que aprender de FG1, 3 de ellas son leyes de conservación y las otras 3 son las leyes de Newton.






