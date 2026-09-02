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
| `flux-collect-icono.svg` | El isotipo suelto, el mismo dibujo que la marca incrustada en `index.html`. La página no lo carga (lleva el suyo como data URI para andar con doble clic); está para reusarlo afuera. |
| `flux-collect-logo.ai` | El original editable de la marca, en Illustrator. Documento CMYK, perfil Coated FOGRA39: el bloque va en C50 M62 Y0 K0, el equivalente de imprenta del `#8C68B1` de la página. |

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
- **Acento:** `#8C68B1`, el violeta exacto del logo (C50 M62 Y0 K0 en el `.ai`).
  Uno solo en toda la página. En oscuro aclara a `#B890DF`, porque un violeta
  medio sobre fondo negro se apaga. `--flare-deep` es la variante que sí tiene
  contraste como texto: `#5B3A80` en claro, `#D4BAEE` en oscuro.
- **Texto sobre el acento:** `--on-flare`. Es el único token que cambia de
  extremo entre temas —blanco en claro, `#1B0F2A` en oscuro— porque el acento
  cruza el punto medio de luminancia al cambiar de tema y el contraste se da
  vuelta con él.
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
