SEO Y METADATOS — QUÉ HACER AL PUBLICAR
=========================================

1) DOMINIO REAL
-----------------
En el <head> del HTML puse el dominio de ejemplo:
    https://www.andresrepetto.com/
Aparece en 5 lugares: <link rel="canonical">, og:url, og:image (x1),
twitter:image, y el "url"/"image" del JSON-LD al final del <head>.
Buscá "andresrepetto.com" (Ctrl+F) y reemplazalo por el dominio real
una vez que lo tengan.

2) IMAGEN PARA COMPARTIR EN REDES (og-image.jpg)
--------------------------------------------------
Adjunté el archivo og-image.jpg (1200x630, el tamaño recomendado por
Facebook/WhatsApp/LinkedIn/X). Subilo a la raíz del sitio, junto al
HTML, para que quede en:
    https://tu-dominio.com/og-image.jpg
Esto es necesario porque las redes sociales necesitan poder
"descargar" esa imagen desde una URL pública para armar la vista
previa del link — no pueden usar las imágenes que están incrustadas
dentro del HTML (base64). Sin este paso, al compartir el link en
WhatsApp o LinkedIn no se va a ver ninguna imagen.

Podés probar cómo queda la vista previa una vez publicado en:
- https://www.opengraph.xyz/
- https://cards-dev.twitter.com/validator

3) YA IMPLEMENTADO
--------------------
- <meta name="description"> con el resumen que Google muestra en
  los resultados de búsqueda.
- Open Graph completo (Facebook, WhatsApp, LinkedIn) y Twitter Card.
- Datos estructurados (JSON-LD, schema.org/Person) para que Google
  entienda que la página es sobre una persona pública, su profesión
  y su actividad — mejora cómo puede mostrarse en los resultados.
- theme-color, apple-touch-icon, meta robots.

4) VERSIÓN EN INGLÉS — DETECCIÓN DE IDIOMA
---------------------------------------------
Dejé el código de detección de idioma del navegador YA ESCRITO pero
comentado (desactivado) en el <script> final del HTML, buscá:
    "Detección de idioma del navegador"

Cuando la versión en inglés esté lista:
  1. Publicarla en una URL, por ejemplo https://www.andresrepetto.com/en/
  2. Descomentar el bloque de JS y poner ahí esa URL real.
  3. Agregar el mismo bloque (invertido) en la home en inglés, para
     que si alguien de habla hispana entra ahí, lo mande de vuelta.
  4. Agregar en el <head> de AMBAS versiones:
       <link rel="alternate" hreflang="es" href="https://www.andresrepetto.com/">
       <link rel="alternate" hreflang="en" href="https://www.andresrepetto.com/en/">
       <link rel="alternate" hreflang="x-default" href="https://www.andresrepetto.com/">
     (Esto no se agregó todavía porque apuntar a una URL en inglés
     que todavía no existe perjudica el posicionamiento en Google.)

No lo activé antes porque redirigir a una página que no existe
todavía rompería la navegación de cualquier visitante de habla
inglesa. Avisame cuando esté lista la versión en inglés y lo
conecto en un momento.

5) LOGOS DE SOCIEDAD RURAL ARGENTINA Y SANCOR SEGUROS
--------------------------------------------------------
La franja de "confían en sus conferencias" se agregó con el nombre
de ambas instituciones en formato tipográfico (texto, no una imagen
del isotipo real), para evitar reproducir sus marcas/logos oficiales
sin autorización. Si me pasás los archivos de logo oficiales (con
autorización de uso), los reemplazo por las imágenes reales
manteniendo el mismo estilo en escala de grises.
