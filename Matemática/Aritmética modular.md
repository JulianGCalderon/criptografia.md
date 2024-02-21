Sea $m >= 1$ un entero, diremos que los enteros $a,b$ son congruentes en módulo $m$ si su diferencia es divisible por $m$:

$$
a \equiv b \mod m
$$

Sean $a_1 \equiv a_2 \mod m$ y $b_1 \equiv b_2 \mod m$, entonces $a_1 + b_1 \equiv a_2 + b_2 \mod m$. Además,$a_1b_1 \equiv a_2b_2 \mod m$.

Sea $a$ un entero, entonces $ab \equiv 1 \mod m$ para algún entero $b$ si y solo si son [[Números primos#Coprimos|coprimos]]. Se dice que $b$ es el inverso multiplicativo de $a$.

La rotación del [[Cifrados por sustitución#Cifrado de Cesar|cifrado de cesar]] se puede pensar como aritmética modular.

## Anillo de enteros

Se define la clase de equivalencia $\mathbb{Z}/m\mathbb{Z}$, o $\mathbb Z_m$, como el [[Anillos|anillo]] de enteros de módulo $m$. Agregamos y multiplicamos elementos del anillo al agregarlos y multiplicarlos como enteros, dividiendo por $m$, y tomando el resto.

Los elementos del anillo que tienen inversa se denominan unidades. Al multiplicar dos unidades, obtendremos otra unidad (esto se debe a que podemos multiplicarlas por sus respectivas inversas para cancelarlas).

Denominaremos $\mathbb{Z}_m^*$ como el [[Grupos|grupo]] de las unidades de módulo $m$. Todos los elementos de este conjunto tienen inversa (por definición). Además, los elementos son todos los coprimos de $m$, por lo que según la [[Función de Euler]], $\phi(m) = |\mathbb{Z}_m^*|$.
