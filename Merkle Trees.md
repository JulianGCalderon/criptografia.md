---
draft: true
---

Un Merkle Tree es una estructura de dato basado en el concepto de una [[Función hash]].

Se tiene un conjunto de datos de cardinalidad $n$, y se les aplica una función de Hash de a pares. Luego, tendré otro conjunto de datos de cardinalidad $n/2$. Esto se repite hasta obtener un único hash $h$.

Si yo cambio uno solo de los datos, entonces el hash $h$ del nodo raíz será distinto. Esta es una forma de [[Comprimoso|comprometerme]] a un conjunto de datos.
