# Analisis bioinformatico de microARNs y genes diana
Los miRNAs participan en la regulación de genes implicados en el desarrollo del cáncer de mama; sin embargo, no siempre se conoce con claridad qué miRNAs alterados y qué genes diana asociados poseen mayor relevancia biológica. Por ello, es necesario integrarlos mediante herramientas bioinformáticas.

## Título
**Análisis bioinformático de microARNs y genes diana asociados al cáncer de mama mediante integración de bases de datos públicas**

---

## 1. Planteamiento del problema

El cáncer de mama es una de las enfermedades oncológicas más estudiadas a nivel molecular debido a su alta heterogeneidad biológica. En este contexto, los microARNs (miRNAs) cumplen un papel regulador clave, ya que modulan la expresión génica a nivel postranscripcional mediante su unión a ARN mensajeros diana. Las alteraciones en los perfiles de expresión de miRNAs se han relacionado con proliferación celular, apoptosis, invasión tumoral, metástasis y resistencia terapéutica.

A pesar de la disponibilidad de grandes volúmenes de datos ómicos en repositorios públicos, todavía existe la necesidad de integrar perfiles de expresión de miRNAs con predicción y validación de genes diana para identificar biomarcadores y rutas moleculares implicadas en la enfermedad.

### Pregunta de investigación
**¿Qué miRNAs diferencialmente expresados y qué genes diana asociados podrían estar implicados en la regulación molecular del cáncer de mama?**

---

## 2. Justificación

Este proyecto es importante porque permite identificar miRNAs con posible valor como biomarcadores diagnósticos, pronósticos o terapéuticos. Desde el punto de vista bioinformático, el estudio aprovecha datos públicos y herramientas accesibles, lo que lo hace viable técnica y económicamente.

Además, integra análisis de expresión, predicción de genes diana, validación experimental y enriquecimiento funcional, generando resultados útiles para la investigación biomédica y traslacional.

---

## 3. Objetivos

### 3.1 Objetivo general
**Identificar miRNAs diferencialmente expresados y sus genes diana potenciales asociados al cáncer de mama mediante análisis bioinformático de bases de datos públicas.**

### 3.2 Objetivos específicos
1. Seleccionar un conjunto de datos públicos con perfiles de expresión de miRNAs en muestras de cáncer de mama y controles sanos.
2. Identificar los miRNAs diferencialmente expresados entre ambos grupos.
3. Predecir y recopilar los genes diana de los miRNAs seleccionados usando bases de datos especializadas.
4. Construir una red de interacción miRNA-gen diana.
5. Realizar análisis de enriquecimiento funcional y de vías biológicas de los genes diana.
6. Priorizar miRNAs y genes con mayor relevancia biológica como posibles biomarcadores o reguladores clave.

---

## 4. Hipótesis

### 4.1 Hipótesis general
Los miRNAs diferencialmente expresados en cáncer de mama regulan genes diana involucrados en rutas moleculares asociadas a proliferación, apoptosis, invasión y progresión tumoral.

### 4.2 Hipótesis específica
La integración de datos de expresión de miRNAs con bases de datos de predicción y validación experimental permitirá identificar una red regulatoria miRNA-gen diana con relevancia biológica en cáncer de mama.

---

## 5. Variables de estudio

### 5.1 Tabla de variables

| Variable | Definición conceptual | Definición operacional | Dimensiones | Indicadores |
|---|---|---|---|---|
| Expresión de miRNAs | Nivel de abundancia relativa de microARNs en muestras biológicas | Valores de expresión obtenidos de un dataset público de miRNA | miRNAs sobreexpresados, miRNAs subexpresados, magnitud del cambio, significancia estadística | log2FC, p ajustado, número de miRNAs significativos |
| Genes diana de miRNAs | Genes regulados postranscripcionalmente por unión de miRNAs | Genes diana predichos y/o validados en bases de datos especializadas | genes predichos, genes validados, grado de interacción, participación en rutas biológicas | número de genes diana, score de predicción, evidencia experimental, rutas enriquecidas |

---

## 6. Metodología

### 6.1 Enfoque de investigación
- **Enfoque:** cuantitativo
- **Tipo de investigación:** aplicada
- **Diseño:** no experimental, descriptivo-comparativo y bioinformático

### 6.2 Fuente de datos
Se emplearán bases de datos públicas de expresión de miRNAs y de interacción miRNA-gen. El análisis se realizará a partir de datasets obtenidos de GEO y de bases de datos especializadas para predicción y validación de genes diana.

