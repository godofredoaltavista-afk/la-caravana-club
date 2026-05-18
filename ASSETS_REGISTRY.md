# LA CARAVANA CLUB — Registro de Assets
**Qué imágenes usa cada frontend · qué PNGs hay que producir · dónde van**
*Actualizado: 2026-05-14 · Mayo Experience*

---

## 📁 Estructura de carpetas

```
van-caravan-club/
├── index.html          ← Frontend NATURALIS (editorial handcraft)
├── booking.html        ← Frontend COMMERCE (dropshipping premium)
├── css/
│   ├── variables.css   ← design tokens + 3 temas
│   └── components.css  ← rombos, sellos, patterns, cards
├── assets/
│   ├── CLUB DE CARAVANA MAYO.pdf   ← fuente del copy (22MB, 30+ páginas)
│   ├── icons/          ← SET CAMP — íconos SVG/PNG (verde sobre blanco)
│   ├── logos/          ← logo La Caravana Club (varias versiones)
│   └── pngs/           ← PNGs de fondo para meter texto adentro
├── experiences/
│   ├── patagonia/  norte/  sierras/   ← fotos por destino
└── js/                 ← scripts compartidos (futuro)
```

---

## 🖼️ Imágenes que YA se usan (carpeta `../caravan club/`)

> ⚠️ La carpeta `caravan club/` está FUERA de `van-caravan-club/`. Para que carguen en localhost, servir desde `d:\ANTS on MARS\` o mover los assets adentro.

| Archivo | Usado en | Sección |
|---|---|---|
| `1e4fc363-...jpg` | index + booking | Hero background |
| `WhatsApp...15.28.51.jpeg` | index (collage) + booking (van card Mecha) | — |
| `WhatsApp...15.30.24.jpeg` | index (collage) + booking (van card La Niña) | — |
| `WhatsApp...16.15.50.jpeg` | index (collage) + booking (van card Violeta) | — |
| `WhatsApp...12.44.09.jpeg` | index (collage) + booking (van card Gato/Mancha) | — |
| `screencapture-instagram-vanliferent-ok...png` | — (pendiente) | reels preview |
| `screencapture-...pinterest...png` | — (pendiente) | moodboard |

---

## 🎯 SET CAMP — Íconos a producir (`assets/icons/`)

Reemplazar TODOS los emojis por íconos. Estilo: **shape verde inglés #2D4A3E sobre blanco**, o blanco con trazo. Cortar de la imagen "CAMP" doodle que pasó Franco (tiene linterna, hamaca, ollita+café, sillita, carpa, fogón, hacha, pinos, etc.).

| Ícono | Reemplaza emoji | Dónde se usa | Estado |
|---|---|---|---|
| `camp-tent.svg` | ⛺ | includes, hero | ⬜ producir |
| `camp-fire.svg` | 🔥 | argumento, valores, booking bg | ⬜ producir |
| `camp-lantern.svg` | 💡 | includes (GPS/luz) | ⬜ producir |
| `camp-hammock.svg` | 🛏 | van specs (camas) | ⬜ producir |
| `camp-coffee-pot.svg` | ☕ | includes (kit bienvenida) | ⬜ producir |
| `camp-chair.svg` | 🪑 | valores | ⬜ producir |
| `camp-hatchet.svg` | 🪓 | — | ⬜ producir |
| `camp-pine.svg` | 🌲 | dividers, collage | ⬜ producir |
| `camp-paw.svg` | 🐕 | pet-friendly (todas) | ⬜ producir |
| `camp-mate.svg` | 🧉 | check-list | ⬜ producir |
| `camp-map.svg` | 🗺 | GPS, ruta | ⬜ producir |
| `camp-shield.svg` | 🛡 | seguro, garantías | ⬜ producir |
| `camp-water.svg` | 💧 | agua cristalina | ⬜ producir |
| `camp-wine.svg` | 🍷 | cata de vinos | ⬜ producir |
| `camp-moon.svg` | 🌙 | noche experience | ⬜ producir |
| `camp-wrench.svg` | 🔧 | asistencia mecánica | ⬜ producir |

> **Provisorio:** mientras no estén los PNG, los frontends usan rombos con SVG pattern + el ícono. Cuando estén los PNG, swap directo: `<img src="assets/icons/camp-X.svg">` adentro del rombo.

---

## 🖼️ PNGs de fondo para texto (`assets/pngs/`)

Franco va a cargar PNGs originales (vectores de naturaleza, texturas, óvalos con puntitos grises equidistantes como referencia de dimensión). Los frontends los van a usar como `background-image` de contenedores donde se mete texto.

| Slot | Para qué | Ejemplo de uso |
|---|---|---|
| `png-oval-light.png` | placeholder de dimensión (blanco + puntitos grises equidistantes) | rombos de íconos |
| `png-texture-piedra.png` | fondo de sección piedra | sección "Nosotros" |
| `png-texture-agua.png` | fondo celeste con ondas | sección agua/ríos |
| `png-banner-stamp.png` | PNG con marco para meter título adentro | headers de sección |
| `png-moodboard.png` | tablero verde de corte | sección galería |

---

## 📋 Mayo Experience — datos para el copy (del PDF + NotebookLM)

**Nombre experiencia 1:** Mayo Experience — Córdoba Serrana · 22-24 mayo 2026 · 3 días / 2 noches
**Frase:** "Ningún camino es largo con buena compañía"
**Ruta:** Valle de Calamuchita — visita las 3 Best Tourism Villages 2026 (ONU Turismo): La Cumbrecita, Villa General Belgrano, Los Reartes.

**Itinerario:**
- **Día 1 Vie 22:** 14:00 check-in VAN LIFE (Lisandro de la Torre 318, V.C.P.) · 17:00 salida ruta · 18:30 San Clemente (cena Rancho Pampa Alta) · 20:00 Potrero de Garay · pernocte frente al lago
- **Día 2 Sáb 23:** 09:00 desayuno frente al lago · 10:30 Villa General Belgrano · 12:30 almuerzo · 15:00 Santa Rosa · 16:30 acampe Complejo Playa Miami · 20:00 cata de vinos · 21:30 Cena Experience (cordero, fogón, música)
- **Día 3 Dom 24:** 09:00 desayuno → La Cumbrecita · 11:30 caminata cascada · 13:30 almuerzo · 17:30 merienda cierre Dique Los Molinos · 20:30 vuelta VAN LIFE + Experience Check-Out

**Flota (nombres reales del PDF):**
| Unidad | Vehículo | Capacidad |
|---|---|---|
| La Niña | Toyota Hilux 4x4 | 3 pax |
| Franquie | Mercedes Benz | 7 pax |
| Gato/Mancha | Renault Master | 5 pax |
| Violeta | Peugeot Partner | 4 pax |

**Precios base:** Mercedes Sprinter "Mecha" U$S 300/día · Toyota Hilux "La Niña" U$S 230/día

**Incluye:** motorhome · coordinación integral + asistencia · planificación de ruta + roadmap · pensión completa (almuerzos, cenas, experiencias gastro) · 1 bebida sin alcohol por persona/comida · Cena Experience · cata de vinos · grupo privado de coordinación
**No incluye:** bebidas alcohólicas (salvo cata) · ropa de cama / toallas

**Check-list para llevar:** equipo de mate / kit desayuno · frazadas/mantas (va a estar fresco) · toalla/higiene · jarro térmico · ropa de cama o bolsa de dormir

**Miedos a resolver:** sin experiencia previa (te acompañan) · seguridad (organizado, acompañado) · independencia (no es convoy obligatorio) · pet-friendly (el perro viene)

**Cierre:** "Unite a la caravana que recorre los pueblos más lindos de la Argentina. Sostenible, seguro y auténticamente nuestro. ¡Bienvenidos a la experiencia!"

---

## 🔌 Conexiones Google a embeber

| Feature | Cómo | Dónde |
|---|---|---|
| Google Maps ubicación | iframe embed — Lisandro de la Torre 318, Villa Carlos Paz | footer + sección contacto |
| Google Reviews | cards crema-sobre-crema, nombre + micro-foto + estrellas | sección reseñas |
| Instagram @vanliferent.ok | link + preview de reels deslizables | sección social |
| WhatsApp +5493541665284 | `wa.me` con mensaje pre-armado | todas las CTA |

---

*Ir tildando ⬜→✅ a medida que se producen los assets.*
