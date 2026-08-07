CÓMO ACTIVAR EL ENVÍO DE EMAILS DEL FORMULARIO
================================================

Esta es una página estática (un solo archivo HTML), no tiene servidor propio.
Para que el formulario mande el correo a andresrepetto.redes@gmail.com sin
necesidad de programar un backend, el archivo usa el servicio gratuito
Web3Forms. Son 2 minutos de configuración:

1. Entrá a https://web3forms.com/
2. Ingresá el email andresrepetto.redes@gmail.com y creá tu "Access Key"
   (te la envían al instante a esa casilla, no pide tarjeta ni registro
   completo).
3. Abrí el archivo andres-repetto-landing.html con un editor de texto,
   buscá (Ctrl+F) el texto:

       TU_ACCESS_KEY_DE_WEB3FORMS

   Aparece 2 veces (una en el HTML del formulario, otra en el script).
   Reemplazá ambas por la clave que te mandaron, por ejemplo:

       value="a1b2c3d4-e5f6-7890-abcd-1234567890ab"

4. Guardá el archivo y subilo a tu hosting. Listo: cada envío del
   formulario llega como email a andresrepetto.redes@gmail.com, con
   nombre, empresa, cargo, email, teléfono y mensaje del interesado.

Plan gratuito de Web3Forms: envíos ilimitados, sin límite mensual.

PROTECCIÓN ANTI-SPAM YA INCLUIDA
---------------------------------
- Honeypot: un campo invisible para personas que los bots suelen
  completar automáticamente; si llega completo, se descarta el envío.
- Captcha matemático simple ("¿cuánto es 4 + 7?") que se regenera en
  cada intento fallido.
- Web3Forms además aplica su propio filtro de spam del lado del
  servidor.

Si en el futuro recibís spam igual, podés sumar reCAPTCHA v2/v3 de
Google (Web3Forms lo soporta de forma nativa) — decime y lo agrego.

ALTERNATIVA
-----------
Si preferís no depender de un servicio externo, la otra opción es
tener un backend propio (por ejemplo un pequeño servidor Node/PHP con
Nodemailer o PHPMailer) que reciba el POST del formulario y envíe el
correo. Es más trabajo de implementar y mantener; avisame si te
interesa ese camino en vez de Web3Forms.
