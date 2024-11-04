# Trading con Machine Learning: Clasificación

El mundo del trading financiero es un entorno **altamente competitivo y dinámico**, donde predecir los movimientos del mercado representa un desafío constante, incluso para los profesionales más experimentados. Con una sólida experiencia en el campo del trading, me he propuesto crear un modelo de **Machine Learning (ML)** para mejorar mi desempeño en los mercados y aplicar estos conocimientos en un entorno real.

---

## Hipótesis del Proyecto

Este proyecto busca responder a la pregunta: ¿Es posible mejorar el rendimiento de una estrategia de trading mediante la aplicación de modelos de clasificación de Machine Learning? La hipótesis es que, al **identificar y aprender patrones en operaciones exitosas**, se puede filtrar aquellas operaciones con menor probabilidad de éxito, optimizando así el rendimiento general de la estrategia.

## Objetivo General

El objetivo principal de este proyecto es mejorar cuatro métricas clave de una estrategia de trading mediante modelos de clasificación de ML:

- **Return [%]**: Aumentar el retorno porcentual de la inversión.
- **Max. Drawdown [%]**: Reducir el drawdown máximo, minimizando las pérdidas acumuladas.
- **Win Rate [%]**: Incrementar la tasa de operaciones ganadoras respecto al total de operaciones.
- **Número de trades perdidos consecutivos**: Disminuir esta métrica para permitir una gestión de riesgo más agresiva y confiable.

## Metodología del Proyecto

El proyecto se estructura en tres fases, cada una diseñada para maximizar el rendimiento de la estrategia y explorar las capacidades de Machine Learning en un contexto de trading.

### 1. Backtest de la Estrategia Inicial

Este módulo se centra en la estrategia algorítmica original, evaluando sus resultados, fortalezas y debilidades. El objetivo es comprender a fondo el funcionamiento de la estrategia antes de incorporar Machine Learning, estableciendo una línea de base sobre la cual se medirán las mejoras.

### 2. Modelado y Optimización de Modelos de ML

Este es una introducción de la lógica utilizada para el modelado de los algoritmos:

- **Modelado para Operaciones Largas y Cortas**: Al entrenar modelos separados para operaciones largas y cortas, cada modelo puede captar patrones específicos y optimizar sus predicciones para cada tipo de operación.

- **Ingeniería de Características Clave**: Para mejorar la precisión del modelo y enfocarse en información relevante, se implementa una ingeniería de características detallada que agrupa los indicadores técnicos en ventanas temporales. Este enfoque permite extraer patrones significativos mientras se controla la dimensionalidad del modelo. En lugar de utilizar cada valor individual de los indicadores técnicos, se calculan métricas estadísticas (media, desviación estándar, mínimo, máximo, mediana, entre otras) en una ventana de tiempo de 3 periodos para cada característica.

- **Selección Estratégica de Características y Evaluación de Modelos**: Utilizando un análisis iterativo basado en la importancia de características, el proyecto evalúa y compara múltiples algoritmos, como **XGBoost**, **LightGBM**, y **CatBoost**, para seleccionar el modelo con el mayor potencial de rendimiento y menor riesgo.

- **Optimización y Afinación Precisa**: Mediante la optimización de hiperparámetros con validación cruzada temporal (**TimeSeriesSplit**), el modelo se ajusta a los datos específicos de series temporales, maximizando su precisión en un entorno volátil.

### 3. Análisis de Resultados y Conclusiones

En esta fase, se interpretan los resultados obtenidos para evaluar el impacto de los modelos de ML en las métricas clave de la estrategia de trading. Se extraen conclusiones sobre la efectividad del modelo mejorado y se plantean recomendaciones para futuros ajustes y optimizaciones. 

Este análisis permite ver de manera integral cómo el modelo de ML ha transformado la estrategia inicial, destacando las áreas de mejora y las oportunidades para seguir explorando nuevas metodologías.

---

Este README proporciona una visión general del proceso, con detalles adicionales disponibles en los notebooks correspondientes a cada módulo. A medida que se continúa explorando y ajustando la estrategia, los próximos pasos incluyen la experimentación con otros modelos, como redes neuronales, y el análisis de patrones más complejos para perfeccionar aún más el rendimiento en trading.
