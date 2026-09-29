# ENAHO 2025: Ingreso laboral, modelo de Mincer y red neuronal

Proyecto de análisis del ingreso laboral en el Perú utilizando microdatos de la **Encuesta Nacional de Hogares (ENAHO) 2025**.

El objetivo es analizar cómo varía el ingreso de los trabajadores dependientes según características educativas, demográficas y laborales, y comparar la capacidad predictiva de un **modelo lineal de ingresos tipo Mincer** frente a una **red neuronal MLP**.

## Pregunta de investigación

¿Cómo varía el ingreso de los trabajadores dependientes según educación, sexo, área de residencia y actividad económica, y cuánto aportan estas variables a la predicción del ingreso?

## Datos

Se utilizan microdatos de la **ENAHO 2025**, integrando principalmente los módulos:

- Módulo 200: características de los miembros del hogar.
- Módulo 300: educación.
- Módulo 400: salud y afiliación a seguros.
- Módulo 500: empleo e ingresos.

Luego del proceso de integración, limpieza y selección se construye una muestra analítica de trabajadores ocupados con ingreso laboral positivo y variables consistentes.

Los microdatos originales no se incluyen en este repositorio.

## Metodología

El proyecto incluye:

- Integración y limpieza de microdatos ENAHO.
- Construcción de variables de educación, experiencia potencial, área, sector e informalidad.
- Análisis descriptivo de brechas de ingreso.
- Estimación de una ecuación de ingresos tipo **Mincer** mediante OLS con errores estándar robustos.
- Entrenamiento de una **red neuronal MLPRegressor**.
- Comparación predictiva de ambos modelos utilizando el mismo conjunto de prueba.

La variable objetivo utilizada en los modelos es:

```text
ln_ingreso = log(ingreso_mensual)

## Herramientas

- Python
- pandas
- NumPy
- statsmodels
- scikit-learn
- matplotlib
- Jupyter Notebook

## Origen del proyecto
Este proyecto amplía un trabajo académico grupal realizado en el curso de Ciencia de Datos Aplicada, reemplazando la base simplificada del ejercicio original por microdatos reales de ENAHO 2025.
Se reconoce a Emilio Augusto Vera Meza como compañero del trabajo académico de origen.