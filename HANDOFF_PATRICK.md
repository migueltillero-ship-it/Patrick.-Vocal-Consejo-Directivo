# Handoff — Sitio para Patrick (Vocal Consejo Directivo / Cónsul Honorario de Francia)

## 1) Archivos a subir al repo `Patrick.-Vocal-Consejo-Directivo`

Sube desde tu carpeta local. Nombres exactos:

- `Patrick_intro_horizontal.mp4` — intro desktop
- `Patrick_intro_vertical.mp4` — intro móvil vertical
- `Arrival_at_the_Terminal.mp3` (o el MP3 que quieras) — audio de fondo
- `Patrick_foto_oficial_1.png` … `Patrick_foto_oficial_4.jpg` — carrusel del hero
- `CV_Patrick_Espanol.pdf`, `CV_Patrick_Francais.pdf` — descargas
- `logo_consulado_francia.png` (+ `logo_afsc.png` si aplica) — logos institucionales

Opcional: folder de Drive con fotos para la galería filmstrip — anota el ID (lo que va después de `/folders/` en la URL).

## 2) Prompt para pegar en la nueva sesión de Claude Code

Abre claude.ai/code → New session → repo `migueltillero-ship-it/Patrick.-Vocal-Consejo-Directivo` → pega:

```
Actúa como Desarrollador Full-Stack, QA y Diseñador UI/UX.

CONTEXTO
Voy a replicar la arquitectura del sitio personal que tengo en
producción en
https://github.com/migueltillero-ship-it/afsc-direccion (rama main,
archivo index.html). Es una landing institucional de ~3900 líneas
con estas capacidades funcionales:

- Fondo 3D animado tipo Vanta sobre canvas Three.js.
- Intro cinematográfico de 3 fases con video pantalla completa,
  branding central, botón "Entrar" y arranque de audio de fondo en
  fade-in. En móvil vertical, swap automático a la versión vertical
  del video.
- Cursor personalizado dual (dot + ring magnético) con null-safety.
- Galería tipo FILMSTRIP horizontal arrastrable (mouse + touch),
  auto-scroll infinito con pausa al hover, lightbox modal para zoom
  desde Drive (`lh3.googleusercontent.com/d/...=w2400`).
- Formularios EmailJS (service_k9b1j7y) con fallback a WhatsApp y
  mailto si la API falla.
- Modales de Cita, Clase de prueba, Inscripción y Testimonios.
- Selector de idioma ES/FR/EN basado en data-attrs.
- Botón de audio flotante, barra de scroll-progress y back-top.
- SEO ejecutivo (og:image, twitter card, schema Person).
- Null-safety en todos los handlers (cursor, audio, modales,
  formularios, lightbox).

TAREA
Clona la arquitectura COMPLETA de ese index.html en este repo,
adaptándola al perfil de PATRICK [APELLIDO] como Vocal del Consejo
Directivo y Cónsul Honorario de Francia para Chiapas y Tabasco.
Decide tú mismo la dirección visual (paleta, tipografías, efectos
3D) en función de la identidad consular y de la obra de Patrick —
preséntame al final una breve justificación del sistema visual
elegido.

REGLA ABSOLUTA DE CONTENIDO
NO INVENTES NINGÚN DATO. Si un dato (fecha, lugar, distinción,
parentesco, cifra, cita) no está confirmado en este prompt o en
los archivos del repo, NO lo coloques. Deja el campo fuera o usa
un placeholder claramente marcado `[POR CONFIRMAR]` que yo
reemplazaré. Esta regla aplica a biografía, trayectoria, fechas,
hitos históricos y referencias a terceros.

Cambios obligatorios respecto al original:
1. Nombre, cargo, biografía, trayectoria → Patrick. Usa solo los
   datos que te pase explícitamente. Si no recibes biografía, deja
   la sección con un placeholder.
2. Foto del hero y carrusel → Patrick_foto_oficial_1..4 del repo.
3. Video intro horizontal/vertical → Patrick_intro_horizontal.mp4 /
   Patrick_intro_vertical.mp4 del repo.
4. PDFs CV → CV_Patrick_Espanol.pdf / CV_Patrick_Francais.pdf.
5. Audio de fondo → Arrival_at_the_Terminal.mp3 del repo.
6. Logo institucional → logo_consulado_francia.png (+ logo_afsc.png
   si está disponible).
7. Sección "Servicios" → adáptala a las funciones consulares:
   asistencia a connacionales franceses, gestión documental,
   enlace institucional, promoción cultural, vínculos académicos.
8. Sección "Legado Francia–Chiapas" (NUEVA, entre Bio y
   Servicios). Reusa este bloque base con data-attrs ES/FR/EN ya
   listos para el selector de idioma:

   <section id="historia" class="alt z10">
     <div class="container">
       <div class="sec-head reveal">
         <p class="eyebrow"
            data-es="Presencia Consular"
            data-fr="Présence Consulaire"
            data-en="Consular Presence">Nuestra Historia</p>
         <h2 class="sec-title"><em
            data-es="Legado Francia-Chiapas"
            data-fr="Héritage France-Chiapas"
            data-en="France-Chiapas Legacy">Legado Francia-Chiapas</em></h2>
       </div>
       <div class="about-grid">
         <div class="about-text reveal d1">
           <p data-es="La presencia consular francesa en Chiapas ha sido un pilar fundamental en la historia del Soconusco. Desde el auge del eje cafetalero a finales del siglo XIX hasta nuestra labor contemporánea, el Consulado ha sido un puente entre culturas."
              data-fr="La présence consulaire française au Chiapas est un pilier de l'histoire du Soconusco. Depuis l'essor de l'axe caféier à la fin du XIXe siècle jusqu'à notre travail contemporain, le Consulat est un pont entre les cultures.">La
              presencia consular francesa en Chiapas ha sido un pilar
              fundamental en la historia del Soconusco. Desde el auge
              del eje cafetalero a finales del siglo XIX hasta
              nuestra labor contemporánea, el Consulado ha sido un
              puente entre culturas.</p>
         </div>
       </div>
     </div>
   </section>

   Dentro de esta sección puedes mencionar a "Robert de Bréon" como
   antecedente histórico vinculado al eje cafetalero del Soconusco,
   PERO únicamente con esa mención de nombre. NO añadas fechas,
   fincas, parentescos ni atribuciones que yo no haya confirmado
   por escrito. Si quieres más densidad histórica, deja
   `[POR CONFIRMAR]`.
9. Sección que exalte la obra de Patrick (trayectoria,
   distinciones, gestión cultural, vínculo Francia–México): SOLO
   con los datos que yo te pase. Lo que no tengas, fuera.
10. Galería filmstrip → usa el folder de Drive cuyo ID te paso en
    el siguiente mensaje. Si te digo "sin folder", omite la
    galería por completo (no inventes imágenes ni placeholders
    decorativos).
11. SEO: og:image y schema Person actualizados a Patrick y a la
    URL de GitHub Pages de este repo. En `knowsAbout` del schema
    puedes incluir "Soconusco", "café", "relaciones
    Francia–México" como temas; no agregues afiliaciones, premios
    ni fechas sin confirmación.

INSTRUCCIONES PARA LA EJECUCIÓN
- Empieza por WebFetch a
  https://raw.githubusercontent.com/migueltillero-ship-it/afsc-direccion/main/index.html
  para obtener el código fuente de referencia COMPLETO.
- Lista los archivos del repo (`ls`) para confirmar qué assets ya
  están disponibles antes de cablearlos. Si un asset listado en
  esta tarea no está en el repo, NO inventes una ruta — déjalo
  como `[ASSET PENDIENTE]` y avísame al final.
- Construye el index.html completo en una sola pasada.
- Aplica las MISMAS protecciones de null-safety que en AFSC.
- Entrégame el archivo listo para producción: commit + push a main
  (o PR draft si la rama está protegida).

Cuando termines, dime:
- commit hash y URL del PR si aplica
- justificación del sistema visual elegido
- lista de placeholders `[POR CONFIRMAR]` / `[ASSET PENDIENTE]`
  que dejaste pendientes
```

## 3) Preguntas que Claude te hará después

Ten esto a mano (lo que no tengas, dilo y queda como `[POR CONFIRMAR]`):

- `GALLERY_FOLDER_ID` del Drive (si no, "sin folder").
- Apellido completo de Patrick.
- Biografía corta (3–4 líneas).
- Datos verificables sobre Robert de Bréon o el eje cafetalero del
  Soconusco que quieras citar textualmente.
- Cualquier preferencia visual fuerte (si no, deja que Claude
  proponga).
