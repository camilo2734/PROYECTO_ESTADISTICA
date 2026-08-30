# PROYECTO_ESTADISTICA
PROYECTO CRUCE ENTRE SABER 11 Y SABER PRO 2014-2025

```{r}
install.packages("stringdist")
```

```{r}
library(tidyverse)
library(readxl)
library(janitor)
library(dplyr)
library(readr)
library(dplyr)
library(stringi)
library(stringr)
library(stringdist)
```


# BASE LIMPIA SABER 11 2010-1
```{r}
saber11_20101 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20101.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20101 <- saber11_20101 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
  ) 
```

# BASE LIMPIA SABER 11 2010-2
```{r}
saber11_20102 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20102.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20102 <- saber11_20102 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
  ) 
```

# BASE LIMPIA SABER 11 2011-1
```{r}
saber11_20111 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20111.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20111 <- saber11_20111 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
  ) 
```

# BASE LIMPIA SABER 11 2011-2
```{r}
saber11_20112 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20112.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20112 <- saber11_20112 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
  ) 
```


# BASE LIMPIA SABER 11 2014-1
```{r}
saber11_20121 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20121.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20121 <- saber11_20121 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    recaf_punt_c_naturales,
    recaf_punt_ingles,
    recaf_punt_matematicas,
    recaf_punt_lectura_critica,
    recaf_punt_sociales_ciudadanas,
  ) %>%
  rename(
    punt_c_naturales = recaf_punt_c_naturales,
    punt_ingles = recaf_punt_ingles,
    punt_matematicas = recaf_punt_matematicas,
    punt_lectura_critica = recaf_punt_lectura_critica,
    punt_sociales_ciudadanas = recaf_punt_sociales_ciudadanas
  )
```

# BASE LIMPIA SABER 11 2012-2
```{r}
saber11_20122 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20122.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20122 <- saber11_20122 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    recaf_punt_c_naturales,
    recaf_punt_ingles,
    recaf_punt_matematicas,
    recaf_punt_lectura_critica,
    recaf_punt_sociales_ciudadanas,
  ) %>%
  rename(
    punt_c_naturales = recaf_punt_c_naturales,
    punt_ingles = recaf_punt_ingles,
    punt_matematicas = recaf_punt_matematicas,
    punt_lectura_critica = recaf_punt_lectura_critica,
    punt_sociales_ciudadanas = recaf_punt_sociales_ciudadanas
  )
```

# BASE LIMPIA SABER 11 2013-1
```{r}
saber11_20131 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20131.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20131 <- saber11_20131 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    recaf_punt_c_naturales,
    recaf_punt_ingles,
    recaf_punt_matematicas,
    recaf_punt_lectura_critica,
    recaf_punt_sociales_ciudadanas,
  ) %>%
  rename(
    punt_c_naturales = recaf_punt_c_naturales,
    punt_ingles = recaf_punt_ingles,
    punt_matematicas = recaf_punt_matematicas,
    punt_lectura_critica = recaf_punt_lectura_critica,
    punt_sociales_ciudadanas = recaf_punt_sociales_ciudadanas
  )
```

# BASE LIMPIA SABER 11 2013-2
```{r}
saber11_20132 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20132.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20132 <- saber11_20132 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    recaf_punt_c_naturales,
    recaf_punt_ingles,
    recaf_punt_matematicas,
    recaf_punt_lectura_critica,
    recaf_punt_sociales_ciudadanas,
  ) %>%
  rename(
    punt_c_naturales = recaf_punt_c_naturales,
    punt_ingles = recaf_punt_ingles,
    punt_matematicas = recaf_punt_matematicas,
    punt_lectura_critica = recaf_punt_lectura_critica,
    punt_sociales_ciudadanas = recaf_punt_sociales_ciudadanas
  )
```


