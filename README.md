
# Análisis bioinformático de microARNs y genes diana
Este proyecto es desarrollado con la finalidad de analizar el comportamiento de un grupo de miRNA para determinar las dianas usando las bases de datos disponibles.  Para lograrlo seguimos los siguientes pasos:

1. Consultamos la base de datos [TargetScan](https://www.targetscan.org/vert_80/) donde encontramos los genes diana que vamos a analizar
   - Escribimos o pegamos el nombre del miRNA a analizar
   - Descargamos los resultados en formato `.xlsx` [ver ejemplos en la carpeta](genes_diana/xlsx/)
   - Pasamos a un archivo de texto el listado de los genes obtenidos por cada uno de los miRNA [ver ejemplos en la carpeta](genes_diana/txt/)
   - Generamos un diagrama de Venn para obtener los genes diana comunes, con la herramienta de [PSB](https://bioinformatics.psb.ugent.be/webtools/Venn/)

2. Usamos la base de datos [UniProt](https://www.uniprot.org/) para buscar la función biológica de los genes diana comunes

3. Identificamos las rutas de señalización con [GeneCodis](https://genecodis.genyo.es/)

Las imagenes generadas en el proyecto se encuentran en la carpeta [images](images/) de este repositorio.

También encontramos el código fuente desarrollado para este análisis con Python se encuentra en la carpeta [src/Python](src/Python/) y código en R con ejemplos de reducción de dimensionalidad en la carpeta [src/R](src/R/)


Los miRNAs participan en la regulación de genes implicados en el desarrollo del cáncer de mama; sin embargo, no siempre se conoce con claridad qué miRNAs alterados y qué genes diana asociados poseen mayor relevancia biológica. Por ello, es necesario integrarlos mediante herramientas bioinformáticas.

# Flujo de Trabajo en Bipython y R para el análisis de miRNA´s
El flujo de trabajo integra **Biopython** y **R** para el análisis de miRNAs desde la obtención de secuencias hasta la interpretación funcional. Inicialmente, las secuencias se descargan desde **miRBase** y se someten a un proceso de filtrado y selección de miRNAs maduros mediante Biopython. Posteriormente, se realiza la predicción de blancos *in silico* (miRNA–mRNA) utilizando herramientas como miRanda. Los resultados se integran con datos de expresión y se analizan en R mediante enfoques estadísticos (e.g., DESeq2) para identificar miRNAs diferencialmente expresados y sus posibles genes diana. Finalmente, se lleva a cabo la visualización y anotación funcional, incluyendo análisis de enriquecimiento (GO) y representación de redes regulatorias, permitiendo la interpretación biológica de los patrones observados.

<img width="1536" height="1024" alt="work_flow" src="https://github.com/user-attachments/assets/b0d6bda2-2880-4595-90e0-93c746645c0b" />



<br><br>

## Programación Científica

### Grupo No. 5, Integrantes:
|Nombre  |
|--|
| Deivis Martínez|
| Carlos Pérez|
| Freddy Rodríguez|

<div style="text-align: center;">
<img width="300" height="200" alt="Logo UNIR" src="https://upload.wikimedia.org/wikipedia/commons/d/df/Logo_UNIR.png" />
</div>
