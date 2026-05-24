# Urban Flow

## Sprint actual: Sprint 2

## Objetivo

Desarrollar un sistema que determine qué multas de velocidad
tienen evidencia visual válida, relacionando el dataset de
infracciones con imágenes capturadas por los radares urbanos.

## Introducción y contexto

Los radares urbanos de Vaalserberg generan registros
administrativos de multas de forma automática. Las cámaras
asociadas registran evidencia visual que acompaña y valida
cada infracción. Sin embargo, no todas las multas tienen imagen
asociada, no todas las imágenes corresponden a una infracción,
y puede haber errores de detección.

En este sprint se procesa el dataset de imágenes, se extraen
las patentes mediante OCR y se relacionan con el dataset
depurado del Sprint 1.
