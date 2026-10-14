# Soulsical — sistema de diseño en Divi (versión clara, 2026-10-01)

Generado a partir de `design-system-soulsical-light.md` ("The Luminous Stage"). Sustituye a la primera versión
oscura (`design-system-soulsical.md`, descartada): se reutilizaron los mismos ids, renombrando donde hacía falta.
Lo marcado con *propuesto* no venía en el documento. Política de diseño: estricta (`{"mode":"tokens"}`).
Muestra: página borrador 22 "Sistema de diseño (muestra)".

## Fuentes (Personalizador)
- Encabezado → Anton (`$Encabezado`) · Texto Principal → Poppins (`$Texto Principal`)

## Colores
| Nombre | Valor | Origen |
|---|---|---|
| Color Primario (personalizador) | #794fc9 | doc: Spotlight Purple |
| Color Secundario (personalizador) | #907f9c | doc: Ash Lavender |
| Color del Texto de Encabezados | #1e1b24 | doc: Balanced Charcoal |
| Color del Texto Principal | #525252 | doc (text-neutral-600 del texto) |
| Color Del Enlace | #794fc9 | doc |
| primary-hover | #683eb8 | doc: hover del botón |
| lilac | #c2adcd | doc: Soft Lilac (píldoras, badges) |
| text-muted | #737373 | doc: Neutral Muted Gray |
| surface | #ffffff | doc |
| surface-low | #f8f7fa | doc: Gallery Off-White |
| surface-container | #f5f3f6 | doc (footer, inputs) |
| surface-high | #efecf2 | *propuesto* |
| border | #e9e5ee | doc: Soft Border |
| outline | #d6cfdd | *propuesto* (bordes de campos algo más visibles) |
| surface-inverse | #1e1b24 | *propuesto* (banda oscura ocasional) |
| on-primary | #ffffff | doc |
| error | #ffb4ab → #ba1a1a | *propuesto* (error legible sobre blanco) |
| shadow | #1e1b24 | *propuesto*; las sombras del doc usan `$gcid-primary-color/8` |

## Escala (390 → 1440 px)
| Variable | Valor |
|---|---|
| text-hero | 64 → 160 (*propuesto*: marca de agua del footer) |
| text-display | 48 → 96 (doc text-5xl → 8xl) |
| text-stat | 36 → 60 (doc 4xl → 6xl) |
| text-h2 | 30 → 48 (doc 3xl → 5xl) |
| text-h3 / h4 | 24 → 28 / 20 → 22 (*propuesto*) |
| text-lead | 18 → 20 (doc) |
| text-body | 14 → 16 (doc) |
| text-button | 12 → 14 (doc) |
| text-small / text-label | 14 / 12 |
| space-section | 80 → 128 (doc py-20 → py-32) |
| space-gutter / xl / l | 20→64 / 56→96 / 40→64 |
| space-m / s / xs / 2xs | 32 / 24 / 16 / 8 |
| radius-s / m / l / full | 4 / 6 (rounded-md) / 12 (tarjetas) / 999 |

## Presets
- heading: `display` (h1, 0.9), `h2` (0.95), `h2-accent` (primario), `h3`, `h4`, `stat` (primario), `hero`,
  `watermark` (text-hero, primario al 10 %). Anton, mayúsculas.
- text: `body` (1.625), `lead`, `small` (text-muted), `label` (600, 0.1em, primario), `label-muted` (secundario).
- button: `primary-sm` y `secondary-sm` (12 px, padding 8/24: cabecera y sitios compactos). `primary` (Poppins 600 mayúsculas, primario → primary-dark, sombra violeta en hover), `secondary`
  (contorno primario, fondo primario/5 en hover), `link`. Radio radius-m, sin icono. Padding space-xs space-s
  (16/24; el doc dice 10/24, no hay token de 10).
- group: `card` (blanco, radius-l, sombra violeta 8 %, sube 6 px en hover), `glass` (blanco 85 %, blur 12 px),
  `layout` (neutro, para grupos estructurales).
- section: `surface`, `surface-low`, `surface-container` (footer), `spotlight` (radial primario 10 % → blanco),
  `inverse` (charcoal). Todas con padding vertical space-section.

## Reglas
- Sin bordes sólidos para separar secciones: cambios de tono (`surface` ↔ `surface-low`).
- Tarjetas blancas sobre `surface-low`; texto largo alineado a la izquierda; composición asimétrica.

## Variante oscura del hero ("The Velvet Stage", para páginas puntuales)
Colores: `surface-dark` #131313, `primary-deep` #250059, `primary-light` #d3bbff, `on-dark` #e5e2e1,
`on-dark-muted` #cbc4d2. Presets: section `spotlight-dark` (radial primary-deep → surface-dark 70 %),
heading `display-dark`, text `lead-dark`, `small-dark`, `label-dark`, button `primary-dark` (Anton, primario →
primary-light con brillo) y `secondary-dark` (fantasma claro), group `glass-dark`. Ejemplo en la página 22,
segunda sección ("Portada oscura").

- image: `photo` (radius-l). Todas las fotos de contenido.

## Iconos
Phosphor Light, 47 iconos en `icons/` (ver `icons/README.md`). Módulo SVG + presets `icon`, `icon-sm`, `icon-lg`,
`icon-muted`, `icon-dark`, `icon-badge`; variables `icon-s` 20, `icon-m` 28, `icon-l` 40→48. Sin iconos de fuente.

## Theme Builder
Plantilla 42 (activa, por defecto). Cabecera (layout 41): section `header` (sticky) con dos filas:
- "Fila escritorio" (oculta en tablet y móvil): logo, menú `nav` (ubicación Primary Menu), botones `primary-sm` / `secondary-sm`.
- "Fila móvil y tablet" (oculta en escritorio, ≤980 px): logo + módulo de código "Menú móvil" = hamburguesa (Phosphor list/x)
  y panel a todo el ancho bajo la cabecera (slide down/up, separadores primario al 10 %, Anton text-h4). Fuente:
  `mobile-menu.html` (HTML+CSS+JS, solo `var(--gcid-*)`/`var(--gvid-*)`). **Una sola fuente**: el panel se rellena
  con la cabecera de escritorio: enlaces del menú de WordPress (Apariencia → Menús, con un nivel de submenú) + los
  botones de la cabecera; el primer botón (Comprar entradas) va al final como botón destacado, el resto (Contacto)
  como opciones. No hay que tocar el módulo para cambiar el menú. Pie (layout 51): section `footer`, textos `legal-dark`, iconos
`icon-social-dark`; enlaces legales a /aviso-legal/, /politica-de-privacidad/, /politica-de-cookies/.
