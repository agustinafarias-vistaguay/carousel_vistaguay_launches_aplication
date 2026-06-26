# Antigravity Memory Protocol - Memory Log

## Estado Deseado (Desired State)
El objetivo es permitir que la página HTML, la cual corre dentro de un WebView de React Native, pueda comunicarse con la aplicación nativa a través de un puente de mensajería (PostMessage) con un payload de navegación actualizado (`EditProfileDrones`). Además, se busca limpiar el código HTML duplicado, eliminar los estilos en línea rígidos en favor de las clases de Tailwind CSS y CSS (.glass-card), unificar el modo claro/oscuro en el body con los nuevos colores de fondo definidos por el usuario, corregir la legibilidad de todos los textos en modo oscuro (incluyendo los títulos, pasos y las tarjetas de la sección de versatilidad) con las clases de Tailwind, adaptar las tarjetas glassmorphism en el modo oscuro para una mejor integración visual, eliminar los colores no utilizados en la configuración de Tailwind, y actualizar las copias orientadas a pilotos/experts utilizando la imagen original de la aplicación colocada en la ruta requerida.

## Diff Log
- **Estado Inicial:** 
  - Varios links duplicados en el `<head>`.
  - Atributos style vacíos en la etiqueta `<html>`.
  - Tarjetas con estilos en línea rígidos (`style="..."` con fondos sólidos y sin backdrop filter) sobreescribiendo el efecto glassmorphism.
  - Párrafo duplicado en el Hero.
  - Copias de flujo y CTA orientadas a "solicitar aplicación" (flujo de cliente) en lugar de "Vistaguay Experts" (flujo de pilotos).
  - Deep link apuntando a `NewTaskStepTwo` en lugar de la edición de flota en `EditProfileDrones`.
  - Falta de la imagen local para el Hero (`images/add-drone/t50.jpg`), lo que provocaba que se rompiera visualmente la sección.
  - Configuración extendida de colores en Tailwind con decenas de tokens no utilizados.
  - Textos invisibles o con mal contraste en el modo oscuro al cambiar el fondo del body a `#292B28`.
  - Tarjetas glassmorphism con brillo excesivo sobre el fondo del modo oscuro.
  
- **Estado Actual:** 
  - Se eliminó el `<link>` duplicado para `Material Symbols Outlined` y el atributo `style=""` en `<html>`.
  - Se unificó el fondo dinámico del body: `class="bg-[#F6F9F6] dark:bg-[#292B28]"`, y se eliminó la regla `background-color` rígida en el `<style>`.
  - Se actualizó el token `background` en la configuración de Tailwind a `#F6F9F6`.
  - Se eliminaron todos los colores no utilizados de la configuración extendida de Tailwind, dejando únicamente `background`, `on-surface` y `on-background`.
  - Se removieron por completo todos los atributos `style="..."` de las tarjetas para que funcione el estilo nativo de `.glass-card`.
  - Se agregaron las clases `dark:text-white` en todos los títulos principales (h1 y h2), en los textos descriptivos de los tres pasos del flujo y en los textos de las 4 tarjetas de la sección de Versatilidad.
  - Se cambiaron las clases de contraste en los párrafos de Hero (`dark:text-white/60`) y de la sección de valor (`dark:text-neutral-200`).
  - Se introdujo una regla CSS específica en el bloque `<style>` para `.dark .glass-card` que oscurece el fondo de las tarjetas y reduce el borde en modo oscuro.
  - Se actualizaron los textos de la sección Hero, Versatilidad, Pasos (01, 02, 03) y CTA al final ("Registrar mis drones") enfocados en "Vistaguay Experts".
  - Se copió el archivo de imagen original de la aplicación `images/image_aplication.jpg` a la ruta esperada `images/add-drone/t50.jpg` sin generar imágenes nuevas.
  - Se actualizó la función `handleDeepLink()` para enviar el payload de navegación correcto (`EditProfileDrones`) para registrar drones en la app.

## Registro de Procesos
- [x] Eliminar duplicados y errores sintácticos en `index.html`. (Completado)
- [x] Configurar el `<body>` y Tailwind para soportar dinámicamente fondos claro/oscuro. (Completado)
- [x] Eliminar colores no utilizados en la configuración extendida de Tailwind en `index.html`. (Completado)
- [x] Agregar variantes de contraste para el modo oscuro (`dark:text-white`, `dark:text-white/60`, `dark:text-neutral-200`) a los textos y títulos de `index.html`. (Completado)
- [x] Agregar la clase `dark:text-white` a las etiquetas `<span>` de las 4 tarjetas de Versatilidad en `index.html`. (Completado)
- [x] Agregar regla CSS `.dark .glass-card` en la sección de estilos de `index.html` para el comportamiento de las tarjetas en modo oscuro. (Completado)
- [x] Eliminar atributos `style="..."` de todas las tarjetas para restaurar glassmorphism. (Completado)
- [x] Modificar textos de Hero, sección de Versatilidad, proceso de 3 pasos y CTA final. (Completado)
- [x] Copiar la imagen original de `images/image_aplication.jpg` a la ruta esperada `images/add-drone/t50.jpg`. (Completado)
- [x] Modificar payload en la función `handleDeepLink()` en el script de JS. (Completado)
- [x] Sincronizar memoria del proyecto en `/.agents/memory.md`. (Completado)
