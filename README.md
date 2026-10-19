# SyllabusAI

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21423173.svg)](https://doi.org/10.5281/zenodo.21423173)

**Aplicación:** https://fborrasumh.github.io/sillabusAI/ · **Idiomas de la interfaz:** español (por defecto), inglés y portugués de Brasil (`?lang=en`, `?lang=pt`).

Genera la **guía docente** de una asignatura universitaria con el documento, el vocabulario y las normas del país: guía docente (España), ficha da unidade curricular (Portugal), programa de asignatura (México, Argentina, Chile), syllabus (Colombia), sílabo (Perú) o plano de ensino (Brasil). El **modo genérico** sirve para cualquier país o institución y no cita ninguna normativa. Es un único fichero (`index.html`) sin servidor; funciona con la clave de OpenAI, Google Gemini o Anthropic Claude de cada persona.

## Novedades de la versión 3.0.1

- **Descarga en Word arreglada.** El documento .docx se genera ahora en el propio navegador, sin cargar librerías externas: ya no aparece «No se pudo cargar una librería: ¿hay conexión?» y funciona sin conexión, con bloqueadores de contenido y en redes institucionales con proxy.
- La lectura de PDF y Word subidos prueba un servidor alternativo (jsDelivr) si cdnjs no responde, y el mensaje de error explica qué hacer.

## Novedades de la versión 3.0

- **Selector de país o modo genérico.** El país cambia el nombre del documento, sus apartados, la terminología, el sistema de créditos (ECTS, SATCA, RTF, crédito de 48 h, SCT-Chile, crédito peruano o carga horaria en horas), la escala de calificación, el mecanismo de recuperación y la exigencia de asistencia. Todos los valores son editables.
- **Documento oficial de cada país:** memoria verificada, ficha acreditada por la A3ES, PPC y DCN, plan con RVOE, documento maestro, plan de estudios…
- **Ementa, sumilla o contenidos mínimos** (Brasil, Perú, Argentina): se reproducen literalmente y el código avisa de los temas oficiales que no aparecen en el temario.
- **Idioma de la guía independiente del de la interfaz:** español de España, español neutro, portugués de Brasil o de Portugal, inglés, catalán, valenciano, gallego y euskera.
- **Tres proveedores de IA** con desplegable de los modelos de cada clave.
- **Interfaz en tres idiomas** y tres guías de ejemplo que se abren sin clave (España, Brasil y modo genérico).
- **Migración automática** de las guías, el formulario y la clave de la versión 2.

## Cómo funciona

Siete asistentes (contexto, competencias, resultados de aprendizaje, contenidos y horas, evaluación, metodología y cronograma, compromisos institucionales) trabajan en paralelo según sus dependencias. Cada uno recibe la ficha de la asignatura con el contexto normativo del país elegido. Si uno falla, «Reintentar» continúa sin repetir lo hecho.

## Qué comprueba el código (sin IA)

- Que los pesos de evaluación sumen 100 % y ninguno supere el máximo fijado.
- Que cada resultado de aprendizaje se trabaje en algún bloque y se evalúe en algún instrumento (matriz de alineamiento), y que se evalúe cada competencia específica.
- Que las horas de bloques y actividades cuadren con los créditos o la carga horaria.
- Que los códigos de competencia existan en el documento oficial pegado; si la IA reformula el texto de un código oficial, **el código restaura el texto literal**.
- Que el temario cubra la ementa, sumilla o contenidos mínimos oficiales.
- Que se describan la recuperación y, donde el país lo exige, la asistencia.
- Que el cronograma cubra las semanas lectivas y que los resultados usen verbos evaluables (en el idioma de la guía).
- Los mínimos habituales de bibliografía (Brasil) y la existencia de cada referencia en OpenAlex y Crossref.

## Privacidad

Las guías y la clave se guardan solo en el navegador (IndexedDB y `localStorage`). Al proveedor de IA viajan los datos de la asignatura y el documento oficial, con correos y teléfonos enmascarados y tras un aviso previo con muestra; **el profesorado nunca se envía**. A OpenAlex y Crossref viaja solo el texto de cada referencia.

## Límites

- Los valores normativos de cada país (escalas, horas por crédito, asistencia, recuperación) son los habituales y varían entre instituciones: revísalos con el reglamento propio.
- Las etiquetas del documento en catalán, gallego y euskera deben revisarlas hablantes nativos.
- La revisión automática no sustituye la del profesorado ni la de la comisión. El texto lo genera un modelo de lenguaje.

## Cómo citar

Borrás Rocher, F. (2026). *SyllabusAI* (versión 3.0.1) [Software]. Universidad Miguel Hernández de Elche. https://doi.org/10.5281/zenodo.21423173

El DOI es el de concepto y apunta siempre a la última versión. Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher · Universidad Miguel Hernández de Elche.
