# 🏔 La Caravana Club

> **Van life expeditions, Patagonia & beyond.**
> Landing experiencia + ecommerce conectado a Google · WhatsApp · Instagram.
> Producto digital de **South Hustles Studio**, Córdoba.

![Vanilla JS](https://img.shields.io/badge/Vanilla%20JS-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)
![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)

![banner](enhanced/png/Group%2049.png)

---

## 🎯 Concepto

**La Caravana Club** no es un alquiler de vans — es un **club de expediciones curadas** que combina:

- 🚐 Flota motorhome propia (vans 4x4 equipadas full)
- 🗺 Rutas pre-armadas en Patagonia, Norte y Sierras
- 👥 Comunidad cerrada con cuotas mensuales y experiencias mayo / oct / dic
- 📱 Ecommerce conversacional: discovery web → cierre WhatsApp → fidelización Instagram

> El sitio es la **puerta de entrada al club**. La conversión sucede en WhatsApp.
> Instagram retiene y reactiva. Google captura intención de búsqueda y trae tráfico orgánico.

---

## 📑 Índice

- [Concepto](#-concepto)
- [Stack & Arquitectura](#-stack--arquitectura)
- [Flow de Ecommerce Conversacional](#-flow-de-ecommerce-conversacional)
- [Experiencia Mayo — Featured Drop](#-experiencia-mayo--featured-drop)
- [Secciones del Sitio](#-secciones-del-sitio)
- [Paleta & Tipografías](#-paleta--tipografías)
- [Estructura del Repo](#-estructura-del-repo)
- [Deploy](#-deploy)
- [Conexiones Externas](#-conexiones-externas-roadmap)
- [Filosofía de Iteración](#-filosofía-de-iteración)
- [Próximas Mejoras](#-próximas-mejoras)
- [Créditos](#-créditos)

---

## 🛠 Stack & Arquitectura

**Vanilla-first.** Sin build step, sin bundlers, sin frameworks pesados. Lo que ves en el repo es lo que Vercel deploya.

```
HTML5 semántico  ─ index.html (todo CSS/JS inline al final del body)
CSS3 modular     ─ css/variables.css (tokens) + css/components.css (base)
JS vanilla       ─ Spring physics, parallax, intersection observers, scroll triggers
Google Fonts     ─ Playfair Display · Inter · JetBrains Mono · Caveat
Assets           ─ assets/icons/ (SVG line-icons) · enhanced/png/ (stickers branding)
```

### Por qué vanilla y no Next.js / Vite

| Criterio | Vanilla | Next.js |
|---|---|---|
| Time-to-deploy primera versión | ⚡ minutos | horas |
| Edición quirúrgica producción | ✅ directo | requiere rebuild |
| Peso bundle final | ~220KB | ~600KB+ |
| Curva de iteración con cliente | inmediata | merge → CI → preview |
| Cuando justifica migrar | nunca para landing | cuando hay CMS / auth / dashboard |

**Regla:** mientras el sitio sea una landing de conversión, vanilla gana. El día que entre dashboard de socios o backoffice de reservas, se migra a Next + API routes.

---

## 🔁 Flow de Ecommerce Conversacional

```
                ┌─────────────────────────────────────────┐
                │     DISCOVERY                           │
                │  Google Search / Instagram AD / WA      │
                │  → landing lacaravana.club              │
                └─────────────────────────────────────────┘
                                  │
                                  ▼
        ┌──────────────────────────────────────────────────────┐
        │  CONSIDERATION                                       │
        │  • Hero parallax + HUD widget (transmite premium)    │
        │  • Slider expediciones con %OFF (urgencia + precio)  │
        │  • Flota vans + amenities (resuelve "¿es para mí?")  │
        │  • Reseñas Google embebidas (prueba social)          │
        │  • UGC Instagram grid (comunidad real)               │
        └──────────────────────────────────────────────────────┘
                                  │
                                  ▼
        ┌──────────────────────────────────────────────────────┐
        │  INTENT                                              │
        │  Email capture popup (4s) → WhatsApp deeplink        │
        │  Banner Mayo Experience → mensaje pre-armado WA      │
        │  Booking form → genera mensaje WA con datos          │
        └──────────────────────────────────────────────────────┘
                                  │
                                  ▼
        ┌──────────────────────────────────────────────────────┐
        │  CONVERSION (sucede en WhatsApp, no en el sitio)     │
        │  +54 9 3541 665284 — cierre humano + reserva manual  │
        └──────────────────────────────────────────────────────┘
                                  │
                                  ▼
        ┌──────────────────────────────────────────────────────┐
        │  RETENTION                                           │
        │  Instagram @vanliferent.ok → contenido expediciones  │
        │  WhatsApp broadcast → reactivación drops mayo/oct    │
        └──────────────────────────────────────────────────────┘
```

### Mensajes WhatsApp pre-armados

| Trigger | Mensaje |
|---|---|
| Pop-up lead capture | `Hola! Quiero pertenecer a La Caravana Club 🚐` |
| Mayo banner | `Me interesa info de las próximas expediciones 🏔` |
| Footer CTA | `Hola! Quiero pertenecer a La Caravana Club — ¿cuándo es la próxima salida?` |
| Booking form | Construido dinámicamente con datos del formulario (van, fechas, ruta) |

### Por qué WhatsApp y no checkout web

1. **Ticket alto** (USD 400–1500 por experiencia) requiere conversación humana
2. **Customización** (fechas, pet-friendly, asientos extra) imposible en form rígido
3. **Confianza** — Argentina interior compra mejor por WA que por tarjeta web
4. **Cero fricción de pago** — link de transferencia o MP por WA, no fees Stripe

---

## 🌄 Experiencia Mayo — Featured Drop

La sección hero secundaria del sitio. Producto estrella: **expedición Mayo 2026**.

| Atributo | Detalle |
|---|---|
| Destino | Patagonia · Ruta 40 sur |
| Duración | 7 noches / 8 días |
| Salidas | 2026-05-10 y 2026-05-24 |
| Capacidad | 4 vans · máx 16 personas |
| Incluye | Van full equipada, ruta guiada, fogones, mate kit, asistencia 24/7 |
| Precio early bird | -25% hasta 2026-04-15 |
| CTA primaria | Email capture → WhatsApp con mensaje pre-armado |
| CTA secundaria | Booking form completo → resumen WA |

### UX touches específicos del drop Mayo

- **Banner card editorial** con foto van + tipografía Playfair grande
- **Email capture inline** con focus ring dorado animado
- **Badge %OFF** con keyframe pulse cada 3.2s
- **Countdown sutil** hasta fecha de salida (no agresivo)
- **Pop-up de salida** después de 4s con copy específico de Mayo

---

## 📐 Secciones del Sitio

| # | Sección | ID | UX touch |
|---|---|---|---|
| 1 | Nav floating pill | `.nav` | Glassmorphism + scroll-hide |
| 2 | Hero + widget HUD | `.hero` | Parallax + starfield canvas |
| 3 | Collage editorial | `.section-collage` | Grid asimétrico tipo magazine |
| 4 | Marquee rojo | `.marquee-section` | Loop infinito |
| 5 | Expediciones slider | `#expediciones` | Cards con %OFF badge + hover lift |
| 6 | Mayo Experience | `#itinerario` | Banner card + email capture inline |
| 7 | Best Tourism Villages | `.section-villages` | 3 destinos curados |
| 8 | Flota vans | `#flota` | Side panels spring-physics click-to-expand |
| 9 | Argumento económico | `.section-argumento` | Rombos candy con números |
| 10 | Valores / garantías | `.section-valores` | Iconos blancos grandes + microcopy |
| 11 | Reseñas Google | `#resenas` | (placeholder API embed) |
| 12 | Marquee verde | `.marquee-section` | Loop contrasentido al rojo |
| 13 | UGC Instagram | `#comunidad` | Grid 8 imágenes + HUD hover tilt |
| 14 | Stickers scroll horizontal | `.section-stickers` | 12 PNGs scroll-triggered |
| 15 | Booking form | `#booking` | → WhatsApp con mensaje generado |
| 16 | Footer | `.footer` | WA CTA prominente + redes |
| 17 | Pop-up lead capture | `#popupOverlay` | Timer 4s · escape-friendly |

---

## 🎨 Paleta & Tipografías

### Colores

```css
--crema:        #F5EDD8;   /* fondo principal, calidez */
--tinta:        #1A1410;   /* texto, casi negro cálido */
--borde:        #8B1A2A;   /* bordo, acento primario */
--dorado:       #D4A843;   /* highlight, CTA secundarios */
--celeste:      #7ECFD4;   /* fresco, badges */
--turquesa:     #5BC8C0;   /* %OFF, urgencia suave */
--verde-ingles: #2D4A3E;   /* naturaleza, dark variant */
--piedra:       #9B9186;   /* neutros, dividers */
```

### Tipografías (Google Fonts)

| Familia | Uso |
|---|---|
| **Playfair Display** | Títulos editoriales grandes, hero, banners |
| **Inter** | Body copy, labels, navegación |
| **JetBrains Mono** | Datos, coordenadas, HUD widget, technical labels |
| **Caveat** | Notas handcraft, stamps, microcopy de comunidad |

---

## 📂 Estructura del Repo

```
la-caravana-club/
├── index.html                  ← Landing principal (220KB, CSS/JS inline)
├── README.md                   ← Este archivo
├── WORKFLOW_CLAUDE.md          ← Protocolo Claude Code + GitHub + Vercel
├── ASSETS_REGISTRY.md          ← Inventario de assets
├── vercel.json                 ← Config Vercel (cache headers, clean URLs)
├── .gitignore
│
├── css/
│   ├── variables.css           ← Tokens diseño (paleta, tipografías, spacing)
│   └── components.css          ← Estilos base reutilizables
│
├── assets/
│   └── icons/                  ← 17 SVG line-icons (camp-*.svg)
│
└── enhanced/
    └── png/                    ← Stickers branding Group 49–83 (35 PNGs)
```

---

## 🚀 Deploy

### Local

```bash
# Cualquier static server:
npx serve .
# o
python -m http.server 4040
```

Abrir `http://localhost:4040`.

### Vercel (producción)

1. New Project → Import desde `godofredoaltavista-afk/la-caravana-club`
2. Framework Preset: **Other** (static)
3. Build Command: vacío
4. Output Directory: vacío (root)
5. Deploy → URL: `https://la-caravana-club.vercel.app`

**Auto-deploy** activo en cada push a `main`.

---

## 🔌 Conexiones Externas (Roadmap)

| Servicio | Estado | Uso |
|---|---|---|
| **WhatsApp Business** | ✅ activo | Deeplinks `wa.me/5493541665284?text=...` |
| **Google Reviews API** | 🟡 pendiente | Embed reseñas reales en `#resenas` |
| **Google Analytics 4** | 🟡 pendiente | Tracking funnel discovery → WA |
| **Meta Pixel** | 🟡 pendiente | Retargeting Instagram AD |
| **Instagram Basic Display** | 🟡 pendiente | UGC grid auto-pull `@vanliferent.ok` |
| **Mailchimp / ConvertKit** | 🟡 pendiente | Email capture → lista activa |
| **Google Calendar API** | 🟡 pendiente | Botón "agregar a calendario" expediciones |
| **MercadoPago link** | 🟡 pendiente | Pago seña vía WA |

### Estrategia de integración

> No conectar todo de una. Cada API agregada **debe medirse 2 semanas** antes de la siguiente.
> Orden propuesto: GA4 → Meta Pixel → Google Reviews → IG UGC → Mailchimp.

---

## 🧭 Filosofía de Iteración

(ver `WORKFLOW_CLAUDE.md` completo)

### 1. Additive only
Nunca romper lo que funciona. Toda mejora es **adición o refinamiento** de lo existente. Si hay duda → CSS override con `!important` antes de refactorear el componente.

### 2. Quirúrgico
Cada cambio tiene **target preciso**: línea, selector, sección. No limpiar código "de paso". **Un cambio visible = un commit.**

### 3. Frontend only (por ahora)
Todo vive en `index.html`. Sin build steps, sin bundlers. Lo que ves es lo que se deploya.

### 4. Verificar imports antes de commit
Cualquier archivo nuevo referenciado en el HTML (`<img src>`, `<link href>`) **debe existir en el repo**. Vercel rompe silenciosamente si falta un asset.

### 5. Mobile-first siempre
El 80% del tráfico llega desde Instagram AD → mobile. **Diseñar mobile, refinar desktop.**

---

## 🔮 Próximas Mejoras

### Stage 3 — Identidad visual personalizada
- [ ] **Banners custom Franco** → reemplazar `enhanced/png/Group *.png` con artwork propio
- [ ] **Logo GLB 3D giratorio** con delay de mouse (Three.js fiber)
- [ ] **Banner Figma exportado** → zona entre secciones (1030×300 desktop / 440×50 mobile)
- [ ] **Stickers PNG fondo transparente** con scroll-trigger activado por sección

### Stage 3 — Microinteracciones
- [ ] Mousehover **tilt 3D** en cards expediciones (vanilla-tilt)
- [ ] **Cursor custom** con trail dorado en hover sobre CTAs
- [ ] **Loading states** animados en email capture (spring spring spring)
- [ ] **Página de carga** con starfield + logo morph
- [ ] **Transiciones entre secciones** tipo barba.js (page transitions sin reload)

### Stage 3 — Re-organización UX
- [ ] Reordenar secciones según calor de scroll (mover flota arriba de villages)
- [ ] **Menú mejorado**: dropdown con previews de expediciones
- [ ] **Mega-menú mobile** con tabs
- [ ] **Sticky CTA WhatsApp** que aparece después de scroll 60vh

### Stage 3 — Ecommerce profundo
- [ ] Google Reviews API embed real
- [ ] Email capture → Mailchimp + tag por sección de origen
- [ ] Meta Pixel + GA4 + funnel tracking
- [ ] **Calendar embed** con disponibilidad real por van
- [ ] **App de información del vehículo** (pop-up tipo card con specs, fotos, video)

### Stage 3 — Performance & SEO
- [ ] Lazy load imágenes (`loading="lazy"` + intersection observer)
- [ ] Preload hero image + critical CSS
- [ ] OG tags completos (share WhatsApp / Instagram preview)
- [ ] Schema.org `TravelAgency` + `TouristTrip` markup
- [ ] Sitemap.xml + robots.txt

---

## 🤝 Créditos

**Producto digital de South Hustles Studio**
Diseño, dev, copy: Franco Altavista · Córdoba, Argentina
Estética: dark+lime+cyan, three.js, splats, vanlife editorial

**WhatsApp**: [+54 9 3541 665284](https://wa.me/5493541665284)
**Instagram**: [@vanliferent.ok](https://instagram.com/vanliferent.ok)
**Email**: francoaltavista@gmail.com

---

<sub>🤖 Workflow asistido con Claude Opus 4.7 vía Claude Code · ediciones quirúrgicas, additive-only, verificación de imports pre-push.</sub>