# BASE LIMPIA SABER 11 2014-1
```{r}
saber11_20141 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20141.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20141 <- saber11_20141 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    recaf_punt_c_naturales,
    recaf_punt_ingles,
    recaf_punt_matematicas,
    recaf_punt_lectura_critica,
    recaf_punt_sociales_ciudadanas,
  ) %>%
  rename(
    punt_c_naturales = recaf_punt_c_naturales,
    punt_ingles = recaf_punt_ingles,
    punt_matematicas = recaf_punt_matematicas,
    punt_lectura_critica = recaf_punt_lectura_critica,
    punt_sociales_ciudadanas = recaf_punt_sociales_ciudadanas
  )
```

# BASE LIMPIA SABER 11 2014-2
```{r}
saber11_20142 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20142.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20142 <- saber11_20142 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
  )
```

# BASE LIMPIA SABER 11 2015-1
```{r}
saber11_20151 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20151.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20151 <- saber11_20151 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
  )
```

# BASE LIMPIA SABER 11 2015-2
```{r}
saber11_20152 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20152.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20152 <- saber11_20152 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
  )
```

# BASE LIMPIA SABER 11 2016-1
```{r}
saber11_20161 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20161.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20161 <- saber11_20161 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2016-2
```{r}
saber11_20162 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20162.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20162 <- saber11_20162 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2017-1
```{r}
saber11_20171 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20171.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20171 <- saber11_20171 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2017-2
```{r}
saber11_20172 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20172.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20172 <- saber11_20172 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```


# BASE LIMPIA SABER 11 2018-1
```{r}
saber11_20181 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20181.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)
saber11_20181 <- saber11_20181 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2018-2
```{r}
saber11_20182 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20182.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20182 <- saber11_20182 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2019-1
```{r}
saber11_20191 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20191.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20191 <- saber11_20191 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2019-2
```{r}
saber11_20192 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20192.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20192 <- saber11_20192 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2020-1
```{r}
saber11_20201 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20201.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20201 <- saber11_20201 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2020-2
```{r}
saber11_20202 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20202.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20202 <- saber11_20202 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2021-1
```{r}
saber11_20211 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20211.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20211 <- saber11_20211 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2021-2
```{r}
saber11_20212 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20212.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20212 <- saber11_20212 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2022-1
```{r}
saber11_20221 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20221.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20221 <- saber11_20221 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2022-2
```{r}
saber11_20222 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20222.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20222 <- saber11_20222 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2023-1
```{r}
saber11_20231 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20231.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20231 <- saber11_20231 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2023-2
```{r}
saber11_20232 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20232.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20232 <- saber11_20232 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2024-1
```{r}
saber11_20241 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20241.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20241 <- saber11_20241 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2024-2
```{r}
saber11_20242 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20242.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20242 <- saber11_20242 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2025-1
```{r}
saber11_20251 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20251.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20251 <- saber11_20251 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```

# BASE LIMPIA SABER 11 2025-2
```{r}
saber11_20252 <- read_delim(
  "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER 11/Examen_Saber_11_20252.txt",
  delim = ";",
  show_col_types = FALSE,
  na = c("", "NA")
)

saber11_20252 <- saber11_20252 %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    cole_jornada,
    cole_bilingue,
    cole_area_ubicacion,
    cole_calendario,
    cole_naturaleza,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    punt_c_naturales,
    punt_ingles,
    punt_matematicas,
    punt_lectura_critica,
    punt_sociales_ciudadanas,
    punt_global,
    percentil_c_naturales,
    percentil_ingles,
    percentil_lectura_critica,
    percentil_matematicas,
    percentil_sociales_ciudadanas,
    percentil_global,
  )
```


## BASE LIMPIA SABER 11 UNIDAS
```{r}
saber11 <- bind_rows(
  saber11_20101,
  saber11_20102,
  saber11_20111,
  saber11_20112,
  saber11_20121,
  saber11_20122,
  saber11_20131,
  saber11_20132,
  saber11_20141,
  saber11_20142,
  saber11_20151,
  saber11_20152,
  saber11_20161,
  saber11_20162,
  saber11_20171,
  saber11_20172,
  saber11_20181,
  saber11_20182,
  saber11_20191,
  saber11_20192,
  saber11_20201,
  saber11_20202,
  saber11_20211,
  saber11_20212,
  saber11_20221,
  saber11_20222,
  saber11_20231,
  saber11_20232,
  saber11_20241,
  saber11_20242,
  saber11_20251,
  saber11_20252
)
saber11 <- saber11 %>%
  distinct(periodo, estu_consecutivo, .keep_all = TRUE)
