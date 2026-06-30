# Memoria del Proyecto - Benefits Seguros Grupo Gaman

## Estado Deseado vs Real
- **Deseado**: El botón "COTIZAR MI DRON" debe enviar un `postMessage` con el payload de cotización cuando se abre dentro de la app (entorno embebido en WebView o iframe), pero también abrir la URL en el navegador de manera normal cuando se acceda de manera independiente.
- **Real**: El archivo `code.html` fue renombrado a `index.html`. Se actualizó la lógica en `index.html` de modo que la prevención del comportamiento por defecto (`event.preventDefault()`) solo se ejecute si detectamos que la página está embebida en un iframe, dentro de un WebView de React Native (`window.ReactNativeWebView`), o mediante parámetros clave de la app en la URL (`embed=true`, `webview=true`, `app=true`). También se añadió compatibilidad nativa para enviar el `postMessage` a `ReactNativeWebView`.

## Registro de Procesos
- [x] Modificar `index.html` para agregar `id="btn-cotizar"` al botón "COTIZAR MI DRON".
- [x] Añadir la función JavaScript en `index.html` para enviar el `postMessage` con el payload indicado.
- [x] Implementar detección dinámica de entorno embebido para permitir navegación tradicional en navegadores independientes.
- [x] Asegurar soporte para `window.ReactNativeWebView` al enviar el `postMessage` stringificado si está presente.
