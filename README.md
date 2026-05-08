# Flowii ✦

**Campo de partículas ASCII reactivo al cursor · Standalone · Sin dependencias**
<img width="1883" height="955" alt="{E524BC0B-E621-48C2-89CA-1BE650A75D79}" src="https://github.com/user-attachments/assets/7a694943-f01b-4c39-9c28-9a00a242ff04" />

<img width="1897" height="956" alt="{99EF910D-0D9E-405C-9248-6940D28958C9}" src="https://github.com/user-attachments/assets/d5c614c1-7240-418f-b7b5-96f272a5b11c" />


---

Flowii nació como un recurso visual dentro de otro proyecto personal. Con el tiempo el efecto cobró vida propia y decidí extraerlo, pulirlo y compartirlo como herramienta independiente. Se añadió un editor visual completo con panel de control, drag & drop y exportación integrada — para que cualquiera pueda usarlo o simplemente jugar con él sin tener que tocar una sola variable.

---

## ¿Qué es?

Un **campo de partículas ASCII reactivo al cursor**, renderizado sobre canvas 2D. Cada celda de la cuadrícula tiene estado propio — intensidad, morph, desplazamiento, tono de color — y reacciona en tiempo real a la posición del ratón. Sin WebGL. Sin librerías. Un único archivo HTML.

```
archivo único · ~1400 líneas · vanilla JS · 0 dependencias
```

---

## ✦ Características

**Tipografía**
- 🔤 Charset activo con 7 presets — ASCII, numérico, Katakana, Braille, Griego, bloques, matemáticas
- ✏️ Charset y carácter de reposo completamente editables
- 👁️ Toggle para mostrar u ocultar el carácter de reposo
- 📐 Tamaño de fuente ajustable (recalcula la cuadrícula al vuelo)

**Color**
- 🎨 8 paletas predefinidas — Matrix, Fuego, Hielo, Púrpura, Rosa, Dorado, B/N, Arcoíris
- 🖍️ Color picker para fijar un color concreto (desactiva la rotación automática de hue)
- 🌈 Control de saturación, luminosidad y velocidad de rotación de hue
- 🔆 Gradiente por distancia, mezcla de hue por celda, opacidad máxima

**Física**
- 🧲 Radio de influencia del cursor (hasta 1500px)
- 🔷 Forma del radio configurable — rombo, círculo, cuadrado y todo lo intermedio (métrica Minkowski)
- 💨 Fuerza de repulsión y suavizado de movimiento
- ⏱️ Tiempo de inactividad, persistencia (cola), ganancia de intensidad
- 📈 Perfil de influencia configurable (lineal → borde duro)

**Ruido & Oscilación**
- 〰️ Amplitud X/Y y frecuencia de la oscilación base

**Renderizado**
- 🎞️ Estela (trail) — longitud del rastro visual
- 🔀 Velocidad, umbral y decaimiento del morph entre caracteres
- 🖌️ Color de fondo con color picker (activo solo con fondo sólido)
- 👁️ Toggle fondo sólido / transparente

**Exportación**
- 📦 Descarga HTML standalone con todos los parámetros horneados
- 📄 Descarga JS y CSS por separado
- 🎲 Botón Random — varía charset, forma de radio, física, color y más
- ↺ Reset a valores originales

---

## 🚀 Uso

Abre `flowii.html` en el navegador. No hay servidor, no hay instalación.

Mueve el cursor sobre el canvas y ajusta los parámetros desde el panel lateral. Cuando estés satisfecho, pulsa **Descargar HTML** y tendrás un archivo listo para incrustar en cualquier proyecto.

---

## 📁 Estructura

```
flowii.html   ← todo en un único archivo
```

---

## 🔧 Incrustar en tu proyecto

El iframe funciona, pero tiene una limitación: los eventos de ratón del iframe son independientes del documento padre, por lo que el efecto no reacciona al cursor cuando está sobre contenido externo al iframe.

**La forma correcta** es incrustar el JS directamente en tu página:

