# Urban Flow

## Sprint 1

## Objetivo
Aplicar conocimientos de versionado, organización y limpieza
de código, y utilización de pandas para depurar datos históricos
de multas por exceso de velocidad.

## Introducción y Contexto
La localidad de Vaalserberg (Bélgica), en zona fronteriza con
Países Bajos y Alemania, cuenta con radares urbanos de detección
de infracciones por exceso de velocidad.
Los registros históricos provienen de sistemas heredados con
errores de formato y datos faltantes, generando registros
inconsistentes en el nuevo sistema.
El objetivo del Sprint 1 es analizar y depurar esos datos para
poder incorporarlos al nuevo sistema sin inconsistencias.

## Conclusiones Finales
Analizando los datos del dataset se observan una gran cantidad de datos mal
formateados provientes del sistema anterior.

Durante la limpieza de los datos , a las horas inválidas se reemplazaron
por 00:00 y esto generó que el gráfico de infracciones por hora muestre
una concentración de multas en la medianoche y esto no refleja la realidad
sino la acumulación de datos sucios.
Lo mismo Ocurrió con las fechas reemplazadas por 1932-01-01,
una fecha claramente irreal pero altero los datos de los promedios.

Una mejora posible sería excluir del análisis estadístico los registros con
fecha 1932-01-01 y hora 00:00, tratándolos como datos faltantes en lugar de
valores reales, lo que daría resultados más representativos del
comportamiento real de las infracciones.
