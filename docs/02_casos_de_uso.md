# Especificación de Casos de Uso

---

# UC-01 — Proporcionar canción

## Descripción

Este caso de uso permite al usuario proporcionar un archivo de audio al sistema para su posterior análisis y búsqueda de similitud.

## Actor principal

Usuario

## Precondiciones

* El usuario debe poseer un archivo de audio válido (.wav o .mp3).

## Flujo principal

1. El usuario selecciona un archivo de audio.
2. El sistema valida el formato del archivo.
3. El sistema almacena temporalmente el archivo.
4. El sistema confirma la carga exitosa.

## Postcondiciones

* El archivo de audio queda disponible para el análisis acústico.

## Flujos alternativos

* Formato de archivo inválido.
* Archivo de audio corrupto.
* Error durante la carga del archivo.

---

# UC-02 — Analizar características acústicas

## Descripción

El sistema extrae características acústicas relevantes del archivo de audio proporcionado.

## Actor principal

Sistema

## Precondiciones

* Debe existir un archivo de audio válido.

## Flujo principal

1. El sistema carga la señal de audio.
2. El sistema preprocesa el audio.
3. El sistema extrae características acústicas como MFCC, centroide espectral, chroma y tempo.
4. El sistema almacena las características extraídas.

## Postcondiciones

* Se genera una representación numérica de las características acústicas.

## Flujos alternativos

* Error durante el procesamiento del audio.
* Propiedades de audio incompatibles.

---

# UC-03 — Encontrar música similar

## Descripción

Permite al sistema identificar canciones acústicamente similares a partir de una canción proporcionada.

## Actor principal

Usuario

## Precondiciones

* La canción debe haber sido analizada correctamente.
* La base de datos debe contener canciones indexadas.

## Flujo principal

1. El usuario proporciona una canción para comparación.
2. El sistema genera un embedding de la canción.
3. El sistema compara el embedding contra embeddings almacenados.
4. El sistema calcula puntuaciones de similitud.
5. El sistema retorna las canciones más similares.

## Postcondiciones

* Se muestra una lista ordenada de canciones similares.

## Flujos alternativos

* No se encontraron canciones similares.
* Error durante el cálculo de similitud.

---

# UC-04 — Escuchar canción

## Descripción

Permite al usuario reproducir una canción seleccionada dentro de los resultados obtenidos.

## Actor principal

Usuario

## Precondiciones

* La canción debe existir dentro del sistema.

## Flujo principal

1. El usuario selecciona una canción.
2. El sistema carga el audio.
3. El sistema inicia la reproducción.

## Postcondiciones

* La canción seleccionada es reproducida.

## Flujos alternativos

* Error durante la reproducción.
* Archivo no disponible.

---

# UC-05 — Almacenar canciones

## Descripción

Permite al sistema almacenar canciones procesadas junto con sus embeddings y metadatos asociados.

## Actor principal

Sistema

## Precondiciones

* La canción debe haber sido procesada correctamente.

## Flujo principal

1. El sistema almacena los metadatos de la canción.
2. El sistema almacena los embeddings generados.
3. El sistema actualiza la base de datos.

## Postcondiciones

* La canción queda disponible para futuras búsquedas de similitud.

## Flujos alternativos

* Error de conexión con la base de datos.
* Error durante el almacenamiento.

---

# UC-06 — Recomendar canciones

## Descripción

Permite al sistema recomendar canciones basadas en el análisis de similitud acústica.

## Actor principal

Sistema

## Precondiciones

* El análisis de similitud debe haberse completado.

## Flujo principal

1. El sistema evalúa las puntuaciones de similitud.
2. El sistema selecciona las canciones más relevantes.
3. El sistema muestra las recomendaciones al usuario.

## Postcondiciones

* Las canciones recomendadas son presentadas al usuario.

## Flujos alternativos

* Error durante la generación de recomendaciones.

---

# UC-07 — Integrar nueva canción

## Descripción

Permite al sistema procesar e integrar nuevas canciones dentro de la base de datos de búsqueda por similitud.

## Actor principal

Sistema

## Precondiciones

* Debe proporcionarse una canción válida.

## Flujo principal

1. El sistema analiza la nueva canción.
2. El sistema genera embeddings.
3. El sistema almacena la información procesada.
4. La canción queda disponible para futuras búsquedas.

## Postcondiciones

* La base de datos se actualiza con nueva información musical.

## Flujos alternativos

* Error durante la generación de embeddings.
* Error al actualizar la base de datos.