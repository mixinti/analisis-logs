# Analisis de Logs e Identificacion de Incidentes

Este repositorio contiene un entorno de analisis basado en Jupyter Notebooks para procesar logs estructurados de servidores, identificar momentos criticos de fallas en el sistema y diagnosticar las causas raiz mediante comparaciones contra baselines.

## Caracteristicas Tecnicas

* **Procesamiento de Series Temporales:** Agrupacion y remuestreo de eventos en ventanas de tiempo dinamicas (5 minutos) para identificar picos de error.
* **Deteccion de Anomalias:** Calculo del porcentaje de eventos fallidos (bad rate) y filtrado de ruido para aislar el periodo exacto del incidente.
* **Diagnostico de Causa Raiz:** Segmentacion automatica de errores por servicio, endpoint y mensajes de error mas frecuentes durante la falla.
* **Analisis Comparativo:** Evaluacion del comportamiento del incidente frente al rendimiento normal (baseline) en terminos de latencia, tasa de error y respuestas 5xx.

## Arquitectura del Proyecto

* `Analis de Logs.ipynb`: Notebook principal que realiza la carga de datos, exploracion, deteccion del momento critico, diagnostico y graficacion.
* `server_logs.csv`: Dataset con los registros de auditoria, marcas de tiempo, latencias y codigos de estado HTTP de los microservicios.
