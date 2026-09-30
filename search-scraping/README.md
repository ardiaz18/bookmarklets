# Search Scraping

Extrae los resultados de la primera página de la SERP de Google en una tabla, con detección de AI Overview.

## Qué muestra

- Posición, título, URL y dominio de cada resultado orgánico (hasta 30)
- Indica si la URL aparece también en el AI Overview de Google
- Total de resultados y URLs detectadas en AIO

## Funciones

- **Copy TSV**: copia la tabla al portapapeles en formato TSV (pegable en Sheets/Excel)
- Normalización de URLs (elimina trailing slashes, fragmentos, resuelve redirecciones de Google)
- Filtra enlaces internos de Google y elementos no visibles

## Uso

1. Haz una búsqueda en Google
2. Haz clic en el bookmarklet
3. Se muestra un overlay con la tabla de resultados

## Nota

El DOM de Google cambia frecuentemente, así que este bookmarklet puede necesitar actualizaciones periódicas.

## Instalación

Crea un nuevo marcador y pega como URL el contenido de `bookmarklet.js`.
