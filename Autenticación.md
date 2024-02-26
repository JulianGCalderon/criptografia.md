Se debe poder adjuntar una Firma digital a los documentos que verifiquen la identidad de la persona que envía el mensaje. Esta firma digital no debe poder ser falsificada.

La [[Encriptación asimétrica]] permite esto, ya que podemos firmar el archivo con nuestra clave privada, demostrando que fui yo el que envío el mensaje. Por lo general, se aplica una [[Función hash]] a los datos y estos se firman con algún protocolo como [[RSA]].

Otras técnicas conocidas son:

- [[Firma de Schnorr]]
- [[HMAC]]
- DSA
- ECDSA
- EdDSA
