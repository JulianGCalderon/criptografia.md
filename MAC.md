---
draft: true
---

Un MAC, o código de autenticación de mensaje, es una porción de información que da certeza de que el contenido del mensaje no fue modificado. Se requiere de una [[Función hash]] $H$.

1. Parto de un mensaje $m$, una clave $K$.
2. Encripto el mensaje $m$ en un mensaje cifrado $C$.
3. Calculo el MAC como $H(K \oplus \text{outerpad} || H(K \oplus \text{innerpad} || C))$
4. Envío $C||\text{MAC}$

El uso de una MAC es vulnerable a un [[Ataque de reproducción]]
