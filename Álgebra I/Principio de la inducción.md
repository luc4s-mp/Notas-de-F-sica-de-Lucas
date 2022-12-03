# Principio de la inducción
## Problema Inicial - La suma de Gauss
El profesor de matemáticas de Gauss un día vío que este ya habia terminado todo su trabajo en la clase, y el joven se resistía a quedarse quieto. Entonces, para que este se distrajera, el profesor le dijo que sumanara los primeros 100 números naturales. 
Sin embargo, su intento fue en vano porque Gauss no tardó más que unos pocos segundos en decir la respuesta, $5050$! _¿Cómo lo hizo?_ 

Al final de esta lección probaremos como para ver como avanzamos en nuestro entendimiento. 

## El principio básico
La idea central detras de la inducción es de poder mostrar la validez de cada enunciado de la lista usando la validez del anterior. Así, sólo basta disparar el proceso en el punto de partida para desencadnar una reacción en cadena que probará la validez de todos los enunciados. Se suele comparar al principio de inducción con "una pila de dominos cayendo", si podemos hacer caer el primero, entonces podemos hacer caer todos.
Cada vez que nos encontremos que queremos probar una lista de enunciados son verdad (se parte del enunciado 1, luego el enunciado 2 y así) podemos utilizar el principio de inducción. 

Sin saberlo ya hicimos una prueba por en inducción en [[N]] cuando probamos que todo número natural es positivo. Este teorema se basó en el tercero de los axiomas de peano y este es el que nos permite formular el siguiente teorema.

> #Definición **Principio de Inducción.** Sea $P(n)$ una propiedad enunciada para $n \in \mathbb{N}$ supongamos que se cumple que 
> 1.  **(Caso Base)** $P(1)$ es verdadero. 
> 2. **(Paso inductivo)** $\forall  k \in \mathbb{N}, P(k)$ es verdadera, implica que $P(k+1)$ es verdadera. Entonces, $P(n)$ es verdadera para $\forall n \in \mathbb{N}$. 

**Demostración.** Consideremos el conjunto
$$H = \{n \in \mathbb{N} : P(n) \text{ es verdadera}\}$$
Por definición, $H \subseteq \mathbb{N}$. Basta probar que $H$ satisface el axioma N°3 (o de otra forma es uno de los "[[Conjuntos]] Inductivos") y así $H = \mathbb{N}$, y de esta manera probamos que la proposición $P(n)$ es verdadera para todo $n \in \mathbb{N}$. Ahora, 
1. $1 \in H$, pues $P(1)$ es verdadera por hipótesis.
2. Si $k \in H$, es decir $P(k)$ es verdadera, entonces de la segunda hipótesis se sigue que $P(k+1)$ es verdadera y por lo tanto $k+1 \in H$.
Luego $H = \mathbb{N}$ como queríamos ver. $\blacksquare$

Sin el principio de inducción, para probar tal cosa, habría que encontrar una demostración para cada enunciado, y al haber infinitos enunciados esta tarea se hace (literalmente) interminable.

---

### No cometas estos errores en la inducción
En las pruebas por inducción, es impresindible llevar a cabo la prueba del paso inicial y la prueba del paso inductivo. Hay que tener cuidado, no porque el caso $P(1)$ sea verdadero no significa que el paso inductivo se cumpla y viceversa.
Por ejemplo, la proposición $P(n) \; : \; n^2 = n^3 \text{ para todo } n \in \mathbb{N}$ es claramente falsa pero para $P(1) : 1^2 = 1^3$ funciona, pero el paso inductivo no. O para la proposición 
$$R(n) : 1+2+3+ \dots + n = \frac{1}{8}(2n+1)^2$$
Si nos salteamos el caso base y pasamos el paso inductivo, supongamos que $P(k)$ vale para $k \in \mathbb{N}$ y veamos que $P(k+1)$ vale. Por hipótesis inductiva (así le decimos a $P(k)$):
$$1+2+3+\dots + k + (k+1) = \frac{1}{8}(2k + 1)^2 + (k+1)$$
Queremos ver que
$$\frac{1}{8}(2k+1)^2 + (k+1) = \frac{1}{8}(2(k+1)+1)^2$$
Ahora, $\frac{1}{8} (2k+1)^2 + (k+1) = \frac{1}{8}(4k^2 + 4k + 1) + (k+1) = \frac{1}{8}(4k^2 + 12k + 9)$ y $\frac{1}{8}(2(k+1)+1)^2 = \frac{1}{8}(2k+3)^2 = \frac{1}{8}(4k^2 + 12k + 9)$. Por lo que probamos el paso inductivo.
Sin embargo $P(1)$ no es verdadera, porque $P(1) : 1 \neq \frac{1}{8}(2(1)+1)^2 = \frac{9}{8}$ . 

