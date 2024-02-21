---
draft: true
---

Consideramos el conjunto $\mathbb{Z}_p^*$. Se puede probar que $(\mathbb{Z}_p^*, \times)$ es un [[Grupos|grupo]]. Luego su [[Grupos#Multiplicación|multiplicación]] será la operación de potenciación.

El problema del logaritmo discreto consiste en hallar $n$ tal que $a^n \equiv b \mod p$, conociendo $a,b$. Este es un problema computacionalmente complejo. Para acelerar la potenciación, utilizaremos el algoritmo de [[Exponenciación binaria]].

Para resolverlo, es necesario factorizar $p$, por lo que es una operación muy costosa si es un [[Números primos|número primo]] grande. Es necesario que sea un primo para evitar ataques como el [[Ataque de Pohlig-Hellman]], o el [[Ataque de búsqueda de colisiones]].
