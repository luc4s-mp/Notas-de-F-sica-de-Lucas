# ¿Cómo calculamos el dominio de una función?
Para calcular el dominio de una función, debemos tener en cuenta el dominio que posee por defecto una función en R.
$$Img(f) = \{f(x) : a \in Dom(f) \}$$
Muchas veces, el domino no suele estar por deferecto, sino que **restrigido**. Es decir, existen puntos para $\mathbb{R}$ que no existen en la función y debemos extraerlos.
## Dominio de funciones polinomincas
Las funciones polinómicas suelen tener un dominio siempre en $\mathbb{R}$.

--- 
## Dominio de funciones racionales
En las funciones racionales debemos tener en cuenta que dividir por 0 está indefinido. Entonces puediendo escribir a las funciones racionales como: $\frac{P(x)}{Q(x)}$ (el cociente de dos polinomios), el dominio está dado por:
$$f(x) = \frac{P(x)}{Q(x)} \implies Q(x) \neq 0 \wedge Dom(f): \mathbb{R} - \{Ceros(Q)\}$$
## Dominio de funciones radicales
En las funciones radicales debemos tener en cuanta que la raíz par de un número debe ser siempre positiva, ya que las raíces par de números negativos no están definidas en $\mathbb{R}$, entonces:
$$f(x) = \sqrt[n]{x}, \forall n\mod(2) = 0 \implies x \geq 0 \wedge Dom(f): {intervalo \space en \space el \space que \space x \geq 0}$$

---
## Dominio de funciones trigonométricas
En las funciones trigonométricas normalemente el dominio son todos los $\mathbb R$.
## Dominio de funciones logaritmicas
En las funciones logarítmicas debemos tener en cuanta la indeterminación $\log{0}$ y el logaritmo de un número negativo (ambos están indefinidos). Entonces, podemos decir que su dominio es:
$$f(x) = \log_{n} x \implies x > 0 \wedge Dom(f): [0, \infty)$$
## Dominio de funciones exponenciales
Las funciones exponenciales están definidas para todos los números reales $\mathbb R$.

#Primer-año 
#Matemática 