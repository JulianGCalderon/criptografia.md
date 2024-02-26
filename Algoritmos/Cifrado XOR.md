Definimos una clave $k$ y un mensaje $m$ como un conjunto de bits $\{0, 1\}^n$. Luego podemos encriptar y desencriptar de la forma:

$$
\begin{align}
C = m \oplus k \\
m = C \oplus k
\end{align}
$$

La probabilidad de que yo desencripte el mensaje sin necesidad de la clave es de $\frac 12^n$. Debido a esto, se dice que es un **secreto perfecto**.

Requiere que yo encuentre una clave que tenga el mismo tamaño que el mensaje que yo quiero encriptar. Una posible solución a esto es utilización de un [[Cifrado por bloques]]. Otra solución es utilizar una clave inicial para generar un flujo infinito. Este sería un tipo de [[Cifrado por flujo]].
