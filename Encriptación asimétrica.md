A diferencia de la [[Encriptación simétrica]], tendremos dos claves. Una clave pública, y una clave privada. Estas claves están vinculadas, pero no se podrá derivar la clave privada a partir de la clave pública.

Los mensajes encriptados con una de las claves pueden ser desencriptados por la otra clave. Esto permite que las entidades ya no se tengan que poner de acuerdo en una clave común, sino que cada una encripta utilizando la clave publica de la otra entidad.

Para esto, es necesario algún mecanismo para la obtención de [[Certificados de clave pública]] que aseguren la autenticidad de las mismas.

Algunos mecanismos para la generación de estas claves son:

- [[RSA]]
