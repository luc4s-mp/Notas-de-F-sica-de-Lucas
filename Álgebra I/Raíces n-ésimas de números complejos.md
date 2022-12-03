# Potenciación en $\mathbb{C}$
#Definición Si $z \in \mathbb{C}, \; , \in \mathbb{N}$ ([[C]]) se define la potencia $n$-ésima de $z$ en forma recursiva:
- $z^1 = z$
- $z^{n+1} = z^n \cdot z$
- $z^0 = 1$

## Lema
> Sea $z, w \in \mathbb{C}$ y $n, m \in \mathbb{N} \cup \{0\}$:
> 1. $z^{n+m} = z^n \cdot z^m$
> 2. $(zw)^n = z^n \cdot w^n$
> 3. $(z^n)^m = z^{n \cdot m}$

### Proposición
> Sea $z \in \mathbb{C}-\{0\}, \; n \in \mathbb{N}, \; z = |z|e^{i \alpha}, \; \alpha = arg(z)$; entonces se cumple que
> 1. $z^n = |z|^n(\cos n\alpha + (\text{sen } n\alpha)i)$
> 2. $arg(z^n) = n \cdot arg(z) - 2\pi k, \; k \in \mathbb{Z}$ tal que $0 \leq n \cdot arg(z) - 2\pi k < 2 \pi k$, o sea $\frac{n \cdot arg(z)}{2 \pi} - 1 < k \leq \frac{n \cdot arg(z)}{2 \pi}$
> 3. $$arg(\overline{z}) = \begin{cases}
>   -arg(z) + 2\pi & \text{ si } \;\; arg(z) > 0 \\ 0 & \text{ si } \;\; arg(z) = 0
>   \end{cases}$$
>   4. $$arg(z^{-1}) = \begin{cases}
>   -arg(z) + 2\pi & \text{ si } \;\; arg(z) > 0 \\ 0 & \text{ si } \;\; arg(z) = 0
>   \end{cases}$$

#### Demostración
1. Aplicar el [[Principio de la inducción]] y la formula de De Moivre. 
2. $z^n = (|z|e^{i \alpha})^n \implies_{\text{por (1) }} |z|^n e^{in \alpha}$. Por lo visto en [[Forma Trigonométrica o polar de C]] se tiene que $n \alpha - arg(z^n) = 2k \pi$ para algún $k \in \mathbb{Z}$ y luego sale el $k$ del enunciado.
3. $arg(\bar{z}) = ?$. Si $z \in \mathbb{R}$, $arg(z) = 0 = arg(\bar{z})$
	Si $z \notin \mathbb{R} \implies \alpha = arg(z) \in (0, 2\pi)$.
	$0 < \alpha < 2\pi \implies -2\pi < -\alpha < 0 \implies 0 < -\alpha + 2\pi < 2\pi \implies -\alpha < 2\pi$
	$\implies -\alpha + 2\pi \in (0, 2\pi)$
Como $\cos (-\alpha +2\pi) = \cos(-\alpha)$ y $\text{sen } (-\alpha + 2\pi) = \text{sen } (-\alpha)$, entonces $\bar{z} = 1e^{-i \alpha} \implies arg(\bar{z}) = -\alpha + 2\pi$ 
4. $arg(z^{-1}) = arg(\bar{z})$ y sale el resultado.

---

## Las raíces $n$-ésimas de $\mathbb{C}$
Supongamos que queremos encontrarle solución a esta ecuación $w^n = z, \; n \in \mathbb{N}$. Si $z = 0 \implies w = 0$. Tomemos $z \in \mathbb{C}-\{0\}, \; n \in \mathbb{N}$ y queremos hallar $\{w \in \mathbb{C}: w^n = z\}$. Sea $\rho = |z| > 0$ y $\alpha = arg(z) \in [0, 2\pi)$, $w \neq 0$.
Como se tiene que cumplir $w^n = z \implies |w^n| = |z| \implies |w| = |z|^{1/n}$. Luego, $arg(w^n) = arg(z) \in [0, 2\pi) \implies n\cdot arg(w) - 2k\pi = arg(z)$. Despejamos $arg(w) = \frac{\alpha + 2\pi k}{n} \in [0, 2\pi) \implies 0 \leq \frac{\alpha + 2\pi k}{n} < 2\pi$. Entonces, sabiendo que $0 \leq \alpha < 2\pi$:
$$-1 < \frac{-\alpha}{2\pi} \leq k < n-\frac{\alpha}{2\pi}$$
Resumiendo, el conjunto solución de $w$ está formado por
$$\{w \in \mathbb{C}: w^n = z\} = \Bigg \{w \in \mathbb{C}: w = |z|^{1/n} \Bigg( \cos \Big(\frac{arg(z)+2\pi k}{n} \Big) + \text{sen } \Big( \frac{arg(z)+2\pi k}{n} \Big) \Bigg) \Bigg\}$$
De manera gráfica, las raíces se colocan en los vértices de un polígono regular de $n$ lados, siendo 1 uno de sus vértices. Se denominan *raícves $n$-ésimas de la unidad*. El conjunto $G_n$  tiene n elementos distintos de $\mathbb{C}$ que forman un $n$-ágono regular en la circunferencia unidad de un plano complejo.
$$G_n := \{w \in \mathbb{C}: w^n = 1\}, \; n \in \mathbb{N} = \{w_k = e^{\frac{2k \pi}{n} i}, \; 0 \leq k \leq n-1\} \subset \mathbb{C}$$

![[Pasted image 20211215194520.png]]
![[Pasted image 20211215195736.png]]

---

### Proposición
> Se cumplen las siguientes propiedades, $n \in \mathbb{N}$:
> 1. $m \in \mathbb{Z}$ y $z \in G_n$, $m = nq + r, \; 0 \leq r < n$
> 2. $z, w \in G_n \implies z \cdot w \in G_n$
> 3. $1 \in G_n$
> 4. $z \in G_n \implies \bar{z} \in G_n$
> 5. $z \in G_n \implies z^{-1} \in G_n$
> 6. $z \in G_n \implies {\bar{z}}^k = (z^{-1})^k = z^{n-k}, \; \forall k \in \mathbb{Z}$ 
> 7. Si $n > 1$, entonces
> $$\sum_{w \in G_n} w = 0 \;\; \text{ y } \;\; \prod_{w \in G_n} w = \begin{cases}
> 1 & \text{ si } n \text{ es impar} \\
  -1 & \text{ si } n \text{ es par} 
> \end{cases}$$

#Matemática #Primer-año 