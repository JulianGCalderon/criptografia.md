Es un algoritmo para de [[Encriptación asimétrica]] que se basa en el [[Problema del logaritmo discreto]] para generar claves vinculadas.

## Generación de claves

Partimos de dos [[Números primos]] $p,q$ suficientemente grandes, tal que $n = p\cdot q$ sea computacionalmente imposible de factorizar.

Luego hallamos $e, d$ tal que $e \cdot d \equiv 1 \mod \varphi(n)$. Donde $\varphi$ es la [[Función de Euler]].

Se debe elegir un valor inicial de $e$ coprimo con $\varphi(n)$ Por lo general, se plantea $e = 2^{16} +1$.

Calculamos $d$ tal que se cumpla la congruencia.

La clave privada pública será el par $(e, n)$. El número $n$ es lo que le da la *unicidad* a nuestra clave.

## Encriptación

Interpreto el mensaje como un número entre natural menor a $n$. Si el mensaje es muy grande, lo podemos partir en distintos bloques.

Hallo el número $c$ (nuestro mensaje cifrado) tal que:

$$
m^e \equiv c \mod n
$$

Luego, la desencriptación será:

$$
c^d \equiv m \mod n
$$

Debido a la relación vista anteriormente, podemos asegura su funcionamiento.

$$
m^{ed} = m^{1 + k\varphi(n)} = m(m^{\varphi})^k = m \mod n
$$
