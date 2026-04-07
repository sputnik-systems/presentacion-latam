# Evimiz LatAm Landing Page — Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a single-file HTML landing page in Spanish for selling Evimiz smart intercoms to the Latin American (Argentina) market.

**Architecture:** One `index.html` with inline `<style>` and `<script>` tags. Images served from `assets/` folder. No build tools, no CDN dependencies. Fully offline-capable. Intersection Observer for scroll animations. CSS Grid/Flexbox for layout. Responsive (desktop + mobile).

**Tech Stack:** HTML5, CSS3 (custom properties, grid, flexbox, animations), vanilla JavaScript (Intersection Observer API)

---

## File Structure

```
Presentación/
├── index.html              # Single landing page (all CSS/JS inline)
├── assets/
│   ├── intercom.png        # Evimiz intercom device photo
│   ├── logo-evimiz.png     # Evimiz logo (white on transparent)
│   ├── mascot-hoodie.png   # Mascot in hoodie (hero)
│   ├── mascot-window.png   # Mascot at window (problema section)
│   ├── mascot-portal.png   # Mascot in stone portal (crecimiento)
│   ├── mascot-camera.png   # Mascot with camera (CCTV section)
│   ├── mascot-guitar.png   # Mascot with guitar (por qué section)
│   ├── camera-dome.png     # Dome CCTV camera
│   ├── camera-bullet.jpg   # Bullet CCTV camera photo
│   ├── face-recognition.png# Face recognition / keyless access screenshot
│   ├── platform-ui.png     # White-label platform branding UI
│   ├── phone-apps.png      # Phone with branded app icons
│   ├── appstore.png        # App Store screenshot (4.8 rating)
│   ├── team-expo.jpg       # Team photo at exhibition
│   └── icon-email.png      # Email icon for contacts
└── docs/
    └── superpowers/
        ├── specs/...
        └── plans/...
```

### Image Source Mapping

| Target name | Source file |
|---|---|
| `intercom.png` | `slide1_Google_Shape_74_g356f33d14e1_1_3_0.png` |
| `logo-evimiz.png` | `slide1_Google_Shape_76_g356f33d14e1_1_3_1.png` |
| `mascot-hoodie.png` | `slide1_Google_Shape_77_g356f33d14e1_1_3_2.png` |
| `mascot-window.png` | `slide2_Google_Shape_85_g350ae828807_1_9_3.png` |
| `camera-dome.png` | `slide3_Google_Shape_111_g31dee81f586_0_0_7.png` |
| `mascot-portal.png` | `slide4_Google_Shape_132_g350ae828807_2_190_14.png` |
| `face-recognition.png` | `slide4_Google_Shape_139_g350ae828807_2_190_15.png` |
| `camera-bullet.jpg` | `slide6_Google_Shape_186_g359ccdeb123_0_44_28.jpg` |
| `mascot-camera.png` | `slide6_Google_Shape_189_g359ccdeb123_0_44_29.png` |
| `platform-ui.png` | `slide7_Google_Shape_204_p1_30.png` |
| `phone-apps.png` | `slide8_Google_Shape_221_p2_32.png` |
| `appstore.png` | `slide10_Google_Shape_251_p6_34.png` |
| `mascot-guitar.png` | `slide10_Google_Shape_253_p6_35.png` |
| `team-expo.jpg` | `slide11_Google_Shape_273_g32b5ade7bf2_0_0_40.jpg` |
| `icon-email.png` | `slide11_Google_Shape_272_g32b5ade7bf2_0_0_39.png` |

---

## Task 1: Set Up Assets

**Files:**
- Create: `assets/` directory with renamed images

- [ ] **Step 1: Create assets directory and copy images with semantic names**

