---
draft: true
---

Para firmar un mensaje $m$, partimos de un generador $g$ de un [[Grupos]], una clave privada $x$, y una [[Función hash]]. La clave de verificación será $y = g^x$.

Para la creación de firma, haremos:

- Elegimos $k$ al azar
- $r = g^k$
- $e = H(r || m)$
- $S = k - x\cdot e$
- La firma del mensaje será: $(S, e)$

Para la verificación, haremos:

- $r_v = g^S \cdot y^e$
- $e_s = H(r_v || m)$
- Si $e_v = e$, entonces la firma se verifica.

Si repetimos el mismo $k$, entonces se podrá derivar $x$ con aritmética simple.
