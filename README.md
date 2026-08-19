# OSA Web

Landing y páginas de producto de **OSA**, marca de accesorios de escritorio vendidos en drops limitados (no en reposición continua). Dominio de producción: **[osa.limited](https://osa.limited)**.

## 🚧 Estado: en construcción activa

Esta web **no está terminada**. Es el sitio real de una marca en fase de lanzamiento (Drop 001 aún no disponible), así que se actualiza constantemente: nuevas secciones, copy, ajustes de accesibilidad y rendimiento. Lo que hay en este repo puede ir por delante de lo que está publicado en `osa.limited` en un momento dado, no es un proyecto cerrado y congelado, es el work-in-progress de un lanzamiento en marcha.

## Sobre el proyecto

OSA es mi propia marca, accesorios de escritorio (empezando por un deskpad) vendidos en drops limitados. Esta web es la puerta de entrada, historia de la marca, cómo funciona un drop, tarjeta de socio con programa de puntos, y acceso a la lista de espera del primer lanzamiento.

Soy Emmanuel (EMMS), graduado en DAM (Desarrollo de Aplicaciones Multiplataforma), en Zaragoza. Diseño, escribo y despliego esta web yo mismo.

## Tech stack

- **HTML5, CSS3, JavaScript vanilla**, sin frameworks ni build step. Cada página es un HTML autocontenido, simple de mantener, sin dependencias, carga rápida.
- **Tipografía autoalojada** vía `@font-face` (woff2 con fallback woff), sin llamadas a Google Fonts ni CDNs externas.
- **Diseño responsive mobile-first**, con las páginas verificadas a 390px de ancho.
- **Accesibilidad**: contraste de texto ajustado a WCAG AA (mínimo 4.5:1).
- **SEO y metadatos**: Open Graph, Twitter Cards, `sitemap.xml`, `robots.txt`.
- **Cabeceras de seguridad**: Content-Security-Policy, `X-Content-Type-Options`, `Referrer-Policy`, `Permissions-Policy` y HSTS vía `_headers`.
- **Hosting**: [Netlify](https://netlify.com). Dominio registrado y gestionado en Hostinger.
- **Email marketing**: integración con Klaviyo para la lista de espera.

## Cómo se ha construido

Diseño, contenido y decisiones de marca son míos. Para la implementación uso **Claude (Anthropic) como asistente de desarrollo**: iterar CSS más rápido, depurar comportamientos de layout (`position: sticky`, z-index, media queries), y revisar accesibilidad y seguridad antes de publicar. Es una herramienta de pair-programming, no quien decide qué construir.

## Estructura

```
web/
├── index.html      Home
├── timeline.html    Historia de la marca (fases I-IV)
├── tarjeta.html       Tarjeta de socio, programa de puntos
├── fondos.html          Fondos de pantalla de regalo (lead magnet)
├── pistas.html             Pistas del Drop 001
├── terminos.html             Términos y condiciones
├── 404.html
├── fonts/                       Tipografías autoalojadas (ver Licencias)
├── img/                           Imágenes propias del sitio
├── _headers                           Cabeceras de seguridad (Netlify)
├── robots.txt
└── sitemap.xml
```

## Licencias de fuentes

Array (Pangram Pangram) y Supreme (Fontshare) son tipografías con licencia comercial/de uso propio y **no se incluyen** en este repositorio. Geist (Vercel, open source) sí está pensada para redistribuirse. Si clonas el repo, las páginas cargarán con la fuente de sistema como fallback.
