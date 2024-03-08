# TFG
## Repositorio de Herramientas para Procesamiento y Evaluación de Imágenes Médicas
Este repositorio contiene una serie de herramientas y cuadernos de Jupyter que han sido útiles en el desarrollo de mi Trabajo de Fin de Grado (TFG) dedicado a la Mejora de Imágenes de Resonancia Magnética Tridimensionales aplicando técnicas de Inteligencia Computacional. Estas herramientas están diseñadas específicamente para trabajar con imágenes en formato NIfTI y abordan diferentes aspectos del flujo de trabajo de procesamiento y evaluación.

### Contenido:
1. La carpeta https://github.com/koopa31/SegSRGAN/tree/cc393b9a702a23be3075bae6e80924e2d05c66fe



1. Cuaderno de Jupyter para Visualización de Imágenes NIfTI: Este cuaderno proporciona código y ejemplos para la visualización de imágenes médicas en formato NIfTI, permitiendo una mejor comprensión y exploración de los datos.

2. Cuaderno de Jupyter para Preprocesamiento de Imágenes NIfTI: Este cuaderno contiene las funciones y técnicas de preprocesamiento que se han utilizado durante el desarrollo de mi proyecto para su posterior utilización con el modelo SegSRGAN.

3. Archivos del Modelo SegSRGAN: Se incluyen los archivos del modelo SegSRGAN, provenientes de otro repositorio, para facilitar su acceso y utilización en este contexto.

4. Carpeta de Pesos del Reentreno: Esta carpeta contiene los pesos obtenidos en cada época del reentreno del modelo SegSRGAN llevado a cabo durante el proyecto. El reentreno se realizó con 40 imágenes del conjunto de datos ATLAS v2.0 para poder obtener mejores resultados de súper-resolución. Para el conjunto de datos ATLAS v2.0, los pesos que mejor resultado proporcionaban son los de la época 215.

5. Cuaderno de Jupyter para Evaluación de Resultados con el Modelo SegSRGAN: Este cuaderno incluye código para evaluar los resultados obtenidos utilizando el modelo SegSRGAN. Se emplean las métricas PSNR, SSIM e IFC para evaluar la súper-resolución comparando las imágenes HR ground-truth con las generadas por el modelo. La segmentación generada por el modelo es evaluada mediante el índice DICE.
