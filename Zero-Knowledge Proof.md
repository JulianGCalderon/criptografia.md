---
aliases:
  - ZKP
---

Una prueba de conocimiento nulo permite a una entidad demostrar la veracidad de una declaración sin revelar ninguna información adicional, además de la veracidad de la declaración en sí.

En un sistema de ZKP, existe un **prover** que quiere probar una declaración, y un **verifier** que quiere verificar la prueba de una declaración. Un protocolo de ZKP debe cumplir las siguientes propiedades:

- **Completeness:** Si la declaración es cierta, entonces el *prover* debe poder convencer al *verifier*.
- **Soundness**: Un *prover* no puede convencer a un *verifier* de una declaración falsa.
- **Zero-Knowledge:** No se debe revelar más información que la declaración en sí.
