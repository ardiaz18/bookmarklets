# Extract Schema

Extrae y lista todos los tipos de Schema Markup (JSON-LD) presentes en la página actual.

## Qué hace

- Busca todos los bloques `<script type="application/ld+json">` del DOM
- Recorre recursivamente el JSON para extraer cada `@type`
- Muestra los tipos encontrados en un overlay sobre la página

## Uso

1. Navega a cualquier URL
2. Haz clic en el bookmarklet
3. Aparece un panel con la lista de `@type` detectados

## Instalación

Crea un nuevo marcador y pega como URL el contenido de `bookmarklet.js`.
