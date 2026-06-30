# Memoria del Proyecto - Benefits Seguros Grupo Gaman

## Estado Deseado vs Real
- **Deseado**: Agregar un evento `postMessage` al botón "COTIZAR MI DRON" en `code.html` con un payload específico para integrarlo con una app contenedora (WebView).
- **Real**: Se agregaron el atributo `id="btn-cotizar"` al botón y el script correspondiente en la sección `<script>` que previene el comportamiento por defecto y envía el `postMessage` tanto a `window.parent` como al propio `window`.

## Registro de Procesos
- [x] Modificar `code.html` para agregar `id="btn-cotizar"` al botón "COTIZAR MI DRON".
- [x] Añadir la función JavaScript en `code.html` para enviar el `postMessage` con el payload indicado y prevenir el comportamiento predeterminado.
- [x] Verificar que no existan errores de sintaxis en `code.html`.
