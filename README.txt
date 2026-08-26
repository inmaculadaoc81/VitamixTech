VitamixTech ONE PAGE

Dominio:
https://vitamixtech.com.es/

Teléfono caja y botones:
+34 914 46 85 03

Diagnóstico:
20 € + IVA

Incluye:
- Logotipo + isotipo propios
- WhatsApp 24/365
- Recogida
- Atención telefónica
- Google Business
- YouTube
- Cal.com
- Formulario SMTP
- Chatbot n8n
- Mapa
- SEO One Page
- Sección específica Vitamix: motor, cuchillas, vaso, controles y refrigeración

Variables SMTP compartidas en Vercel:
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada únicamente en Vercel]
CONTACT_EMAIL=soporte@kelatos.com

El correo no aparece visible en la web; solo se utiliza en /api/contacto.

Google Analytics:
G-H78CMVGG8T

REVISIÓN (fixes adicionales aplicados):
- Ya tenía menú móvil, colisión del chatbot corregida, borde blanco del
  chat y schema.org (de un commit anterior); no se ha tocado nada.
- Botón de teléfono del menú (.navcall): acortado a solo el número
  (mismo problema de línea partida visto en otros repos de la familia);
  añadido white-space:nowrap.
- Añadida sección de contenido SEO propio (#guia), enlazada en el menú.
- Banner de cookies: no existía. Añadido (Aceptar / Rechazar / Política
  de privacidad → https://kelatos.com/privacy-policy/), con diseño
  apilado a ancho completo en móvil.
- H1 de portada reescrito, corto (≤10 palabras) e incluyendo la marca
  (Vitamix), con el tamaño aumentado: "Tu Vitamix no funciona. ¿Merece
  la pena repararla?"

REDIRECCIÓN DE URLS ANTIGUAS:
Este sitio era antes multipágina (tenía /servicios/... y /modelos/...,
eliminados en commits anteriores al pasar a one-page). Añadido
middleware.mjs: cualquier URL que no sea "/" redirige (301) a la home.
Añadida la dependencia "@vercel/functions" en package.json.
