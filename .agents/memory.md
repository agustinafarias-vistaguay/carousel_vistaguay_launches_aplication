# Antigravity Memory Protocol - Memory Log

## Estado Deseado (Desired State)
El objetivo es permitir que la página HTML, la cual corre dentro de un WebView de React Native, pueda comunicarse con la aplicación nativa a través de un puente de mensajería (PostMessage). Específicamente, el botón principal de CTA con el texto "Solicitar ahora" debe iniciar una navegación deep link al presionar.

## Diff Log
- **Estado Inicial:** El botón "Solicitar ahora" era un `<button>` estándar sin comportamiento de deep link o evento onClick asociado. No había puente de comunicación implementado en la página HTML.
- **Estado Actual:** 
  - Se modificó el botón con texto "Solicitar ahora" para incluir el atributo `onclick="handleDeepLink()"`.
  - Se implementó la función global `handleDeepLink()` dentro de una etiqueta `<script>` al final del archivo `code.html` para comprobar `window.ReactNativeWebView` y enviar el payload con formato `JSON.stringify({ type: 'NAVIGATE', screen: 'RequestFlow', params: { id: '123' } })`.

## Registro de Procesos
- [x] Identificar el botón "Solicitar ahora" en `code.html`. (Completado)
- [x] Agregar atributo `onclick="handleDeepLink()"` al botón. (Completado)
- [x] Agregar la función JavaScript `handleDeepLink` para comunicación mediante `postMessage` en `ReactNativeWebView`. (Completado)
- [x] Crear y registrar estado en `/.agents/memory.md`. (Completado)
