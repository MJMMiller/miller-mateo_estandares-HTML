# Respuesta a la auditoría

- Auditado: Mateo Miller (N.º 15)
- Auditor: Mateo Molina (N.º 16)

## Respuesta a cada hallazgo

| N.º de hallazgo | Decisión | Justificación con la norma | Evidencia antes y después | Commit |
|---|---|---|---|---|
| 1 | `index.html`, línea 149: la ayuda de la fecha decía solo «Fecha de salida» y no indicaba qué fechas se aceptan (del 1/11/2026 al 31/12/2027) | WCAG 3.3.2 (Etiquetas o instrucciones) | [antes](evidencias/extra-01-antes.png), [después](evidencias/extra-01-despues.png) | 091ed08, 817eabf |
| 2 | Acepta | El estándar WHATWG no obliga a que todo campo esté dentro de un `fieldset`, y el campo ya tenía su `label` asociado. Aun así se acepta como mejora: los demás campos están agrupados, y poner «Comentarios» en un `fieldset` con `legend` «Información adicional» mantiene la misma estructura en todo el formulario y le da contexto al lector de pantalla. | [antes](evidencias/resp-02-antes.png), [después](evidencias/resp-02-despues.png) | c4b36a0 |

## Problemas adicionales encontrados por mí

| N.º | Problema | Norma | Evidencia antes y después | Commit |
|---|---|---|---|---|
| 1 | `index.html`, línea 149: la ayuda de la fecha decía solo «Fecha de salida» y no indicaba qué fechas se aceptan (del 1/11/2026 al 31/12/2027) | WCAG 3.3.2 (Etiquetas o instrucciones) | [antes](evidencias/extra-01-antes.png), [después](evidencias/extra-01-despues.png) | 091ed08 |
| 2 | `index.html`, línea 153: la ayuda de la hora decía «Hora d salida» (con error) y no indicaba el horario permitido (cada 30 minutos, de 06:00 a 10:00) | WCAG 3.3.2 (Etiquetas o instrucciones) | [antes](evidencias/extra-02-antes.png), [después](evidencias/extra-02-despues.png) | 21900e9 |