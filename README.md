# dna-damage-detector-cnn
Automatic comet assay image analysis using CNN and image processing


# Clasificación y Conteo Automático de Células en el Ensayo Cometa
Este proyecto desarrolla un método automático para la clasificación y conteo de células en imágenes del Ensayo Cometa, utilizando técnicas de Procesamiento Digital de Imágenes y Aprendizaje de Máquinas. El Ensayo Cometa es un método ampliamente empleado para estudiar el daño en el ADN de células, pero tradicionalmente su evaluación se realiza de manera manual, lo que consume tiempo y es propenso a errores. Este método automatiza este proceso, logrando una precisión de hasta el 97.44%.
El proyecto actualmente es utilizado en el Laboratorio de Biología Celular de la Pontificia Universidad Javeriana de Cali.

## Características principales
- **Procesamiento de imágenes**: Utiliza técnicas de reconstrucción morfológica (h-domos) para mejorar la calidad de las imágenes y resaltar las células cometa.
- **Modelos de aprendizaje profundo**: Entrena y compara varias arquitecturas de redes neuronales convolucionales (U-Net, UNet++, DeepLabV3+, LinkNet, PAN) con codificador ResNet50 para la segmentación semántica de las células.
- **Aplicación de escritorio**: Interfaz gráfica (desarrollada con PyQt5) que permite cargar imágenes, procesarlas y obtener resultados en formato de imagen etiquetada y archivo Excel con datos cuantitativos de cada célula (área, intensidad, tipo de daño en el ADN).
- **Validación exhaustiva**: Los resultados automáticos se compararon con evaluaciones manuales de expertos, demostrando una mayor precisión y confiabilidad.
## Resultados destacados
- Precisión (IoU Score) de hasta **97.44%** con la arquitectura UNet++ y imágenes procesadas con h-domo (h=200).
- Reducción significativa del tiempo de análisis: de 30-60 minutos (manual) a pocos segundos.
- Clasificación del daño en el ADN en cinco categorías: sin daño, leve, moderado, serio y crítico.
- Comparación favorable con herramientas existentes (como OpenComet), superándolas en precisión y reduciendo falsos positivos/negativos.
## Tecnologías utilizadas
- **Lenguaje de programación**: Python 3.6
- **Librerías principales**:
  - PyTorch (para redes neuronales)
  - OpenCV (procesamiento de imágenes)
  - NumPy, Pandas (manejo de datos)
  - scikit-image (transformaciones de imágenes)
  - Albumentations (aumentación de datos)
  - PyQt5 (interfaz gráfica)
  - Matplotlib, Seaborn (visualización)
- **Herramientas**: ImageJ (preprocesamiento de imágenes), Git (control de versiones).
- **Modelos de ML**: U-Net, UNet++, DeepLabV3+, LinkNet, PAN, ResNet50 (codificador).
## Metodología
1. **Preprocesamiento de imágenes**:
   - Conversión a escala de grises (canal verde) y aplicación de la técnica de h-domos para resaltar las células.
   - Eliminación de ruido y artefactos mediante umbralización y filtrado por área.
2. **Entrenamiento de modelos**:
   - Comparación de cinco arquitecturas de redes neuronales para segmentación semántica (tres clases: cabeza, cola, fondo).
   - Aumentación de datos (espejo vertical) para mejorar la generalización.
   - Validación mediante métricas IoU y Dice loss.
     
3. **Validación**:
   - Comparación con evaluaciones manuales de tres investigadores.
   - Análisis de IoU entre máscaras predichas y Ground Truth.
  
4. **Desarrollo de la aplicación**:
   - CometScanner es una aplicación diseñada para abordar de manera eficiente y precisa la clasificación de células del Ensayo Cometa. Su función principal es evaluar el daño al ADN representado por cada célula en una imagen importada, facilitando así la investigación en biología celular y genética.
   
   - El propósito fundamental de CometScanner es ofrecer a la comunidad científica y a profesionales en biología celular y genética una herramienta avanzada y fácil de usar para la clasificación y cuantificación precisa del daño al ADN en células del Ensayo Cometa. La aplicación está diseñada para agilizar y mejorar significativamente el proceso de análisis de imágenes, permitiendo una investigación más eficiente. Esto se logrará mediante la creación de una interfaz intuitiva que permita la importación y clasificación de imágenes del Ensayo Cometa, la automatización de la clasificación de células según el daño del ADN, la facilitación de la interpretación de resultados a través de una representaci ón visual clara, la personalización de la ubicación de almacenamiento de los resultados para los usuarios, y la provisión de recursos de ayuda, como tutoriales en video, para garantizar una experiencia de usuario sin complicaciones.
## Instalación y uso
El código de este proyecto está disponible en [GitHub](https://github.com/JuanesAF/dna-damage-detector-cnn). Para ejecutar la aplicación:
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/tu-repositorio.git
   cd tu-repositorio
   ```
2. Instalar las dependencias (se recomienda usar un entorno virtual):
   ```bash
   pip install -r requirements.txt
   ```
3. Ejecutar la aplicación:

A continuación, abra su entorno
de desarrollo Python preferido

   ```bash
   python Application.py
   ```
**Nota**: Debe ajustar la ruta del archivo del modelo entrenado en el código "Application". Además, es necesario modificar la ruta del archivo "label_class_dict.csv" dentro del código "model".

## 📁 Estructura del Repositorio

```plaintext
comet-assay-analyzer/
├── Application.py          # Script principal de la interfaz gráfica
├── model.py                # Definición del modelo de segmentación (CNN)
├── hmax.py                 # Procesamiento morfológico (h-domes)
├── label_class_dict.csv    # Diccionario de clases para la clasificación
├── COMETS.ui               # Archivo de diseño de la interfaz (Qt Designer)
├── README.md               # Documentación del proyecto
├── cells.gif               # GIF ilustrativo de células cometa
├── comet.gif               # GIF ilustrativo del proceso
├── videos.gif              # GIF de demostración de uso

## Contribuciones
Las contribuciones son bienvenidas. Si deseas mejorar el proyecto, por favor crea un fork del repositorio y envía tus pull requests.

## Contacto
- E-mail: [jeaf016@hotmail.com](mailto:jeaf016@hotmail.com)
- LinkedIn: [LinkedIn](https://www.linkedin.com/in/juanesacostaf)
---
**Palabras clave**: Procesamiento Digital de Imágenes, Inteligencia Artificial, Redes Neuronales Convolucionales, Ensayo Cometa, ADN, Segmentación Semántica, Aprendizaje Profundo.CNN, AI
