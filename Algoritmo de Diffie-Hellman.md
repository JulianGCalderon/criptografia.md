---
draft: true
---

En la década del 70, se descubrió un mecanismo seguro de intercambio de clave a partir de este algoritmo.

1. Se elige un primo $p$ y un generador $g$ del algún subgrupo del $\mathbb Z_p$. Se debe elegir un $p$ y un $g$ suficientemente grande.
2. Cada entidad elige $a,b$ respectivamente, como elementos del subgrupo.
3. Cada entidad calcula $PK_i = g^{i}$, y se intercambian los valores calculados.
	1. La primera entidad calcula $(PK_b)^a = (g^b)^a$
	2. La segunda entidad calcula $(PK_a)^b = (g^a)^b$
4. Ambos entidades tendrán $g^{ab}$, que podrán utilizar para generar una clave a través de una función *KDF (key definition function)*.

Este algoritmo también puede ser aplicado con otros grupos, como el de [[Curvas elípticas]]