```

## RUTA RAPIDA PARA LOS ARCHIVOS DE SABER PRO
```{r}
ruta_pro <- "C:/Users/eduar/OneDrive/Escritorio/PRUEBA SABER PRO"
```

## BASE LIMPIA SABER PRO 2014
```{r}
saberpro_2014 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2014.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
  )
```

## BASE LIMPIA SABER PRO 2015
```{r}
saberpro_2015 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2015.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
  )
```

## BASE LIMPIA SABER PRO 2016
```{r}
saberpro_2016 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2016.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
    punt_global,
    mod_ingles_pnal,
    mod_razona_cuantitativo_pnal,
    mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal,
    percentil_global,
  )
```


## BASE LIMPIA SABER PRO 2017
```{r}
saberpro_2017 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2017.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
    punt_global,
    mod_ingles_pnal,
    mod_razona_cuantitativo_pnal,
    mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal,
    percentil_global,
  )
```

## BASE LIMPIA SABER PRO 2018
```{r}
saberpro_2018 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2018.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
    punt_global,
    mod_ingles_pnal,
    mod_razona_cuantitativo_pnal,
    mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal,
    percentil_global,
  )
```

## BASE LIMPIA SABER PRO 2019
```{r}
saberpro_2019 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2019.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
    punt_global,
    mod_ingles_pnal,
    mod_razona_cuantitativo_pnal,
    mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal,
    percentil_global,
  )
```

## BASE LIMPIA SABER PRO 2020
```{r}
saberpro_2020 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2020.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
   periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
    punt_global,
    mod_ingles_pnal,
    mod_razona_cuantitativo_pnal,
    mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal,
    percentil_global,
  )
```

## BASE LIMPIA SABER PRO 2021
```{r}
saberpro_2021 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2021.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
    punt_global,
    mod_ingles_pnal,
    mod_razona_cuantitativo_pnal,
    mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal,
    percentil_global,
  )
```


## BASE LIMPIA SABER PRO 2022
```{r}
saberpro_2022 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2022.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_fechanacimiento,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
    punt_global,
    mod_ingles_pnal,
    mod_razona_cuantitativo_pnal,
    mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal,
    percentil_global,
  )
```


## BASE LIMPIA SABER PRO 2023
```{r}
saberpro_2023 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2023.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    estu_depto_reside,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_fechanacimiento,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
    punt_global,
    mod_ingles_pnal,
    mod_razona_cuantitativo_pnal,
    mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal,
    percentil_global,
  )
```


## BASE LIMPIA SABER PRO 2024
```{r}
saberpro_2024 <- read.delim(
  file.path(ruta_pro, "Examen_Saber_Pro_Genericas_2024.txt"),
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
) %>%
  select(
    periodo,
    estu_consecutivo,
    estu_estudiante,
    inst_cod_institucion,
    inst_nombre_institucion,
    estu_snies_prgmacademico,
    estu_prgm_academico,
    estu_nucleo_pregrado,
    estu_fechanacimiento,
    estu_genero,
    fami_educacionmadre,
    fami_educacionpadre,
    fami_estratovivienda,
    fami_tienecomputador,
    fami_tieneinternet,
    mod_ingles_punt,
    mod_razona_cuantitat_punt,
    mod_lectura_critica_punt,
    mod_competen_ciudada_punt,
    mod_comuni_escrita_punt,
    punt_global,
    mod_ingles_pnal,
    mod_razona_cuantitativo_pnal,
    mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal,
    percentil_global,
  )
