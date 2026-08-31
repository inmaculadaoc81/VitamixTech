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
  (Vitamix), con el tamaño aumentado. Iterado en varios commits
  posteriores (afirmativo, sin interrogación, sin condicionales, sin
  "Descubre") hasta el texto final actual: "Tu Vitamix no funciona.
  Le devolvemos toda su potencia."

REDIRECCIÓN DE URLS ANTIGUAS:
Este sitio era antes multipágina (tenía /servicios/... y /modelos/...,
eliminados en commits anteriores al pasar a one-page). Añadido
middleware.mjs: cualquier URL que no sea "/" redirige (301) a la home.
Añadida la dependencia "@vercel/functions" en package.json.

REVISIÓN ADICIONAL (esta pasada — auditoría completa):
- H1, schema.org (teléfono único, coincide en todas partes), og:*,
  canonical (https), borde del chat, sección SEO, banner de cookies,
  package.json y middleware ya estaban todos correctos. Solo se ha
  actualizado este README, que documentaba una versión anterior y ya
  superada del H1. No se ha tocado ningún archivo del sitio.

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente):
- H1 repetía la plantilla "no funciona" usada en varios repos.
  Reescrito con síntoma específico: "Tu Vitamix se apaga sola al
  usarla. La reparamos." (9 palabras).
- BUG REAL — quitada la etiqueta rotada del hero (.hero-label,
  "Batidoras Vitamix · Madrid") que sobresalía y se solapaba con la
  caja de información en anchos de tablet, mismo patrón detectado hoy
  en AcerTech y KoboldTech (aquí con un tercer nombre de clase
  distinto: .hero-label).
- BUG REAL — dos textos decorativos gigantes sin reducción de tamaño
  en móvil/tablet: ".problems::after" ("VITAMIX", 170px) y
  ".blender-art::before" ("POTENCIA", 92px). Añadida reducción en
  tablet (100px/56px) y móvil (60px/40px).
- Enlace de política de privacidad: la casilla existía pero sin
  enlace. Añadido a https://kelatos.com/privacy-policy/, en azul y
  subrayado.
- Añadida franja de aviso de servicio técnico independiente debajo
  del menú (no existía).
- Añadido "Sábados, domingos y días festivos estamos cerrados" debajo
  del horario.
- Botón "Atención Telefónica..." sin icono, a diferencia del de
  WhatsApp. Añadido (verificado con cuidado el cierre de </a>).
- Verificado: schema.org ya usaba correctamente el único teléfono que
  tiene este repo; formulario correctamente conectado a
  /api/contacto.
