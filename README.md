# Trading con Machine Learning: Clasificación

El mundo del trading financiero es un entorno **altamente competitivo y dinámico**, donde predecir los movimientos del mercado representa un desafío constante, incluso para los profesionales más experimentados. Con una sólida experiencia en el campo del trading, me he propuesto crear mi primer modelo de **Machine Learning (ML)** para mejorar mi desempeño en los mercados y aplicar estos conocimientos en un entorno real.

## Hipótesis del Proyecto

¿Es posible mejorar el rendimiento de una estrategia de trading mediante la aplicación de modelos de clasificación de Machine Learning? Esta es la pregunta central que guía este proyecto. La hipótesis es que, al **identificar y aprender patrones** presentes en operaciones exitosas, es posible filtrar aquellas operaciones con menor probabilidad de éxito, optimizando así el rendimiento general de la estrategia.

## Objetivo General

El objetivo principal de este proyecto es mejorar cuatro métricas clave de una estrategia de trading mediante la aplicación de modelos de clasificación de ML:

- **Return [%]**: Aumentar el retorno porcentual de la inversión.
- **Max. Drawdown [%]**: Reducir el drawdown máximo, minimizando las pérdidas desde el pico hasta el valle más profundo.
- **Win Rate [%]**: Incrementar el porcentaje de operaciones ganadoras respecto al total de operaciones realizadas.
- **Número de trades perdidos consecutivos**: Disminuir esta métrica para poder gestionar el riesgo de manera más agresiva.

## Enfoques Metodológicos

Para abordar la hipótesis, el proyecto sigue un enfoque principal:

- **Aprendizaje de Patrones en Operaciones Ganadoras**: Analizar si existen patrones distintivos en las entradas ganadoras que el modelo de ML pueda aprender. Este aprendizaje permitiría filtrar las operaciones de menor calidad, optimizando la selección de trades y, en última instancia, mejorando la estrategia general.

## Metodología del Proyecto

El desarrollo del proyecto sigue una estructura organizada en tres fases:

### 1. Backtest de la Estrategia Inicial
  - **1.1 Carga y preparación de datos**: Recolectar y procesar los datos históricos necesarios para la estrategia de trading.
  - **1.2 Lógica de la estrategia y backtest**: Implementar la lógica de la estrategia base y ejecutar el backtest para evaluar su rendimiento inicial.
  - **1.3 Análisis de resultados**: Interpretar los resultados del backtest inicial para establecer una línea de base y definir las métricas de mejora.

### 2. Modelado y Optimización de Modelos de ML
  - **2.1 Evaluación preliminar y selección de modelos**: Entrenar rápidamente múltiples modelos (como **CatBoost**, **Random Forest**, y **LightGBM**) para evaluar su rendimiento en función del AUC Score. Esto permite identificar el modelo con mayor potencial.
  - **2.2 Optimización de hiperparámetros**: Ajustar el modelo seleccionado utilizando **RandomizedSearchCV** con validación cruzada temporal (**TimeSeriesSplit**), para maximizar su capacidad predictiva y adaptarlo a los datos de la serie temporal.
  - **2.3 Separación de operaciones largas y cortas**: Entrenar modelos separados para operaciones largas y cortas, lo que permite capturar mejor las características específicas de cada tipo de operación.
  - **2.4 Ingeniería de características**: Generar métricas estadísticas (promedio, mínimo, máximo) en ventanas temporales de lag para capturar información clave, facilitando así la capacidad predictiva del modelo.
  - **2.5 Selección de características para cortos**: Filtrar las características menos relevantes en el modelo de cortos utilizando la importancia de características del **LGBMClassifier**, aplicando un filtro de 20% para optimizar el modelo.

### 3. Análisis de Resultados y Conclusiones
  - **3.1 Interpretación de resultados**: Evaluar el impacto de los modelos de ML en las métricas clave de la estrategia de trading, comparando el rendimiento optimizado frente a la estrategia original.
  - **3.2 Conclusiones y próximos pasos**: Determinar la viabilidad y efectividad de la estrategia mejorada, y explorar posibles optimizaciones y ajustes para mejorar aún más el rendimiento del modelo en el futuro.

## Resultados y Conclusión

Este proyecto presenta un análisis exhaustivo de la aplicación de Machine Learning en el trading, mostrando el potencial de los modelos de clasificación para mejorar las métricas de rendimiento de una estrategia de trading. Los resultados obtenidos han permitido optimizar el **win rate** y reducir el **drawdown máximo**, acercándome al objetivo de desarrollar una estrategia más robusta y rentable.

Este README proporciona una visión general del proceso, con detalles adicionales disponibles en los notebooks correspondientes a cada módulo. A medida que continúo explorando y ajustando esta estrategia, los siguientes pasos incluyen experimentar con otros modelos de ML, como redes neuronales, y probar enfoques alternativos para la identificación de patrones en el trading.
