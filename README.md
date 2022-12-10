# Fine Tuning - VGG16: Satellite Images

### Contexto

El objetivo principal de este proyecto es la clasificación de suelos en las imágenes de satélite obtenidas del conjunto de datos WorldStrat, empleando la red convolucional VGG16.

### Contenido

El conjunto de datos WorlStrat contiene aproximadamente 10.000 km2 de ubicaciones, consiguiendo de esta forma una variedad ordenada de tipos de suelos a lo largo del mundo: edificios, bosques, campos de béisbol, ríos, autopistas, ...

Cada categoría se compone de imágenes de alta resolución procedentes del Airbus SPOT, combinadas con las de los satélites Sentinel-2 con menor resolución. 
Para la realización de este proyecto únicamente se emplearon 10 clases de las 35 existentes: Airplanes, Bareland, City Building, Coastline, Farmland, Forest, Highway, Marina, Residents y Rivers, con alrededor de 400 imágenes por categoría con un tamaño de 256x256 pixels.

Para la resolución de la clasificación de tipos de suelo, se empleó Keras y la red convolucional VGG16, entrenada con el conjunto de datos ImageNet. Con Transfer-Learning se puede conseguir mejoras en la precisión sin emplear más tiempo para el entrenamiento.

Si sólo se realiza una extracción de características, es decir, se añade un nuevo clasificador al modelo ya entrenado se obtiene una precisión del ~97%. Con el Fine-Tuning, realizado en este cuaderno, se consiguió un ~99% dejando las 2 últimas capas del modelo base entrenables. 

### Referencias

Conjunto de datos: Cornebise, Julien and Orsolic, Ivan and Kalaitzis, Freddie, "The WorldStrat Dataset: Open High-Resolution Satellite Imagery With Paired Multi-Temporal Low-Resolution", 2022.
