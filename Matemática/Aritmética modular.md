---
draft: true
---

**Congruencia:** Se dice para [[Enteros]] que $a \equiv b \mod p$ si y solo si $a = p\cdot n + b$. Si son congruentes, entonces $a-b$ es divisible por $p$.

En la aritmética modular, solo nos quedamos con el resto de las operaciones (al dividirlas por el órden $p$).

Se define la clase de equivalencia $\mathbb{Z}_p$ como los números resultantes al aplicar aritmética modular con órden $p$ primo. En este conjunto, definimos la operación de suma $+$ donde tras aplicar la suma tradicional, nos quedamos con el módulo del número en el órden $p$. La tupla $(\mathbb{Z}_p, +)$ es un [[Grupos|Grupo]].

## Multiplicación

Definiremos la operación de multiplicación $(\cdot)$ como la aplicación de la operación de grupo de suma, $n$ veces.

$$
a\cdot n = \underbrace{a+a+a+\dots}_{n \text{veces}}
$$

Un problema común es hallar el menor número positivo $k$ tal que en el grupo, $x\cdot k = 0$.

## Potencia

Consideramos el conjunto $\mathbb{Z}_p^*$ como $\mathbb{Z}_p - \{0\}$. Se puede probar que $(\mathbb{Z_p^*}, \times)$ es un grupo. Luego definiremos la operación de potencia como la aplicación de la operación del grupo, $n$ veces.

El resultado se puede reducir entre medio de las multiplicaciones (según la aritmética modular), y el resultado será el mismo.

El problema del logaritmo discreto consiste en hallar $x$ tal que $a^n = b$, conociendo $a,b$. Este es un problema computacionalmente complejo.

> [!note] Complejidad de $a^n$
> Para calcular $a^n$, puedo elevar al cuadrado sucesivamente y luego multiplicar directamente las potencias restantes: $a \to a^2 \to a^4 \to a^8 \to a^9$
