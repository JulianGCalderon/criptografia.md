---
aliases:
  - Polinomio
---

Definiremos un polinomio $R[x]$ como una función del estilo:

$$
p(x) = a_0 + a_1x + a_2x^2 + \cdots + a_nx^n
$$

La tupla $(R[x], +, \cdot)$ cumple los axiomas de [[Anillos]], por lo que son muy útiles en la criptografía. Factorizar polinomios en una operación muy costosa.

## Interpolación

Los coeficientes del polinomio son los valores $(a_0, a_1, \cdots, a_n)$. A partir de los coeficientes podemos evaluar un polinomio, pero a partir de los valores dados por múltiples evaluaciones, podemos hallar el polinomio que los cumple.

Dados $n+1$ puntos, existe un único polinomio de grado $n$ que cumpla todos los puntos.

## Multiplicación

La multiplicación de polinomios de forma tradicional es una operación muy costosa, por lo que una mejor forma de computarlo es evaluar el punto en los polinomios individuales y luego multiplicar los resultados.

Una vez tengo la tabla de evaluaciones, puedo interpolar el polinomio resultante sin necesidad de calcularlo tradicionalmente.
