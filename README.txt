PLANTILLA DE INVITACIÓN WEB — VERSIÓN CORREGIDA
================================================

Esta carpeta contiene una invitación web estática lista para GitHub Pages.
No necesita PHP, base de datos ni servidor especial.

ARCHIVOS
--------
index.html  -> estructura de la invitación.
style.css   -> diseño, colores, tamaños y adaptación móvil.
script.js   -> DATOS EDITABLES, contador, galería, música y WhatsApp.
assets/     -> fotos y música.

1) CAMBIAR LOS DATOS
--------------------
Abre script.js y modifica únicamente el bloque que empieza con:

const DATA = {

Ahí puedes cambiar nombres, fecha, lugar, padres, padrinos, ceremonia,
recepción, fotos, portada y número de WhatsApp.

IMPORTANTE: dateISO usa el formato:
2026-11-07T20:30:00

El número de WhatsApp debe estar en formato internacional, por ejemplo:
51999999999

2) CAMBIAR FOTOS
----------------
Reemplaza las imágenes de assets/fotos/ manteniendo los mismos nombres:
hero.jpg.jpg
foto1.jpg.jpg
foto2.jpg.jpg
...
foto9.jpg.jpg

También puedes editar la lista photos dentro de script.js si quieres
usar otros nombres de archivo.

3) CAMBIAR MÚSICA
-----------------
Reemplaza:
assets/musica/musica.mp3

Se recomienda usar un archivo MP3 optimizado para web.

4) PROBAR EN TU COMPUTADORA
---------------------------
Puedes abrir index.html directamente en Chrome para revisar la mayor parte
de la invitación. Para una prueba idéntica a GitHub Pages es mejor usar un
servidor local, pero no es obligatorio.

5) SUBIR A GITHUB PAGES
-----------------------
A. Entra a GitHub y crea un repositorio nuevo.
B. Sube index.html, style.css, script.js y la carpeta assets.
C. En el repositorio entra a Settings > Pages.
D. En Build and deployment selecciona Deploy from a branch.
E. Selecciona la rama principal (normalmente main) y la carpeta / (root).
F. Guarda.
G. GitHub generará una dirección parecida a:
   https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/

6) SI USAS TU PROPIO DOMINIO
----------------------------
GitHub Pages también permite configurar un dominio personalizado desde
Settings > Pages > Custom domain.

CORRECCIONES REALIZADAS
-----------------------
- Se corrigieron las referencias a church.address y reception.address.
- Los enlaces de Google Maps ahora se asignan correctamente.
- Se eliminó el problema de generar enlaces <a> dentro de otros <a>.
- La portada ahora se puede cambiar desde DATA.hero.
- El título del navegador se actualiza con los nombres.
- WhatsApp utiliza encodeURIComponent para conservar correctamente tildes,
  saltos de línea y caracteres especiales.
- La galería y el visor de fotos se generan automáticamente.
- Se mejoró el bloqueo de desplazamiento durante la pantalla inicial y el
  visor de fotografías.

NOTA
----
GitHub Pages publica archivos estáticos. La confirmación de asistencia abre
WhatsApp; esta plantilla NO guarda las confirmaciones en una base de datos.


VERSIÓN SIN PANTALLA DE INICIO
Esta versión abre directamente la invitación. Ya no existe el sobre ni el botón "Presionar para abrir". La música queda disponible mediante el botón ♫ porque los navegadores normalmente bloquean la reproducción automática con sonido.


CAMBIO DE DISEÑO — JAMAICA + DORADO
------------------------------------
La invitación utiliza una temática verde Jamaica y dorado.

FLECHA
------
La flecha de "DESLIZA" en la portada es dorada.

AMENIZADORES
------------
Se agregó una sección "Quienes amenizan" con 4 espacios de fotos.
Para colocar tus propias imágenes, en cada bloque de .artist-photo dentro
de index.html puedes reemplazar el contenido por, por ejemplo:

<img src="assets/fotos/amenizador1.jpg" alt="Amenizador 1">

Luego guarda las imágenes dentro de assets/fotos/.
También puedes cambiar el nombre y descripción de cada artista directamente
en index.html.


ACTUALIZACIÓN: La temática principal utiliza PANTONE 19-1554 TCX (Savvy Red), referencia digital HEX #951528, combinada con dorado. La sección de artistas se titula únicamente “AMENIZAN”.


Fotos de AMENIZAN: incluidas directamente en assets/amenizadores/ y ya vinculadas a la invitación.

MÚSICA AUTOMÁTICA
La invitación intenta reproducir musica.mp3 automáticamente al abrirse. Los navegadores modernos pueden bloquear el audio con sonido; si eso ocurre, la primera interacción del visitante (clic, toque o tecla) inicia la música automáticamente. El botón ♫ permite pausarla o reanudarla.