```


## BASE LIMPIA SABER PRO
```{r}
saberpro_total <- bind_rows(
  saberpro_2014,
  saberpro_2015,
  saberpro_2016,
  saberpro_2017,
  saberpro_2018,
  saberpro_2019,
  saberpro_2020,
  saberpro_2021,
  saberpro_2022,
  saberpro_2023,
  saberpro_2024
) %>%
  distinct()
```


## BASE LIMPIA cruce entre saber 11 y saber pro 2010-2025
```{r}
cruce <- read.delim(
  "C:/Users/eduar/Downloads/Cruce Examen Saber 11 - Examen Saber Pro.txt",
  sep = ";",
  header = TRUE,
  stringsAsFactors = FALSE,
  check.names = FALSE
)

cruce_saber11_saberpro <- cruce %>%
  mutate(
    anio_sb11 = as.numeric(substr(periodo_sb11, 1, 4)),
    anio_sbpro = as.numeric(substr(periodo_sbpro, 1, 4))
  ) %>%
  filter(
    anio_sb11 >= 2010 & anio_sb11 <= 2024,
    anio_sbpro >= 2014 & anio_sbpro <= 2024,
    (anio_sbpro - anio_sb11) >= 2
  ) %>%
  select(
    estu_consecutivo_sb11,
    periodo_sb11,
    estu_consecutivo_sbpro,
    periodo_sbpro
  ) %>%
  distinct()
```

## BASE FINAL
```{r}
# Preparar Saber 11
saber11_final <- saber11 %>%
  rename(
    periodo_sb11 = periodo,
    estu_consecutivo_sb11 = estu_consecutivo,
    estu_estudiante_sb11 = estu_estudiante,
    cole_bilingue_sb11 = cole_bilingue,
    cole_area_ubicacion_sb11 = cole_area_ubicacion,
    cole_calendario_sb11 = cole_calendario,
    cole_naturaleza_sb11 = cole_naturaleza,
    punt_c_naturales_sb11 = punt_c_naturales,
    punt_ingles_sb11 = punt_ingles,
    punt_matematicas_sb11 = punt_matematicas,
    punt_lectura_critica_sb11 = punt_lectura_critica,
    punt_sociales_ciudadanas_sb11 = punt_sociales_ciudadanas,
    fami_educacionmadre_sb11 = fami_educacionmadre,
    fami_educacionpadre_sb11 = fami_educacionpadre,
    fami_estratovivienda_sb11 = fami_estratovivienda,
    fami_tienecomputador_sb11 = fami_tienecomputador,
    fami_tieneinternet_sb11 = fami_tieneinternet,
    punt_global_sb11 = punt_global,
    estu_depto_reside_sb11 = estu_depto_reside,
    cole_jornada_sb11 = cole_jornada,
    percentil_c_naturales_sb11 = percentil_c_naturales,
    percentil_ingles_sb11 = percentil_ingles,
    percentil_lectura_critica_sb11 = percentil_lectura_critica,
    percentil_matematicas_sb11 = percentil_matematicas,
    percentil_sociales_ciudadanas_sb11 = percentil_sociales_ciudadanas,
    percentil_global_sb11 = percentil_global,
  )

