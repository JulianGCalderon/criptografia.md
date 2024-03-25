Plonk es una implementación de un sistema [[zk-SNARK]]. Se distingue de otras implementaciones debido a que tiene un *setup* universal.

## Representación

Para representar el programa, convertirá el programa en un circuito con compuertas aritméticas. Esto permite representarlo con polinomios de forma más fácil.

## Reducción

Luego, traduciremos la traza de ejecución del programa en una tabla con las entradas y salidas de cada compuerta.

![[plonk_aritmetizacion.png]]

Luego, se pueden construir polinomios interpolando los valores. El grado de los polinomios es proporcional con la cantidad de compuertas del circuito.

Si la expresión aritmética es correcta, los polinomios en los que evaluamos son perfectamente divisibles por el *vanishing polynomial*.

## Compromiso

Para comprometerse a esta representación polinomial, utilizaremos un [[Polynomial Commitment Scheme|PCS]]. Si queremos que el *setup* sea universal, utilizaremos alguno como [[KZG]].

## Verificación

Una vez el *prover* envía su compromiso al polinomio que codifica la ejecución, el *verifier* debe verificar que:

- Se utilizaron los *public inputs* correctos. Para esto, se utilizará el *vanishing polynomial*.
- Las compuertas se evaluaron correctamente. Para hacer esto se utilizará unos polinomios predefinidos *"selector"* que depende de las compuertas y no de las entradas.
- La relación entre las compuertas es correcta. Esto implica que la salida de cierta compuerta se alimente a la entrada de la siguiente. Para hacer esto se utilizará un polinomio predefinido *"wiring"*, que se construye permutando los índices de las compuertas y codificando esto en un polinomio.
- El resultado del circuito, y el de la última compuerta, es cero.
