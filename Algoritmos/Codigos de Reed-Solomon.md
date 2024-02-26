Un código es una función $C$ sobre un cuerpo finito $\mathbb F_p^k$ hacia un cuerpo finito $\mathbb F_p^n$. Se utilizan para asegurar la [[Integridad]] de un mensaje, y corregir errores sobre el mismo. Uno de los códigos que más se utilizan son los códigos lineales. En estos códigos, se cumple que $C(x+y) = C(x) + C(y)$.

- Cada símbolo está constituido por $m$ bits consecutivos
- Cada palabra consta de $k$ símbolos de información, y $r$ símbolos de paridad.
- La longitud de la palabra-código es $n = k + r$.
- Se establece la relación $n = 2^m - 1$ entre la longitud de la palabra-código $n$ y el número de símbolos $2^m$.
- Es capaz de corregir $t$ errores, donde $t = n/2$.
- Como medida de distancia entre dos códigos $A, B$ se utiliza la [[Distancia de Hamming]].

A partir de una información, creamos un [[Polinomios|Polinomio]] utilizando sus valores como coeficientes de un polinomio. Luego, evaluamos el polinomio en puntos predefinidos. Este conjunto de evaluaciones (junto a los puntos predefinidos) serán los códigos.

Si el mensaje tiene algunos errores, puedo utilizar los puntos redundantes (códigos) para obtener el mensaje original, [[Polinomios#Interpolación|interpolando]] el único polinomio que pasa por esos puntos.
