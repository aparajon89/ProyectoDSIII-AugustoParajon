# ProyectoDSIII – Augusto Parajón  
Análisis predictivo de demanda y riesgo de quiebre de stock en e-commerce mediante Deep Learning y NLP

Proyecto Final – Data Science III  
Autor: Augusto Parajón  
Fecha: 2026  

---

## Descripción del proyecto

Este proyecto aborda un problema crítico del canal e-commerce en retail: la dificultad de anticipar quiebres de stock en un contexto caracterizado por alta intermitencia de la demanda, rotación frecuente del catálogo y decisiones operativas mayormente reactivas.

El objetivo central no es predecir ventas con exactitud transaccional, sino reducir la incertidumbre en la planificación, anticipando situaciones de riesgo mediante un enfoque integrado de análisis exploratorio, modelado predictivo con Deep Learning y una capa interpretativa basada en Procesamiento de Lenguaje Natural (NLP).

El sistema desarrollado está orientado a funcionar como una herramienta de alerta temprana, alineada con la lógica real de negocio, que permita priorizar decisiones de abastecimiento y gestión del surtido antes de que se materialicen quiebres de stock en el canal digital.

---

## Objetivos

- Construir una señal de demanda histórica consistente a partir de datos reales de ventas.
- Analizar la estructura de la demanda y su grado de intermitencia a distintos niveles de agregación.
- Identificar el nivel óptimo de modelado para aplicaciones predictivas.
- Desarrollar un modelo de Deep Learning que actúe como señal anticipada de demanda futura.
- Incorporar NLP como capa analítica complementaria para interpretar el mix de productos.
- Integrar predicción y stock en una lógica de negocio orientada a la gestión del riesgo de quiebre.
- Traducir resultados técnicos en criterios accionables para el uso operativo diario.

---

## Datos utilizados

Origen: datos internos simulados de un entorno retail e-commerce.

Fuentes principales:
- Ventas históricas con información de producto.
- Stock disponible.
- Clasificación de productos (Rubro y Familia).

Nivel de análisis:
- SKU (uso exploratorio).
- Familia (nivel principal de modelado y decisión).

Variables clave:
- Fecha  
- SKU  
- Demanda diaria  
- Rubro  
- Familia  
- Descripción de producto (para NLP)

---

## Metodología

### Preparación de datos
- Limpieza y depuración de ventas (anulaciones y notas de crédito).
- Normalización de claves de producto.
- Construcción de un panel SKU–día completo.
- Tratamiento controlado de intermitencia extrema.
- Validaciones de cobertura y consistencia.

### Análisis exploratorio de datos (EDA)
- Análisis temporal global de la demanda.
- Evaluación de intermitencia a nivel SKU.
- Comparación de niveles de agregación: SKU, Rubro y Familia.
- Decisión empírica del nivel Familia como base del modelado.

### Deep Learning
- Modelado de demanda agregada a nivel Familia.
- Uso de ventanas temporales y redes Conv1D.
- Entrenamiento y evaluación temporal sin fuga de información.
- Interpretación del modelo como señal anticipada, no como predictor transaccional.

### Procesamiento de Lenguaje Natural (NLP)
- Uso de descripciones reales de productos.
- Preprocesamiento estándar (tokenización, stopwords, stemming).
- Análisis exploratorio de texto y n-gramas.
- Vectorización TF-IDF.
- Agregación semántica por Familia para interpretación del mix de productos.

### Integración y lógica de negocio
- Uso conjunto de demanda proyectada y stock disponible.
- Definición cualitativa del riesgo de quiebre.
- Lógica de decisión basada en priorización.
- Delimitación explícita del alcance y los límites del sistema.

---

## Hallazgos clave

- La demanda a nivel SKU presenta una intermitencia extrema que invalida su uso directo en modelos predictivos.
- El nivel Familia concentra una señal más estable, interpretable y alineada con la lógica de planificación real.
- El Deep Learning resulta viable como generador de señales anticipadas de demanda agregada.
- El NLP aporta valor interpretativo al caracterizar semánticamente las familias de productos.
- La integración de predicción y stock permite anticipar tensiones futuras y priorizar la atención operativa.

---

## Aplicación práctica

En un escenario operativo real, el sistema puede utilizarse de la siguiente manera:

- Ejecución periódica del modelo (por ejemplo, semanal).
- Generación de una vista priorizada de Familias según nivel de riesgo.
- Uso por parte de planificación, compras y gestión e-commerce.
- Enfoque preventivo en lugar de reactivo.
- Soporte a decisiones de reposición, redistribución o ajuste del surtido.

El sistema no automatiza decisiones, sino que ordena la agenda operativa, reduce la incertidumbre y mejora la anticipación.

---

## Escalabilidad y evolución

- Integración directa con sistemas ERP para actualización automática.
- Extensión del horizonte de forecast.
- Incorporación de métricas de servicio adicionales.
- Uso avanzado de NLP para detección de cambios en el mix de productos.
- Implementación de dashboards ejecutivos para consumo no técnico.

---

## Conclusión

Este proyecto demuestra que el valor del Data Science aplicado no reside en la complejidad del modelo, sino en su capacidad de adaptarse al contexto real del negocio, reducir riesgos y mejorar decisiones. Al priorizar el nivel correcto de análisis, definir claramente el rol de cada técnica y mantener la interpretabilidad, el sistema desarrollado se posiciona como una solución sólida, escalable y directamente aplicable al entorno de retail e-commerce.

---

## Contenido del repositorio

- Notebook principal del proyecto.
- Código de preparación de datos, EDA, modelado y NLP.
- Documentación conceptual de la lógica de negocio.
- Archivo README.
