# Práctica 2 ML: Predicción de la demanda eléctrica en España

Práctica 2 de la asignatura de Machine Learning (Máster en Inteligencia Artificial, UMU, curso 2026/27). Todos los ficheros de esta práctica están en la carpeta `Entregable2/` del repositorio.

El objetivo es predecir la **demanda eléctrica real diaria del sistema peninsular para los 7 días siguientes** (*t+1, …, t+7*) a partir de la información disponible hasta el día *t*, con datos abiertos de Red Eléctrica de España (REData) entre el 1 de enero de 2021 y el 31 de diciembre de 2023. El modelo debe poder usarse en la práctica, así que al predecir solo puede utilizar la información que realmente existe en ese instante. Los modelos se construyen con `skforecast`.

**Estado:** en curso.

## Componentes del grupo

- Alberto Caballero Tello (alberto.caballerot@um.es)
- Cesar Martín Castellanos (cesar.m@um.es)
- Jose Francisco González (josefrancisco.gonzalem@um.es)

## Estructura de la carpeta

| Fichero | Descripción |
|---|---|
| `ML-Entregable2.ipynb` | Notebook principal: EDA, preprocesado, selección de variables, modelos, evaluación y conclusiones |
| `data/ree_horario.csv` | Demanda real, prevista y programada (MW) y precios spot y PVPC (€/MWh), una fila por hora (26.280 filas) |
| `data/ree_generacion_diaria.csv` | Energía generada por tecnología (MWh), una fila por día (1.095 filas) |
| `requirements.txt` | Librerías y versiones exactas usadas |
| `Practica_2_Machine_Learning_Demanda_Ele_ctrica.pdf` | Enunciado de la práctica |

## Cómo reproducirlo

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/alberct96/ML-Entregables.git
   cd ML-Entregables/Entregable2
   ```
2. Crear y activar un entorno virtual (Python 3.12):
   ```bash
   python -m venv .venv
   # Windows
   .venv\Scripts\activate
   # Linux / Mac
   source .venv/bin/activate
   ```
3. Instalar las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
4. Abrir `ML-Entregable2.ipynb` con Jupyter o VS Code y ejecutar todas las celdas en orden. El notebook usa rutas relativas a su carpeta (`data/`), así que el directorio de trabajo debe ser `Entregable2/` (es lo que hacen por defecto Jupyter y VS Code).

La semilla aleatoria está fijada (`SEED = 42`) para que los resultados sean reproducibles.

## Evolución del proyecto

### Semana 1 (23 nov - 29 nov): puesta en marcha

- Creada la carpeta `Entregable2/` con el enunciado y los datos.
- `requirements.txt` con las versiones fijadas de la asignatura, incluidas `skforecast`, `statsmodels` y `optuna`.
- Notebook con la estructura de la práctica según el enunciado: análisis exploratorio, preprocesado, selección de variables, modelado con `skforecast`, evaluación, análisis estadísticos (opcional) y conclusiones.
