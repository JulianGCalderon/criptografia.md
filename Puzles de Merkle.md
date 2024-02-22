Es un protocolo de intercambio de claves. Se basa en la elaboración de puzles (problemas computacionales) de complejidad moderada que dificultan que un tercero que intercepta la comunicación obtenga la clave.

Una entidad envía $n$ puzles a otra entidad. La entidad opuesta solo debe resolver uno de los desafíos y comunicarle cuál desafío resolvió utilizando la misma clave.

Un tercero debe resolver todos los desafíos, pues no sabe cuál de todos los desafíos fue elegido por el destinatario.

Esta diferencia entre el costo del atacante y el costo del destinatario esperado se denomina *gap* computacional. Usualmente este *gap* computacional no es suficiente.
