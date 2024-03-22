La idea es representar el problema a través de la siguiente ecuación:

$$
Az\cdot Bz = Cz 
$$

Donde definiremos $z$ como:

$$
z = (1,u,w)^\tau
$$

Se podrá utilizar el lenguaje **Circom** para representar circuitos en este sistema de restricciones.

## Representación

Podremos representar ecuaciones matemáticas simples de suma y multiplicación:

$$
a + b = c \qquad a \cdot b = c
$$

Para representar ecuaciones más complejas, necesitamos definir variables auxiliares:

$$
a \cdot (b+c) = d \iff
\begin{cases}
a \cdot e = d \\
b + c = e
\end{cases}
$$

Si queremos representar una división, utilizaremos el pequeño teorema de Fermatt.

$$
a/b = c \iff ab^{-1} = c \iff ab^{p-2} = c
$$
