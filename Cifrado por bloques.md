Una unidad de cifrado por bloques una unidad de cifrado de clave simétrica que opera en grupos de bits de longitud fija, llamados bloques.

## Modos de operación

Tiene distintos modos de funcionamiento:

- **Electronic Code-Book (ECB):** Los mensajes se dividen en bloques y cada uno de ellos es cifrado por separado utilizando la misma clave $K$. Este método es inseguro ya que es más facil obtener patrones, y es vulnerable a [[Análisis de frecuencia de letras]]
- **Cipher-block chaining (CBC):** A cada bloque antes de ser cifrado ser cifrado se le aplica una operación XOR con el bloque cifrado anterior. Para hacer cada mensaje único se utiliza un [[Vector de inicialización]]