# Preparar Saber Pro
saberpro_final <- saberpro_total %>%
  rename(
    periodo_sbpro = periodo,
    estu_consecutivo_sbpro = estu_consecutivo,
    estu_estudiante_sbpro = estu_estudiante,
    mod_competen_ciudada_punt_sbpro = mod_competen_ciudada_punt,
    mod_comuni_escrita_punt_sbpro = mod_comuni_escrita_punt,
    mod_ingles_punt_sbpro = mod_ingles_punt,
    mod_lectura_critica_punt_sbpro = mod_lectura_critica_punt,
    mod_razona_cuantitat_punt_sbpro = mod_razona_cuantitat_punt,
    inst_cod_institucion_sbpro = inst_cod_institucion,
    inst_nombre_institucion_sbpro = inst_nombre_institucion,
    estu_snies_prgmacademico_sbpro = estu_snies_prgmacademico,
    estu_prgm_academico_sbpro = estu_prgm_academico,
    estu_fechanacimiento_sbpro = estu_fechanacimiento,
    estu_genero_sbpro = estu_genero,
    fami_educacionmadre_sbpro = fami_educacionmadre,
    fami_educacionpadre_sbpro = fami_educacionpadre,
    fami_estratovivienda_sbpro = fami_estratovivienda,
    fami_tienecomputador_sbpro = fami_tienecomputador,
    fami_tieneinternet_sbpro = fami_tieneinternet,
    estu_nucleo_pregrado_sbpro = estu_nucleo_pregrado,
    estu_depto_reside_sbpro = estu_depto_reside,
    mod_ingles_pnal_sbpro = mod_ingles_pnal,
    mod_razona_cuantitativo_pnal_sbpro = mod_razona_cuantitativo_pnal,
    mod_lectura_critica_pnal_sbpro = mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal_sbpro = mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal_sbpro = mod_comuni_escrita_pnal,
    punt_global_sbpro = punt_global,
    mod_ingles_pnal_sbpro = mod_ingles_pnal,
    mod_razona_cuantitativo_pnal_sbpro = mod_razona_cuantitativo_pnal,
     mod_lectura_critica_pnal_sbpro = mod_lectura_critica_pnal,
    mod_competen_ciudada_pnal_sbpro = mod_competen_ciudada_pnal,
    mod_comuni_escrita_pnal_sbpro = mod_comuni_escrita_pnal,
     percentil_global_sbpro = percentil_global,
  )
1.617405
# Unir las tres bases mediante la tabla de cruce
base_final <- cruce_saber11_saberpro %>%
  left_join(
    saber11_final,
    by = c("estu_consecutivo_sb11", "periodo_sb11")
  ) %>%
  left_join(
    saberpro_final,
    by = c("estu_consecutivo_sbpro", "periodo_sbpro")
  ) %>%
  distinct()
```


## limpiar las variables categoricas de la saber 11

```{r}
base_final_limpia <- base_final %>%
  mutate(
    # departamento reside
    estu_depto_reside_sb11 = case_when(
  estu_depto_reside_sb11  == "BOGOTA" ~ "BOGOTÁ",
  TRUE ~ estu_depto_reside_sb11 
    ),
    # Colegio bilingüe
    cole_bilingue_sb11 = case_when(
      cole_bilingue_sb11 == "S" ~ "S",
      cole_bilingue_sb11 == "N" ~ "N",
      TRUE ~ NA_character_
    ),

    # Área del colegio
    cole_area_ubicacion_sb11 = case_when(
      cole_area_ubicacion_sb11 %in% c("URBANO", "URBANA") ~ "URBANA",
      cole_area_ubicacion_sb11 == "RURAL" ~ "RURAL",
      TRUE ~ NA_character_
    ),

    # Calendario
    cole_calendario_sb11 = case_when(
      cole_calendario_sb11 %in% c("A", "B", "OTRO") ~ cole_calendario_sb11,
      TRUE ~ NA_character_
    ),

    # Naturaleza del colegio
    cole_naturaleza_sb11 = case_when(
      cole_naturaleza_sb11 %in% c("OFICIAL", "NO OFICIAL") ~ cole_naturaleza_sb11,
      TRUE ~ NA_character_
    ),

    # Educación de la madre
    fami_educacionmadre_sb11 = case_when(
  fami_educacionmadre_sb11 %in% c(
    "Secundaria (Bachillerato) completa",
    "Educación profesional completa",
    "Técnica o tecnológica completa",
    "Secundaria (Bachillerato) incompleta",
    "Primaria completa",
    "Postgrado",
    "Primaria incompleta",
    "Educación profesional incompleta",
    "Técnica o tecnológica incompleta",
    "Ninguno"
  ) ~ fami_educacionmadre_sb11,
  TRUE ~ NA_character_
),

    # Educación del padre
    fami_educacionpadre_sb11 = case_when(
  fami_educacionpadre_sb11 %in% c(
    "Secundaria (Bachillerato) completa",
    "Educación profesional completa",
    "Secundaria (Bachillerato) incompleta",
    "Técnica o tecnológica completa",
    "Primaria incompleta",
    "Primaria completa",
    "Postgrado",
    "Educación profesional incompleta",
    "Técnica o tecnológica incompleta",
    "Ninguno"
  ) ~ fami_educacionpadre_sb11,
  TRUE ~ NA_character_
),

    # Estrato
    fami_estratovivienda_sb11 = case_when(
      fami_estratovivienda_sb11 %in% c(
        "Estrato 1",
        "Estrato 2",
        "Estrato 3",
        "Estrato 4",
        "Estrato 5",
        "Estrato 6",
        "Sin Estrato"
      ) ~ fami_estratovivienda_sb11,
      TRUE ~ NA_character_
    ),

    # Computador
    fami_tienecomputador_sb11 = case_when(
      fami_tienecomputador_sb11 %in% c("Si", "No") ~ fami_tienecomputador_sb11,
      TRUE ~ NA_character_
    ),

    # Internet
    fami_tieneinternet_sb11 = case_when(
      fami_tieneinternet_sb11 %in% c("Si", "No") ~ fami_tieneinternet_sb11,
      TRUE ~ NA_character_
    )
  )
