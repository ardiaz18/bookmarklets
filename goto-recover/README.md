# Goto Recover

Resuelve las URLs de destino reales detrás de los enlaces `/goto?url=` que Google Search usa para usuarios no logueados.

## Qué hace

- Recorre el DOM de la SERP buscando tokens `/goto` en los `href`
- Recupera la URL real desde el estado inline (`var m={...}`), comentarios HTML y protobufs
- Reescribe los enlaces in situ: `href` pasa a ser la URL real, `ping` se elimina
- Guarda el token original en `data-goto-token` y el nivel de confianza en `data-goto-kind`
- Observa cambios en el DOM para resolver bloques que se cargan dinámicamente

## Niveles de resolución

- **exact**: URL extraída de un protobuf `req`
- **embedded**: URL completa encontrada como string en los datos
- **adjacent**: URL del comentario link-preview adyacente
- **inferred**: URL prestada de otro resultado con mismo host y título
- **derived**: key moments de YouTube (URL padre + `t=`)
- **domain**: solo se conoce el dominio

## Uso

1. Navega a una página de resultados de Google (sin estar logueado)
2. Haz clic en el bookmarklet
3. Los enlaces se reescriben con las URLs reales. Resumen en la consola

## Autor

Desarrollado por [Natzir Turrado](https://github.com/natzir) — [Repo original](https://github.com/natzir/goto-recover).

## Instalación

Crea un nuevo marcador y pega como URL el contenido de `bookmarklet.js`.
