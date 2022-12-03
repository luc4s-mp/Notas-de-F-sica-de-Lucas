# Ecuaciones Cinemáticas
Estas ecuaciones aparecen en casos especiales muy comúnes en los problemas de física.

## ¿Qué ocurre cuando la rapidez es constante?
La función de la rapidez se va a ver como $v(t) = v$. Notemos que al derivar la función posición obtenemos la función rapidez y al derivar esta última obtenemos la función aceleración. Sabemos que la derivada de una constante es 0, por lo tanto $a(t) = 0$ lo cual era obvio ya que si la velocidad no cambia entonces la acelaración es 0. Ahora para encontrar la función posición necesitamos de la [[Integración]]:
$$\frac{\mathrm{d}x(t)}{\mathrm{d}t} = v(t) \implies \int v(t) \mathrm{d}t = x(t) \implies x(t) = \int v(t) \mathrm{d}t = vt + v_0$$
Siendo $v_0$ una constante que surge de la integración la cual llamaremos *velocidad inicial* ya que si $t = 0$ entonces $v(0 \text{ s}) = v_0$. 

## ¿Qué ocurre cuando la aceleración es constante?
La función aceleración va a ser $a(t) = a$. Ahora, para obtener la función velocidad y la función posición necesitamos integrar la misma. 
$$v(t) = \int a(t) \mathrm{d}t = at + v_0$$
$$x(t) = \int v(t) \mathrm{d}t = \iint a(t) \mathrm{d}t = x_0 + v_0t + \frac{1}{2}at^2$$
Notemos que $x_0$ y $v_0$ son la posición inicial y la velocidad inicial de la partícula, constantes que se obtienen al integrar. Aquí tenemos dos de las ecuaciones cinemáticas más importantes, pero requerimos de una más para situaciones en las cuales el tiempo sea un elemento no relevante. Para poder encontrar esta ecuación de la ecuación (1) vamos a despejar $t$ de tal manera que nos queda: $t = \frac{v - v_0}{a}$. A esta misma la reemplazamos en la ecuación (2) y obtenemos:
$$v_f^2 = v_0^2 + 2a \Delta x$$
También podemos encontrar esta ecuación usando los conocimienos del análisis matemático.
#Primer-año #Física 