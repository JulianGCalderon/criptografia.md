El acrónimo SNARK proviene del inglés: *Succinct Non-Interactive Argument of Knowledge*. Es un sistema de construcción de una [[Zero-Knowledge Proof]].

- Es **non-interactive**, pues puede ser almacenada y no debe ser repetida por los distintos *verifiers*.
- Es **succinct**, pues la verificación es relativamente corta.
- Finalmente, **argument of knowledge** refiere a la habilidad de producir una prueba convincente de una declaración a un *witness* o testigo:
	- El término **argument** refiere (vagamente) a que se puede realizar una prueba criptográfica de una declaración.
	- El término **knowledge** refiere a que cada *prover* debe conocer un *witness*.

En términos prácticos, permite probar la correcta ejecución de un dado cómputo, sin revelar los valores usados.

Usualmente, son implementados en los siguientes pasos:

- **Representación** del cómputo a probar, como una serie de restricciones sobre variables. Una de las técnicas más utilizadas es [[R1CS]].
- **Reducción** de las restricciones en ecuaciones [[Polinomios|polinómicas]]. Para esto podremos utilizar técnicas como.
- **Transformación** de las ecuaciones, y una clave secreta, a un espacio homomórfico, utilizando [[Curvas elípticas#Pares de curvas elípticas|pares de curvas elípticas]], a partir la misma clave secreta (que luego será desechada). Estas claves pueden ser generadas en conjunto entre múltiples particpantes para asegurar que ninguno la conozca por completo.
- **Construcción** de las pruebas a partir de evaluar los polinomios en el espacio homomórfico.
- **Verificación** de las pruebas, verificando que los puntos evaluados sean válidas en el espacio homomórfico.

Una de las implementaciones más simples de este sistema es el [[Baby SNARK]].
