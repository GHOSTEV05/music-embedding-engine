# Modelo de Dominio

## Descripción General

El modelo de dominio representa los principales conceptos y relaciones involucradas en el sistema de recomendación musical basado en aprendizaje automático. El objetivo del modelo es describir cómo interactúan las entidades relacionadas con el análisis acústico, la generación de representaciones musicales y la producción de recomendaciones.

El sistema se centra en el procesamiento de canciones y en la generación de representaciones acústicas capaces de capturar características relevantes del audio para posteriormente encontrar similitudes entre canciones.

---

# Entidades del Dominio

## Cancion

Representa una canción proporcionada al sistema para su análisis y procesamiento.

La entidad contiene la información principal del audio y sirve como punto de partida para la extracción de características acústicas.

### Responsabilidades

* Proveer el audio a analizar.
* Asociarse con características acústicas.
* Participar en el proceso de recomendación.

---

## CaracteristicasAcusticas

Representa el conjunto de propiedades acústicas extraídas de una canción.

Estas características describen matemáticamente distintos aspectos del audio, permitiendo que el sistema procese y compare canciones.

### Ejemplos de características

* MFCC
* Tempo
* Chroma Features
* Centroide espectral

### Responsabilidades

* Representar información acústica de la canción.
* Facilitar el análisis musical computacional.

---

## ExpertoMusical

Representa el componente central encargado de analizar canciones y generar recomendaciones musicales.

Esta entidad interactúa con las canciones, las representaciones acústicas y la memoria musical para producir resultados basados en similitud.

### Responsabilidades

* Analizar canciones.
* Generar representaciones acústicas.
* Generar recomendaciones.
* Utilizar la memoria musical del sistema.

---

## MemoriaMusical

Representa el componente encargado de almacenar información musical procesada por el sistema.

Permite conservar representaciones acústicas y conocimiento previamente generado para futuras búsquedas y comparaciones.

### Responsabilidades

* Almacenar información musical.
* Facilitar búsquedas posteriores.
* Mantener representaciones acústicas persistentes.

---

## RepresentacionAcustica

Representa una representación matemática o vectorial de una canción generada a partir de sus características acústicas.

Esta entidad es utilizada para calcular similitud entre canciones y generar recomendaciones.

### Responsabilidades

* Representar canciones mediante embeddings o vectores.
* Permitir cálculos de similitud.
* Facilitar el proceso de recomendación.

---

## Recomendacion

Representa el resultado generado por el sistema después de analizar y comparar canciones.

Las recomendaciones corresponden a canciones consideradas similares según sus propiedades acústicas.

### Responsabilidades

* Presentar canciones relacionadas.
* Mostrar resultados al usuario.
* Facilitar el descubrimiento musical.

---

# Relaciones del Modelo

* El componente ExpertoMusical analiza canciones.
* Las canciones poseen características acústicas.
* El componente ExpertoMusical genera representaciones acústicas.
* La MemoriaMusical almacena representaciones acústicas.
* El componente ExpertoMusical genera recomendaciones musicales.
* Las representaciones acústicas permiten establecer relaciones de similitud entre canciones.

---

# Objetivo del Modelo

El propósito de este modelo de dominio es representar conceptualmente el funcionamiento del sistema antes de su implementación técnica, identificando las entidades principales y sus relaciones dentro del problema de recomendación musical basada en características acústicas y aprendizaje automático.
