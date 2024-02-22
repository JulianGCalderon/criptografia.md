La técnica CMAC, o *Cipher-Based Message Authentication Code* es una técnica criptográfica para autenticar mensajes. Se requiere de un cifrado de bloque $E$, un mensaje $m$, y una clave $k$.

Consiste en partir el mensaje en bloques y aplicarle $E$ a cada bloque sucesivamente, utilizando una clave $k$, en cadena. Al resultado de cada operación se la aplica XOR con el siguiente bloque.

El uso de CMAC es vulnerable a un [[Ataque de reproducción]]