```

## limpiar las variables categoricas de la saber pro

```{r}
base_final_limpia <- base_final_limpia %>%
  mutate(
    
    # ============================================================
    # DEPARTAMENTO DONDE RESIDE - SABER PRO
    # ============================================================
    
    estu_depto_reside_sbpro = case_when(
      estu_depto_reside_sbpro == "BOGOTA" ~ "BOGOTÁ",
      TRUE ~ estu_depto_reside_sbpro
    ),
    
    
    # ============================================================
    # GÉNERO - SABER PRO
    # ============================================================
    
    estu_genero_sbpro = case_when(
      estu_genero_sbpro %in% c("F", "M") ~ estu_genero_sbpro,
      TRUE ~ NA_character_
    ),
    
    
    # ============================================================
    # EDUCACIÓN DE LA MADRE - SABER PRO
    # ============================================================
    
    fami_educacionmadre_sbpro = case_when(
      fami_educacionmadre_sbpro %in% c(
        "Secundaria (Bachillerato) completa",
        "Educación profesional completa",
        "Técnica o tecnológica completa",
        "Secundaria (Bachillerato) incompleta",
        "Primaria completa",
        "Postgrado",
        "Primaria incompleta",
        "Educación profesional incompleta",
        "Técnica o tecnológica incompleta",
        "Ninguno"
      ) ~ fami_educacionmadre_sbpro,
      TRUE ~ NA_character_
    ),
    
    
    # ============================================================
    # EDUCACIÓN DEL PADRE - SABER PRO
    # ============================================================
    
    fami_educacionpadre_sbpro = case_when(
      fami_educacionpadre_sbpro %in% c(
        "Secundaria (Bachillerato) completa",
        "Educación profesional completa",
        "Técnica o tecnológica completa",
        "Secundaria (Bachillerato) incompleta",
        "Primaria completa",
        "Postgrado",
        "Primaria incompleta",
        "Educación profesional incompleta",
        "Ninguno"
      ) ~ fami_educacionpadre_sbpro,
      TRUE ~ NA_character_
    ),
    
    
    # ============================================================
    # ESTRATO - SABER PRO
    # ============================================================
    
    fami_estratovivienda_sbpro = case_when(
      fami_estratovivienda_sbpro == "Estrato 1" ~ "Estrato 1",
      fami_estratovivienda_sbpro == "Estrato 2" ~ "Estrato 2",
      fami_estratovivienda_sbpro == "Estrato 3" ~ "Estrato 3",
      fami_estratovivienda_sbpro == "Estrato 4" ~ "Estrato 4",
      fami_estratovivienda_sbpro == "Estrato 5" ~ "Estrato 5",
      fami_estratovivienda_sbpro == "Estrato 6" ~ "Estrato 6",
      fami_estratovivienda_sbpro == "Sin Estrato" ~ "Sin Estrato",
      fami_estratovivienda_sbpro == "Estrato 0" ~ "Sin Estrato",
      TRUE ~ NA_character_
    ),
    
    # COMPUTADOR - SABER PRO

    
    fami_tienecomputador_sbpro = case_when(
      fami_tienecomputador_sbpro %in% c("Si", "No") ~
        fami_tienecomputador_sbpro,
      TRUE ~ NA_character_
    ),
    

    # INTERNET - SABER PRO
    
    fami_tieneinternet_sbpro = case_when(
      fami_tieneinternet_sbpro %in% c("Si", "No") ~
        fami_tieneinternet_sbpro,
      TRUE ~ NA_character_
    )
  )


