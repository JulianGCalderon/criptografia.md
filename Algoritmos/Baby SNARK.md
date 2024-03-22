Es una implementación de un sistema [[zk-SNARK]] simple, que exhibe el funcionamiento principal, pero que no asegura la propiedad de [[Zero-Knowledge Proof|ZKP]], ya que permite obtener información oculta de los polinomios.

## Representación

Para este protocolo, se representa a las restricciones del sistema como una matriz $A:\mathbb F^{m \times n}$ de un [[Cuerpos|Cuerpo]] tal que un vector $\vec a: \mathbb F^n$ es solución del sistema si y solo si:

$$
U\vec a \circ U\vec a = 1
$$

Donde $\circ$ representa el producto de Hadamard (elemento a elemento).

Esta representación es NP-completa, lo que implica que puede ser utilizada para representar cualquier problema de satisfacibilidad booleana.

## Reducción

Buscaremos transformar la representación matricial en un conjunto de [[Polinomios]].

En primer lugar, definiremos $u_i$ como el polinomio asociado a la columna $i$, tal que:

$$
u_i(r_j) = U_{j,i}
$$

Luego, podremos calcular el problema polinómico asociado como

$$
P(X) = \Big(\sum_{i=0}^{n-1} a_iu_u(X)\Big)^2 - 1 = 0
$$

Se pueden separar las declaraciones según las entradas públicas al sistema $i < l$, y el lado del testigo $i \geq l$.

## Configuración

Este protocolo requiere de una configuración confiable para construir un CRS, o *common reference string*.

La configuración parte de la representación matricial $\{u_i\}_{i \geq 0}$, y generará, de forma aleatoria, las *trapdors* $\tau$, $\beta, \gamma$. Luego, podremos derivar el CRS:

$$
\sigma := [1, \tau, \cdots, \tau^m, \gamma, \gamma\beta, \{\beta u_i(\tau)\}_{i \geq l}]_G
$$

> [!note] Notación
>  La notación $[x]_G$ implica que se debe calcular en el generador del grupo $G$.

Además, se deben pre computar los siguientes valores.

$$
[t(\tau), \{u_i(\tau)\}_{i \geq 0}]_G
$$

Se utiliza como polinomio objetivo $t$ el polinomio con raíces en $i$ con $i \leq n-1$.

El protocolo está construido alrededor de tres *trapdors*:

- $\tau$: Permite evaluar cualquier polinomio de grado $m$ en el espacio homomórfico.
- $\beta$: Restringe al *prover* a únicamente utilizar una combinación lineal de los polinomios dados.
- $\gamma$: Permite verificar la consistencia de las restricciones.

## Prueba

Queremos probar que conocemos una solución $\vec a$ para el polinomio $P(X)$, a partir del CRS $\sigma$. Para esto, debemos calcular $h(X)$ tal que $h(X) = P(X) / t(X)$.

Computaremos la prueba, a partir de los valores pre computados de $[\tau^n]_G$:

-  $H = [h(\tau)]_G$
- $V_w = \sum_{i \geq l} a_i [u_i(\tau)]_G$
- $B_w = \sum_{i \geq l} a_i [\beta u_i(\tau)]_G$

La prueba será la tupla de estos valores.

## Verificación

Primero, computo la prueba desde el lado del *verifier*, como:

- $V_s = \sum_{i < l}a_i[u_i(\tau)]_G$
- $V = V_s + V_w$

Luego, debo ver que las restricciones se cumplan en el espacio homomórfico utilizando la función de par.

$$
\begin{align}
e(H, [t(\tau)]_G) = e(V, V) \implies h(\tau) t(\tau) = p(\tau)\\
e(B_w, [\gamma]_G) = e([\gamma\beta]_G, V_w) \implies \gamma\beta p(\tau) = \gamma\beta p(\tau) 
\end{align}
$$
