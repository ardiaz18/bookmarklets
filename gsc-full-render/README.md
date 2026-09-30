# GSC Full Render

Reconstruye la página completa desde el HTML renderizado por Google en la herramienta URL Inspection de Search Console.

## Qué hace

- Toma el HTML que Google renderizó y lo muestra completo en la pestaña Screenshot (que normalmente corta a ~1750px)
- Lista todos los enlaces de la página con filtros: destino, rel, crawlable, visibilidad, tipo de URL
- Marca los recursos que Google no pudo cargar (bloqueados por robots.txt, errores HTTP)
- Señala imágenes lazy que nunca se cargaron
- Exporta los enlaces a CSV

## Uso

1. En Search Console → URL Inspection, abre *View tested page* o *View crawled page*
2. Haz clic en el bookmarklet
3. La pestaña Screenshot muestra la página completa. Clic de nuevo para desactivar

## Autor

Desarrollado por [Natzir Turrado](https://github.com/natzir) — [Repo original](https://github.com/natzir/gsc-full-render).

## Instalación

Crea un nuevo marcador y pega como URL el contenido de `bookmarklet.js`.