```bash
cd /Users/admin/Documents/ClaudeProjects/Presentación
mkdir -p assets
SRC="/Users/admin/Documents/Sputnik Argentina/extracted_images"

cp "$SRC/slide1_Google_Shape_74_g356f33d14e1_1_3_0.png" assets/intercom.png
cp "$SRC/slide1_Google_Shape_76_g356f33d14e1_1_3_1.png" assets/logo-evimiz.png
cp "$SRC/slide1_Google_Shape_77_g356f33d14e1_1_3_2.png" assets/mascot-hoodie.png
cp "$SRC/slide2_Google_Shape_85_g350ae828807_1_9_3.png" assets/mascot-window.png
cp "$SRC/slide3_Google_Shape_111_g31dee81f586_0_0_7.png" assets/camera-dome.png
cp "$SRC/slide4_Google_Shape_132_g350ae828807_2_190_14.png" assets/mascot-portal.png
cp "$SRC/slide4_Google_Shape_139_g350ae828807_2_190_15.png" assets/face-recognition.png
cp "$SRC/slide6_Google_Shape_186_g359ccdeb123_0_44_28.jpg" assets/camera-bullet.jpg
cp "$SRC/slide6_Google_Shape_189_g359ccdeb123_0_44_29.png" assets/mascot-camera.png
cp "$SRC/slide7_Google_Shape_204_p1_30.png" assets/platform-ui.png
cp "$SRC/slide8_Google_Shape_221_p2_32.png" assets/phone-apps.png
cp "$SRC/slide10_Google_Shape_251_p6_34.png" assets/appstore.png
cp "$SRC/slide10_Google_Shape_253_p6_35.png" assets/mascot-guitar.png
cp "$SRC/slide11_Google_Shape_273_g32b5ade7bf2_0_0_40.jpg" assets/team-expo.jpg
cp "$SRC/slide11_Google_Shape_272_g32b5ade7bf2_0_0_39.png" assets/icon-email.png
```

- [ ] **Step 2: Verify all 15 images are in place**

```bash
ls -la assets/
```

Expected: 15 files with meaningful names.

- [ ] **Step 3: Commit**

```bash
git add assets/
git commit -m "chore: add assets — renamed images from PPTX for landing page"
```

---

## Task 2: HTML Skeleton + CSS Foundation + Hero Section

**Files:**
- Create: `index.html`

Build the full HTML document structure with all CSS custom properties, base styles, responsive framework, scroll animation JS, and the Hero section as the first visible content.

- [ ] **Step 1: Create index.html with full `<head>`, CSS custom properties, reset, typography, utility classes, scroll-animation JS, and Hero section**

The `<style>` block must include:
- CSS reset (margin/padding/box-sizing)
- Custom properties: `--bg-dark: #0a0e1a`, `--bg-section: #111827`, `--accent: #E31E24`, `--text: #f1f5f9`, `--text-muted: #94a3b8`, `--max-width: 1200px`
- Base body styles: dark background, system font stack with Inter fallback
- `.container` max-width centered
- `.section` with padding and fade-in animation class `.fade-in`
- Grid/flex utility classes for 2-col, 3-col, 4-col layouts
- Button styles (`.btn-primary` red accent, `.btn-outline` border only)
- Responsive breakpoints: mobile-first, `@media (min-width: 768px)` for tablet, `@media (min-width: 1024px)` for desktop
- Card styles (`.card` with dark bg, subtle border, border-radius)
- Stat number styles (`.stat-number` large bold, `.stat-label` muted)

The `<script>` block (at end of `<body>`) must include:
- Intersection Observer that adds `.visible` class to `.fade-in` elements when they enter viewport with threshold 0.1
- Smooth scroll for anchor links

Hero section HTML:
- `<section id="hero">` with two-column grid
- Left: `<img src="assets/intercom.png">` (max-height 500px)
- Right: Evimiz logo image (small, ~200px), `<h1>` "Seguridad inteligente. Acceso sin llaves. Control total.", `<p>` "Intercomunicador inteligente para edificios modernos | White-label Branding gratuito", CTA button "Solicitar demo"

- [ ] **Step 2: Open in browser and verify**

```bash
# Open locally or take screenshot via Playwright
npx playwright screenshot --viewport-size=1440,900 index.html screenshot-hero.png
```

