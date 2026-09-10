# Página en construcción

Sitio estático, sin dependencias ni build. Se abre con doble click en `index.html`
o se sirve con cualquier server estático (`python3 -m http.server`).

## Archivos

- `index.html` — contenido de la página.
- `styles.css` — fondo cuadriculado, tipografías, layout, estilo de los bordes.
- `edges.js` — física de los bordes ASCII (repelencia, curva, disparo, arrastre con jitter).

## Pendientes

**Título (PNG).** Guardá la imagen en `assets/titulo.png`, borrá el
`<header class="title-slot"></header>` de `index.html` y descomentá la línea del
`<img class="title-image">` que está justo arriba.

**Tipografía Exposure Trial.** Poné los archivos en `fonts/` con estos nombres:

```
fonts/ExposureTrial-Regular.woff2   (o .otf)
fonts/ExposureTrial-Italic.woff2    (o .otf)
```

Se usa en títulos, subtítulos (`.subtitle`, en itálica), botones (`.button`),
los términos AGI/ASI y el footer. Mientras los archivos no estén, cae a un serif
del sistema sin romper nada. El cuerpo de texto es Helvetica; los dígitos de los
bordes, Inter con cifras tabulares.

## Ajustes de los bordes

Los parámetros de la física están arriba de todo en `edges.js`: alcance de la
repelencia, fuerza del disparo, velocidad de retorno, jitter.
