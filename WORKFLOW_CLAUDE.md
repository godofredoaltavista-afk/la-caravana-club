# WORKFLOW — La Caravana Club × South Hustles Studio
## Protocolo de trabajo Claude Code + GitHub + Vercel

---

## # CONTEXTO DEL PROYECTO

**Producto**: Landing de experiencia van life — La Caravana Club
**Stack**: HTML/CSS/JS vanilla + Vercel deploy
**Repo**: GitHub → francoaltavista-glitch
**Deploy**: Vercel automático desde branch `main`
**Objetivo inmediato**: Super landing experiencia Mayo 2026 → link para AD de Instagram

---

## ## REGLAS DE TRABAJO FUNDAMENTALES

### ### 1. ADDITIVE ONLY
- Nunca romper lo que ya funciona
- Toda mejora es una adición o refinamiento de lo existente
- Si hay duda: agregar CSS con `!important` en override antes de refactorear el componente original

### ### 2. QUIRÚRGICO
- Cada cambio tiene target preciso: línea, selector, sección
- No limpiar código "de paso" sin que se pida explícitamente
- Un cambio visible → un commit

### ### 3. FRONTEND ONLY
- Todo vive en `index.html` (CSS inline + JS inline al final del body)
- Assets: `assets/icons/` para SVG, `enhanced/png/` para PNGs branding
- Sin build steps, sin bundlers — lo que ves es lo que se deploya

### ### 4. VERIFICAR IMPORTS ANTES DE COMMIT
- Cualquier archivo nuevo referenciado en el HTML (`<img src="...">`, `<link href="...">`) debe existir en el repo
- Vercel rompe silenciosamente si falta un asset — revisar antes de push

---

## ## CONEXIONES MCP DISPONIBLES

```
MCP NotebookLM → notebooks del proyecto Van Life Rent / La Caravana Club
MCP Canva → assets visuales y banners
MCP Google Drive → archivos de referencia
```

### Consultar NotebookLM para:
- Copies y descripción de expediciones
- Información de flota
- FAQs de la marca
- Contexto de handoff sessions anteriores

---

## ## FLUJO DE DEPLOY

```
Editar index.html
→ git add van-caravan-club/index.html
→ git commit -m "feat: descripción del cambio"
→ git push origin main
→ Vercel auto-deploy (~30s)
→ Verificar en preview URL de Vercel
→ Compartir link en AD de Instagram / PDF WhatsApp / cadena de email
```

---

## ## SECCIONES DEL SITIO — Estado actual

| Sección | ID | Estado |
|---|---|---|
| Nav floating pill | `.nav` | ✅ mejorada |
| Hero con widget HUD | `.hero` | ✅ con parallax + starfield |
| Collage editorial | `.section-collage` | ✅ |
| Marquee 1 (rojo) | `.marquee-section` | ✅ nuevo |
| Expediciones slider | `#expediciones` | ✅ con %OFF badges |
| Mayo Experience | `#itinerario` | ✅ + banner card + email capture |
| 3 Best Tourism Villages | `.section-villages` | ✅ |
| Flota vans | `#flota` | ✅ con side panels spring-physics |
| Argumento económico | `.section-argumento` | ✅ rombos candy |
| Valores/garantías | `.section-valores` | ✅ iconos blancos grandes |
| Reseñas Google | `#resenas` | ✅ |
| Marquee 2 (verde) | `.marquee-section` | ✅ nuevo |
| UGC galería Instagram | `#comunidad` | ✅ nuevo — HUD hover tilt |
| Stickers scroll horizontal | `.section-stickers` | ✅ nuevo — 12 PNGs |
| Booking form | `#booking` | ✅ → WhatsApp |
| Footer | `.footer` | ✅ + WA CTA prominente |
| Pop-up lead capture | `#popupOverlay` | ✅ nuevo — 4s timer |

---

## ## ASSETS PENDIENTES DE CARGAR

```
# Imágenes reales (reemplazar placeholders gradientes):
- Hero: foto van en ruta Patagonia
- Cards expediciones: fotos de cada destino
- UGC grid: screenshots Instagram @vanliferent.ok (8 imágenes)
- Mayo banner: foto expedición mayo

# PNGs branding (ya en enhanced/png/):
- Group 49.png → Group 83.png (stickers van life)
- Logo circular PNG para nav / secciones

# Banners a exportar de Figma:
- Formato: 1030 × 300px → entre footer sections
- Formato: 440 × 50px → mobile product card
```

---

## ## PRÓXIMAS MEJORAS PENDIENTES

### ### Stage 3 — Assets reales
- [ ] Cargar fotos reales en placeholders de gradiente
- [ ] Logo GLB 3D giratorio con delay de mouse (Three.js)
- [ ] Banner Figma exportado → zona entre secciones
- [ ] Stickers PNG con fondo transparente → scroll trigger activado

### ### Stage 3 — Ecommerce
- [ ] Integrar Google Reviews API (o embed widget)
- [ ] Conectar email capture con servicio real (Mailchimp / ConvertKit)
- [ ] Analytics: Meta Pixel + Google Analytics 4

### ### Stage 3 — Performance
- [ ] Lazy load imágenes (`loading="lazy"`)
- [ ] Preload hero image
- [ ] OG tags completos para share en WhatsApp / Instagram

---

## ## PALETA DE COLORES

```css
--crema: #F5EDD8
--tinta: #1A1410
--borde: #8B1A2A    /* bordo */
--dorado: #D4A843
--celeste: #7ECFD4
--turquesa: #5BC8C0
--verde-ingles: #2D4A3E
--piedra: #9B9186
```

---

## ## TIPOGRAFÍAS (Google Fonts)

```
Playfair Display → títulos editoriales grandes
Inter → body copy, labels
JetBrains Mono → datos, coordenadas, HUD
Caveat → notas handcraft, stamps
```

---

## ## WHATSAPP — número y mensajes pre-armados

```
Número: +54 9 3541 665284
WA link base: https://wa.me/5493541665284

# Pop-up lead:
?text=Hola! Quiero pertenecer a La Caravana Club 🚐

# Booking form:
?text=Hola! Me interesa reservar... (construido dinámicamente)

# Mayo capture:
?text=Me interesa info de las próximas expediciones 🏔

# Footer CTA:
?text=Hola! Quiero pertenecer a La Caravana Club — ¿cuándo es la próxima salida?
```
