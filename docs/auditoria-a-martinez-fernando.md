# Auditoría a Fernando Martínez

- Auditor: Mateo Miller (N.º 15)
- Auditado: Fernando Martínez (N.º 14)
- Repositorio: https://github.com/MHFERNANDO/Martinez-Fernando-TiendaArtesanias
- Fecha: 25/10/2026

## Ficha del compañero

| N.º | Temática | Campo especial | Breakpoint | Restricción |
|---|---|---|---|---|
| 14 | Tienda de artesanías | Rango numérico (range) | 768 px | Estados del formulario solo con :valid, :invalid y :has() |

## Qué esperaba encontrar

| Requisito | Qué esperaba | ¿Cumple? |
|---|---|---|
| Base 1: estructura | header, nav, main, section, aside, footer y títulos en orden | Sí |
| Base 2: formulario | 5 campos con label, fieldset y validación | Sí |
| Base 3: tabla | caption, thead, tbody y scope | Sí |
| Base 4: responsive | Grid, Flexbox y que se vea bien en 360 px | No (hallazgos 1 y 2) |
| Base 5: colores | Todos los colores como variables --color-... | No (hallazgo 4) |
| Base 6: teclado | Todo se puede usar con Tab | Sí |
| Base 7: validadores | 0 errores | No (hallazgos 3 y 6) |
| Base 8: imágenes | Todas con alt | No (hallazgo 3) |
| Ficha: range | Rango con min, max y label | Sí |
| Ficha: 768 px | El diseño cambia en 768 px | Solo en computadora (hallazgo 1) |
| Ficha: estados | Solo :valid, :invalid y :has() | No (hallazgo 5) |
| ficha.md | Archivo docs/ficha.md | Sí |

## Hallazgos

| N.º | Requisito | Ubicación | Hallazgo | Norma | Evidencia | Severidad |
|---|---|---|---|---|---|---|
| 1 | Base 4: responsive | index.html, línea 6 | El meta viewport está comentado, por eso en el celular la página se ve pequeña, como en computadora | WCAG 1.4.10 | [celular](evidencias/fer-01-celular.png), [código](evidencias/fer-01b-codigo.png) | Alta |
| 2 | Base 4: responsive | index.html, línea 92 (iframe de 600 px) | Con un ancho real de 360 px (DevTools en modo Desktop) el mapa es más ancho que la pantalla y parte del contenido se corta | WCAG 1.4.10 | [captura](evidencias/fer-02-360px.png) | Alta |
| 3 | Base 8: imágenes | index.html, línea 25 | La imagen principal no tiene alt; el validador marca error | WCAG 1.1.1 | [código](evidencias/fer-03-codigo.png), [validador](evidencias/fer-03-validador.png) | Alta |
| 4 | Base 5: colores | estilos.css, líneas 140, 188 y 222 | Hay colores escritos directo (#ddd, #555, #ccc) y no como variables | Requisito base 5 | [colores 1](evidencias/fer-04a.png), [colores 2](evidencias/fer-04b.png), [colores 3](evidencias/fer-04c.png) | Media |
| 5 | Ficha: estados del formulario | estilos.css, líneas 251 a 268 | Usa `:user-valid` y `:user-invalid`, pero la ficha pide `:valid` e `:invalid` | Ficha N.º 14 | [captura](evidencias/fer-05-css.png) | Alta |
| 6 | Base 7: validador HTML | index.html, `<head>` (líneas 5 a 9) | Falta `<meta charset="utf-8">`; el validador marca error y lee la página como windows-1252 | WHATWG HTML (declaración de codificación) | [validador](evidencias/fer-03-validador.png) | Media |