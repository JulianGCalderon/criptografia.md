---
draft: true
---

Se dice $(G, +)$ que, siendo $G$ un conjunto y $+$ su operación binaria asociada, es un grupo si se cumple que:

- Para todo $a,b \in G$, $a+b \in G$.
- Existe $0 \in G$ tal que $a + 0 = a$, $\forall a \in G$
- Sea $a,b,c \in G$ entonces $(a+b)+c = a+(b+c)$.
- Para todo $a \in G$, $\exists b \in G$ tal que $a+b = 0$.

Se define el **orden** del grupo como su cantidad de elementos.

## Multiplicación

Definiremos la operación de multiplicación $(\times)$ como la aplicación de la operación de grupo, $n$ veces.

$$
a\times n = \underbrace{a+a+a+\dots}_{n \text{veces}}
$$

Se dice que un número $a$ es **generador** del grupo $(G, +)$, si $\forall b \in G$, existe un $n$ natural tal que $a \times n = b$.

## Subgrupos

Un subgrupo $H$ es un subconjunto de los elementos de $G$ tal que, tras la misma operación, respeta los axiomas del grupo.

El orden del elemento $a$ de un grupo $G$ es el orden del subgrupo $H$ generado al multiplicar al elemento $a$ por todo número natural.
