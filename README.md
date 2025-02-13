# tarea-POWER-BI

Instrucciones para la entrega

1) Crear un nuevo repositorio en GitHub

El repositorio debe ser específico para esta tarea y contener los archivos correspondientes.

2) Adjuntar tu archivo .pbix

El archivo TAREA POWER BI NANDE 3.pbix debe subirse al repositorio. Este archivo contiene el dashboard desarrollado con la base de datos seleccionada.

3) Crear un archivo README.md

Descripción del dashboard

El dashboard en Power BI fue construido utilizando una base de datos con indicadores económicos, laborales y de gasto público.

Elementos clave del dashboard:

Tarjetas KPI: Se incluyeron tarjetas para visualizar indicadores como el PIB, la inflación y el índice de Gini.

Gráficos de tendencias: Se implementaron gráficos de líneas para analizar la evolución de diferentes variables a lo largo del tiempo.

Segmentaciones: Se agregaron filtros interactivos para facilitar la exploración de los datos.

Relaciones entre tablas: Se establecieron relaciones para conectar distintas fuentes de información y mejorar la interactividad del dashboard.

Cálculos y Métricas (DAX)

Algunas medidas incluidas en el modelo son:

Total del PIB

Total PIB = SUM('base 1'[PIB])

Inflación Promedio

Inflacion Promedio = AVERAGE('base 1'[INFLACIÓN])

Índice de GINI Promedio

GINI Promedio = AVERAGE('base 1'[INDICE DE GINI])

Variación del PIB (% Cambio Año a Año)

Variacion PIB (%) = 
VAR AnioAnterior = CALCULATE(SUM('base 1'[PIB]), PREVIOUSYEAR('base 1'[AÑO]))
RETURN 
IF(AnioAnterior = BLANK(), BLANK(), (SUM('base 1'[PIB]) - AnioAnterior) / AnioAnterior * 100)

Variación de la Inflación (%)

Variacion Inflacion (%) = 
VAR AnioAnterior = CALCULATE(AVERAGE('base 1'[INFLACIÓN]), PREVIOUSYEAR('base 1'[AÑO]))
RETURN 
IF(AnioAnterior = BLANK(), BLANK(), (AVERAGE('base 1'[INFLACIÓN]) - AnioAnterior) / AnioAnterior * 100)

Gasto en Educación como % del PIB

Gasto Educacion % = 
DIVIDE(SUM('base 1'[GAS_EDU_SUP]), SUM('base 1'[PIB])) * 100

Gasto en Salud como % del PIB

Gasto Salud % = 
DIVIDE(SUM('base 1'[Gasto corriente en salud (% del PIB)]), SUM('base 1'[PIB])) * 100

Tasa de Desempleo Promedio

Desempleo Promedio = AVERAGE('base 1'[DESEMP, TO (% DE LA FZA LAB TO)])

Tasa de Fuerza Laboral sobre la Población Total

Fuerza Laboral % = 
DIVIDE(SUM('base 1'[FZA_LAB]), SUM('base 1'[POBLACIÓN])) * 100

4) Subir ambos archivos al repositorio

Asegúrate de que tanto el archivo .pbix como el README.md estén en el repositorio antes de la entrega final.

# Adjunto la imagen de la tarea creada

![image](https://github.com/user-attachments/assets/9b44f5ad-2c2e-4c87-b02c-5b17c8958784)

