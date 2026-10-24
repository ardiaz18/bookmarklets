# ChatGPT Fan-out

Muestra las búsquedas que ChatGPT lanza de verdad cuando usa la búsqueda web (el *query fan-out*) y las fuentes que usa para responder, sin abrir DevTools.

## Qué muestra

Por cada pregunta de la conversación:

- **Fan-out**: las consultas reales del campo `search_model_queries`
- **Fuentes citadas**: lo que aparece enlazado en la respuesta (componentes `Cite`, `Link` y fichas de negocio `Entity` con web)
- **Fuentes consultadas**: resultados de búsqueda leídos pero no citados (`search_result_groups`)

Las fuentes se agrupan por dominio. Se eliminan los parámetros `utm_` y las imágenes de `images.openai.com`.

## Funciones

- **CSV**: descarga búsquedas y fuentes (separador `;`, listo para Excel en español)
- **JSON**: copia el resultado al portapapeles
- **Diagnóstico**: lista las peticiones capturadas y permite copiar el JSON crudo

## Uso

1. Abre chatgpt.com y recarga la página
2. Haz clic en el bookmarklet **antes** de preguntar: se activa la captura en directo
3. Haz la pregunta; el panel se rellena mientras ChatGPT responde

Con sesión iniciada también lee conversaciones ya existentes (`/c/…`). Sin sesión (incógnito) solo funciona la captura en directo.

## Nota

Lee las respuestas de las peticiones `conversation` de la propia web de ChatGPT. Si OpenAI cambia el formato del JSON, puede necesitar ajustes.

## Instalación

Crea un nuevo marcador y pega como URL el contenido de `bookmarklet.js`.
