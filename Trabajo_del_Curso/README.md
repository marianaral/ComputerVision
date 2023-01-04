# Trabajo del Curso de la asignatura de Visión por Computador - Pictionary


En este proyecto se ha realizado una pequeña aplicación del conocido juego de Pictionary, utilizando la visión por computador

 ---

### Índice

[Motivación]()

[Objetivo]()

[Procedimiento](#procedimiento)

[Descripción técnica](#descripción-técnica)

[Fuentes y tecnologías utilizadas](#fuentes-y-tecnologías-utilizadas)

[Conclusiones]()

[Créditos materiales no originales]()

[Autores](#autores)

 ---


## Procedimiento

En primer lugar se ha creado un entorno de conda.

```
conda create --name pictionary python==3.9
conda activate pictionary
```

A continuación, instalamos todas las librerías necesarias para la realización del proyecto.

```
pip install mediapipe 
pip install opencv-python
```
Tras las instrucciones anteriores, ya se tiene el entorno preparado para realizar la práctica 

## Descripción técnica

Una vez listo el entorno con las librerías necesarias, lo primero que hay que realizar es la importación de las librerías y la iniciación de la cámara del equipo, como se ha hecho en proyectos anteriores.

```
import cv2
import mediapipe as mp
import numpy as np

vid = cv2.VideoCapture(0)

while(True): 
    ret, frame = vid.read()
    
    #Se hace flip del frame para hacer efecto espejo
    frame = cv2.flip(frame,1)
 
    cv2.imshow("Pictionary", frame)
    cv2.waitKey(1)

    # Detenemos pulsado ESC
    if cv2.waitKey(20) == 27:
         break
  
# Libera el objeto de captura
vid.release()
# Destruye ventanas
cv2.destroyAllWindows()
```

El siguiente paso consiste en 

## Fuentes y tecnologías utilizadas

- [Conda](https://docs.conda.io/en/latest/)

- [Mediapipe](https://mediapipe.dev/)

- [OpenCV](https://opencv.org/)

- [Guiones de las prácticas de la asignatura](https://github.com/otsedom/otsedom.github.io/tree/main/VC)

## Créditos materiales no originales

- [Utilización de la librería Mediapipe para la detección de la mano](https://www.section.io/engineering-education/creating-a-hand-tracking-module/#:~:text=Hand%20tracking%20using%20MediaPipe%20involves%20two%20stages%3A%201,landmarks%20on%20the%20cropped%20image%20of%20the%20hand.)

- [Acceder al atributo label de multi_handedness de Mediapipe](https://stackoverflow.com/questions/67455791/mediapipe-python-link-landmark-with-handedness)


## Autores
[María Naranjo Almeida](https://github.com/marianaral)

[Alberto Melián Rodríguez](https://github.com/Aeronpsaro)
