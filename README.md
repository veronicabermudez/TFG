# TFG
## Repositorio de Herramientas para Procesamiento, Súper-Resolución, Segmentación y Evaluación de Imágenes Médicas
Este repositorio contiene una serie de herramientas y cuadernos de Jupyter que han sido útiles en el desarrollo de mi Trabajo de Fin de Grado (TFG) dedicado a la Mejora de Imágenes de Resonancia Magnética Tridimensionales aplicando técnicas de Inteligencia Computacional. Estas herramientas están diseñadas específicamente para trabajar con imágenes en formato NIfTI y abordan diferentes aspectos del flujo de trabajo de procesamiento y evaluación. Además se incluyen las herramientas referentes al modelo SegSRGAN de aprendizaje profundo, utilizado durante el trabajo. 

### Contenido:
1. El cuaderno de Jupyter TFG/PreprocesamientoImagenes.ipynb/ contiene los pasos seguidos para el preprocesamiento de las imágenes NIfTI empleadas durante el proyecto. Estos pasos han sido realizados previamente a la realización de pruebas con el modelo de aprendizaje profundo o a su propio entrenamiento.

2. La carpeta https://github.com/koopa31/SegSRGAN/tree/cc393b9a702a23be3075bae6e80924e2d05c66fe es un subdirectorio dentro de este. Se trata del código referente al modelo de aprendizaje profundo SegSRGAN, el cual ha sido elegido como estrategia para conseguir la súper-resolución y segmentación de imágenes MRI en este proyecto.

3. La carpeta TFG/Archivos csv utilizados/ se trata de un conjunto de archivos que han sido objeto del modelo de aprendizaje profundo para su entrenamiento (ATLAS_E.csv) y para distintas pruebas (ATLAS_P10.csv, ATLAS_P9.csv y OASIS_P7.csv). Estos archivos contienen las rutas de los datos empleados en cada caso. Para todas las pruebas del proyecto se han utilizado archivos con esta estructura. 

4. La carpeta TFG/training_weights/ contiene todas las versiones de los pesos generados durante el reentrenamiento del modelo SegSRGAN. El reentreno se realizó con 40 imágenes del conjunto de datos ATLAS v2.0 para poder obtener mejores resultados de súper-resolución. Para estas imágenes, los pesos que mejor resultado proporcionaban son los de la época 215.

5. La carpeta TFG/weights_TFG/ incluye los pesos que se han utilizado en las pruebas iniciales del modelo de aprendizaje profundo (Perso_without_data_augmentation) y en las pruebas finales (SegSRGAN_epoch_215_TFG), posteriores a su reentreno.

6. La carpeta TFG/Evaluación/ contiene archivos relativos a la evaluación de los resultados del proyecto. En primer lugar, el cuaderno de Jupyter EvaluacionResultados.ipynb está compuesto por código para la evaluación de las imágenes producidas por el modelo de aprendizaje profundo. Se emplean las métricas PSNR, SSIM e IFC para evaluar la súper-resolución comparando las imágenes HR ground-truth con las generadas por la arquitectura SegSRGAN. Por otro lado, la segmentación generada por el modelo es evaluada mediante el índice DICE. Se incluyen también gráficas que facilitan dicha evaluación. Además en esta carpeta se incluyen los archivos dice_entreno.csv y psnr_entreno.csv con los resultados de índice DICE y PSNR, respectivamente, para los pesos generados durante cada epoch del reentreno del modelo. 

7. Por último, el cuaderno de Jupyter TFG/VisualizacionNIfTI.ipynb/ proporciona código y ejemplos para la visualización de imágenes médicas en formato NIfTI, permitiendo una mejor comprensión y exploración de los datos.
