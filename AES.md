AES, o *Advanced Encryption Standard*, es un esquema de [[Cifrado por bloques]].

El algoritmo toma $128$ bits de texto plano y devuelve $128$ bits de cifrado a partir de una clave de $128/192/256$ bits.

## Funcionamiento

El algoritmo de **key scheduler** es utilizado para calcular todas las claves de ronda a utilizar dada una clave inicial.

AES considera cada bloque como una grilla de $4\times 4$ bytes.

Cada ronda de encriptación consiste en cuatro pasos:

1. `SubBytes`: Cada byte es sustituido por otro byte, a través de una *lookup table* llamada `S-box`.
2. `ShiftRows:`: Se intercambian las filas de forma particular.
3. `MixColumns`: Se realiza una multiplicación de matriz, donde cada columna se multiplica por una matriz específica y la posición de cada byte de la columna es cambiada.
4. `AddRoundKeys`:  Al resultado de la etapa anterior se le aplica XOR con la clave de ronda correspondiente.
