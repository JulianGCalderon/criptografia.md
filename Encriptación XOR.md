Definimos una clave $k$ y un mensaje $m$ como un conjunto de bits $\{0, 1\}^n$. Luego podemos encriptar y desencriptar de la forma:

$$
\begin{align}
C = m \oplus k \\
m = C \oplus k
\end{align}
$$

Este tipo de encriptación se denomina **one time pad**, ya que solo se puede utilizar la misma clave una sola vez.

La probabilidad de que yo desencripte el mensaje sin necesidad de la clave es de $\frac 12^n$. Debido a esto, se dice que es un **secreto perfecto**.

Requiere que yo encuentre una clave que tenga el mismo tamaño que el mensaje que yo quiero encriptar. Una posible solución a esto es utilización de un [[Stream Cipher]].

Si yo cambio bits en el mensaje cifrado, esos bits serán intercambiados en el mensaje original. Esto permite que alguien intercepte el mensaje y modifique los contenidos del mismo. Necesitamos un mecanismo para asegurar la integridad del mensaje. Para eso utilizaremos [[MAC]]
