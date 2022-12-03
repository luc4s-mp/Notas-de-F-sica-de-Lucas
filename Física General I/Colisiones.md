# Colisiones
Aplicaremos los conceptos aprendidos en [[Momento Lineal]] y [[Dinámica y leyes De Newton]] para entender que ocurre cuando dos cuerpos yendo a velocidades distintas chocan. No nos va a importar el momento exacto de la colisión, debido a que ocurren una serie de reacciones complicadas de entender. Vamos a analizar lo que ocurre antes y después de la misma.

## Choques Inelásticos o plásticos
Supongamos que tenemos la siguiente situación:
Un cuerpo 1 se está moviendo a una velocidad $v_{1i}$ miestras que un cuerpo 2 está en reposo $v_{2i} = 0$, en un instante dado estos dos chocan "pegandose" y yendo a la misma velocidad $v_f$ . 
![[Pasted image 20220424181507.png]]
Como es un problema en una dimensión vamos a tratar unicamente con la componente horizontal del momento lineal $P_{x,i} = P_{x,f}$ , siendo $P_{x, i}$ es el momento lineal del sistema antes del choque y $P_{x, f}$ es el momento lineal después del choque. Notemos que sabemos que el momento lineal se conserva porque las únicas fuerzas que existen son interiores.
Supongamos que sabemos que la masa del cuerpo 1, $m_1$, y la masa del cuerpo 2, $m_2$, son iguales. Entonces,
$$\begin{align}
\vec{P_i} & = \vec{P_f} \\
P_{i,x} & = P_{f,x} \\
m_1 v_{1i} + 0 & = (m_1 + m_2) v_f \\
v_f & = \frac{m_1}{m_1 + m_2} v_{1i} \\
& = \frac{m_1}{2m_1} v_{1i} \\
& = \frac{1}{2}v_{1i}
\end{align}$$
Este resultado parece obvio a simple vista, si ambos cuerpos con una misma masa chocan y siguen en una misma velocidad unidos, la velocidad que tienen después del choque va a ser la mitad de la inicial. Y podemos probar esto para masas diferentes, por ejemplo si $m_1 = 2 m_2$ entonces la velocidad obtenida después del choque es $\frac{2}{3}v_{1i}$ .

*Esta técnica de encontrar la velocidad evade totalmente preguntarnos cuanto tiempo tomo la colisión o cuanta fuerza actuó, lo cual nos evita entrar en ciertos problemas.*

Analicemos que ocurre en las colisiones con respecto a la [[Energía]] ¿Se conserva en este caso al igual que el momento lineal? Para que esto suceda es necesario que la energía cinética antes de la colisión $K_i$ sea igual a la energía cinética después de la colisión $K_f$. 
Para que esto ocurra tiene que pasar que $\Delta K = K_i - K_f = 0$. Por lo tanto
$$\begin{align}
K_i - K_f = \frac{1}{2}2m_1v_{i1}^2 - \frac{1}{2}2m_1v_f^2 & = m_1v_{i1}^2 + m_1 \Big(\frac{1}{2}v_{i1} \Big)^2 \\ 
& = m_1v_{i1}^2 - \frac{1}{4}m_1v_{i1}^2 \\
& \neq 0
\end{align}$$
 Sin embargo, si analizamos detenidamente el sistema resulta que la energía mecánica sí se conserva. Lo que está ocurriendo aquí es que al colisionar dos objetos un poco de energía cinética se pierde en **calor o sonido**. Entonces, $K_i = K_f + {\text{calor}}$.  

Concluimos entonces que *la energía cinética no se conserva en una colisión, se pierde un poco de ella en sonido o calor, pero la energía mecánica sí se conserva*. 

Podemos distinguir entonces dos tipos de colisiones, **elásticas** en las cuales la enegía cinética no cambia ($\Delta K = 0$) o **inelásticas o plásticas** en las cuales sí cambia ($\Delta K \neq 0$). Este tipo de colisiones en las cuales los objetos se "pegan" y se mueven juntos a la misma velocidad se suelen llamar **perfectamente inelásticos**. 
En los choques perfectamente inelásticos ocurre que $\vec{v}_{f1} = \vec{v}_{f2} = \vec{v}_f$ .

## Choques elásticos
Supongamos una nueva situación en la cuál dos cuerpos de masa $m_1$ y $m_2$  chocan en un momento dado del tiempo y chocan de manera tal que al principio el cuerpo 1 tenia una velocidad $v_{1i}$ y cuando choca se la "tranfiere" al cuerpo dos que estaba en reposo $v_{2i} = 0$, tal que ahora el cuerpo 1 está en reposo $v_{1f} = 0$ y el cuerpo 2 tiene una velocidad $v_{2f}$ .


#Física #Primer-año 