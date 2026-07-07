# ⚽ Alineación Mundialista — Chipax

Rompehielos interactivo para las reuniones de equipo de Chipax, con temática Mundial de Fútbol. Se sortea a un chipaxiano, elige una pelota que revela una posición de cancha (Arquero, Defensor, Mediocampista, Delantero o Entrenador), y esa persona nombra a un colega de cualquier equipo de Chipax que cumpla ese rol. La cancha se va llenando con foto + nombre hasta completar la alineación, y al terminar se abre una celebración a pantalla completa con video de fondo.

**Demo en vivo:** https://dalmadiaza.github.io/Rueda-mundialista/

---

## 🎮 Cómo se juega

1. Click en **"¡Sortear chipaxiano!"** → el slot elige a alguien al azar.
2. Esa persona elige una de las 5 pelotas → se revela la posición.
3. El facilitador escribe el nombre que la persona sorteada elige para ese rol y presiona **"Agregar a la cancha"**.
4. Se repite hasta completar las 5 posiciones → aparece la celebración final con confeti y video.
5. Click en **"Nueva ronda"** para volver a empezar con un roster limpio.

---

## 🖼️ Cómo agregar o cambiar fotos

Cada foto debe llamarse igual que el nombre que se escribe en el juego, en **minúsculas, sin espacios, sin tildes ni puntuación** (ej. "Juan Cruz" → `juancruz.jpeg`).

- Formatos soportados: `.jpeg`, `.jpg`, `.png` (el código prueba las tres automáticamente).
- Sube el archivo directo a la raíz del repo, junto al `index.html`.
- Si no existe una foto para el nombre escrito, se muestra automáticamente un avatar con la inicial — no rompe nada.

## 👥 Cómo agregar o editar chipaxianos del sorteo

Abre `index.html`, busca esta línea cerca del inicio del `<script>`:

```js
const CHIPAXIANOS = ["Ado","Alexis","Barbi", ...];
```

Agrega, quita o corrige nombres en esa lista. El nombre que aparece ahí es el que después hay que hacer coincidir con el archivo de foto (ver sección anterior).

## 🎬 Video de celebración

Al completar las 5 posiciones se reproduce un video de fondo. Se configura en esta línea:

```js
const VIDEO_URL = "download.mp4";
```

Sube el archivo con ese mismo nombre a la raíz del repo, o cambia el nombre en esa línea para que coincida. Si lo dejas vacío (`""`), la celebración se muestra sin video.

> ⚠️ GitHub tiene un límite de **25MB por archivo** al subir arrastrando desde el navegador. Si el video pesa más, hay que comprimirlo o subirlo por otra vía (Git LFS, etc.).

## 📐 Ajuste de pantalla

La página se auto-ajusta con JavaScript (`fitToScreen()`) para entrar completa en cualquier resolución sin necesidad de zoom manual. Se recalcula solo al cambiar el contenido o el tamaño de ventana.

---

## 🚀 Publicar cambios (GitHub Pages)

Este sitio se sirve directo desde este repo vía GitHub Pages:

1. **Settings → Pages** → Source: rama `main`, carpeta `/ (root)`.
2. Cualquier archivo que subas a la raíz (fotos, video, o el propio `index.html`) queda publicado automáticamente en 1-2 minutos.
3. Si subes una foto/video nuevo y no aparece, esperá un par de minutos y hacé un **hard refresh** en el navegador:
   - Mac: `Cmd + Shift + R`
   - Windows: `Ctrl + Shift + R`

