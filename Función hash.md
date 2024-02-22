Una función hash es una función que toma una tira de bytes de longitud indeterminada en otra tira de bytes de longitud fija $n$.

$$
H: \{0,1\}^* \to \{0,1\}^n
$$

Algunas propiedades de una buena función hash son:

- **Resistencia a preimagen:** Es imposible computacionalmente, dado $D$, hallar $m$ tal que $H(m) = D$.
- **Resistencia a colisiones:** Es imposible computacionalmente hallar $m_1, m_2$ tales que $H(m_1) = H(m_2)$.

Algunos ejemplos conocidos son:

- MD5
- SHA-3
- Keccak
- Poseidon
- Blake 2/3

Algunas formas de construir funciones de hash, son:

- Merkle-Damgård
- Esponja
