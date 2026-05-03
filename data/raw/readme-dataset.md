# Dataset: Concrete Compressive Strength

## 📌 Descripción

Este proyecto utiliza el dataset **Concrete Compressive Strength**, ampliamente
empleado en estudios de Machine Learning aplicados a Ingeniería Civil.

El dataset contiene información sobre la composición de mezclas de concreto y
su resistencia a la compresión, medida en laboratorio.

## 🌐 Fuente

Repositorio oficial:

https://archive.ics.uci.edu/dataset/165/concrete+compressive+strength

Este dataset forma parte del **UCI Machine Learning Repository**, una de las
principales fuentes públicas de datasets para investigación y docencia.

## 📦 Acceso programático

En este proyecto, los datos se obtienen mediante la biblioteca `ucimlrepo`:

```python
from ucimlrepo import fetch_ucirepo 

# fetch dataset 
concrete_compressive_strength = fetch_ucirepo(id=165) 

# data
X = concrete_compressive_strength.data.features 
y = concrete_compressive_strength.data.targets
````

Esto permite reproducir el análisis sin necesidad de almacenar localmente los datos originales.

## 📊 Descripción general

* Número de muestras: 1030
* Variables de entrada: 8
* Variable de salida: resistencia a la compresión (MPa)
* Tipo de problema: regresión

## 🔬 Variables

Las variables de entrada corresponden a componentes de la mezcla y edad del concreto:

* Cemento
* Escoria de alto horno
* Ceniza volante
* Agua
* Superplastificante
* Agregado grueso
* Agregado fino
* Edad (días)

Variable objetivo:

* Resistencia a la compresión del concreto (MPa)

## 📚 Referencia original

Yeh, I.-C. (1998).
*Modeling of strength of high-performance concrete using artificial neural networks.*
Cement and Concrete Research, Vol. 28, No. 12, pp. 1797–1808.

## 📝 Notas

* Los datos son cargados dinámicamente mediante API.
* No se incluyen copias locales del dataset original en el repositorio.
* Se recomienda consultar la fuente oficial para información adicional.