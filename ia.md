## Inteligencia artificial

Reconocimiento de Entidades Nombradas (NER, por sus siglas en inglés) es una técnica de procesamiento del lenguaje natural que puede utilizarse para identificar y extraer información relevante de textos. En el contexto de las facturas electrónicas, el NER podría utilizarse para identificar y extraer el Registro Federal de Contribuyentes (RFC) y el tipo de factura de un documento de texto. Sin embargo, el NER es una técnica general y puede utilizarse para extraer cualquier tipo de información relevante de textos, no solo información relacionada con facturas electrónicas.

PyTorch y spaCy son librerías de procesamiento del lenguaje natural que pueden utilizarse para construir aplicaciones de procesamiento del lenguaje natural, incluyendo aplicaciones de Reconocimiento de Entidades Nombradas (NER, por sus siglas en inglés). Los transformers son modelos de lenguaje basados en el aprendizaje profundo que han demostrado ser muy efectivos en tareas de procesamiento del lenguaje natural, como la traducción automática y el análisis de sentimiento. Es posible que Spacebot utilice PyTorch, spaCy y transformers para implementar sus funcionalidades de procesamiento del lenguaje natural.

## Arquitectura

El funcionamiento del modelo con las capas que mencionas. 

- CRF (Etiquetado Condicional de Viterbi) es una técnica utilizada para etiquetar secuencias de datos utilizando un modelo probabilístico. 
- El Dropout es una técnica de regularización utilizada para evitar el sobreajuste en los modelos de aprendizaje automático.
- La Normalización de Capas (Layer Normalization) es una técnica utilizada para normalizar los datos de entrada a una capa en un modelo de aprendizaje automáticas
- Las Capas Lineales son capas que realizan una combinación lineal de sus entradas y son ampliamente utilizadas en los modelos de aprendizaje automático. RoBERTa es un modelo de lenguaje basado en el aprendizaje profundo que ha demostrado ser muy efectivo en tareas de procesamiento del lenguaje natural.
- Tanh es una función de activación que se utiliza comúnmente en los modelos de aprendizaje automático.

<img title="" src="https://production-media.paperswithcode.com/models/roberta-conll-ner.png-0000000943-273e0355.png">

### Dataset

Este dataset parece ser un conjunto de datos que contienen información sobre empresas y sus registros tributarios (RFC, por sus siglas en español). Cada fila del conjunto de datos parece contener información sobre una empresa, como su nombre y su RFC, así como información adicional como direcciones y números de identificación. 

Algunas filas también contienen información sobre otras empresas con las que están relacionadas. Es difícil decir con certeza qué hace Spacebot con este conjunto de datos sin más contexto, pero podría utilizarlo para realizar tareas de procesamiento de lenguaje natural, como la extracción de entidades nombradas o la clasificación de empresas en categorías predefinidas.

```textile
(Nombre="SPIRIT AEROSYSTEMS INCORPORATED",)
(NumRegIdTrib="202130528", Nombre="SPIRIT AEROSYSTEMS)
(HSM-000316-H84, HUTCHINSON SEAL DE MEXICO SA DE CV
PELICANOS, HSM-000316-H84, HUTCHINSON SEAL DE MEXICO SA DE CV
PELICANOS)
(HUTCHINSON SEAL DE MEXICO SA DE CV 
PELICANOS, HSM-000316-H84, IN110507, HSM-000316-H84, HUTCHINSON SEAL DE MEXICO SA DE CV
PELICANOS)
(36-1458720, HUTCHINSON SEAL DE MEXICO SA DE CV 
PELICANOS, 76027728, HUTCHINSON SEAL DE MEXICO SA DE CV
PELICANOS, HSM-000316-H84)
(AA Space, Estapack SAPI de CV)
(ESTAPACK SAPI DE CV, EST-040824-HB5, GPV, INTERNATIONAL, DK 2656 2457)
(AA Space, Estapack SAPI de CV)
(AA Space, Estapack SAPI)
```
