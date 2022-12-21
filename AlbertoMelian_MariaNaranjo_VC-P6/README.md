# Práctica 6. Análisis facial

Se ha desarrollado un sistema de identificación de personas. Si la persona no está registrada en el sistema, se le comunica y se le ofrece la posibilidad de registrarse. Además, cuando se reconoce que el usuario está registrado, nos ofrece información sobre su estado de ánimo.

## Contributors
[María Naranjo Almeida](https://github.com/marianaral)

[Alberto Melián Rodríguez](https://github.com/Aeronpsaro)

### Procedimiento ###
Los usuarios que están registrados, tendrán, al menos, una imagen de su cara dentro de la carpeta Registered. Cuando se inicia el programa, éste muestra la cámara y comprueba que la cara que se ve en la cámara tiene un parecido con alguna cara registrada (la similitud de tiene que ser mayor a un umbral, en este caso se ha establecido en un 60%). Si ninguna cara registrada coincide, informa de tal situación y se ofrece la posibilidad registrarse, ejecutando otra celda. 

Cuando reconoce a un usuario registrado, le se le informa con el siguiente mensaje: "Bienvenido/a, [NOMBRE]". A continuación, según el estado de ánimo de la persona, sale un mensaje personalizado. Por ejemplo:

- Si la persona está contenta: Hoy te noto muy contento/a.
- Si la persona está triste o asqueado: Hoy te veo un poco triste. Quizás esta imagen de un gatito te puede ayudar [IMAGEN DE GATITO].
- Si la persona está enfadada: Percibo que estás enfadado. Tomar una infusión puede ayudar a calmarte.
- Con cualquier otra emoción: ¡Que tengas un buen día!

### Funcionamiento ###
Cuando se ejecuta la cuarta celda, lo primero que va a ocurrir es abrirse la cámara durante 5 segundos. Tras esta acción, se imprime si el usuario está registrado o no, de la misma manera que se explicó en el apartado Procedimiento.

Si un usuario quiere registrar una cara, deberá ejecutar la quita celda y se abrirá de nuevo la cámara. Cuando se presione la tecla espacio, se tomará una imagen y se guardará en la carpeta Registered. Se invita al usuario a cambiar el nombre de la imagen para que introduzca su nombre.
