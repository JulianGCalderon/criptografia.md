Se define una curva elíptica $E$ como aquellos puntos $(x,y)$ que pertenecen a un [[Cuerpos|cuerpo]] finito $\mathbb{F}_p$, respetando la Forma de Weierstrass.

$$
y^2 = x^3 + ax + b
$$

Sobre $a,b$ se impone la restricción:

$$
4a^3 + 27b^2 \neq 0
$$

Se cumple que si $(x,y) \in E$, entonces $(x,-y) \in E$. Debido a que hay dado $x$, hay dos valores posibles de $y$, es suficiente $x + 1 \text{bit}$ para derivar $(x,y)$. Esto se denomina **compresión**.

Todas las técnicas que utilizaban el concepto de [[Grupos]] podrían utilizar curvas elípticas para agregarle complejidad computacional. Para alcanzar el mismo nivel de seguridad, se requiere trabajar con cuerpos más pequeños que con [[Aritmética modular]].

Algunas curvas conocidas son:

- Secp256k1
- BLS12-381

## Suma

Definiremos la operación de suma $\oplus$ entre dos puntos $P,Q$ como el inverso al tercer punto que interseca la recta formada por $P, Q$.

![[curva_eliptica_suma.jpg|400]]

Para cumplir la existencia de un elemento neutro, diremos que las rectas paralelas intersecan en el infinito, por lo que $P \oplus -P = 0$, y $P \oplus 0 = P$.

Diremos que para calcular $P \oplus P$, utilizaremos la recta tangente a la curva en $P$.

![[curva_eliptica_inverso.jpg|400]]

Se puede demostrar que la propiedad de asociatividad también se cumple, por lo que diremos que $(E, \oplus)$ es un [[Grupos|grupo]].

## Multiplicación escalar

Se definirá la operación de multiplicación $nP$ como aplicar $P\oplus P\oplus P \dots, n$ veces. Se puede replicar la misma técnica de [[Exponenciación binaria]] para obtener una complejidad computacional de $O(\log n)$.

Esta definición permite considerar el conjunto de los puntos de la curva elíptica como cuerpo.

### Multiplicación multiescalar

La multiplicación multiescalar se utiliza para [[Comprimoso|comprometerme]] a un conjunto de escalares, en lo que se conoce como un **commitment de pedersen**, y se calcula de la siguiente forma:

$$
R = \sum_{k=0}^n a_kP_k
$$

Es muy difícil generar una preimagen para esa ecuación, ya que debería resolver el [[Problema del logaritmo discreto]].

## Proyección sobre un cuerpo finito

Al proyectar las coordenadas sobre $\mathbb{Z_p}$ con $p$ primo, se obtiene un patrón altamente impredecible que es muy útil en la criptografía, y aún sigue cumpliendo la definición de cuerpo finito.

Para esto, la ecuación de la curva será:

$$
y² \mod p = (x³ + ax + b) \mod p
$$

Y la distribución de puntos se verá de la siguiente forma:

![[curva_eliptica_finita.jpg|400]]

Diremos que el **cuerpo base** $\mathbb Z_p$ de la curva elíptica es donde proyectamos las coordenadas, mientras que el **cuerpo escalar** $\mathbb Z_r$ es un cuerpo con la misma cantidad de elementos $r$ que el grupo generado por la curva elíptica.

## Optimizaciones

### Otras curvas elípticas

Las curvas elípticas de **Twisted Edwards** no requiere tener en cuenta casos borde, por lo que son más rápidas para operar.

Las curvas elípticas de **Montgomery** permite hacer ecuaciones en tiempo constante.

### Coordenadas proyectivas

Se puede agregar una coordenada adicional $Z$ para trabajar sobre $(X,Y,Z)$, y definirlas como:

$$
x = X/Z \qquad y = Y/Z
$$

Luego podremos operar con estas nuevas coordenadas, lo que permite que no tengamos que realizar inversiones. Se le asigna a cada punto $(x,y)$ una recta en el espacio. Una vez operado, se puede proyectar sobre el eje de coordenadas original.

En las coordenadas Jacobianas, el pasaje será un poco distinto:

$$
x = X/Z^2 \qquad y = Y/Z^3
$$

## Pares de curvas elípticas

Sean $G$ y $G'$ dos curvas elípticas, entonces un par es una función $G \times G' \to G_T$ tal que se cumple la no degeneración: $e \neq 1$, y la bilinealidad, esto es:

$$
\forall a,b\in \mathbb {F} _{q}^{*},P\in G_{1},Q\in G_{2}:\ e\left(aP,bQ\right)=e\left(P,Q\right)^{ab}
$$

Esto permite esconder números $a,b$ dentro de la curva elíptica a través de encriptarlos con $aP, bQ$ y realizar una multiplicación entre ambos números.

Existe un algoritmo eficiente para computar $e$.
