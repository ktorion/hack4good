# Hackathon For Good: La Región de AWS en España al Servicio de la Sociedad


## Descripción del Proyecto

¿Qué problema estamos tratando de resolver?
Estamos tratando de resolver el reto de Acciona, que consiste en identificar problemas y soluciones para mejorar la eficiencia energética, la sostenibilidad de la infraestructura y las comunidades en las que opera la compañía. Para ello, utilizaremos Opstack para crear un asistente de preguntas y respuestas que tomará multiples fuentes de datos relacionados con acciona, los convertirá en vectores y los utilizará para dar recomendaciones sobre cómo mejorar la eficiencia energética, el consumo del agua, propondra tambien mejoras, y nuevas infraestructuras a medida que se incorporen nuevas herramientas y duentes de datos al modelo llm.

¿Cuál es la solución propuesta?
Nuestra solución propuesta es un asistente de preguntas y respuestas basado en Opstack que utiliza datos sobre infraestructuras para dar recomendaciones de eficiencia energética. Utilizamos fuentes de datos con información real para entrenar el modelo, lo que permite que las recomendaciones sean precisas y efectivas. Nuestro enfoque único para este reto es el uso de Opstack para crear un asistente que pueda procesar y analizar grandes cantidades de datos para dar recomendaciones personalizadas a cada cliente.
## Diagrama de Arquitectura

![Arquitectura LLM-LangChain-OpenAI-Pinecone](https://i.imgur.com/YJkUdk8.png)
)

En este diagrama, podemos observar cuatro componentes principales:
Data-sources: Este es el lugar donde se almacenan todas las fuentes de datos que se utilizarán para entrenar el modelo de LLM y para generar respuestas. Aquí es donde se realiza la preprocesamiento y limpieza de los datos.
LLM (Language Model Microservice): Este componente es el encargado de entrenar el modelo de LLM (por ejemplo, con el framework Hugging Face) y almacenarlo para su posterior uso. Este modelo se entrenará con las fuentes de datos del Data Lake y se utilizará para generar respuestas.
LangChain: Esta herramienta es una biblioteca de procesamiento del lenguaje natural (NLP) que ayuda a transformar las entradas del usuario en un formato legible por el modelo LLM. LangChain también se encargará de formatear y tokenizar la entrada del usuario para que el modelo LLM pueda procesarla adecuadamente.
Pinecone y OpenAI: Estos componentes se encargan de almacenar el modelo LLM y generar respuestas a las preguntas del usuario. El modelo LLM entrenado se almacena en Pinecone para facilitar su acceso y consultas rápidas usando vectores. OpenAI se utiliza para generar las respuestas a las preguntas de los usuarios y crea los embeddings del cuerpo de datos (data warehouse), utilizando el modelo LLM y los datos almacenados en Pinecone.

Cliente: Esta es la interfaz de usuario del asistente virtual que permite a los usuarios interactuar con la aplicación y recibir las respuestas generadas por OpenAI (aun no construido, en proceso)

## Descripción Técnica

Una visión general de:

**Para nuestra solución, hemos planteado una arquitectura basada en microservicios, que nos permite desplegar y escalar los servicios de manera individual y modular. Utilizamos Opstack como motor de procesamiento del lenguaje natural, y proponemos el desarrollo de  una API que conecta el modelo con nuestro asistente de preguntas y respuestas.

**¿Qué tecnologías AWS se han utilizado?**
Hemos utilizado Amazon SageMaker para entrenar el modelo, Amazon EC2 para la infraestructura y Amazon API Gateway para exponer nuestra API.
tambien usamos lambda en un principio, pero debido al poco tiempo del reto solo tenemos disponible un demo de la solucion de indexacion de vectores y las respuestas aportadas por nuestro modelo llm de ultima generacion (gpt-4)

## Team Members
emorek2004@gmail.com
 
## en el archivo adjuntamos un cuaderno de jupyter con la solución en funcionamiento
