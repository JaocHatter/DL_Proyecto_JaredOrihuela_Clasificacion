# DL_Proyecto_JaredOrihuela_Clasificacion
Fine-tuning YoloV12 and RT-DETR for traffic surveillance, the final project of the Deep Learning course taught by PhawAI
## Resumen del Proyecto

Este repositorio contiene el código y los resultados del proyecto final del módulo de Deep Learning de Phaw AI 2025. El objetivo del proyecto es comparar el rendimiento de los modelos de detección de objetos **YOLOv12 (sin fine-tuning)**, **YOLOv12 (con fine-tuning)** y **RT-DETR (con fine-tuning)** para la tarea de detección de vehículos desde una perspectiva aérea. El análisis se realiza sobre un dataset personalizado, evaluando métricas clave como la **precisión media promedio (mAP)**, la **velocidad de inferencia** y la **matriz de confusión**.

El proyecto demuestra la importancia del ajuste fino (*fine-tuning*) de modelos pre-entrenados para una tarea específica, concluyendo que **YOLOv12 (con fine-tuning)** es el modelo con mejor desempeño general, ofreciendo una combinación óptima de alta precisión y velocidad de inferencia.

## Dataset

* **Nombre:** Top-View Vehicle Detection Image Dataset
* **Fuente:** [Kaggle](https://www.kaggle.com/datasets/farzadnekouei/top-view-vehicle-detection-image-dataset)
* **Licencia:** Apache 2.0
* **Clases:** El dataset contiene una única clase, **'Vehicle'**, con imágenes de coches, camiones y autobuses tomadas desde vistas aéreas.
* **División:** 536 imágenes para entrenamiento y 90 imágenes para validación.

## Guía de Ejecución

Para replicar este proyecto, se recomienda utilizar un entorno de **Kaggle Notebooks** debido a la facilidad de acceso al dataset y a los recursos computacionales necesarios.

1.  **Abrir el Notebook:** Accede al notebook del proyecto en el siguiente enlace:
    [https://www.kaggle.com/code/jarex616/deeplearning-trabajofinal-jared](https://www.kaggle.com/code/jarex616/deeplearning-trabajofinal-jared)

2.  **Configurar el entorno:**
    * Ve a la pestaña **`File`** y selecciona **`Open`**.
    * En la pestaña de **`Settings`** o **`Configuración`** de tu notebook, asegúrate de que el **`Accelerator`** esté configurado como **GPU** y que el tipo de GPU sea **`P100`**.

3.  **Ejecución:**
    * El notebook está estructurado de manera secuencial, por lo que simplemente ejecuta cada celda de código de arriba a abajo.
    * El notebook incluye la instalación de las librerías necesarias, la carga del dataset, el entrenamiento de los tres modelos (YOLOv12 sin *fine-tuning*, YOLOv12 con *fine-tuning* y RT-DETR con *fine-tuning*), la evaluación de sus métricas de rendimiento y la generación de los gráficos y matrices de confusión.

## Cómo Generar Resultados

Los resultados y gráficos del entrenamiento se guardan automáticamente en la carpeta `runs/detect/`. Para generar y acceder a los archivos utilizados en el informe, sigue estos pasos:

1.  Ejecuta todas las celdas del notebook hasta el final.
2.  En la última celda del notebook, se utiliza un comando de shell para comprimir la carpeta de resultados en un archivo `.zip`.
3.  Una vez completada la ejecución, la carpeta `/kaggle/working/runs/detect/train/` contendrá todos los gráficos y archivos `.csv` necesarios para el análisis y la tabla comparativa. Puedes descargarlos directamente desde el panel de salida del notebook en Kaggle.

## Enlace al Código

El código completo del proyecto está disponible en el siguiente notebook de Kaggle:

* **Notebook de Kaggle:** [https://www.kaggle.com/code/jarex616/deeplearning-trabajofinal-jared](https://www.kaggle.com/code/jarex616/deeplearning-trabajofinal-jared)

