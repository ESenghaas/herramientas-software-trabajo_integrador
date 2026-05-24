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
