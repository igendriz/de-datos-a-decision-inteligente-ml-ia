# Roteiro de presentación

## De los datos a la decisión inteligente: aplicaciones de Machine Learnig, Data Mining e IA.

---

## Slide 1 — Título de la presentación

**Título:**
**Del dato a la decisión informada**

**Subtítulo:**
Estudio de caso aplicado a la predicción de la resistencia a la compresión del concreto usando Data Mining y Machine Learning

**Contenido sugerido:**
Presentar la idea general de la charla: mostrar cómo un conjunto de datos de ingeniería puede transformarse en conocimiento útil para apoyar decisiones técnicas.

**Mensaje principal:**
No se trata solo de “usar Machine Learning”, sino de construir un flujo completo de análisis: entender el problema, explorar los datos, modelar, evaluar, interpretar y apoyar decisiones.

---

## Slide 2 — Motivación general

**Título:**
¿Por qué hablar de datos en ingeniería?

**Contenido sugerido:**
Muchas áreas de la ingeniería generan datos: ensayos de laboratorio, sensores, inspecciones, registros de mantenimiento, imágenes, simulaciones y datos operacionales.

Sin embargo, los datos por sí solos no generan valor. El valor aparece cuando los datos son organizados, procesados, interpretados y transformados en información útil.

**Mensaje principal:**
La ingeniería moderna necesita integrar conocimiento técnico, análisis de datos y herramientas computacionales.

---

## Slide 3 — Pregunta guía de la presentación

**Título:**
Pregunta central del estudio de caso

**Contenido sugerido:**
**¿Cómo transformar datos experimentales de mezclas de concreto en información útil para apoyar decisiones de ingeniería?**

Explicar que esta pregunta conecta tres dimensiones:

1. El problema físico: resistencia del concreto.
2. El problema de datos: variables, distribución, relaciones y patrones.
3. El problema computacional: construcción de modelos predictivos e interpretables.

**Mensaje principal:**
El objetivo no es solamente predecir un número, sino entender el proceso de análisis completo.

---

## Slide 4 — Contexto del problema de ingeniería

**Título:**
Resistencia a la compresión del concreto

**Contenido sugerido:**
La resistencia a la compresión es una de las propiedades más importantes del concreto. Está relacionada con la composición de la mezcla, la cantidad de agua, cemento, agregados, materiales suplementarios, aditivos y la edad de curado.

Destacar que la relación entre estos factores y la resistencia final no es necesariamente lineal.

**Mensaje principal:**
Este es un problema realista para aplicar Machine Learning porque combina conocimiento de ingeniería y relaciones complejas entre variables.

---

## Slide 5 — Descripción de la base de datos

**Título:**
Base de datos utilizada

**Contenido sugerido:**
La base usada corresponde al conjunto **Concrete Compressive Strength**, disponible en el UCI Machine Learning Repository.

Características principales:

* 1030 observaciones;
* 8 variables de entrada;
* 1 variable de salida;
* datos tabulares;
* variables cuantitativas;
* sin valores ausentes;
* datos originalmente no escalados.

**Mensaje principal:**
Se trata de un dataset simple desde el punto de vista estructural, pero suficientemente rico para discutir un flujo completo de ML aplicado.

---

## Slide 6 — Variables del problema

**Título:**
Variables de entrada y variable objetivo

**Contenido sugerido:**

**Variables de entrada:**

* cemento;
* escoria;
* ceniza volante;
* agua;
* superplastificante;
* agregado grueso;
* agregado fino;
* edad.

**Variable de salida:**

* resistencia a la compresión del concreto, medida en MPa.

**Mensaje principal:**
Cada muestra representa una mezcla de concreto con una composición específica y una resistencia medida experimentalmente.

---

## Slide 7 — Tipo de problema desde Machine Learning

**Título:**
Formulación del problema de Machine Learning

**Contenido sugerido:**
Desde el punto de vista de ML, el problema principal es una tarea de **regresión supervisada**.

La entrada del modelo es:

`composición de la mezcla + edad`

La salida esperada es:

`resistencia estimada en MPa`

**Mensaje principal:**
El modelo aprende una relación aproximada entre las variables de entrada y la resistencia observada experimentalmente.

---

## Slide 8 — Flujo general del estudio de caso

**Título:**
Pipeline del análisis

**Contenido sugerido:**
Presentar el flujo del notebook:

1. Datos experimentales
2. Comprensión del problema
3. Análisis exploratorio de datos
4. Preprocesamiento
5. Representación e ingeniería de características
6. Modelos de Machine Learning
7. Evaluación de resultados
8. Interpretación
9. Toma de decisión informada

**Mensaje principal:**
Un proyecto de ML aplicado no comienza con el algoritmo. Comienza con la comprensión del problema y de los datos.

---

## Slide 9 — Carga y organización inicial de los datos

**Título:**
Primer paso: organizar los datos

**Contenido sugerido:**
Explicar que el notebook carga los datos, renombra las variables y separa:

