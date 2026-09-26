# SyllabusAI

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21423173.svg)](https://doi.org/10.5281/zenodo.21423173)

**Aplicación:** https://fborrasumh.github.io/sillabusAI/

Genera la **guía docente** (sílabo, programa de asignatura) completa de una asignatura universitaria a partir de unos pocos datos, con las competencias oficiales del título y los créditos de cada país. Aplicación de un solo fichero (`index.html`), sin servidor: la clave de OpenAI se guarda solo en el navegador.

## Novedades de la versión 2.0

- Interfaz guiada en cuatro pasos con el estilo de Forja, ejemplos de seis disciplinas y una guía de demostración que se abre sin clave.
- **Competencias oficiales**: pegadas desde la memoria verificada, se citan literalmente con sus códigos; la revisión marca como error cualquier código que no esté en la memoria.
- **Créditos por país** (España, México, Argentina, Colombia, Chile, Perú): horas por crédito, presencialidad y semanas de referencia, editables.
- **Importación** de la guía del curso anterior o de la memoria del título en PDF o Word.
- **Trece apartados**, entre ellos actividades formativas con horas, matriz de alineamiento y compromisos institucionales (ODS, perspectiva de género, uso de IA, atención a la diversidad).
- **Revisión de calidad** con puntuación y botón «Corregir» por aviso.
- **Bibliografía verificada** en OpenAlex y Crossref.
- **Edición directa** del texto, «Rehacer» por apartado, Word completo y proyectos compartibles en JSON.

## Cómo funciona

Siete asistentes, varios en paralelo según sus dependencias: contexto, competencias, resultados de aprendizaje, contenidos y horas, evaluación, metodología y cronograma, y compromisos institucionales. Si uno falla, «Reintentar» continúa sin repetir lo hecho.

La revisión de calidad comprueba, sin IA:

- que los pesos de evaluación sumen 100 % y que ninguno supere el 60 %;
- que cada resultado de aprendizaje y cada competencia específica se evalúen;
- que las horas de bloques y actividades cuadren;
- que el cronograma cubra todas las semanas y exista convocatoria extraordinaria;
- que los resultados usen verbos evaluables.

## Privacidad

La clave se guarda en `localStorage` (`ia_openai_key`) y solo viaja a `api.openai.com`. La verificación bibliográfica envía a OpenAlex y Crossref únicamente el texto de cada referencia. Las guías se guardan en IndexedDB del navegador.

## Cómo citar

Borrás Rocher, F. (2026). *SyllabusAI* (versión 2.0.0) [Software]. Universidad Miguel Hernández de Elche. https://doi.org/10.5281/zenodo.21423173

El DOI anterior es el de concepto: apunta siempre a la última versión. El DOI de cada versión concreta está en [Zenodo](https://doi.org/10.5281/zenodo.21423173). GitHub ofrece la cita en formato APA y BibTeX con el botón *Cite this repository*, a partir de `CITATION.cff`.

Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher · Universidad Miguel Hernández de Elche.
