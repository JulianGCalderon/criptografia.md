a encriptación se puede pensar como una función $E(m, k) = c$ que recibe un mensaje $m$ y una clave $k$, y devuelve un mensaje cifrado $c$. De forma inversa, tendremos la función $D(c, k) = m$ que tomará el mensaje cifrado y obtendrá el mensaje original.

La única cosa que debería ser secreta cuando se envía un mensaje es la clave $k$. Para obtener la dicha clave, podemos utilizar el [[Algoritmo de Diffie-Hellman]], o el método de los [[Merkle Puzzles]].

Existen diversas técnicas de encriptación con clave privada, entre ellas:

- [[Cifrados por sustitución]]
- [[Cifrado XOR]]
- [[AES]]
- ChaCha10
