La técnica HMAC, o *Hash-Based Message Authentication Code* es una técnica criptográfica para [[Autenticación|autenticar]] mensajes y verificar su [[Integridad]]. Se requiere de un [[Función hash]] $H$, un mensaje $m$, y una clave secreta $K$.

Primer se debe encriptar el mensaje, y después se genera el HMAC. Luego se envía el mensaje encriptado junto al HMAC.

$$
 
\operatorname {HMAC} (K,m)=\operatorname {H} {\Bigl (}{\bigl (}K'\oplus opad{\bigr )}\parallel \operatorname {H} {\bigl (}\left(K'\oplus ipad\right)\parallel m{\bigr )}{\Bigr)}
$$

Se define $K'$ como la clave original si su tamaño es menor o igual al tamaño del bloque, o como $H(K)$ en el caso contrario.

El uso de HMAC es vulnerable a un [[Ataque de reproducción]], por lo que se puede combinar con un [[Vector de inicialización]].

Otra vulnerabilidad posible del HMAC es el de un [[Análisis de tiempo variable]], o [[Análisis de potencia]].