# LIMPIEZA DEL NÚCLEO DE PREGRADO - SABER PRO

base_final_limpia <- base_final_limpia %>%
  mutate(
    estu_nucleo_pregrado_sbpro = stri_trans_general(
      estu_nucleo_pregrado_sbpro,
      "Latin-ASCII"
    ),
    
    estu_nucleo_pregrado_sbpro = case_when(
      
      # Faltantes y categorías sin información
      estu_nucleo_pregrado_sbpro %in% c(
        "SIN CLASIFICAR",
        "SIN ESPECIFICAR"
      ) ~ NA_character_,
      
      # Correcciones de escritura
      estu_nucleo_pregrado_sbpro == "DISENIO" ~
        "DISENO",
      
      estu_nucleo_pregrado_sbpro ==
        "AT​ES PLASTICAS, VISUALES Y AFINES" ~
        "ARTES PLASTICAS, VISUALES Y AFINES",
      
      estu_nucleo_pregrado_sbpro ==
        "INGENIERIA ADMNISTRATIVA Y AFINES" ~
        "INGENIERIA ADMINISTRATIVA Y AFINES",
      
      TRUE ~ estu_nucleo_pregrado_sbpro
    )
  )

# LIMPIEZA DE PUNTAJES - SABER PRO
# Se conservan únicamente estudiantes cuyos cinco puntajes:
#   1. Sean numéricos
#   2. Sean valores enteros
#   3. Estén entre 0 y 300
#
# Si alguno de los cinco puntajes incumple el criterio,
# se elimina toda la fila del estudiante.

base_final_limpia <- base_final_limpia %>%
  filter(
    !is.na(mod_competen_ciudada_punt_sbpro),
    !is.na(mod_comuni_escrita_punt_sbpro),
    !is.na(mod_ingles_punt_sbpro),
    !is.na(mod_lectura_critica_punt_sbpro),
    !is.na(mod_razona_cuantitat_punt_sbpro),
    
    mod_competen_ciudada_punt_sbpro >= 0,
    mod_competen_ciudada_punt_sbpro <= 300,
    mod_competen_ciudada_punt_sbpro == floor(mod_competen_ciudada_punt_sbpro),
    
    mod_comuni_escrita_punt_sbpro >= 0,
    mod_comuni_escrita_punt_sbpro <= 300,
    mod_comuni_escrita_punt_sbpro == floor(mod_comuni_escrita_punt_sbpro),
    
    mod_ingles_punt_sbpro >= 0,
    mod_ingles_punt_sbpro <= 300,
    mod_ingles_punt_sbpro == floor(mod_ingles_punt_sbpro),
    
    mod_lectura_critica_punt_sbpro >= 0,
    mod_lectura_critica_punt_sbpro <= 300,
    mod_lectura_critica_punt_sbpro == floor(mod_lectura_critica_punt_sbpro),
    
    mod_razona_cuantitat_punt_sbpro >= 0,
    mod_razona_cuantitat_punt_sbpro <= 300,
    mod_razona_cuantitat_punt_sbpro == floor(mod_razona_cuantitat_punt_sbpro)
  )
```