* matriz de entrada `X`;
* variable objetivo `y`.

También se verifica:

* número de muestras;
* número de variables;
* tipos de datos;
* presencia de valores ausentes;
* unidades físicas.

**Mensaje principal:**
Antes de modelar, es necesario saber exactamente qué datos tenemos y qué significa cada variable.

---

## Slide 10 — Resumen estadístico

**Título:**
Descripción estadística inicial

**Contenido sugerido:**
Mostrar que se calcularon estadísticas básicas para cada variable:

* mínimo;
* máximo;
* media;
* mediana;
* desviación estándar;
* valores ausentes.

Destacar algunos valores importantes:

* resistencia entre aproximadamente 2.33 y 82.6 MPa;
* edad entre 1 y 365 días;
* ausencia de valores faltantes.

**Mensaje principal:**
La estadística descriptiva permite validar coherencia, identificar rangos y detectar posibles problemas antes del modelado.

---

## Slide 11 — Análisis exploratorio de distribuciones

**Título:**
Distribución de las variables

**Contenido sugerido:**
Usar la figura de histogramas con KDE.

Explicar que este análisis permite observar:

* asimetrías;
* concentración de valores;
* posibles valores extremos;
* variables con muchos ceros;
* distribución de la resistencia.

Comentar que algunas variables, como escoria, ceniza volante y superplastificante, presentan muchos valores cercanos o iguales a cero.

**Mensaje principal:**
El EDA permite comprender la estructura de los datos antes de decidir cómo modelarlos.

---

## Slide 12 — Correlación entre variables originales

**Título:**
Relaciones lineales entre variables originales

**Contenido sugerido:**
Usar la matriz de correlación de Pearson de las variables originales.

Destacar relaciones con la resistencia:

* cemento presenta correlación positiva relevante;
* edad también presenta correlación positiva;
* superplastificante tiene correlación positiva moderada;
* agua presenta correlación negativa.

También comentar relaciones entre variables de entrada, como agua y superplastificante.

**Mensaje principal:**
La correlación no explica todo, pero ayuda a identificar tendencias iniciales y relaciones importantes.

---

## Slide 13 — Preprocesamiento de los datos

**Título:**
Preparación para el modelado

**Contenido sugerido:**
Explicar las etapas de preprocesamiento usadas:

* separación entre entrada y salida;
* división de los datos en entrenamiento, validación y prueba;
* escalamiento con `StandardScaler`.

La división utilizada fue:

* entrenamiento;
* validación;
* prueba.

**Mensaje principal:**
Separar correctamente los datos evita evaluar el modelo con información que ya fue usada durante el entrenamiento.

---

## Slide 14 — Por qué usar entrenamiento, validación y prueba

**Título:**
Evaluar correctamente un modelo

**Contenido sugerido:**
Explicar la función de cada conjunto:

**Entrenamiento:** usado para ajustar el modelo.
**Validación:** usado para comparar modelos y tomar decisiones durante el desarrollo.
**Prueba:** usado solo al final para estimar el desempeño real.

**Mensaje principal:**
La evaluación debe simular la aplicación del modelo en datos nuevos.

---

## Slide 15 — Reducción de dimensionalidad

**Título:**
PCA como herramienta exploratoria

**Contenido sugerido:**
Explicar brevemente que PCA permite representar los datos en un espacio de menor dimensión.

En el notebook, PCA se usa para:

* explorar la estructura global de los datos;
* visualizar tendencias;
* analizar posibles agrupamientos;
* observar cómo se distribuyen las muestras según resistencia u otras variables.

**Mensaje principal:**
PCA no es el objetivo final, sino una herramienta para entender mejor la estructura de los datos.

---

## Slide 16 — Ingeniería de características

**Título:**
Crear nuevas variables con sentido físico

**Contenido sugerido:**
Explicar que una etapa central del notebook es crear variables derivadas a partir del conocimiento de ingeniería.

Variables creadas:

* relación agua/cemento;
* material cementicio total;
* relación agua/material;
* proporción de escoria;
* proporción de ceniza volante;
* relación de superplastificante;
* edad.

**Mensaje principal:**
Muchas veces, el modelo mejora no porque el algoritmo sea más complejo, sino porque los datos fueron representados de una forma más informativa.

---

## Slide 17 — Correlación con variables derivadas

**Título:**
Nueva representación de los datos

**Contenido sugerido:**
Usar la matriz de correlación de las variables derivadas.

Destacar que aparecen relaciones más fuertes con la resistencia, por ejemplo:

* material cementicio con correlación positiva;
* relación agua/material con correlación negativa;
* edad con correlación positiva.

También comentar que algunas variables derivadas pueden estar altamente correlacionadas entre sí.

**Mensaje principal:**
Las variables derivadas pueden capturar mejor el conocimiento físico del problema y mejorar la capacidad predictiva del modelo.

---

## Slide 18 — Modelos de regresión evaluados

**Título:**
Comparación inicial de modelos

