Proyecto de Integración de Bases de Datos ICFES

Proyecto desarrollado en RStudio para la integración, limpieza, homologación y validación de las bases de datos Saber 11 y Saber Pro.

Objetivo

Construir una base de datos integrada a partir de los diferentes períodos de Saber 11 y Saber Pro, conservando la trazabilidad del proceso y verificando la correcta vinculación de los registros.

Bases de datos

Se trabajó con las siguientes bases:

saber11: base consolidada de Saber 11. La variable del período se denomina periodo.
saberpro_total: base consolidada de Saber Pro. La variable del período se denomina periodo.
base_final_limpia: base resultante del proceso de integración y limpieza. Las variables de período son periodo_sb11 y periodo_sbpro.
cruces: base utilizada para realizar la vinculación entre los registros de Saber 11 y Saber Pro.
Proceso realizado

El procesamiento de las bases se desarrolló siguiendo estas etapas:

Importación de las bases originales.
Revisión de la estructura de los datos.
Identificación y selección de las variables necesarias.
Revisión de nombres y tipos de variables.
Revisión de valores faltantes y categorías.
Homologación de variables entre los diferentes períodos.
Consolidación de las bases de Saber 11.
Consolidación de las bases de Saber Pro.
Vinculación de Saber 11 y Saber Pro mediante la base cruces.
Construcción de la base final.
Limpieza de la base integrada.
Validación de registros, variables y períodos.
Revisión de la distribución de los registros vinculados.
Importación de archivos TXT

Algunas bases originales se encontraban en formato .txt y estaban separadas por punto y coma (;).

La importación se realizó en R mediante:

base <- read.delim(
  file.choose(),
  header = TRUE,
  sep = ";",
  stringsAsFactors = FALSE
)

Cuando fue necesario convertir una base TXT a CSV se utilizó:

write.csv(
  base,
  "base_convertida.csv",
  row.names = FALSE,
  fileEncoding = "UTF-8"
)
Validación de los datos

Después de importar cada base se realizaron comprobaciones sobre:

Cantidad de registros.
Cantidad de variables.
Nombres de las variables.
Tipos de datos.
Valores faltantes (NA).
Categorías y códigos.
Períodos disponibles.
Registros vinculados.
Correspondencia entre las bases.

Entre las funciones utilizadas para estas comprobaciones se encuentran:

dim(base)
names(base)
glimpse(base)
summary(base)
colSums(is.na(base))
Períodos

Los períodos de Saber 11 y Saber Pro presentan codificaciones diferentes.

En Saber 11 se encuentran períodos como:

20101
20102
20111
20112
20121
20122
...

En Saber Pro se encuentran períodos como:

20153
20163
20173
20182
20183
20184
20194
...

Por esta razón, los períodos fueron revisados antes de establecer correspondencias entre ambas bases.

Vinculación

La vinculación entre Saber 11 y Saber Pro se realizó previamente mediante la base cruces.

Por esta razón, en base_final_limpia los registros ya corresponden a estudiantes que quedaron vinculados durante el proceso de integración.

La relación final se puede revisar mediante:

base_final_limpia %>%
  filter(
    !is.na(periodo_sb11),
    !is.na(periodo_sbpro)
  ) %>%
  count(
    periodo_sb11,
    periodo_sbpro,
    name = "registros_vinculados"
  ) %>%
  arrange(periodo_sb11, periodo_sbpro)
Análisis del rezago

Se calculó la diferencia entre el año correspondiente al período de Saber 11 y el año correspondiente al período de Saber Pro para identificar el comportamiento temporal de los registros vinculados.

La distribución observada mostró diferentes rezagos entre las dos pruebas, por lo que este comportamiento fue revisado antes de establecer criterios para la vinculación temporal.

Reproducibilidad

Para ejecutar el proyecto:

Instalar R y RStudio.
Descargar este repositorio.
Disponer de las bases originales de Saber 11 y Saber Pro.
Mantener las bases originales sin modificaciones manuales.
Instalar los paquetes utilizados en el proyecto.
Abrir los scripts .R.
Ejecutar los scripts siguiendo el orden establecido.
Revisar los resultados de cada etapa.
Comprobar que los registros y variables obtenidos coincidan con las validaciones realizadas durante el proyecto.

Las transformaciones de los datos se realizan mediante código R con el propósito de conservar la trazabilidad y facilitar la reproducción del proceso.

Paquetes principales
library(tidyverse)
library(readr)
library(dplyr)
library(janitor)
Nota sobre las bases de datos

Las bases originales de Saber 11 y Saber Pro pueden no estar incluidas directamente en este repositorio debido a su tamaño y características. Para reproducir el proceso deben ubicarse localmente y utilizarse como entrada de los scripts correspondientes.

Proyecto de Estadística Industrial — Universidad del Magdalena

