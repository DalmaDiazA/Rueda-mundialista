Rompehielos interactivo para las reuniones de equipo de Chipax, con temática Mundial de Fútbol. Se sortea a un chipaxiano, elige una pelota que revela una posición de cancha (Arquero, Defensor, Mediocampista, Delantero o Entrenador), y esa persona nombra a un colega de cualquier equipo de Chipax que cumpla ese rol. La cancha se va llenando con foto + nombre hasta completar la alineación, y al terminar se abre una celebración a pantalla completa con video de fondo.

 Cómo se juega


Click en "¡Sortear chipaxiano!" → el slot elige a alguien al azar.
Esa persona elige una de las 5 pelotas → se revela la posición.
El facilitador escribe el nombre que la persona sorteada elige para ese rol y presiona "Agregar a la cancha".
Se repite hasta completar las 5 posiciones → aparece la celebración final con confeti y video.
Click en "Nueva ronda" para volver a empezar con un roster limpio.

Cómo agregar o cambiar fotos

Cada foto debe llamarse igual que el nombre que se escribe en el juego, en minúsculas, sin espacios, sin tildes ni puntuación (ej. "Juan Cruz" → juancruz.jpeg).


Formatos soportados: .jpeg, .jpg, .png (el código prueba las tres automáticamente).
Sube el archivo directo a la raíz del repo, junto al index.html.
Si no existe una foto para el nombre escrito, se muestra automáticamente un avatar con la inicial — no rompe nada.


Cómo agregar o editar chipaxianos del sorteo

Abre index.html, busca esta línea cerca del inicio del <script>:

jsconst CHIPAXIANOS = ["Ado","Alexis","Barbi", ...];

Agrega, quita o corrige nombres en esa lista. El nombre que aparece ahí es el que después hay que hacer coincidir con el archivo de foto (ver sección anterior).

🎬 Video de celebración

Al completar las 5 posiciones se reproduce un video de fondo. Se configura en esta línea:

jsconst VIDEO_URL = "download.mp4";

Sube el archivo con ese mismo nombre a la raíz del repo, o cambia el nombre en esa línea para que coincida. Si lo dejas vacío (""), la celebración se muestra sin video.


⚠️ GitHub tiene un límite de 25MB por archivo al subir arrastrando desde el navegador. Si el video pesa más, hay que comprimirlo o subirlo por otra vía (Git LFS, etc.).
