# Evimiz LatAm Landing Page — Design Spec

**Fecha:** 2026-04-06
**Estado:** Aprobado
**Autor:** Vadim

## Resumen

Landing page en HTML para presentar Evimiz (marca internacional de Sputnik) a potenciales clientes en Argentina y Latinoamérica. Traducido al español, adaptado al mercado local. Formato scroll (no slides).

## Tecnología

- Un archivo `index.html` con CSS/JS inline
- Imágenes en carpeta `assets/`
- Funciona 100% offline — se puede abrir desde USB, enviar por email
- Animaciones de fade-in al hacer scroll (Intersection Observer API)
- Responsive: desktop + móvil
- Sin dependencias externas (no CDN, no frameworks)

## Estilo Visual

- **Tema:** Oscuro (fondo azul oscuro/negro, como el PPT original)
- **Acento:** Rojo Evimiz (#E31E24)
- **Tipografía:** Sistema sans-serif (Inter via Google Fonts si hay internet, fallback a sistema)
- **Animaciones:** Fade-in suave al aparecer en viewport

## Estructura de Secciones

### 1. Hero
- Foto del intercomunicador a la izquierda, texto a la derecha
- Título: "Seguridad inteligente. Acceso sin llaves. Control total."
- Subtítulo: "Intercomunicador inteligente para edificios modernos"
- Logo Evimiz + "White-label Branding gratuito"
- Botón CTA: "Solicitar demo"

### 2. Problema
- 3 tarjetas con íconos:
  - Sistemas de intercomunicación obsoletos
  - Sin soluciones móviles flexibles
  - Demanda creciente de control de acceso inteligente
- Ilustración del mascota Evimiz al costado

### 3. Solución — Ecosistema Evimiz
- 3 columnas: Plataforma Cloud / App Móvil / Equipamiento
- Precio destacado: "Acceso completo a API por solo $2/mes por dispositivo"
- Íconos de productos: intercomunicador, cámara domo, cámara bullet

### 4. Intercomunicador Inteligente
- Foto grande del intercomunicador
- 4 features en grid:
  - Apertura desde App Móvil
  - Llaves MIFARE y NFC
  - Cámara Full HD 24/7 con IR
  - Cuerpo anti-vandálico IK08 / IP64
- White-label: "Personalice con su propia marca"

### 5. Cámaras CCTV IZI
- Foto de cámara
- Specs: HD 2/5MP, IR 18m, IK11+ IP66, -45°C a 60°C

### 6. Plataforma + Marca Blanca
- Screenshot de la plataforma de branding
- 3 bloques: Soporte multilingüe / Marca personalizada / Propiedad total
- "Despliegue su marca en días, no meses"

### 7. Integración SDK/API
- 4 tarjetas: SDK nativo iOS & Android / Push Notifications / UX integrada / Aumento de DAU
- "Integre el intercomunicador inteligente en su aplicación existente"

### 8. Crecimiento (datos de otra región como ejemplo)
- Etiqueta: "Caso de éxito: región CEI"
- Stats: 4.5M descargas, 2.9M MAU, 1.2M DAU, +11.84% mensual
- 4 métricas: 3-5x sesiones diarias, 85%+ retención, nuevos ingresos, datos & insights
- Screenshot Face Recognition (keyless access)

### 9. ¿Por qué Evimiz?
- Screenshot App Store (rating 4.8)
- "Solución de bajo costo y alto rendimiento"
- "Modelos de negocio probados para PYMES y grandes empresas"
- Mascota con guitarra (elemento memorable)

### 10. Contacto
- Foto del equipo en la exposición
- Placeholders para contactos (email, teléfono, sitio web)
- Botón CTA: "Solicitar una demostración"

## Imágenes a Usar

| Imagen | Fuente | Sección |
|--------|--------|---------|
| Intercomunicador Evimiz | slide1 (foto dispositivo) | Hero, Sección 4 |
| Logo Evimiz (blanco) | slide1 | Hero, Footer |
| Mascota Evimiz (hoodie) | slide1 | Hero |
| Mascota (ventana) | slide2 | Problema |
| Cámara domo | slide3 | Solución |
| Mascota (portal) | slide4 | Crecimiento |
| Face Recognition | slide4 (intercom recognition) | Crecimiento |
| Cámara CCTV bullet | slide6 | Cámaras |
| Mascota con cámara | slide6 | Cámaras |
| Platform branding UI | slide7 | Marca Blanca |
| Phone con apps | slide8 | SDK |
| App Store screenshot | slide10 | Por qué Evimiz |
| Mascota con guitarra | slide10 | Por qué Evimiz |
| Foto equipo exposición | slide11 | Contacto |
| Ícono email | slide11 | Contacto |

## Adaptaciones para LatAm

- Todo el texto en español latinoamericano (ustedes, no vosotros)
- Precios en USD (estándar B2B en Argentina)
- Estadísticas CEI presentadas como "caso de éxito en otra región"
- Sin screenshots con texto en ruso
- Tono profesional pero accesible (no "Why we rock")