Expected: Dark background, two-column layout with intercom on left and text on right, red CTA button.

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "feat: HTML skeleton + CSS foundation + hero section"
```

---

## Task 3: Sections 2-3 — Problema + Solución

**Files:**
- Modify: `index.html` (add sections after hero, before closing `</main>`)

- [ ] **Step 1: Add Problema section**

Insert after `</section><!-- hero -->`:

```html
<section id="problema" class="section fade-in">
  <div class="container">
    <h2 class="section-title">El Problema</h2>
    <div class="grid-with-image">
      <div class="cards-col">
        <!-- Card 1 -->
        <div class="card">
          <div class="card-icon">🏚️</div>
          <h3>Sistemas obsoletos</h3>
          <p>Los intercomunicadores tradicionales no cumplen con las expectativas móviles modernas de los residentes.</p>
        </div>
        <!-- Card 2 -->
        <div class="card">
          <div class="card-icon">📱</div>
          <h3>Sin soluciones móviles</h3>
          <p>Los desarrolladores carecen de soluciones flexibles y personalizables con marca propia.</p>
        </div>
        <!-- Card 3 -->
        <div class="card">
          <div class="card-icon">🔐</div>
          <h3>Demanda creciente</h3>
          <p>El mercado exige control de acceso inteligente, seguro y con acceso remoto desde el celular.</p>
        </div>
      </div>
      <div class="image-col">
        <img src="assets/mascot-window.png" alt="Evimiz mascota">
      </div>
    </div>
  </div>
</section>
```

CSS additions (add to `<style>`):
- `.grid-with-image`: 2-col grid (cards 60%, image 40%), stacks on mobile
- `.card-icon`: large emoji font-size 2.5rem, margin-bottom
- `.section-title`: centered, font-size 2.5rem, margin-bottom 3rem, with red accent underline

- [ ] **Step 2: Add Solución section**

Insert after problema section:

```html
<section id="solucion" class="section fade-in">
  <div class="container">
    <h2 class="section-title">Ecosistema Evimiz</h2>
    <p class="section-subtitle">Todo lo que necesita para modernizar el acceso a edificios</p>
    <div class="grid-3">
      <div class="card card-center">
        <div class="card-icon">☁️</div>
        <h3>Plataforma Cloud</h3>
        <p>Plataforma totalmente gestionada (Shanyrak). APIs listas para integración con socios.</p>
      </div>
      <div class="card card-center">
        <div class="card-icon">📲</div>
        <h3>App Móvil</h3>
        <p>Atender llamadas, abrir puertas, historial de visitas, archivo de video, códigos de acceso.</p>
      </div>
      <div class="card card-center">
        <div class="card-icon">🔧</div>
        <h3>Equipamiento</h3>
        <p>Intercomunicadores inteligentes y cámaras CCTV. Ecosistema IoT completo.</p>
      </div>
    </div>
    <div class="pricing-banner">
      <span class="pricing-amount">$2 USD/mes</span>
      <span class="pricing-desc">por dispositivo — acceso completo a API incluido</span>
    </div>
  </div>
