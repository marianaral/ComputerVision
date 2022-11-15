## Práctica 5. Reconocimiento de matrículas

### Alberto Melián y María Naranjo

Para realizar esta práctica, se ha utilizado YOLOv7 y PyTesseract.

El pipeline para el reconocimiento de matrículas españolas es el siguiente:

1. Con YOLOv7 obtenemos qué elementos están presentes en las imágenes contenidas en la carpeta images.
2. Buscamos las fotos contienen coches.
3. Buscamos contornos rectangulares en las imágenes (matrícula).
4. Recortamos la imagen para solamente tener la matrícula
5. Le pasamos tal imagen a PyTesseract.

Las conclusiones obtenidas de esta práctica son:
1. PyTesseract es bastante sensible y, aunque la imagen tenga texto y esté bien centrado (como en la imagen im1), no consigue leerla. Una hipótesis es que la resolución no es la suficiente o la iluminación no es la adecuada.
2. Mientras más de perfil esté el coche, más difícil es de leer.
3. PyTesseract detecta mejor los números que las letras, como se puede ver en la im3.jpg.
***
Bajo licencia de Creative Commons Reconocimiento - No Comercial 4.0 Internacional