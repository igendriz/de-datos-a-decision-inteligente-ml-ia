## Recomendación práctica

La organización del material seguirá una estrategia orientada a la transparencia, la reproducibilidad, la preservación de versiones estables y la citación académica. Para ello, se recomienda utilizar GitHub como repositorio principal del material, Zenodo como plataforma para preservación de versiones estables con DOI y, posteriormente, un preprint como referencia académica principal asociada al contenido.

### 1. Crear el repositorio en GitHub

El repositorio en GitHub deberá incluir:

- slides de la presentación;
- notebook del estudio de caso;
- `README.md`;
- referencias utilizadas;
- instrucciones de uso;
- archivo de ambiente, como `requirements.txt` o `environment.yml`;
- licencia de uso;
- archivo `CITATION.cff`.

El repositorio funcionará como punto principal de acceso al material didáctico, al código, al notebook y a los recursos complementarios.

### 2. Incluir una sección “Cómo citar” en el `README.md`

El archivo `README.md` deberá contener una sección específica de citación, que podrá ser actualizada conforme estén disponibles las versiones archivadas y el documento académico asociado.

Referencia inicial sugerida para el repositorio:

```text
Sánchez-Gendriz, I. (2026). De los datos a la toma inteligente de decisiones:
aplicaciones de Machine Learning, Data Mining e Inteligencia Artificial en
Ingeniería Civil y de Sistemas [Material didáctico de palestra]. Semana
Internacional de Ingeniería, Universidad Cooperativa de Colombia, 6–8 de mayo
de 2026. GitHub. URL: insertar enlace del repositorio.
````

También puede incluirse una nota como:

```text
La referencia recomendada será actualizada posteriormente con el DOI de la
versión archivada y, en una etapa posterior, con la referencia del preprint
académico asociado al material.
```

### 3. Crear una release estable en GitHub

Después de organizar la versión utilizada en la presentación, se recomienda crear una release estable en GitHub, por ejemplo:

* `v1.0.0`;
* título: `De los datos a la toma inteligente de decisiones — material de la presentación`.

Esta release representará una versión estable del material, adecuada para preservación y referencia.

### 4. Conectar GitHub con Zenodo y archivar la release

Se recomienda conectar el repositorio de GitHub con Zenodo y archivar la release estable. El flujo usual consiste en vincular la cuenta de GitHub con Zenodo, habilitar el repositorio y crear una release en GitHub. A partir de esa release, Zenodo puede archivar la versión y generar un DOI.

El papel de Zenodo será preservar una versión específica del repositorio, incluyendo código, notebook, slides y archivos complementarios. El DOI generado permitirá citar la versión exacta del material utilizado.

Referencia sugerida para la versión archivada:

```text
Sánchez-Gendriz, I. (2026). De los datos a la toma inteligente de decisiones:
aplicaciones de Machine Learning, Data Mining e Inteligencia Artificial en
Ingeniería Civil y de Sistemas [Material didáctico de palestra]. Semana
Internacional de Ingeniería, Universidad Cooperativa de Colombia, 6–8 de mayo
de 2026. Zenodo. DOI: insertar DOI.
```

Nota recomendada:

```text
El repositorio de GitHub contiene la versión de desarrollo y actualización del
material. La versión estable preservada debe citarse mediante el DOI de Zenodo.
```

### 5. Preparar posteriormente un documento académico en formato de preprint

Se recomienda preparar posteriormente un documento académico en formato de preprint, describiendo de manera más formal:

* motivación y contexto;
* fundamentos conceptuales;
* estudio de caso;
* base de datos utilizada;
* pipeline de análisis;
* código y notebook;
* principales resultados;
* discusión sobre el uso de datos, modelos y toma de decisión informada.

Cuando el preprint esté disponible, este deberá ser indicado como la citación académica principal del material.

Referencia sugerida para el preprint:

```text
Sánchez-Gendriz, I. (2026). De los datos a la toma inteligente de decisiones:
aplicaciones de Machine Learning, Data Mining e Inteligencia Artificial en
Ingeniería Civil y de Sistemas. Preprint. DOI/arXiv: insertar identificador.
```

Nota recomendada:

```text
Para citar el material académico asociado a esta presentación, utilice
preferentemente la referencia del preprint. El repositorio de GitHub contiene
el material complementario, y Zenodo preserva una versión estable del código,
notebook, slides y archivos asociados.
```

## Por qué usar también `CITATION.cff`

Se recomienda incluir un archivo `CITATION.cff` en el repositorio. GitHub utiliza este archivo para mostrar automáticamente una sugerencia de citación en la página del proyecto, facilitando la reutilización adecuada del material por parte de otros usuarios.

El archivo `CITATION.cff` puede actualizarse conforme evolucionen las referencias del material:

1. inicialmente, con la referencia del repositorio GitHub;
2. posteriormente, con el DOI de Zenodo;
3. finalmente, con la referencia del preprint, cuando esté disponible.

El uso de `CITATION.cff` es especialmente útil porque mantiene la información de citación de forma explícita, estructurada y visible dentro del propio repositorio.

## Forma sugerida de citación

En la etapa inicial, puede recomendarse citar el repositorio de GitHub:

```text
Sánchez-Gendriz, I. (2026). De los datos a la toma inteligente de decisiones:
aplicaciones de Machine Learning, Data Mining e Inteligencia Artificial en
Ingeniería Civil y de Sistemas [Material didáctico de palestra]. Semana
Internacional de Ingeniería, Universidad Cooperativa de Colombia, 6–8 de mayo
de 2026. GitHub. URL: insertar enlace del repositorio.
```

Después de archivar la release en Zenodo, se recomienda citar la versión estable mediante el DOI:

```text
Sánchez-Gendriz, I. (2026). De los datos a la toma inteligente de decisiones:
aplicaciones de Machine Learning, Data Mining e Inteligencia Artificial en
Ingeniería Civil y de Sistemas [Material didáctico de palestra]. Semana
Internacional de Ingeniería, Universidad Cooperativa de Colombia, 6–8 de mayo
de 2026. Zenodo. DOI: insertar DOI.
```

Después de publicar el preprint, se recomienda utilizarlo como referencia académica principal:

```text
Sánchez-Gendriz, I. (2026). De los datos a la toma inteligente de decisiones:
aplicaciones de Machine Learning, Data Mining e Inteligencia Artificial en
Ingeniería Civil y de Sistemas. Preprint. DOI/arXiv: insertar identificador.
```

## Estrategia final de citación

La estrategia recomendada es utilizar cada plataforma con una función específica:

* **GitHub:** acceso al material, código, notebook, slides y actualizaciones;
* **Zenodo:** preservación de una versión estable del repositorio y generación de DOI;
* **Preprint:** citación académica principal y descripción formal del material.

De esta forma, el material queda disponible, reproducible, preservado y adecuadamente preparado para citación académica.

## Enlaces útiles

* Zenodo: [https://openscience.cern/zenodo](https://openscience.cern/zenodo)
* Guía pyOpenSci sobre citación de código: [https://www.pyopensci.org/lessons/package-share-code/publish-share-code/cite-code.html](https://www.pyopensci.org/lessons/package-share-code/publish-share-code/cite-code.html)
* Documentación de GitHub sobre archivos `CITATION.cff`: [https://docs.github.com/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files](https://docs.github.com/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files)
* Documentación de Zenodo sobre `CITATION.cff`: [https://help.zenodo.org/docs/github/describe-software/citation-file/](https://help.zenodo.org/docs/github/describe-software/citation-file/)

```