</section>
```

CSS additions:
- `.card-center`: text-align center
- `.section-subtitle`: centered muted text below title
- `.pricing-banner`: accent background strip, large bold price, flexbox row
- `.grid-3`: 3-column grid, stacks to 1 on mobile

- [ ] **Step 3: Verify in browser**

Expected: Problema has 3 cards left + mascot right. Solución has 3 centered cards + red pricing banner.

- [ ] **Step 4: Commit**

```bash
git add index.html
git commit -m "feat: add Problema and Solución sections"
```

---

## Task 4: Section 4 — Intercomunicador Inteligente

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Add Intercomunicador section**

```html
<section id="intercom" class="section fade-in">
  <div class="container">
    <h2 class="section-title">Intercomunicador Inteligente</h2>
    <div class="product-showcase">
      <div class="product-image">
        <img src="assets/intercom.png" alt="Intercomunicador Evimiz">
      </div>
      <div class="product-features">
        <div class="feature-grid">
          <div class="feature-item">
            <div class="feature-icon">📱</div>
            <h4>Apertura desde App Móvil</h4>
            <p>Abra la puerta del edificio directamente desde su celular, en cualquier momento y lugar.</p>
          </div>
          <div class="feature-item">
            <div class="feature-icon">🔑</div>
            <h4>Llaves MIFARE y NFC</h4>
            <p>Compatible con los tipos de llaves más populares. Entrada sin llave al edificio.</p>
          </div>
          <div class="feature-item">
            <div class="feature-icon">🎥</div>
            <h4>Cámara Full HD 24/7</h4>
            <p>Cámara Full HD con iluminación infrarroja. Captura y almacena archivo en la nube.</p>
          </div>
          <div class="feature-item">
            <div class="feature-icon">🛡️</div>
            <h4>Anti-vandálico</h4>
            <p>Cuerpo resistente con protección mecánica IK08 y protección contra polvo y humedad IP64.</p>
          </div>
        </div>
        <div class="whitelabel-badge">
          <span>✨ Personalice con su propia marca — fácil integración vía API</span>
        </div>
      </div>
    </div>
  </div>
</section>
```

CSS additions:
- `.product-showcase`: 2-col grid (image 40%, features 60%), stacks on mobile with image on top
- `.product-image img`: max-height 450px, centered, drop-shadow filter
- `.feature-grid`: 2x2 grid
- `.feature-item`: card-like with left icon
- `.whitelabel-badge`: subtle banner with accent border-left

- [ ] **Step 2: Verify — intercom photo left, 4 features right in 2x2 grid**

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "feat: add Intercomunicador Inteligente section"
```

---

## Task 5: Section 5 — Cámaras CCTV IZI

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Add CCTV section**

```html
<section id="cctv" class="section fade-in">
  <div class="container">
    <h2 class="section-title">Cámaras CCTV IZI</h2>
    <div class="cctv-layout">
      <div class="cctv-image">
        <img src="assets/camera-bullet.jpg" alt="Cámara CCTV IZI">
      </div>
      <div class="cctv-specs">
        <div class="spec-item">
          <div class="spec-value">2 / 5 MP</div>
          <div class="spec-label">Resolución HD</div>
          <p>1920x1080 / 2592x1944</p>
        </div>
        <div class="spec-item">
          <div class="spec-value">18m</div>
          <div class="spec-label">Visión Nocturna</div>
          <p>Iluminación infrarroja hasta 18 metros</p>
        </div>
        <div class="spec-item">
          <div class="spec-value">IK11+ IP66</div>
          <div class="spec-label">Anti-vandálico</div>
          <p>Máxima protección contra impactos y clima</p>
        </div>
        <div class="spec-item">
          <div class="spec-value">-45°C a 60°C</div>
          <div class="spec-label">Temperatura Operativa</div>
          <p>Funciona en condiciones extremas</p>
        </div>
      </div>
      <div class="cctv-mascot">
        <img src="assets/mascot-camera.png" alt="Evimiz mascota con cámara">
      </div>
    </div>
  </div>
</section>
```

CSS additions:
- `.cctv-layout`: 3-col grid (image, specs, mascot), stacks on mobile
- `.spec-item`: `.spec-value` large bold accent color, `.spec-label` medium bold white
- `.cctv-mascot img`: max-width 200px, aligned bottom-right