### 6.3 Población y muestra
- **Población:** datasets públicos de expresión de miRNAs relacionados con cáncer de mama.
- **Muestra:** un dataset seleccionado en GEO que contenga muestras tumorales y controles normales, con calidad suficiente y tamaño muestral adecuado.

### 6.4 Criterios de inclusión
- Dataset público disponible en GEO
- Muestras humanas
- Presencia de grupo control y grupo enfermedad
- Datos de expresión de miRNAs
- Información metodológica clara

### 6.5 Criterios de exclusión
- Datasets incompletos
- Muestras sin anotación clínica básica
- Estudios con muy bajo número de muestras
- Datos sin normalización o con metadatos insuficientes

---

## 7. Procedimiento bioinformático

### Fase 1. Búsqueda y selección del dataset
Se buscará en GEO un conjunto de datos de expresión de miRNAs en cáncer de mama y controles sanos.

### Fase 2. Preprocesamiento y control de calidad
Se revisará la calidad del dataset, la distribución de los datos y, de ser necesario, se realizará normalización.

### Fase 3. Identificación de miRNAs diferencialmente expresados
Se aplicará análisis estadístico para identificar miRNAs con diferencias significativas entre grupos, usando criterios como:

- **p ajustado < 0.05**
- **|log2FC| > 1**

### Fase 4. Selección de miRNAs de interés
Se priorizarán los miRNAs con mayor cambio de expresión y relevancia reportada en cáncer.

### Fase 5. Predicción y validación de genes diana
Los genes diana se obtendrán integrando:
- **TargetScan** para predicción
- **miRDB** para predicción complementaria
- **miRTarBase** para validación experimental reportada

### Fase 6. Construcción de red de interacción
Se elaborará una red miRNA-gen diana utilizando Cytoscape o miRNet para explorar redes regulatorias y sus nodos más conectados.

### Fase 7. Enriquecimiento funcional
Se analizarán los genes diana para identificar:
- procesos biológicos
- funciones moleculares
- componentes celulares
- rutas KEGG o Reactome asociadas

### Fase 8. Interpretación biológica
Se discutirán los miRNAs y genes centrales en relación con mecanismos de progresión tumoral y potencial valor clínico.

---

## 8. Bases de datos y herramientas

### 8.1 Bases de datos
- **GEO**: datasets de expresión
- **miRBase**: secuencias y nomenclatura de miRNAs
- **miRTarBase**: interacciones miRNA-gen validadas experimentalmente
- **TargetScan**: predicción de dianas
- **miRDB**: predicción funcional de genes diana

### 8.2 Herramientas de análisis
- **R / RStudio**
- **limma** o **DESeq2**
- **GEO2R**
- **Cytoscape**
- **miRNet**
- **Enrichr**
- **DAVID**

---

## 9. Resultados esperados

Se espera:

1. Identificar un conjunto de miRNAs diferencialmente expresados en cáncer de mama.
2. Obtener una lista priorizada de genes diana predichos y/o validados.
3. Construir una red de interacción miRNA-gen diana.
4. Detectar rutas biológicas relacionadas con proliferación, apoptosis, adhesión celular, angiogénesis o metástasis.
5. Proponer candidatos con potencial uso como biomarcadores moleculares.

---

## 10. Aporte del estudio

El proyecto aportará una caracterización bioinformática de la regulación postranscripcional mediada por miRNAs en cáncer de mama y permitirá priorizar moléculas candidatas para estudios posteriores experimentales o clínicos.

---

## 11. Limitaciones

- Dependencia de la calidad del dataset público
- Variabilidad entre plataformas y estudios
- Predicciones de genes diana que pueden incluir falsos positivos si no se filtran con evidencia experimental
- Necesidad de validación experimental posterior

---

## 12. Cronograma de actividades

| Actividad | Mes 1 | Mes 2 | Mes 3 | Mes 4 |
|---|---|---|---|---|
| Revisión bibliográfica | X | X |  |  |
| Búsqueda y selección del dataset | X |  |  |  |
| Preprocesamiento y control de calidad |  | X |  |  |
| Identificación de miRNAs diferencialmente expresados |  | X |  |  |
| Predicción y validación de genes diana |  | X | X |  |
| Construcción de red de interacción |  |  | X |  |
| Enriquecimiento funcional |  |  | X |  |
| Interpretación de resultados |  |  |  | X |
| Redacción del informe final |  |  | X | X |
| Revisión y presentación final |  |  |  | X |
