# CHANGELOG

## Sprint 1

### Día 1 — Ejercicio 01
Inicialización del repositorio Git.
Creación de la rama Sprint_1.
Generación de la estructura de directorios del proyecto.
Creación de README.md y CHANGELOG.md.

### Día 2 — Ejercicio 02

Descarga del dataset original y almacenamiento
Análisis de tipos de datos y valores nulos.

### Día 3 — Ejercicio 03
Normalizacion de fechas y horas
Normalización de Ubicaciones y Patentes + Eliminación de nulos y Outliers
cálculo de columnas (exceso_velocidad_real/5%) + Filtrado de infracciones + Guardado en interim

### Día 4 — Ejercicio 04
Creación de la Clase FineAnalyzer y todos sus métodos internos

### Día 5 — Ejercicio 05
Gráficos y exportación a /plots

### Día 6 — Ejercicio 06
- Cálculo de porcentajes de error

### Día 7 — Ejercicio 07
- Agrego conclusiones finales al README.md


## SPRINT - 2
### Día 1 — Ejercicio 01
- Creación de rama Sprint_2 a partir de Sprint_1.
- Descarga y descompresión del dataset de imágenes en data/raw/imgs.
- Actualización de README.md con objetivo y contexto del Sprint 2.


### Día 2 — Ejercicio 02
- Listado de imágenes con nombre y tamaño en kb.
- Separación en grupos plates/completes.
- Generación de group_images.json en data/interim.
- Función para mostrar 8 imágenes aleatorias en grilla 2x4.

### Día 3 — Ejercicio 03
- Conversión de imágenes a escala de grises en data/interim/imgs/03_01_gray_scale/plates y completes.
- Suavizado gaussiano en data/interim/imgs/03_02_blur/plates y completes.
- Detección de bordes Canny en data/interim/imgs/03_03_canny/plates y completes.
- Visualización de imágenes procesadas en cada paso.

### Día 4 — Ejercicio 04
- Extracción de patentes de todas las imágenes usando easyocr.
- Match de patentes con dataset de multas (umbral 80%).
- Generación de speeding_fines_image.csv con columnas:
  imagen, patente_imagen, ratio.

### Día 5 — Ejercicio 05
- Cantidad de multas sin imágenes según exceso_velocidad.
- Cantidad de multas con imágenes según exceso_velocidad.
- Cantidad de imágenes sin match con el dataset.
- Cantidad de multas pendientes de pago.
- Cantidad de multas pendientes de pago con imágenes relacionadas.

### Día 6 — Ejercicio 06
- Cálculo de totales y porcentajes de cobertura visual.
- Porcentaje de multas con y sin imagen asociada.
- Porcentaje de multas pendientes de pago con imagen.
- Conclusiones finales del Sprint 2 agregadas al README.md.


## Sprint 3

### Día 1 — Ejercicio 01
- Creación de rama Sprint_3 a partir de Sprint_2.
- Verificación de acceso a todos los datasets generados en sprints anteriores.


### Día 2 — Ejercicio 02
- Creación de directorio /content/remote_dvc como remote DVC local.
- Migración de data/raw/imgs a DVC.
- Migración de data/interim/imgs/03_01_gray_scale a DVC.
- Migración de data/interim/imgs/03_02_blur a DVC.
- Migración de data/interim/imgs/03_03_canny a DVC.


### Día 3 — Ejercicio 03
- Diseño del modelo lógico con clases Vehiculo, Radar, Evidencia y Multa.
- Visualización del diagrama de relaciones entre entidades.

### Día 4 — Ejercicio 04
- Implementación de la función procesar_fila_csv.
- Mapeo de filas del CSV a instancias de las clases del modelo lógico.

### Día 5 — Ejercicio 05
- Diseño del modelo relacional utilizando SQLAlchemy.
- Creación de las tablas Vehiculo, Radar, Multa y Evidencia.
- Definición de claves primarias en todos los modelos.
- Implementación de relaciones entre tablas mediante Foreign Keys y relationship().
- Sobrescritura del método __repr__ para mejorar la legibilidad de los objetos.

### Día 6 — Ejercicio 06
- Creación de la base de datos transito utilizando SQLAlchemy.
- Generación automática de las tablas a partir del modelo relacional.
- Migración de los datos desde el archivo speeding_fines_image.csv.
- Inserción de vehículos, radares, multas y evidencias respetando las relaciones definidas.
- Validación de la cantidad de registros insertados en cada tabla.

### Dia 7 - Ejercicio 07
- Helpers _sep/_header para output tabular consistente.
- Consulta 1: top 10 patentes con mayor cantidad de multas (desc).
- Consulta 2: top 10 multas sin evidencia ordenadas (asc).
- Consulta 3: radares con mayor volumen de infracciones (desc).
- Consulta 4: top 10 patentes reincidentes en periodo dado (desc).
- Consulta 5: porcentaje de multas confirmadas visualmente.


### Día 8 — Ejercicio 08
- Creación de la base de datos vectorial patente_vectorial con OpenCLIP.
- Generación de embeddings de las imágenes con el modelo ViT-B-32.
- Almacenamiento del id del vehículo junto al vector de cada imagen.
- Población de la base vectorial vinculándola con la base relacional.
