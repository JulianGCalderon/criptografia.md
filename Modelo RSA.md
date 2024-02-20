---
draft: true
---

Debemos obtener dos primos $p,q$ suficientemente grandes, donde definimos $p\cdot q = n$. Luego hallamos $e, d$ tal que $e \cdot d \equiv 1 \mod \phi(n)$. Donde $\phi$ es la [[Función de Euler]].

Debido a que podemos factorizar $n$ (ya que partimos de eso), podemos fácilmente calcular $\phi(n)$ a partir de la propiedad vista anteriormente. Luego la obtención de la clave privada $d$ es un problema fácil computacionalmente.

Por lo general, se plantea $e = 2^{16} +1$, y se halla $d$ tal que se cumpla la ecuación dada.

La clave privada pública será el par $(e, n)$. El número $n$ es lo que le da la *unicidad* a nuestra clave.

## Encriptación

Interpreto el mensaje como un número entre $0$ y $n-1$. Si el mensaje es muy grande, lo podemos partir en distintos bloques.

Hallo el número $c$ (nuestro mensaje cifrado) tal que:

$$
m^e \equiv c \mod n
$$

Luego, la desencriptación será:

$$
c^d \equiv m \mod n
$$
