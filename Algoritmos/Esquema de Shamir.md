---
aliases:
  - SSS
  - Shamir Secret Sharing
---

El SSS, o *Shamir Secret Sharing*, es un esquema para compartir una clave secreta $s$ entre $n$ participantes, que necesite una mayoría de $k$ participantes para obtener $s$.

Se define $S$ como la evaluación de un [[Polinomios|polinomio]] $p$ de grado $k-1$ en un punto público $x_s$. Luego, elijo $k$ puntos del polinomio, los evalúo, y le doy una evaluación a cada participante.

Si esos participantes se unen, pueden calcular el secreto original a partir de [[Polinomios#Interpolación|interpolar]] el polinomio original utilizando los $k$ puntos difundidos.
