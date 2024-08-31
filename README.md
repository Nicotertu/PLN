![UBA Logo](assets/fiuba.jpg)  
# **Universidad de Buenos Aires**  
# **Especialización en Inteligencia Artificial**

## Portafolio de Procesamiento de Lenguaje Natural

**Alumno:** Ing. Nicolás Tertusio

**Profesor:** Dr. Rodrigo Cardenas

---

### Descripción del Repositorio

Este repositorio contiene los desafios realizados durante la materia de Procesamiento de Lenguaje Natural (PLN), parte de la Especialización en Inteligencia Artificial de la Universidad de Buenos Aires. El objetivo de este portafolio es demostrar el conocimiento y las habilidades adquiridas en técnicas de PLN, aplicadas a diferentes problemas y datasets. Cada capítulo corresponde a un desafio especifico que aborda un aspecto clave del procesamiento de lenguaje natural.

### Contenido del Repositorio

#### 1. **Desafío 1: Vectorización de texto y Modelo Naïve Bayes**  
En este desafío, se aborda la clasificación de texto utilizando el dataset 20 Newsgroups, un conjunto de datos clásico en el campo del Procesamiento de Lenguaje Natural. Este dataset consiste en un conjunto de artículos de noticias categorizados en 20 diferentes grupos de discusión.

**Objetivos**:

 - **Carga de Datos**: Los datos se cargan utilizando la librería sklearn, que ya proporciona el dataset preprocesado y separado en conjuntos de entrenamiento y prueba.
 - **Vectorización**: Se implementa la vectorización de texto usando TfidfVectorizer, una técnica que convierte el texto en una matriz documento-término, donde cada elemento representa la importancia de una palabra en un documento en comparación con el corpus completo.
 - **Clasificación**: Se entrena un modelo de clasificación Naïve Bayes, específicamente MultinomialNB y ComplementNB, para predecir la categoría de noticias a partir de sus representaciones vectorizadas.
 - **Evaluación**: La efectividad del modelo se mide mediante la métrica de F1-score, evaluando así su precisión en la tarea de clasificación.

Este desafío introduce conceptos fundamentales de PLN, como la vectorización de texto y el uso de modelos probabilísticos para la clasificación de documentos.

#### 2. **Desafío 2: Custom Embeddings con Gensim**  
Este desafío tiene como objetivo la creación de embeddings personalizados a partir de un corpus específico utilizando la biblioteca Gensim. Los embeddings son representaciones vectoriales de palabras que capturan su significado en función del contexto en el que aparecen en los textos. Por motivos de copyright no es posible compartir el corpus utilizado, pero se basa en una aventura para el juego de rol Calabozos y Dragones.

Objetivos:

 - **Generación de Embeddings**: Se construyen embeddings personalizados usando la técnica de Word2Vec, un modelo que entrena vectores de palabras en función de su contexto en un corpus de texto.
 - **Preprocesamiento**: El texto es preprocesado para preparar los datos para el entrenamiento, incluyendo la tokenización y la organización del corpus en oraciones o documentos.
 - **Entrenamiento**: Se entrena el modelo Word2Vec para generar embeddings que luego pueden ser utilizados para diversas tareas de PLN, como similitud de palabras, análisis semántico, entre otros.
 - **Evaluación y Visualización**: Se evalúan las relaciones entre palabras utilizando los embeddings generados, y se visualizan los resultados para interpretar las características semánticas capturadas.

Este desafío profundiza en la creación de representaciones vectoriales de palabras, un componente clave en muchas aplicaciones de PLN.

#### 3. **Desafío 3: Modelo de Lenguaje con Tokenización por Caracteres / Palabras**  
Este desafío explora la creación de un modelo de lenguaje basado en la tokenización por caracteres y palabras, utilizando diferentes arquitecturas de redes neuronales recurrentes (RNNs). El objetivo es entrenar un modelo que sea capaz de generar texto coherente a partir de un corpus específico.

Objetivos:

 - **Preprocesamiento**: El texto se tokeniza a nivel de caracteres y palabras, lo que permite capturar secuencias más finas de información. El dataset se estructura en secuencias de entrenamiento y validación para preparar el modelo.
 - **Modelado**: Se implementan varias arquitecturas de redes neuronales, incluyendo SimpleRNN, LSTM, y GRU. Estas redes se entrenan para predecir el próximo carácter o palabra en una secuencia, un enfoque común en la generación de lenguaje.
 - **Generación de Secuencias**: Se utilizan técnicas como greedy search y beam search (en versiones determinísticas y estocásticas) para generar nuevas secuencias de texto a partir de secuencias de contexto. Se explora el impacto de la temperatura en la variabilidad de las secuencias generadas.
 - **Evaluación**: El desempeño del modelo se evalúa a través de la perplejidad, un indicador de cuán bien el modelo predice la siguiente secuencia de caracteres o palabra. Además, se compara la calidad de las secuencias generadas por las diferentes arquitecturas.

Este desafío permite entender cómo los modelos de lenguaje pueden ser entrenados para generar texto basado en caracteres individuales o palabras completas, y cómo diferentes arquitecturas de RNNs pueden influir en la calidad de las predicciones y las secuencias generadas.

#### 4. **Desafío 4: Titulo 4**  
   Descripcion 4

#### 5. **Desafío 5: Titulo 5**  
   Descripcion 5

---