```html
<!-- Añade el canvas donde quieras — normalmente como fondo fijo -->
<canvas id="flowii-canvas" style="position:fixed;inset:0;width:100%;height:100%;z-index:0;pointer-events:none;"></canvas>

<!-- Incluye el JS exportado -->
<script src="flowii.js"></script>
```

El atributo `pointer-events:none` hace que el canvas sea puramente decorativo y los clics atraviesen hacia el contenido. Quítalo si quieres que el efecto sea interactivo en primer plano.

> El CSS exportado solo contiene estilos de `body` y `canvas`. Si tu proyecto ya los define, no hace falta incluirlo.

---
---

# Flowii ✦

**Cursor-reactive ASCII particle field · Standalone · Zero dependencies**

---

Flowii started as a visual resource inside a personal project. Over time the effect took on a life of its own, so I extracted it, refined it, and released it as a standalone tool. A full visual editor with drag & drop panel and built-in export was added — so anyone can use it or just play with it without having to touch a single variable.

---

## What is it?

A **cursor-reactive ASCII particle field**, rendered on a 2D canvas. Each cell in the grid has its own state — intensity, morph, displacement, color hue — and reacts in real time to the mouse position. No WebGL. No libraries. A single HTML file.

```
single file · ~1400 lines · vanilla JS · 0 dependencies
```

---

## ✦ Features

**Typography**
- 🔤 Active charset with 7 presets — ASCII, numeric, Katakana, Braille, Greek, block, math
- ✏️ Fully editable active and rest characters
- 👁️ Toggle to show or hide the rest character
- 📐 Adjustable font size (recalculates the grid on the fly)

**Color**
- 🎨 8 preset palettes — Matrix, Fire, Ice, Purple, Pink, Gold, B&W, Rainbow
- 🖍️ Color picker to lock a specific color (disables automatic hue rotation)
- 🌈 Saturation, lightness, and hue rotation speed controls
- 🔆 Distance gradient, per-cell hue blend, max opacity

**Physics**
- 🧲 Cursor influence radius (up to 1500px)
- 🔷 Configurable radius shape — diamond, circle, square and everything in between (Minkowski metric)
- 💨 Repulsion strength and movement smoothing
- ⏱️ Idle time, persistence (trail decay), intensity gain
- 📈 Configurable influence profile (linear → hard edge)

**Noise & Oscillation**
- 〰️ X/Y amplitude and frequency of the base oscillation

**Rendering**
- 🎞️ Trail — visual trace length
- 🔀 Morph speed, threshold, and decay between characters
- 🖌️ Background color picker (active only with solid background)
- 👁️ Solid / transparent background toggle

**Export**
- 📦 Download standalone HTML with all parameters baked in
- 📄 Download JS and CSS separately
- 🎲 Random button — varies charset, radius shape, physics, color and more
- ↺ Reset to original values

---

## 🚀 Usage

Open `flowii.html` in a browser. No server, no install.

Move the cursor over the canvas and adjust parameters from the side panel. When you're happy with the result, hit **Download HTML** and you'll have a file ready to embed in any project.

---

## 📁 Structure

```
flowii.html   ← everything in a single file
```

---

## 🔧 Embed in your project

Using an iframe works but has a key limitation: mouse events inside the iframe are isolated from the parent document, so the effect won't react to the cursor when it hovers over content outside the iframe.

**The correct approach** is to embed the JS directly in your page:

```html
<!-- Add the canvas wherever you need it — typically as a fixed background -->
<canvas id="flowii-canvas" style="position:fixed;inset:0;width:100%;height:100%;z-index:0;pointer-events:none;"></canvas>

<!-- Include the exported JS -->
<script src="flowii.js"></script>
```

The `pointer-events:none` attribute makes the canvas purely decorative so clicks pass through to the content below. Remove it if you want the effect to be interactive in the foreground.

> The exported CSS only contains `body` and `canvas` styles. If your project already defines those, you don't need to include it.

---

*Made with cursor and monospace font.*
