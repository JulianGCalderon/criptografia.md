## Cifrado de Cesar

Los caracteres alfabéticos del mensaje son *corridos* $n$ caracteres siguiendo un esquema circular. De forma tal que luego de la letra `z` se sigue con la letra `a`.

En este tipo de cifrados, la clave indicaría la cantidad de posiciones a trasladar. El conocido método `rot13` consiste en un cifrado por sustitución de 13 posiciones.

Para desencriptar, debemos rotar los caracteres en el sentido inverso la misma cantidad de posiciones.

Este tipo de cifrado es muy poco seguro, ya que a un intermediario que no conoce la clave le tomaría a lo sumo 26 intentos hasta obtener el mensaje original, por lo que es vulnerable a un ataque de [[Fuerza bruta]]

## Cifrado por sustitución

El cifrado de cesar es un ejemplo de un cifrado por sustitución, pero en su forma general, un cifrado por sustitución asigna a cada letra del abecedario una nueva letra única (de forma biyectiva) tal que su asignación inversa pueda obtener el mensaje original a partir del mensaje cifrado.

En su forma general, la cantidad de claves posibles es $26!$, por lo que es un poco más seguro. Sin embargo, este tipo de cifrados es vulnerable a [[Análisis de frecuencia de letras]].
