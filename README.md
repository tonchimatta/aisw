# Página en construcción

Sitio estático, sin dependencias ni build. Se abre con doble click en `index.html`
o se sirve con cualquier server estático (`python3 -m http.server`).

## Archivos

- `index.html` — contenido de la página.
- `styles.css` — fondo cuadriculado, tipografías, layout, estilo de los bordes y las carpetas.
- `edges.js` — física de los bordes ASCII (repelencia, curva, disparo, arrastre con jitter, 4 columnas por lado).
- `folders.js` — reordenar las carpetas del cajón arrastrándolas con el dedo o el mouse.

## Pendientes

**Tipografía Exposure Trial.** Ya están en `fonts/ExposureTrial-Regular.otf` y
`fonts/ExposureTrial-Italic.otf`. Se usa en el título, subtítulos (`.subtitle`, en
itálica), botones (`.button`), los términos AGI/ASI, las tabs de las carpetas y el
footer. El cuerpo de texto y los dígitos de los bordes usan Inter (cargada desde
Google Fonts).

**Animación de abrir carpeta.** Cada tab del cajón (`.folder-tab`) ya tiene un
`data-question` identificándola. Falta engancharle el click para la animación de
"sacarla de la caja y abrirla" con el contenido de la respuesta.

## Ajustes de los bordes

Los parámetros de la física están arriba de todo en `edges.js`: cantidad de
columnas (`COLS`), alcance de la repelencia, fuerza del disparo, velocidad de
retorno, jitter.

## Ajustes del cajón de carpetas

Los colores de cada tab se definen inline en `index.html` con `--tab-color` y
`--tab-ink` (color de fondo y de texto). La paleta actual cicla entre 4 tonos:
`#6F7D4E`, `#F3EFE6`, `#2E3F7F`, `#B05038`.
