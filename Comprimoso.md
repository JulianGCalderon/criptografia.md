Es una técnica para comprometerme con un mensaje sin revelarlo. Para esto, creo un mensaje $m$, le aplico una [[Función hash]], y comparto el resultado.

Más adelante, puedo revelar el mensaje original para que se pueda verificar que yo me había comprometido a dicho mensaje previamente.

Esto es vulnerable a un ataque de diccionario, teniendo precomputado múltiples mensajes. Una solución a esto es utilizar un número aleatorio $r$, y aplicar la función de Hash sobre $m || r$. De esta forma, nadie puede derivar el mensaje original.

Al revelar el mensaje original, también debo revelar el número aleatorio $r$.