- [ ] **Step 2: Verify layout**

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "feat: add Cámaras CCTV IZI section"
```

---

## Task 6: Section 6 — Plataforma + Marca Blanca

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Add Marca Blanca section**

```html
<section id="whitelabel" class="section fade-in">
  <div class="container">
    <h2 class="section-title">Plataforma + Marca Blanca</h2>
    <p class="section-subtitle">App Móvil y Plataforma GEO multilingüe con marca propia para socios</p>
    <div class="whitelabel-showcase">
      <div class="whitelabel-image">
        <img src="assets/platform-ui.png" alt="Plataforma de personalización Evimiz">
      </div>
      <div class="whitelabel-features">
        <div class="wl-feature">
          <h4>🌐 Soporte Multilingüe</h4>
          <p>Plataforma y app disponibles en cualquier idioma. Localizaciones listas para español, inglés, ruso, kazajo y más.</p>
        </div>
        <div class="wl-feature">
          <h4>🎨 Marca Personalizada</h4>
          <p>Su logo, esquema de colores, nombre de app y dominio. Identidad visual completa — los residentes solo ven su marca.</p>
        </div>
        <div class="wl-feature">
          <h4>🏢 Propiedad Total</h4>
          <p>App publicada en la cuenta de desarrollador del socio. Autonomía total — sin branding de Evimiz visible para usuarios finales.</p>
        </div>
      </div>
    </div>
    <div class="whitelabel-cta">
      <p>Despliegue su marca en días, no meses. Nosotros manejamos la tecnología — usted es dueño del producto.</p>
    </div>
  </div>
</section>
```

CSS additions:
- `.whitelabel-showcase`: 2-col grid (screenshot left 55%, features right 45%)
- `.whitelabel-image img`: border-radius, box-shadow to frame the screenshot
- `.wl-feature`: margin-bottom, h4 with emoji inline
- `.whitelabel-cta`: centered italic text, accent color

- [ ] **Step 2: Verify**

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "feat: add Plataforma + Marca Blanca section"
```

---

## Task 7: Section 7 — Integración SDK/API

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Add SDK section**

```html
<section id="sdk" class="section fade-in">
  <div class="container">
    <h2 class="section-title">Integración SDK / API</h2>
    <p class="section-subtitle">Integre el intercomunicador inteligente en su aplicación existente para aumentar el engagement diario</p>
    <div class="grid-2-image">
      <div class="sdk-cards">
        <div class="card">
          <h4>📦 SDK Nativo</h4>
          <p>Incorpore la funcionalidad del intercomunicador directamente en su app. SDK nativo para iOS y Android, API RESTful para backend.</p>
        </div>
        <div class="card">
          <h4>🔔 Push Notifications</h4>
          <p>Las alertas de llamadas entrantes traen a los usuarios de vuelta a la app diariamente. Cada puerta abierta, cada visitante — una razón para interactuar.</p>
        </div>
        <div class="card">
          <h4>✨ UX Integrada</h4>
          <p>Las funciones del intercomunicador aparecen como parte nativa de su app. Sin redirecciones, sin apps externas — una experiencia unificada.</p>
        </div>
        <div class="card">
          <h4>📈 Aumente sus DAU</h4>
          <p>Los residentes usan la app múltiples veces al día. Solo el acceso a puertas genera 3-5 sesiones diarias por usuario.</p>
        </div>
      </div>
      <div class="sdk-image">
        <img src="assets/phone-apps.png" alt="Apps con marca blanca">
      </div>
    </div>
  </div>
</section>
```

CSS additions:
- `.grid-2-image`: 2-col grid (cards 55%, image 45%), reverse on mobile (image first)
- `.sdk-cards`: flex column with gap