**Contenido sugerido:**
Presentar los modelos evaluados en el notebook:

* Regresión Lineal;
* Árbol de Decisión;
* Random Forest;
* Gradient Boosting;
* MLP Regressor.

Explicar que estos modelos tienen diferentes niveles de complejidad e interpretabilidad.

**Mensaje principal:**
Comparar modelos permite entender si el problema requiere modelos simples o métodos capaces de capturar relaciones no lineales.

---

## Slide 19 — Resultado de la comparación inicial

**Título:**
Random Forest como modelo principal

**Contenido sugerido:**
Mostrar que Random Forest obtuvo el mejor desempeño en la fase de validación, tanto con variables originales como con variables derivadas.

Resultados aproximados de validación:

* variables originales: R² cercano a 0.913;
* variables derivadas: R² cercano a 0.926.

**Mensaje principal:**
El uso de variables derivadas mejoró el desempeño del modelo durante la validación.

---

## Slide 20 — Cuatro escenarios con Random Forest

**Título:**
Evaluación de diferentes representaciones

**Contenido sugerido:**
Explicar que, después de seleccionar Random Forest, se analizaron cuatro casos:

1. Variables originales.
2. Variables derivadas.
3. Variables originales + derivadas.
4. Variables preseleccionadas.

El objetivo fue comparar no solo modelos, sino también formas diferentes de representar los datos.

**Mensaje principal:**
La pregunta pasa a ser: ¿qué representación de los datos permite un modelo más útil, preciso e interpretable?

---

## Slide 21 — Importancia de características

**Título:**
Interpretación del modelo

**Contenido sugerido:**
Usar la figura de importancia de características.

Destacar:

* con variables originales, edad y cemento aparecen como variables muy importantes;
* con variables derivadas, relación agua/material y edad se vuelven predominantes;
* en los casos combinados y preseleccionados, las variables derivadas mantienen alta relevancia.

**Mensaje principal:**
La interpretación ayuda a entender qué factores están guiando las predicciones del modelo.

---

## Slide 22 — Evaluación final en test

**Título:**
Desempeño de los cuatro casos

**Contenido sugerido:**
Presentar la tabla de métricas del conjunto de prueba:

| Caso | Representación         |     R² |   RMSE |    MAE |
| ---- | ---------------------- | -----: | -----: | -----: |
| 1    | Originales             | 0.8633 | 6.3138 | 4.0360 |
| 2    | Derivadas              | 0.8907 | 5.6440 | 3.9154 |
| 3    | Originales + derivadas | 0.8990 | 5.4268 | 3.7438 |
| 4    | Preseleccionadas       | 0.8991 | 5.4232 | 3.7260 |

**Mensaje principal:**
La mejor representación no necesariamente usa todas las variables posibles. El caso con variables preseleccionadas obtuvo el mejor desempeño y mantuvo un modelo más compacto.

---

## Slide 23 — Valores reales vs. predichos

**Título:**
Visualización del desempeño predictivo

**Contenido sugerido:**
Usar la figura de valores reales vs. predichos.

Explicar cómo leer la figura:

* la diagonal representa la predicción ideal;
* puntos cercanos a la diagonal indican buenas predicciones;
* mayor dispersión indica mayor error;
* los casos 03 y 04 muestran mejor ajuste visual.

**Mensaje principal:**
Las métricas numéricas son importantes, pero las visualizaciones ayudan a interpretar el comportamiento del modelo.

---

## Slide 24 — Extensiones hacia Ingeniería de Sistemas y Software

**Título:**
Del notebook a una solución computacional

**Contenido sugerido:**
Discutir posibles extensiones del estudio de caso:

* mejorar el pipeline con validación cruzada;
* realizar ajuste de hiperparámetros;
* automatizar comparación de modelos;
* implementar un pipeline reproducible con `scikit-learn Pipeline`;
* crear una interfaz web para predicción;
* desarrollar una API;
* construir un dashboard para apoyo a decisiones.

También mencionar extensiones metodológicas:

* clasificación de resistencia en baja, media y alta;
* clustering de mezclas;
* análisis de residuos;
* explicación local de predicciones.

**Mensaje principal:**
El notebook puede evolucionar hacia un producto de software simple, pero realista, integrando datos, modelo e interfaz.

---

## Slide 25 — Conclusiones principales

**Título:**
Mensajes finales

**Contenido sugerido:**
Cerrar con los principales aprendizajes:

1. La calidad del análisis depende de todo el pipeline, no solo del algoritmo.
2. El EDA permite comprender los datos antes del modelado.
3. Las variables derivadas incorporan conocimiento de ingeniería.
4. Random Forest tuvo buen desempeño para capturar relaciones no lineales.
5. La interpretación es esencial para transformar predicciones en decisiones.
6. El mismo flujo puede extenderse a otros problemas de ingeniería y desarrollo de software.

**Mensaje principal:**
Machine Learning aplicado a ingeniería debe ser entendido como un proceso de apoyo a la toma de decisiones, no como una caja negra aislada.
