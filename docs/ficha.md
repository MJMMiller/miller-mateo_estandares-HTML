# Ficha personalizada

| N.º de lista | Temática | Campos especiales del formulario | Breakpoint principal | Restricción especial |
|---|---|---|---|---|
| 15 | Agencia turística | Fecha y hora de reserva | 768 px | Tipografía fluida con clamp(), sin media queries para tamaños de texto |

## Dónde se cumple cada punto

- **Temática:** agencia turística «Andes Tours» (Cuenca, Ecuador).
- **Fecha y hora de reserva:** `index.html`, fieldset «Fecha y hora de reserva»: `input type="date"` con min/max e `input type="time"` con min/max/step.
- **Breakpoint 768 px:** `css/estilos.css`, `@media (min-width: 768px)` cambia el grid de una a dos columnas.
- **clamp():** todos los `font-size` de `css/estilos.css` usan `clamp()`. No hay ningún `font-size` dentro del `@media`.