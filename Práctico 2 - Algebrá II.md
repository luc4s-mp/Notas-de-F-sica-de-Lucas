# Sistemas de Ecuaciones 
##  Ejercicio 8
Determinar todos los valores posibles de $a \in \mathbb{R}$ para los cuales el sistema 
$$\begin{cases}
x_1 + x_2 -x_3 + 2x_4 = a \\
2x_1 + x_2 +x_3 + x_4 = 1 \\
3x_1 + 2x_2 + 0x_3 + 3x_4 = 0 \\
x_1 -x_2 + x_3 + 2x_4 = 1 \\
\end{cases}
\quad \rightarrow \quad 
\left( \; \begin{array}{cc}
1 & 1 & -1 & 2 & | & a \\
2 & 1 & 1 & 1 & | & 1 \\
3 & 2 & 0 & 3 & | & 0 \\
1 & -1 & 1 & 2 & | & 1 \\
\end{array} \; \right)$$
Podemos ver que si sumamos la primera fila con la segunda obtenemos la tercera, esto nos dice que podemos restar ambas y obtener una fila nula lo cual nos serviría para reslver nuestro problema.
$$\overrightarrow{F_1+ F_2} \quad \left( \; \begin{array}{cc}
3 & 2 & 0 & 3 & | & a+1 \\
2 & 1 & 1 & 1 & | & 1 \\
3 & 2 & 0 & 3 & | & 0 \\
1 & -1 & 1 & 2 & | & 1 \\
\end{array} \; \right) \quad \overrightarrow{F_1- F_3} \quad 
\left( \; \begin{array}{cc}
0 & 0 & 0 & 0 & | & a+1 \\
2 & 1 & 1 & 1 & | & 1 \\
3 & 2 & 0 & 3 & | & 0 \\
1 & -1 & 1 & 2 & | & 1 \\
\end{array} \; \right)$$
De esta manera, nos queda que $0x_1 + 0x_2 + 0x_3 + 0x_4 = a+1 \rightarrow 0 = a+1 \rightarrow a = -1$. Resolvamos ahora el sistema si $a= -1$, notemos que entonces nos queda una fila nula, la cual podemos eliminar y resolver el sistema de 3 ecuaciones equivalentes que nos quedaron.
$$\left( \; \begin{array}{cc}
2 & 1 & 1 & 1 & | & 1 \\
3 & 2 & 0 & 3 & | & 0 \\
1 & -1 & 1 & 2 & | & 1 \\
\end{array} \; \right) \quad \overrightarrow{F_1 \leftrightarrow F_3} \quad 
\left( \; \begin{array}{cc}
1 & -1 & 1 & 2 & | & 1 \\
3 & 2 & 0 & 3 & | & 0 \\
2 & 1 & 1 & 1 & | & 1 \\
\end{array} \; \right) \quad \overrightarrow{F_2 - 3F_1} \quad$$
$$\left( \; \begin{array}{cc}
1 & -1 & 1 & 2 & | & 1 \\
0 & 5 & -3 & -3 & | & -3 \\
2 & 1 & 1 & 1 & | & 1 \\
\end{array} \; \right) \quad \overrightarrow{F_2 - 2F_1} \quad
\left( \; \begin{array}{cc}
1 & -1 & 1 & 2 & | & 1 \\
0 & 5 & -3 & -3 & | & -3 \\
0 & 3 & -1 & -3 & | & -1 \\
\end{array} \; \right) \quad \overrightarrow{\frac{1}{5}F_2}$$
$$\left( \; \begin{array}{cc}
1 & -1 & 1 & 2 & | & 1 \\
0 & 1 & -3/5 & -3/5 & | & -3/5 \\
0 & 3 & -1 & -3 & | & -1 \\
\end{array} \; \right) \quad \overrightarrow{F_3 - 3F_2} \quad
\left( \; \begin{array}{cc}
1 & -1 & 1 & 2 & | & 1 \\
0 & 1 & -3/5 & -3/5 & | & -3/5 \\
0 & 0 & 4/5 & 6/5 & | & 4/5 \\
\end{array} \; \right)$$
Luego, $\frac{4}{5}x_3 + \frac{6}{5}x_4 = \frac{4}{5} \rightarrow x_3 = 1- \frac{3}{2}x_4$ . Reemplazamos esto en la 2da ecuación $x_2 + \frac{-3}{5}(1-\frac{3}{2}x_4) + \frac{-3}{5}x_4 = \frac{-3}{5} \rightarrow x_2 + \frac{9}{10}x_4 - \frac{3}{5}x_4 =$  