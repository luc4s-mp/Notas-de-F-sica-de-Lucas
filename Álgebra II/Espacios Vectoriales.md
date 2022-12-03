# Espacios vectoriales
En Introducción a la física (más específico en [[Vectores]]) introducimos el concepto de **vector** como aquel objeto geométrico que proviene de darle sentido a un segmento tal que $\overrightarrow{AB} \neq \overrightarrow{BA}$ y que tiene tres componentes una **amplitud**, una **dirección** y un **sentido**. 
Sin embargo, en la matemática se habla sobre **espacios vectoriales** donde sus elementos se llaman "vectores", pero estos a simple vista no pareciera tener nada que ver con la definición previa que teníamos de vector. En esta nota presentaremos una nueva definición de vector y veremos que nuestra definición previa es tan solo la punta del iceberg de las diversas aplicaciones que se pueden hacer con la definición nueva. 
Esta nueva definición se construye a partir de dos conjuntos, uno es un conjunto $\mathbb{K}$ que es un #Cuerpo y a cuyos elementos llamos **escalares** y otro es el conjunto $V$ a cuyos elementos llamamos **vectores**. El conjunto $V$ tiene que cumplir una serie de requisitos para ser llamado "espacio vectorial", pero antes de presentar directamente la definición, miremos un par de ejemplos para entender de donde sale.
Si $V= \mathbb{R}^2 = \{(x,y) ; x,y \in \mathbb{R}\}$ a quien podemos pensar como el _plano cartesiano_, cada uno de los elementos es una **lista** ordenada con largo 2 y si $V = \mathbb{R}^3 = \{(x,y,z): x,y,z \in \mathbb{R}\}$ que puede ser pensado como el espacio de 3D, sus elementos son una lista ordenada de largo 3. Podríamos generalizar que si $V = \mathbb{R}^n$ a que los elementos son una lista ordenada de largo $n$ o en general los matemáticos lo llaman una $n$-tupla.  

>  #Definición Sea $(\mathbb{K}, + , \cdot)$ un **cuerpo**. Sea $V$ un conjunto no vacío, sea $+$ una operación en $V$ y sea $\cdot$ una acción de $K$ en $V$. Se dice que $(V, +, \cdot)$ es un **$K$-espacio vectorial** si cumplen las siguientes condiciones:
>  1. $(V,+)$ es un **grupo abeliano**. Es decir, $+$ es asociativa, conmutativa, tiene neutro y opuesto.
>  2. La acción $\cdot : K \times V \rightarrow V$ satisface: 
> 	 i. $a \cdot (v+w) = a \cdot v + a \cdot w, \quad \forall \; a \in \mathbb{K}, \; \forall v, w \in V$ 
> 	 ii. $(a+b) \cdot v = a \cdot v + b \cdot v, \quad \forall a,b \in K; \; \forall v \in V$ 
> 	 iii. $1 \cdot v = v, \forall v \in V$ 
> 	 iv. $(a \cdot b) \cdot v = a \cdot (b \cdot v), \forall a,b \in K; \; v \in V$ 

