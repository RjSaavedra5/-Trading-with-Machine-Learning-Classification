|-- /data/                     # Carpeta para almacenar los datos históricos o preprocesados
|   |-- historical_data.csv     # Datos crudos para entrenar el modelo
|   |-- preprocessed_data.csv   # Datos limpios y preprocesados
|
|-- /notebooks/                 # Notebooks para EDA y modelado
|   |-- 01_EDA.ipynb            # Análisis exploratorio de datos
|   |-- 02_Model_Training.ipynb # Entrenamiento de modelos ML
|   |-- 03_Backtesting.ipynb    # Backtesting de la estrategia optimizada
|
|-- /models/                    # Carpeta para almacenar modelos entrenados
|   |-- model_lgbm.pkl          # Modelo entrenado en LightGBM
|   |-- model_xgboost.pkl       # Modelo entrenado en XGBoost
|
|-- /src/                       # Código fuente con las funciones principales del proyecto
|   |-- __init__.py             # Inicializador del paquete
|   |-- data_processing.py      # Funciones para limpiar y procesar datos
|   |-- feature_engineering.py  # Funciones para generar características
|   |-- model_training.py       # Funciones para entrenar y evaluar modelos
|   |-- backtesting.py          # Funciones para el backtesting de la estrategia
|
|-- /docs/                      # Documentación del proyecto
|   |-- requirements.txt        # Librerías necesarias para el proyecto
|   |-- README.md               # Archivo README con la descripción del proyecto
|
|-- main.py                     # Script principal para ejecutar todo el pipeline
|-- .gitignore                  # Especifica qué archivos/directorios no incluir en el repositorio
