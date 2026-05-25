
## Sprint 2

### Objetivo

Aplicar conocimientos de tratamiento de imágenes para desarrollar un
sistema que determine qué multas de velocidad cuentan con evidencia visual
válida, relacionando el dataset depurado del Sprint 1 con las imágenes
capturadas por los radares urbanos.

### Introducción y Contexto

Los radares generan registros administrativos de multas de forma automática
y las cámaras asociadas registran la evidencia visual que valida cada
infracción. Sin embargo, no todas las multas tienen imagen asociada,
no todas las imágenes corresponden a una infracción, y puede haber errores
de detección. El objetivo del Sprint 2 es procesar el dataset de imágenes,
extraer las patentes mediante OCR y relacionarlas con el dataset depurado
del Sprint 1.

### Conclusiones Finales

Analizando los datos del dataset se observa que de un total de 1731
multas procesadas únicamente 330 cuentan con una imagen asociada que
haya podido ser vinculada mediante OCR, lo que representa apenas un
19% de cobertura visual. Esto significa que más del 80% de las
infracciones registradas no tienen evidencia visual válida que
respalde la sanción.

Durante el proceso de matching se identificaron 94 imágenes que no
pudieron asociarse a ninguna multa del dataset, lo que evidencia las
limitaciones del procesamiento sobre imágenes reales.

En cuanto al impacto sobre el cobro, de las 433 multas pendientes de
pago solo 88 (un 20%) cuentan con imagen asociada, lo que implica que
la mayoría de las infracciones impagas no podrían ser respaldadas
visualmente en caso de un reclamo o disputa.

Una mejora posible sería revisar los mecanismos de captura visual
asociados a cada infracción para aumentar la cobertura de evidencia, y
ajustar los criterios de detección de patentes para reducir la
cantidad de imágenes sin match, lo que daría un sistema más robusto.
