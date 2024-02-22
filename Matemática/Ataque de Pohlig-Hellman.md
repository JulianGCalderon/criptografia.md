Se utiliza para resolver una ecuación de la forma $a^x = b \mod n$, donde $a$ es un generador de un [[Grupos|grupo]] de orden $n$ con operación binaria $\times$.

Si $n$ no es un [[Números primos|número primo]], entonces sabremos que el grupo tendrá subgrupos no triviales de orden primo, debido al [[Teorema de Lagrange]].

Este algoritmo es más eficiente cuando $n$ es producto de primos pequeños, ya que podemos reducir el algoritmo para trabajar sobre uno de los subgrupos de orden primo.
