![Logo UNIR](https://es.wikipedia.org/wiki/Archivo:Logo_UNIR.png)

![Bioinformatica](https://technofob.com/wp-content/uploads/2015/10/bioinformatics.jpg)

# Analisis bioinformatico de microARNs y genes diana
Los miRNAs participan en la regulación de genes implicados en el desarrollo del cáncer de mama; sin embargo, no siempre se conoce con claridad qué miRNAs alterados y qué genes diana asociados poseen mayor relevancia biológica. Por ello, es necesario integrarlos mediante herramientas bioinformáticas.

# Flujo de Trabajo en Bipython y R para el análisis de miRNA´s
El flujo de trabajo integra **Biopython** y **R** para el análisis de miRNAs desde la obtención de secuencias hasta la interpretación funcional. Inicialmente, las secuencias se descargan desde **miRBase** y se someten a un proceso de filtrado y selección de miRNAs maduros mediante Biopython. Posteriormente, se realiza la predicción de blancos *in silico* (miRNA–mRNA) utilizando herramientas como miRanda. Los resultados se integran con datos de expresión y se analizan en R mediante enfoques estadísticos (e.g., DESeq2) para identificar miRNAs diferencialmente expresados y sus posibles genes diana. Finalmente, se lleva a cabo la visualización y anotación funcional, incluyendo análisis de enriquecimiento (GO) y representación de redes regulatorias, permitiendo la interpretación biológica de los patrones observados.

<img width="1536" height="1024" alt="work_flow" src="https://github.com/user-attachments/assets/b0d6bda2-2880-4595-90e0-93c746645c0b" />



<br><br>
###Programación Científica
### Grupo No. 5, Integrantes:
|Nombre  |
|--|
| Deivis Martínez|
| Carlos Pérez|
| Freddy Rodríguez|
