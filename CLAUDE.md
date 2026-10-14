# Soulsical Choir (web)

Web del coro Soulsical (soulsicalchoir.com) con Divi 5 y el plugin divi-5-designer (`~/proyectos/divi-5-designer`,
repo aparte: mejoras y fallos del plugin → su `docs/backlog.md`). El usuario escribe en español.

## Sitio
- https://soulsicalchoir.com (con "l"): se trabaja directamente sobre el dominio final, usado como staging.
  Hosting externo (185.14.57.109, LiteSpeed): **sin SSH ni wp-cli**, todo por MCP (`divi5_soulsical`).
  Divi 5.14, tema hijo "Soulsical". Páginas grandes: `D5D_ENV=.env.soulsical ~/proyectos/divi-5-designer/dev/mcp.sh <ability> '<json>'`.
- update-page no toca páginas publicadas: el usuario las pasa a borrador o se usa `live: true` solo si lo pide.
- Antes del lanzamiento: quitar WP_ENVIRONMENT_TYPE/D5D_ALLOWED_HOSTS, los plugins divi-5-designer y MCP Adapter,
  la contraseña de aplicación y la capacidad extra de d5d-mcp, y el noindex.

## Sistema de diseño
- Claro "Luminous Stage". Resumen de todos los tokens y presets: `diseno/design-system-divi.md` (mantenerlo al día).
  Política de diseño ESTRICTA (`{"mode":"tokens"}`): solo presets y variables existentes; auditorías a 0 literales.
- Fuentes por Customizer: `$Encabezado` (Anton), `$Texto Principal` (Poppins).
- Iconos: Phosphor Light en `iconos/` (SVG, nunca fuentes de iconos; listas de iconos = grupos en fila).
  Botón con icono = presets `[estilo, "icon-left"]` + freeForm `--btn-icon` (ver `iconos/button-css.md`).

## Estructura en WordPress
- Theme Builder: plantilla 42; cabecera 41 (fila escritorio + fila móvil con el menú de `snippets/mobile-menu.html`,
  que construye el panel a partir del menú de escritorio); pie 51.
- Páginas: 68 Inicio (portada), 107 Soulsical, 111 Muestras, 113 Contacto (Fluent Forms id 1),
  126/127/128 legales (borradores con [MARCADORES]), 22 muestra del sistema de diseño.

## Trabajo
- `snapshots/`: salidas de get-page antes y después de cada ronda; el usuario edita a mano en Divi, así que
  antes de tocar una página, get-page y comparar con el último snapshot.
- Capturas: `~/proyectos/divi-5-designer/dev/screenshot.sh <url> <out.png> 1440 <alto> 900` con
  `SHOT_CSS='.et_pb_section_0{height:903px}.et_pb_image{opacity:1;transform:none}'` (el 100vh de Divi está en CSS externo).

## Skills
`.claude/skills` es un enlace (fuera de git) a las skills del plugin: `ln -sfn ~/proyectos/divi-5-designer/.claude/skills .claude/skills`.
