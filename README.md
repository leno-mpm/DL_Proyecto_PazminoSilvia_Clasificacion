# Proyecto: Clasificación de Enfermedades en Hojas de Manzano

## 📂 Ruta y Dataset
- **Ruta del proyecto:** `CLASIFICACION`
- **Dataset utilizado:** Plant Pathology 2020 — Foliar Disease of Apples
  - Fuente: [Kaggle](https://www.kaggle.com/datasets/emmarex/plant-pathology-2020-fgvc7)
  - Contiene 3,651 imágenes de hojas de manzano con las siguientes clases:
    - Apple scab
    - Cedar apple rust
    - Healthy
  - Licencia: Pública para fines educativos y de investigación.

## ⚙️ Cómo ejecutar
1. Abrir el notebook en **Google Colab** o **Jupyter Notebook**.
2. Seleccionar entorno con **GPU** (si aplica) para acelerar el entrenamiento.
3. Asegurarse de que la carpeta `DATASET` esté ubicada en la ruta `CLASIFICACION/` dentro de tu Google Drive o en tu equipo.


## 📦 Instalación de dependencias
- Se incluye un archivo `requirements.txt` con todas las librerías necesarias.
- En Colab o Jupyter, ejecutar al inicio del notebook:
```python
!pip install -r /ruta/al/archivo/requirements.txt```
Esto instalará automáticamente TensorFlow, scikit-learn, matplotlib, seaborn, pandas, numpy y otros paquetes necesarios.

## 🏋️‍♀️ Cómo entrenar y evaluar
1. Cargar las imágenes y archivos CSV (`train.csv`, `test.csv`, `sample_submission.csv`).
2. Preprocesar los datos:
   - Redimensionar imágenes a 224x224.
   - Normalizar valores de píxeles entre 0 y 1.
   - Dividir en `train`, `validation` y `test`.
3. Entrenar modelos de clasificación usando **Transfer Learning** con 3 arquitecturas:
   - ResNet50
   - MobileNetV2
   - EfficientNetB0
4. Realizar Fine-Tuning si aplica para mejorar desempeño.
5. Evaluar los modelos usando las métricas:
   - Accuracy
   - F1 macro
   - Precision macro
   - Recall macro
6. Generar matrices de confusión para cada modelo y guardar los resultados en `/results`.

## 📊 Cómo generar la tabla y el gráfico de métricas
1. Al final del entrenamiento, ejecutar el bloque de evaluación que calcula métricas para cada modelo.
2. Se genera un archivo CSV `model_metrics.csv` en la carpeta `/results`.
3. Las gráficas de métricas (accuracy, F1, precision, recall) se guardan como imágenes PNG en `/results/evaluation_figures/`.
4. Las inferencias de ejemplo también se guardan en `/results/final_results/inference_images/`.


---
**Nota:** Todos los resultados y figuras se encuentran organizados dentro de la carpeta `/results` para facilitar su revisión y descarga.
