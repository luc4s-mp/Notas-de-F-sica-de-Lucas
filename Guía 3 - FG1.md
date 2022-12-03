# Guía 3 - Física General

## Problema 5
En un modelo simplificado se puede suponer que, como consecuencia de la fuerza de atracción gravitatoria, la tierra describe una órbita circular alrededor del sol, que permanece fijo en el espacio.
1. Utilizando un sistema de coordenadas polares con origen en el centro del sol, dé una expresión para la fuerza $F_{TS}$  que experimenta la tierra como consecuencia de la presencia del sol.
2. Sabiendo que la distancia Tierra-Sol es de $1,4957 \times 10^8$ km, que la masa del sol es $1,991 \times 10^{30}$ kg y que la masa de la tierra es de $5,974 \times 10^{24}$ kg, calcule el módulo de $F_{TS}$ .
3. Si el período de revolución de la tierra alrededor del sol es de $T = 365,2564$ días, calcule la aceleración centrípeta de la tierra, en un sistema de coordenadas polares semejante al utilizado en  (1).

### Resolución
**IDENTIFICAR**: Buscamos primero un sistema de coordenadas polares que nos describa la expresión para la fuerza $\vec{F}_{TS}$ que por la tercera ley de Newton sabemos que $F_{ST} = - F_{TS}$.  Luego, nos piden calcular su módulo para lo cuál utilizaremos la ley de gravitación $F_g = G\frac{mM}{r^2}$  y por último nos dan el periódo de una revolución de la tierra para calcular la aceleración centripeta que sabemos por el movimiento circular que es $\vec{a} = -R \omega^2 \cdot \hat{u}_{\rho} (t)$ y su modulo se puede calcular como $a = \frac{v^2}{R}$.  

**PLANTEAR**: Planteemos el sistema de coordenadas con centro en el sol.
![[Pasted image 20220409190834.png | 350]]
**EJECUTAR**: Teniendo en cuenta que $F_{ST} = F_{TS} = F_T$ y el sistema de coordenadas polares podemos expresar al vector $\vec{F}_{TS} = -F_T \cdot \hat{u}_{\rho} = - \frac{G M_S M_T}{r^2} \hat{u}_{\rho}$  utilizando la ley de gravitación. (Fin del Apartado 1). 
$$\begin{align}
|\vec{F}_{TS}| & =  \frac{6,672 \times 10^{-11} \text{Nm}^2 / \text{kg}^2 \cdot 1,991 \times 10^{30} \text{ kg} \cdot 5,974 \times 10^{24} \text{ kg}}{(1,4957 \times 10^8 \text{ km})^2}  \\
& = \frac{79,358 \times 10^{43}}{2,237 \times 10^{16}} N \\
& = 3,547 \times 10^{28} N
\end{align}$$
(Fin del Apartado 2)
Por último, yo sé que la formula para calcular la velocidad angular es $v = \frac{2\pi R}{T}$, entonces sabiendo que $T = 365,2564 \text{ dias} = 31588153 \text{ s} = 3,15 \times 10^7 \text{ s}$,  $v = \frac{2\pi \cdot (6,371 \times 10^6)}{3,15 \times 10^{7}} \frac{\text{rad}}{\text{s}} = 1,27 \frac{\text{m}}{\text{s}}$. Y el módulo de la aceleración $a = \frac{v^2}{R} = \frac{{1,262}^2}{6,371 \times 10^6} \frac{\text{m}}{\text{s}} = 12678,29 \frac{\text{m}}{\text{s}}$.  

## Problema 7
Un resorte de constante elástica $k$  tiene uno de sus extremos fijo y el otro coincide con el punto de coordenadas $x_0$, cuando no está deformado. A este extremo, se adhiere una masa $m$ que se desplaza hasta la coordena $x_1$, donde se la suelta. 
1. Determina las funciones $x(t)$, $v(t)$ y $a(t)$ y grafiquelas.
2. Calcule el período, la frecuencia, las coordenadas extremas del movimiento y el módulo de la velocidad de la masa $m$, en el punto de equilibrio. Suponga que $k = 8$ N/m, $m = 2$ kg, $x_0 = 40$ cm y $x_1 = 50$ cm.

### Resolución
**IDENTIFICAR**: 