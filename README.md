# Semana 8 — Algoritmos de clasificación

**Autor:** David Alonso Torres Rivas  
**Programa:** Especialización en Analítica y Ciencia de Datos — Universidad de Cundinamarca

## Objetivo
Comparar Decision Tree, Random Forest, SVM, K-NN y Naive Bayes sobre un mismo problema.

## Datos
Se usa `load_breast_cancer()` de Scikit-learn: 569 observaciones y 30 variables predictoras. Según la guía, `1 = maligno` y `0 = benigno`.

> Ejercicio académico; no es una herramienta de diagnóstico médico.

## Metodología
- Partición común 80/20, `random_state=42`, `stratify=y`.
- Decision Tree: `max_depth=4`. Random Forest: 100 árboles.
- SVM: kernel RBF con escalamiento. K-NN: k=5 con escalamiento. Naive Bayes: GaussianNB sin escalamiento.
- Métricas: Accuracy, Precision, Recall, F1-score y matriz de confusión.
- Selección: priorizar Recall para maligno; F1-score y Accuracy como criterios secundarios.

## Resultados de referencia

| Modelo        |   Accuracy |   Precision |   Recall |   F1-score |
|:--------------|-----------:|------------:|---------:|-----------:|
| Decision Tree |     0.9123 |      0.9444 |   0.8095 |     0.8718 |
| Random Forest |     0.9737 |      1.0000 |   0.9286 |     0.9630 |
| SVM           |     0.9737 |      1.0000 |   0.9286 |     0.9630 |
| K-NN          |     0.9561 |      0.9744 |   0.9048 |     0.9383 |
| Naive Bayes   |     0.9386 |      1.0000 |   0.8333 |     0.9091 |

## Archivos
- `Semana8_Algoritmos_Clasificacion.ipynb`: notebook comentado.
- `Informe_Semana8_Clasificacion.pdf`: informe breve.
- `resultados_comparacion.csv`: métricas y conteos de las matrices.
- `figuras/`: comparación de métricas y matrices por modelo.
- `requirements.txt`: dependencias.

## Ejecución
Abrir el notebook en Google Colab y ejecutar las celdas en orden. No se requiere descargar un CSV porque el dataset se carga desde Scikit-learn. Para entorno local: `pip install -r requirements.txt`.

## Fuentes
- https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html
- https://scikit-learn.org/stable/modules/model_evaluation.html#classification-metrics
- https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic
