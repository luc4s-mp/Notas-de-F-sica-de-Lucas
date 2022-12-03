# Derivada puntal de una función
#Definición Sea $f$ un de las [[Funciones en R]] y $x_0 \in Dom(f)$. Si existe un intervalo $(a, b)$ tal que $x_0 \in (a, b) \subset Dom(f)$, para definir la derivada vamos a utilizar el [[Límite finito de Funciones]], diremos que $f$ es derivable en $x_0$ si
$$\lim_{h \rightarrow 0} \frac{f(x_0 + h) - f(x_0)}{h} \in \mathbb{R}$$
O equivalentemente si 
$$\lim_{x \rightarrow x_0} \frac{f(x)-f(x_0)}{x - x_0} \in \mathbb{R}$$
Si alguno de los límites en (1) o (2) existe, entonces existe el otro y son iguales entre ellos, se puede verificar haciendo $h = x -x_0$. Si alguno de los límites no existe, diremos que $f$ *no es derivable $x_0$*. Si una función es derivable en $x_0$ la denotamos $f'(x_0)$.

---

## Interpretación gráfica de la derivada
![[Pasted image 20211215234012.png]]
$f'(x)$ es la pendiente de la recta tangente de $f$ en el punto $x_0$ y tal recta tangente está dada por la fórmula
$$T(x) = f'(x_0)(x-x_0) + f(x_0)$$
$f'(x)$ es la pendiente y $[f(x_0)-f'(x_0) \cdot x_0]$ es la ordenada al origen. 
Podemos definir también a la recta normal $N(x)$ de $f$ en el punto $x_0$, como la recta perpendicular a $T(x)$ que pase por el punto $(x_0, f(x_0))$. Esto es
$$N(x) = \frac{-1}{f(x_0)}(x-x_0) + f(x_0)$$

---

### Teorema. "Diferenciabilidad implica continuidad"
> Si una función $f$ es derivabl en un punto $x_0$, entonces $f$ es continua en $x_0$.

El teorema presentado muestra una relación directa entre los conceptos de **continuidad** y **diferenciabilidad** de una función. 

---

#### Demostración
Notemos que
![[Pasted image 20211216002851.png]]
Luego, $\lim_{x \rightarrow x_0} f(x) = f(x_0)$, es decir, $f$ es continua en $x_0$.

---

Las operaciones de derivadas 




#Matemática #Primer-año 