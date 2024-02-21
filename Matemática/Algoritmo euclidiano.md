Sean $a,b$ dos enteros, entonces:

$$
a = bq + r
$$

Sea $d$ un [[Divisibilidad#Común divisor|divisor común]] de $a,b$ entonces $d$ también es divisor de $bq$, luego $d$ es divisor de $a-bq = r$.

Similarmente, sea $e$ un divisor común de $b,r$, entonces $d$ también es divisor de $b(q-1)$, luego $d$ es divisor de $b + b(q-1) + r = bq + r = a$.

Luego, todos los divisores de $a,b$ son divisores de $r$, y todos los divisores de $r,b$ son divisores de $a$. Entonces:

$$
\gcd(a,b) = \gcd(b,r)
$$

Si repetimos la división con resto con $b,r$ obtendremos:

$$
b = rq' + r'
$$

En donde $r' < r$, puesto que $r < a$. Si continuamos el proceso, eventualmente $r$ será cero, y entonces $\gcd(s, 0) = 0 = \gcd(a,b)$.

## Algoritmo euclidiano extendido

Siempre es posible escribir el mínimo común divisor como combinación lineal de los elementos, de la siguiente forma:

$$
ua + vb = \gcd(a,b)
$$

Esto se puede demostrar a partir de la aplicación del algoritmo euclidiano:

$$
\begin{gather}
a = bq_1 + r_1 \\
b = r_1q_2 + r_2 \\
r_1 = r_2q_3 + r_3 \\
\vdots \\
r_{t-2} = r_{t-1}q_{t} + 0
\end{gather}
$$

Luego, podemos despejar $r_0$ y reemplazarla en la siguiente ecuación, despejar $r_1$ y reemplazarla en la siguiente ecuación, así sucesivamente hasta obtener $r_{t-1}$ como combinación lineal de $a,b$.

De forma general, si $a,b$ son [[Números primos#Coprimos|coprimos]], entonces podremos computar $u,v$ a través de las secuencias $P_n, Q_n$.

$$
\begin{gather}
P_1 = q_1 \qquad Q_1 = 1 \\
P_2 = q_2P_1 + 1 \qquad Q_2 = q_2Q_1 \\
P_i =  q_iP_{i-1} + P_{i-2} \qquad Q_i = q_iQ_{i-1} + Q_{i-1}
\end{gather}
$$

Finalmente,

$$
u = (-1)^tQ_{t-1} \qquad v = (-1)^{t+1}P_{t-1}
$$
