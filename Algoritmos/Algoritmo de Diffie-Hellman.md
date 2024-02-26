Es un mecanismo seguro de intercambio de clave entre dos entidades Alice y Bob, que utiliza la teoría de [[Grupos]].

Se elige un generador $g$ del algún grupo $G$ de orden $p$. Se debe elegir un $g$ y un $r$ suficientemente grande. Luego:

1. Se elige una clave privada del grupo:
	1. Alice elige el elemento $a$.
	2. Bob elige el elemento $b$.
2. Cada entidad calcula su clave pública:
	1. Alice calcula $A = g^a$.
	2. Bob calcula $B = g^b$.
3. Las entidades intercambian las claves públicas
4. Cada entidad calcula la clave compartida:
	1. Alice calcula $K = B^a = g^{ab}$
	2. Bob calcula $K = A^b = g^{ab}$

Este algoritmo también puede ser aplicado con otros grupos, como el de [[Curvas elípticas]].
