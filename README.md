# TP Final Integrador — Predicción de Cancelaciones Amazon

Notebook de análisis y modelado predictivo para detectar órdenes canceladas en ventas de Amazon.

## Requisitos

- Python 3.10+
- Jupyter Notebook o JupyterLab

## Instalación

1. Crear entorno virtual (recomendado):

```bash
python -m venv venv
```

2. Activar el entorno:

**Windows (PowerShell):**
```powershell
.\venv\Scripts\Activate.ps1
```

**Windows (CMD):**
```cmd
venv\Scripts\activate.bat
```

**Linux/macOS:**
```bash
source venv/bin/activate
```

3. Instalar dependencias:

```bash
pip install -r requirements.txt
```

## Ejecución

1. Colocar el archivo `Amazon Sale Report.csv` en la misma carpeta que el notebook.

2. Iniciar Jupyter:

```bash
jupyter notebook
```

3. Abrir `TP_FINAL_INTEGRADOR.ipynb` y ejecutar las celdas en orden (Cell → Run All).

## Estructura del Proyecto

```
Tp_final_integrador/
├── TP_FINAL_INTEGRADOR.ipynb   # Notebook principal
├── Amazon Sale Report.csv                # Dataset (no incluido en repo)
├── requirements.txt                      # Dependencias Python
└── README.md                             # Este archivo
```

## Modelos Implementados

| Modelo | Preprocesamiento | Manejo de Desbalanceo |
|--------|-----------------|----------------------|
| Logistic Regression | StandardScaler + OneHotEncoder | class_weight='balanced' |
| Random Forest | StandardScaler + OneHotEncoder | class_weight='balanced' |

## Métricas Evaluadas

- Accuracy
- AUC-ROC
- Precision, Recall, F1-Score
- Validación cruzada 5-fold estratificada
- Matriz de confusión
- Importancia de variables
