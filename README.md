![UBA Logo](assets/fiuba.jpg)  
# **Universidad de Buenos Aires**  

**Especialización en Inteligencia Artificial**

**Alumno:** Ing. Nicolás Tertusio

**Profesor:** Dr. Rodrigo Cardenas

## Portafolio de Procesamiento de Lenguaje Natural

Este repositorio contiene los desafios realizados durante la materia de Procesamiento de Lenguaje Natural (PLN), parte de la Especialización en Inteligencia Artificial de la Universidad de Buenos Aires. El objetivo de este portafolio es demostrar el conocimiento y las habilidades adquiridas en técnicas de PLN, aplicadas a diferentes problemas y datasets. Cada capítulo corresponde a un desafio especifico que aborda un aspecto clave del procesamiento de lenguaje natural.

### 1. **Desafío 1: Vectorización de texto y Modelo Naïve Bayes**  
En este desafío, se aborda la clasificación de texto utilizando el dataset 20 Newsgroups, un conjunto de datos clásico en el campo del Procesamiento de Lenguaje Natural. Este dataset consiste en un conjunto de artículos de noticias categorizados en 20 diferentes grupos de discusión.

**Objetivos**:

 - **Carga de Datos**: Los datos se cargan utilizando la librería sklearn, que ya proporciona el dataset preprocesado y separado en conjuntos de entrenamiento y prueba.
 - **Vectorización**: Se implementa la vectorización de texto usando TfidfVectorizer, una técnica que convierte el texto en una matriz documento-término, donde cada elemento representa la importancia de una palabra en un documento en comparación con el corpus completo.
 - **Clasificación**: Se entrena un modelo de clasificación Naïve Bayes, específicamente MultinomialNB y ComplementNB, para predecir la categoría de noticias a partir de sus representaciones vectorizadas.
 - **Evaluación**: La efectividad del modelo se mide mediante la métrica de F1-score, evaluando así su precisión en la tarea de clasificación.

Este desafío introduce conceptos fundamentales de PLN, como la vectorización de texto y el uso de modelos probabilísticos para la clasificación de documentos.

### 2. **Desafío 2: Custom Embeddings con Gensim**  
Este desafío tiene como objetivo la creación de embeddings personalizados a partir de un corpus específico utilizando la biblioteca Gensim. Los embeddings son representaciones vectoriales de palabras que capturan su significado en función del contexto en el que aparecen en los textos. Por motivos de copyright no es posible compartir el corpus utilizado, pero se basa en una aventura para el juego de rol Calabozos y Dragones.

Objetivos:

 - **Generación de Embeddings**: Se construyen embeddings personalizados usando la técnica de Word2Vec, un modelo que entrena vectores de palabras en función de su contexto en un corpus de texto.
 - **Preprocesamiento**: El texto es preprocesado para preparar los datos para el entrenamiento, incluyendo la tokenización y la organización del corpus en oraciones o documentos.
 - **Entrenamiento**: Se entrena el modelo Word2Vec para generar embeddings que luego pueden ser utilizados para diversas tareas de PLN, como similitud de palabras, análisis semántico, entre otros.
 - **Evaluación y Visualización**: Se evalúan las relaciones entre palabras utilizando los embeddings generados, y se visualizan los resultados para interpretar las características semánticas capturadas.

Este desafío profundiza en la creación de representaciones vectoriales de palabras, un componente clave en muchas aplicaciones de PLN.

### 3. **Desafío 3: Modelo de Lenguaje con Tokenización por Caracteres / Palabras**  
Este desafío explora la creación de un modelo de lenguaje basado primeramente en la tokenización por caracteres y segundo por palabras, utilizando diferentes arquitecturas de redes neuronales recurrentes (RNNs). El objetivo es entrenar un modelo que sea capaz de generar texto coherente a partir de un corpus específico.