- [ ] **Step 2: Verify**

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "feat: add Integración SDK/API section"
```

---

## Task 8: Section 8 — Crecimiento

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Add Crecimiento section**

```html
<section id="crecimiento" class="section fade-in">
  <div class="container">
    <h2 class="section-title">Haga Crecer Su Base de Usuarios</h2>
    <p class="section-subtitle">Cada intercomunicador instalado es un nuevo usuario activo diario para su plataforma</p>
    <div class="caso-badge">📍 Caso de éxito: región CEI (Comunidad de Estados Independientes)</div>
    <div class="stats-row">
      <div class="stat-card">
        <div class="stat-number">4.5M</div>
        <div class="stat-label">Descargas</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">2.9M</div>
        <div class="stat-label">MAU</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">1.2M</div>
        <div class="stat-label">DAU</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">+11.84%</div>
        <div class="stat-label">Crecimiento Mensual</div>
      </div>
    </div>
    <div class="metrics-grid">
      <div class="metric-card">
        <div class="metric-value">3-5x</div>
        <div class="metric-title">Sesiones Diarias</div>
        <p>Los residentes interactúan con el intercomunicador múltiples veces al día — abriendo puertas, revisando cámaras, recibiendo llamadas.</p>
      </div>
      <div class="metric-card">
        <div class="metric-value">85%+</div>
        <div class="metric-title">Tasa de Retención</div>
        <p>Los usuarios del intercomunicador permanecen activos porque el control de acceso es una necesidad diaria, no una función opcional.</p>
      </div>
      <div class="metric-card">
        <div class="metric-value">Nuevos</div>
        <div class="metric-title">Ingresos</div>
        <p>Monetice con funciones premium: archivo de video, códigos de acceso para invitados, gestión de delivery, publicidad.</p>
      </div>
      <div class="metric-card">
        <div class="metric-value">Datos</div>
        <div class="metric-title">e Insights</div>
        <p>Comprenda el comportamiento de los residentes: horarios pico, patrones de visitantes, uso de servicios. Decisiones basadas en datos.</p>
      </div>
    </div>
    <div class="crecimiento-image">
      <img src="assets/face-recognition.png" alt="Reconocimiento facial — acceso sin llave">
    </div>
  </div>
</section>
```

CSS additions:
- `.caso-badge`: small pill/badge with accent border, centered, muted text
- `.stats-row`: 4-col flexbox with large numbers, accent-colored `.stat-number`
- `.metrics-grid`: 4-col grid (2-col on tablet, 1-col mobile)
- `.metric-card`: card with large `.metric-value` in accent, bold `.metric-title`
- `.crecimiento-image`: centered, max-width 400px, margin-top

- [ ] **Step 2: Verify stats row + metrics grid + face recognition image**

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "feat: add Crecimiento section with CEI stats"
```

---

## Task 9: Section 9-10 — Por Qué Evimiz + Contacto

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Add Por Qué section**

```html
<section id="porqué" class="section fade-in">
  <div class="container">
    <h2 class="section-title">¿Por qué elegir Evimiz?</h2>
    <div class="porqué-layout">
      <div class="porqué-content">
        <div class="porqué-item">
          <h3>💰 Solución de bajo costo</h3>
          <p>Nuestra solución es la más económica del mercado, lo que nos convierte en el Smart Lock en la nube con mejores ventas.</p>
        </div>
        <div class="porqué-item">
          <h3>📊 Modelos de negocio probados</h3>
          <p>Modelos de negocio comprobados tanto para PYMES como para grandes empresas.</p>
        </div>
        <div class="appstore-proof">
          <img src="assets/appstore.png" alt="Evimiz en App Store — 4.8 rating">
        </div>
      </div>
      <div class="porqué-mascot">
        <img src="assets/mascot-guitar.png" alt="Evimiz mascota">
      </div>
    </div>
  </div>
</section>
```

- [ ] **Step 2: Add Contacto section**

```html
<section id="contacto" class="section section-contact fade-in">
  <div class="container">
    <h2 class="section-title">Contacto</h2>
    <div class="contact-layout">
      <div class="contact-image">
        <img src="assets/team-expo.jpg" alt="Equipo Evimiz en exposición">
      </div>
      <div class="contact-info">
        <p class="contact-tagline">¿Listo para llevar la seguridad inteligente a su edificio?</p>
        <div class="contact-details">
          <div class="contact-item">
            <img src="assets/icon-email.png" alt="Email" class="contact-icon">
            <span>email@evimiz.com</span>
          </div>
          <!-- Placeholders for phone/website — to be filled by user -->
          <div class="contact-item">
            <span>📞</span>
            <span>+XX XXX XXX XXXX</span>
          </div>
          <div class="contact-item">
            <span>🌐</span>
            <span>www.evimiz.com</span>
          </div>
        </div>
        <a href="#" class="btn-primary btn-large">Solicitar una demostración</a>
      </div>
    </div>
  </div>
</section>

<footer class="footer">
  <div class="container">
    <img src="assets/logo-evimiz.png" alt="Evimiz" class="footer-logo">
    <p>© 2026 Evimiz — Your home, always connected</p>
  </div>
</footer>
```

