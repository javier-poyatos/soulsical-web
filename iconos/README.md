# Iconos Soulsical — Phosphor Light

Fuente: Phosphor Icons 2.1.1 (`@phosphor-icons/core`, peso *light*, licencia MIT en `LICENSE-phosphor`).
Todos con `viewBox="0 0 256 256"` y `fill="currentColor"`: el color lo pone el preset del módulo SVG.

## Uso en Divi
- Módulo **SVG** con el código del icono pegado (sin subirlo a medios) y uno de estos presets:
  `icon` (28 px, primario), `icon-sm` (20 px, para listas), `icon-lg` (40→48 px), `icon-muted` (secundario),
  `icon-dark` (primary-light, sobre el hero oscuro), `icon-badge` (círculo primario/10 de 60 px).
- Tamaños: variables `icon-s`, `icon-m`, `icon-l`.
- **Regla**: nada de iconos de fuente (Elegant Themes / Font Awesome). Listas con icono = grupo en fila
  (`icon-sm` + texto `body`); botones sin icono; la flecha del acordeón queda en un color del sistema.
- Para reutilizar en el Visual Builder: copiar el módulo desde la sección «Iconos» de la página 22
  (Sistema de diseño) y pegarlo donde haga falta.
- Iconos nuevos: solo de Phosphor *light* (`package/assets/light/<nombre>-light.svg`), añadidos aquí.

## Biblioteca (47)
- Interfaz: arrow-right, arrow-up-right, caret-down, caret-right, plus, minus, x, check, list, magnifying-glass,
  download, link
- Eventos: calendar-blank, calendar-check, clock, map-pin, ticket, buildings, church, confetti, heart,
  handshake, gift
- Música y escena: microphone-stage, microphone, music-notes, music-note, playlist, play-circle, mask-happy,
  sparkle, star
- Personas y formación: users-three, graduation-cap, chat-circle-text, quotes
- Contacto y redes: envelope-simple, phone, whatsapp-logo, instagram-logo, youtube-logo, spotify-logo,
  tiktok-logo, facebook-logo
- Estados: check-circle, info, warning-circle

## Botones con icono a la izquierda
Preset de botón `icon-left`, apilado sobre el de estilo: `["primary", "icon-left"]` (vale con secondary, link,
primary-dark, secondary-dark). Dibuja el icono en el `:before` del botón como máscara CSS pintada con el color
del texto (cambia con el hover). Cada botón dice qué icono usa con una línea en su CSS personalizado
(Free-form): las tienes listas en `button-css.md`.