Objetivos:

 - **Preprocesamiento**: El texto se tokeniza a nivel de caracteres o palabras, lo que permite capturar secuencias más finas de información. El dataset se estructura en secuencias de entrenamiento y validación para preparar el modelo.
 - **Modelado**: Se implementan varias arquitecturas de redes neuronales, incluyendo SimpleRNN, LSTM, y GRU. Estas redes se entrenan para predecir el próximo carácter o palabra en una secuencia, un enfoque común en la generación de lenguaje.
 - **Generación de Secuencias**: Se utilizan técnicas como greedy search y beam search (en versiones determinísticas y estocásticas) para generar nuevas secuencias de texto a partir de secuencias de contexto. Se explora el impacto de la temperatura en la variabilidad de las secuencias generadas.
 - **Evaluación**: El desempeño del modelo se evalúa a través de la perplejidad, un indicador de cuán bien el modelo predice la siguiente secuencia de caracteres o palabra. Además, se compara la calidad de las secuencias generadas por las diferentes arquitecturas.

Este desafío permite entender cómo los modelos de lenguaje pueden ser entrenados para generar texto basado en caracteres individuales o palabras completas, y cómo diferentes arquitecturas de RNNs pueden influir en la calidad de las predicciones y las secuencias generadas.

### 4. **Desafío 4: LSTM Bot QA**  
Este desafío utiliza el dataset ConvAI2 (Conversational Intelligence Challenge 2) originalmente armado para crear agentes capaces de mantener una conversación en cualquier tipo de tema. Se utilizan las mismas técnicas de tokenización empleadas en el desafío anterior para construir un bot que responda preguntas de usuario.

Objetivos:

 - **Preprocesamiento**: El texto se tokeniza, se agregan los tokens de eos (end of sentence) y sos (start of sentence) y se crean los diccionarios idx2word y word2idx para transformar tokens a palabras y viceversa.
 - **Embeddings**: Se utilizan embeddings pre-entrenados de GloVe para transformar tokens de entrada en vectores.
 - **Modelado**: Se diseña y entrena una estructura encoder-decoder basadas en unidades recurrentes de tipo LSTM con una capa densa con activación tipo softmax para las predicciones finales.
 - **Inferencia**: Pruebas del modelo por medio de inferencias haciendo dando entradas de texto para recibir respuestas demuestran que para ciertas secuencias que se encuentran muy presentes en el dataset, se obtienen respuestas coherentes, pero para otras secuencias mas inusuales o completamente nuevas, las respuestas son incoherentes.

Este desafío muestra una de las formas en las que comenzaron a utilizar la tokenizacion de palabras y los vectores de embeddings para resolver tareas como conversaciones. 

### 5. **Desafío 5: Análisis de sentimiento y transfer learning con BERT**  
Este último desafío aborda el tema de análisis de sentimiento utilizando el modelo BERT como base. Se aplican técnicas generales de inteligencia artificial como es transfer learning por medio de fine tuning y feature extraction para ajustar el modelo base de BERT a la tarea de determinar si los reviews de una aplicacion son positivos, negativos o neutros.

Objetivos:

 - **Preprocesamiento**: El dataset utilizado da los comentarios y puntaje (del 1 al 5) de los usuarios a una aplicación. Los datos desbalanceados se corrigieron cambiando la escala de 1 a 5 por una clasificación de positivo, neutro o negativo.
 - **Feature extraction**: Congelando el modelo BERT se entrena una capa densa para clasificar los reviews. Los resultados son mejores que un modelo completamente aleatorio, y consiguen clasificar con buena precisión reviews positivos. Sin embargo tiene problemas para clasificar correctamente reviews negativos y neutros.
 - **Fine tuning**: Utilizando un learning rate mas bajo y sin congelar el modelo BERT, se entrena el modelo para clasificar los reviews. Los resultados son considerablemente mejores: el modelo aprende a diferenciar con alta precisión las tres categorias, aunque presenta algunas dificultades para diferenciar neutro de positivo y neutro de negativo.

Este desafío muestra el poder de transfer learning y cómo se puede utilizar en el entorno de Procesamiento de Lenguaje Natural. Se encara el problema de análisis de sentimiento, una tarea compleja que puede resultar compleja incluso para las personas. La mayor barrera resultó diferenciar neutro de positivo y neutro de negativo, que en el lenguaje a veces pueden estar separados por lineas muy delgadas.

---