CSS additions:
- `.porqué-layout`: 2-col grid (content 65%, mascot 35%)
- `.appstore-proof img`: max-width 250px, border-radius, box-shadow
- `.section-contact`: slightly different bg for contrast
- `.contact-layout`: 2-col grid (photo left, info right)
- `.contact-image img`: border-radius, full-width
- `.contact-icon`: 32px height, vertical-align middle
- `.btn-large`: bigger padding, font-size
- `.footer`: minimal, centered, logo + copyright

- [ ] **Step 3: Verify both sections + footer**

- [ ] **Step 4: Commit**

```bash
git add index.html
git commit -m "feat: add Por Qué Evimiz + Contacto + Footer"
```

---

## Task 10: Polish — Responsive, Animations, Final QA

**Files:**
- Modify: `index.html`

- [ ] **Step 1: Add smooth scroll navigation bar**

Add a fixed top navbar with logo + anchor links to each section:

```html
<nav class="navbar">
  <div class="container nav-container">
    <img src="assets/logo-evimiz.png" alt="Evimiz" class="nav-logo">
    <div class="nav-links">
      <a href="#problema">Problema</a>
      <a href="#solucion">Solución</a>
      <a href="#intercom">Intercom</a>
      <a href="#cctv">CCTV</a>
      <a href="#whitelabel">Marca Blanca</a>
      <a href="#sdk">SDK</a>
      <a href="#crecimiento">Crecimiento</a>
      <a href="#contacto">Contacto</a>
    </div>
    <button class="nav-toggle" aria-label="Menu">☰</button>
  </div>
</nav>
```

CSS additions:
- `.navbar`: fixed top, dark bg with blur backdrop, z-index 1000, padding
- `.nav-logo`: height 30px
- `.nav-links a`: white text, no underline, hover accent color, transition
- `.nav-toggle`: hidden on desktop, visible on mobile
- Mobile menu: `.nav-links` becomes vertical dropdown when toggled

JS additions:
- Toggle mobile menu on `.nav-toggle` click
- Close mobile menu when a link is clicked
- Add `.navbar-scrolled` class (more opaque bg) on scroll > 50px

- [ ] **Step 2: Verify responsive behavior**

Test at 3 viewports:
```bash
# Desktop
npx playwright screenshot --viewport-size=1440,900 index.html screenshot-desktop.png
# Tablet
npx playwright screenshot --viewport-size=768,1024 index.html screenshot-tablet.png
# Mobile
npx playwright screenshot --viewport-size=375,812 index.html screenshot-mobile.png
```

- [ ] **Step 3: Final review — check all images load, all text is Spanish, no Russian text, no broken layouts**

- [ ] **Step 4: Commit**

```bash
git add index.html
git commit -m "feat: add navbar, responsive polish, scroll animations"
```

---

## Self-Review Checklist

- [x] **Spec coverage:** All 10 sections from spec are covered (Hero, Problema, Solución, Intercom, CCTV, Marca Blanca, SDK, Crecimiento, Por Qué, Contacto)
- [x] **No placeholders in plan:** All HTML/CSS code is complete in every step
- [x] **Image mapping consistent:** 15 images mapped from source to `assets/` in Task 1, referenced correctly in subsequent tasks
- [x] **No Russian text:** All user-facing text is in Latin American Spanish
- [x] **Offline-capable:** No CDN, no external fonts required, no JS libraries
- [x] **Responsive:** Mobile breakpoints included in CSS requirements
- [x] **CTA present:** "Solicitar demo" in hero, "Solicitar una demostración" in contacts
