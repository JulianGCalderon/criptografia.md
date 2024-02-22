Para firmar un mensaje $m$, partimos de un generador $g$ de un [[Grupos]] de orden $p$. Está basado en el [[Problema del logaritmo discreto]]

Necesitaremos una clave privada $x$ y una clave pública de verificación $y = g^x$.

## Firma

Para firmar un mensaje $m$, entonces:

- Elegimos $k$ al azar
- Sea $r = g^k$
- Sea $e = H(r || m)$
- Sea $S = k - x\cdot e$

La firma del mensaje será: $(S, e)$

## Verificación

Para verificar el mensaje, entonces:

- Sea $r_v = g^S \cdot y^e$
- Sea $e_s = H(r_v || m)$

Si $e_v = e$, entonces $r_v = r$, por lo que la firma se verifica.

## Ataques

Si utilizamos el mismo $k$ para firmar dos mensajes, entonces se podrá derivar la clave secreta $x$ con aritmetica simple.
