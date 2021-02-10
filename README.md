# REDES GENERATIVAS ADVERSARIAS (GANs) / Pix2Pix

Tutorial Youtube: Dot CSV Generando FLORES realistas con IA - Pix2Pix | IA NOTEBOOK #5

*   https://www.youtube.com/watch?v=YsrMGcgfETY&t=4202s

Tutorial pix to pix https://www.tensorflow.org/tutorials/generative/pix2pix
Paper https://phillipi.github.io/pix2pix/
Imagenes http://www.robots.ox.ac.uk/~vgg/data/flowers/102/index.html

Imagenes Monet: 

https://www.kaggle.com/shcsteven/paired-landscape-and-monetstylised-image

# DISEÑO DE LA ARQUITECTURA DE LA  RED

SE SIGUE DISEÑO DEL PAPER

La red tiene dos partes
*   Generador de imagenes
*   Discriminador

##Generador de imagenes

  * La arquitectura del generador es una U-Net modificada.
  * Cada bloque en el codificador es (Conv -> Batchnorm -> Leaky ReLU)
  * Cada bloque en el decodificador es (Transposed Conv -> Batchnorm -> Dropout (aplicado a los primeros 3 bloques) -> ReLU)
  * Hay conexiones de salto entre el codificador y el descodificador (como en U-Net).
