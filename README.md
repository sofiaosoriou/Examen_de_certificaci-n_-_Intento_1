# Examen_de_certificaci-n_-_Intento_1

Este proyecto consiste en la limpieza, exploración, modelado y evaluación de modelos de clasificación aplicados a un dataset real de calidad de vinos tintos y blancos.

## Estructura del Proyecto

- dataset/
  - winequality-red.csv
  - winequality-white.csv
- models/
  - modelo_knn_red_wine.pkl
  - modelo_knn_white_wine.pkl
- Sofía Osorio Urrutia - Examen de certificación – Intento 1.ipynb

## Resumen del Análisis

1. Carga y Limpieza de Datos
   - Se cargaron los datasets de vino tinto y blanco.
   - Se eliminaron duplicados y se trataron outliers según normativas internacionales para asegurar la calidad de los datos.

2. Exploración de Datos (EDA)
   - Se realizaron análisis estadísticos y visualizaciones (histogramas, boxplots, mapas de calor, scatterplots) para entender la distribución y relaciones entre variables.
   - Se identificaron correlaciones relevantes, como la relación entre alcohol y calidad.

3. Modelado
   - Se probaron tres modelos de clasificación:
     - **Logistic Regression**
     - **KNeighborsClassifier** (KNN, optimizado con Optuna)
     - **LGBMClassifier** (LightGBM, optimizado con Optuna)
   - Se dividieron los datos en entrenamiento y prueba, y se aplicó escalado de variables numéricas.

4. Evaluación
   - Se evaluó el desempeño de los modelos usando accuracy y matrices de confusión.
   - Resultados principales:
     - Para vino tinto, el mejor modelo fue KNN.
     - Para vino blanco, el mejor modelo fue LGBMClassifier.
     - Logistic Regression tuvo el peor desempeño en ambos casos.

5. Exportación de Modelos
   - Los modelos seleccionados se exportaron en formato `.pkl` para su uso futuro.

## Resultados de Accuracy

| Tipo de Vino | LogisticRegression | KNeighborsClassifier | LGBMClassifier |
|--------------|-------------------|---------------------|---------------|
| Red          | 0.1875            | 0.5367              | 0.357         |
| White        | 0.51388           | 0.5252              | 0.537878      |

## Conclusiones

El modelo KNN es el más adecuado para vinos tintos, mientras que LGBMClassifier es el mejor para vinos blancos.
Se recomienda aumentar la cantidad de datos para vinos tintos para mejorar la precisión de los modelos.
