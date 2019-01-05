# tm-socialmedia

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/d7d598ca45d64cd08ee8b4e14f1f6cfb)](https://app.codacy.com/app/davix16/tm-socialmedia?utm_source=github.com&utm_medium=referral&utm_content=davix16/tm-socialmedia&utm_campaign=Badge_Grade_Settings)

Predicción de género en Twitter. Máster en Big Data, asignatura Text Mining en Social Media



## Abstract
Esta tarea ha sido centrada en el estudio y modelado del género de los autores en Twitter. Haciendo uso de una extensa colección de tweets, se han extraído un conjunto de características diferenciadoras del género: emojis, preposiciones, palabras usadas, media de palabras por tweet... 

Con Python como lenguaje, y haciendo uso de diferentes técnicas, algunas de ellas avanzadas (Machine Learning), el objetivo ha sido predecir en base a un tweet el género de la persona que lo escribe, con el mayor acierto posible.

Uno de los principales retos encontrados ha sido la mala escritura presente en general en las redes sociales, y más concretamente, en Twitter. Las faltas gramaticales, las repeticiones de caracteres, faltas de signos de puntuación, etc, han ocasionado numerosos problemas a la hora de realizar el procesamiento del texto y la extracción de las características buscadas.

Las predicciones se han realizado con modelos de Machine Learning, realizando un ajuste de los parámetros de control en busca de un mejor resultado. Entre los modelos usados para evaluar encontramos los siguientes: SVM (Super Vector Machine), Árboles de Decisión, Random Forest y Redes Neuronales.



## Ejecución
Dentro de la carpeta **pan-ap17-bigdata**, se pueden encontrar el código fuente y los dataset necesarios. Esta será la ruta que debamos marcar como el directorio activo (si lo ejecutas desde un IDE como Spyder)

Los tweets en formato XML que se usan para entrenar y predecir los modelos se encuentran en las carpetas training y test, respectivamente. _Es necesario descomprimir los RAR incluidos en ambas carpetas para tener los XML sueltos_.

**Fase 1: Procesado.** Para el procesamiento de los datos, se debe ejecutar el archivo **_Test1.py_**. Al acabar ese archivo, se genera un txt denominado _lista_modelo.txt_ que será la entrada utilizada en la Fase 2.

**Fase 2: Entrenamiento.** Para el entrenamiento de los datos, se debe ejecutar el archivo **_Test2.py_**. Utilizando el archivo resultante de la Fase 1, entrenará los modelos y nos facilitará unos porcentajes de acierto (**en base a datos de entrenamiento**).


## Conclusiones y trabajo futuro
A lo largo de esta tarea se ha abordado el problema de la predicción del género en Twitter. No obstante, por limitaciones de tiempo, no se ha podido abordar el problema en su totalidad. Entre las tareas que se quedan pendientes para una futura iteración se encuentran:

* Aplicar los modelos entrenados a los datos de testing.
* Mejorar el procesamiento de los tweets, eliminando signos de puntuación, caracteres repetidos... Se han escapado algunos.
* Utilizar un análisis sintáctico de los tweets para detectar los adjetivos y su género, en lugar de una lista limitada y una separación en función a la terminación de los mismos.
* Probar más modelos, buscando una mejor aproximación, más rápida.
* Implementar un TF-IDF en lugar de un simple TF en la creación de las bolsas de palabras más repetidas en cada género. Creemos que puede marcar una gran diferencia.
* Abordar el problema de la identificación de la variedad del lenguaje. Al margen de los mismas características ya empleadas, creemos que el uso de los dominios de las webs acortadas en los enlaces puede ser realmente interesante, aunque potencialmente costoso en tiempo.

Finalmente, se está en general muy satisfecho con los resultados obtenidos, superiores al **70\%**. Y se cree que aún hay margen de mejora.