> **Claves de la Inducción**
> 1. Simpre realizar el caso base.
> 2. Podemos empezar con la hipótesis inductiva (HI) y llegar a lo que queremos probar o incluso podemos empezar de los que queremos probar, pero siempre tenemos que usar HI en algún momento.


### Teorema (Principio de Inducción "corrida")
Este teorema se utiliza cuando tenemos que una proposición no funciona para *todos* los números naturales, sino a partir de un cierto número.  
> Sea $n_0 \in \mathbb{Z}$ y sea $P(n)$, $n \geq n_0$, una afirmación sobre $\mathbb{Z}_{\geq n_0}$. Si P satisface: 
	> -  **(Caso Base)** $P(n_0)$ es verdadera
	> - **(Paso Inductivo)** $\forall h \geq n_0$, P(h) Verdadera $\implies P(h+1)$ Verdadera, entonces P(h) es Verdadero, $\forall n \in \mathbb{N}$

**Demostración.** Sea el conjunto $H = \{n \in \mathbb{N}: P(n + n_0 -1) \text{ es verdadera}\}$. Vemos que $H = \mathbb{N}$ , es decir cumple el axioma N°3 (o la definición un conjunto inductivo):
1. $n = 1, \; P(1+n_0 -1) = P(n_0) \iff 1 \in H$ es verdadera.
2. Sea $h \in H$, por el principio de la inducción debemos comprobar que $P(h + N +1)$ es verdadera, asumimos que lo es y vemos que $h +1 \in H$. Queremos ver que $P(h+1 + n_0-1)$ es verdadera: $h+1 + n_0-1 = h +n_0$. Por lo tanto, $P(h + n_0)$ es verdadera $\implies P(h + h_0 -1)$ es verdadera.
De esta forma, queda demostrada la proposición inicial.

---

## La suma de Gauss - Resolución
Veamos que podemos resolver la suma de gauss para la suma no solo para todos los números naturales hasta 100, sino que para cualquier $n$ que queramos usando **inducción**. 
En realidad gauss no usó inducción, él usó un método bastante elegante, e incluso usted podrá considerar más bonito que la inducción. El le designó a la suma de los 100 primeros números el valor $S$ y luego volvió a sumar $S$ pero ahora las números están ordenados "al revés" y se dió cuenta lo siguiente:
![[Pasted image 20220630110742.png]]
Luego, $2S = 100 \cdot 101 \Rightarrow S = (100 \cdot 101)/2 = 5050$!!!  
Entonces, esto lo podemos generalizar de la siguiente manera:
$$P(n): \forall n \in \mathbb{N}, \;\; 1+2+\dots+ (n-1) + n = \frac{n(n+1)}{2}$$
Pero, ¿Cómo sabemos que esta fórmula funciona para cualquier número $n$? Podemos probarlo usando inducción:
- **Caso Base**: $P(1) : (1(1+1))/2 = 2/2 = 1$ , entonces $P(1)$ es verdadera.
- **Paso Inductivo**: Asumimos $P(k) : 1+2+ \dots + k = (k(k+1)/2$ verdadera y queremos demostrar que $P(k+1)$ verdadera también.
	Por hipótesis inductiva sabemos $$1+2+\dots + k + (k+1) \underset{(HI)}{=} \frac{k(k+1)}{2} + (k+1)$$
	Entonces, se tiene que cumplir que
	$$(k+1)+\frac{k(k+1)}{2} = \frac{(k+1)((k+1)+1)}2$$
	Lo cual es verdad pues $\frac{k(k+1)}{2} + (k+1) = \frac{k(k+1) + 2(k+1)}2 = \frac{k^2 + k + 2k + 2}{2} = \frac{k^2 + 3k +2}{2}$ 
	y $\frac{(k+1)(k+2)}{2} = \frac{k^2 + 3k + 2}{2}$ . Por lo que $k+1 \in \mathbb{N}$ y $P(n)$ es verdadero para todo $n \in \mathbb{N}$. $\blacksquare$  

Notemos que para que pudieramos probar que esta propiedad es verdadera, necesitabamos saber la formula $n(n+1)/2$ de antemano. Esto es lo malo de la inducción, y ¿Cómo hacemos para obtener esta formula? se preguntará, pues básicamente como lo hizo gauss, mirando como actua la propiedad y luego nos aseguramos que esta funciona usando inducción. 

---
 