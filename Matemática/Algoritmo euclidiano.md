Sean $a,b$ dos enteros, entonces:

$$
a = bq + r
$$

Sea $d$ un divisor común de $a,b$ entonces $d$ también es divisor de $bq$, luego $d$ es divisor de $a-bq = r$.

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
