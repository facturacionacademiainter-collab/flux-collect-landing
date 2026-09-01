# Flux Collect — web de presentación

Landing de una sola página de **Flux Collect**, la plataforma de inteligencia
de cobranzas de Moovi Solutions.

Sin build, sin dependencias, sin framework: un único archivo HTML con su CSS y
su JS adentro. Se abre con doble clic y anda.

## Los archivos

| Archivo | Qué es |
|---|---|
| `index.html` | **La página.** Es lo que sirve GitHub Pages. Autocontenido. |
| `collectiq-landing.html` | El mismo contenido sin el envoltorio `<html>/<head>/<body>`, para publicarlo como Artifact. Se mantiene por el nombre viejo del producto porque la URL publicada depende de esa ruta. |

`index.html` se genera a partir de `collectiq-landing.html`: se le antepone el
doctype y los meta, y se parte en `</style>` para separar el `<head>` del
`<body>`. Si tocás uno, regenerá el otro.

## Lo único que viene de afuera

Tres familias tipográficas de Google Fonts — **Archivo** (títulos), **Barlow
Semi Condensed** (el wordmark de la marca) e **IBM Plex Sans/Mono** (cuerpo y
etiquetas). Todo lo demás —el logo, los gráficos, los mockups de producto, el
campo de partículas del hero— es SVG y Canvas escritos a mano. No hay una sola
imagen de mapa de bits.

## Diseño

- **Fondo:** blanco perlado `#F6F5F1`. Los paneles son blanco puro y sus
  superficies internas se hunden, no se levantan: es la regla que cambia de
  signo cuando el fondo pasa de oscuro a claro.
- **Acento:** `#EB5F22`, el naranja exacto del logo. Uno solo en toda la página.
- **Tinta:** `#1D1D1B`, el negro del logo.
- **Temas:** claro y oscuro, resueltos a nivel de tokens. Respeta la
  preferencia del sistema y el `data-theme` explícito.
- **Accesibilidad:** foco visible en todo lo navegable por teclado, y el campo
  de partículas se congela con `prefers-reduced-motion`.

## Ver la página localmente

Abrí `index.html` en el navegador. No hace falta servidor.

## Datos

Los números de la página (carteras, montos, probabilidades, nombres de
clientes) son **de demostración**, y así está aclarado en el pie.
