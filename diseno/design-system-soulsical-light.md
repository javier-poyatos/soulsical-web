# Design System Document: Soulsical — "The Luminous Stage" (Light Mode)

## 1. Overview & Creative North Star: "The Digital Curator & The Luminous Stage"
This design system is not a standard utility template; it is a live theatrical performance translated into a high-end editorial and archival experience. While the Dark mode represents the intimate, backstage mystery of the auditorium (*The Velvet Stage*), this **Light mode (*The Luminous Stage*)** captures the clarity, radiance, and daylight focus of the rehearsals, masterclasses, and modern art gallery archives.

Our Creative North Star is **The Digital Curator**: treating every screen like a premium printed Broadway playbill, an art monograph, or an haute-couture exhibition catalogue. We balance profound theatrical emotion with modern typographic discipline, generous gallery whitespace, and deliberate tonal shifts.

---

## 2. Color Palette & Atmospheric Hierarchy

The Light palette replaces deep dark velvety blacks with pristine gallery whites, architectural warm off-whites, and soft ash lavenders, letting the signature Broadway purples act as resonant spotlights.

### Primary Colors
- **Spotlight Purple (Brand Primary):** `#794FC9` (RGB: `121, 79, 201`)
  - Role: Key CTAs, brand moments, primary headline accents, and active focus indicators.
- **Ash Lavender (Secondary / Structural Tones):** `#907F9C` (RGB: `144, 127, 156`)
  - Role: Subtle secondary labels, category tags, decorative dividers, and secondary actions.
- **Soft Lilac (Surface Tint / Accent):** `#C2ADCD` (RGB: `194, 173, 205`)
  - Role: Highlight pill backgrounds, subtle notification cards, and tertiary badges.

### Neutral & Background Foundations
- **Base Canvas (Pristine White):** `#FFFFFF` (RGB: `255, 255, 255`)
  - Role: Main backdrop for high-contrast typography and clear negative space.
- **Surface Low (Gallery Off-White):** `#F8F7FA` or `#F5F3F6` (RGB: `245, 243, 246`)
  - Role: Subtle section containers, input form backdrops, and card groupings.
- **Balanced Charcoal (Primary Text):** `#1E1B24` (RGB: `30, 27, 36`)
  - Role: High-legibility headlines and primary reading body text.
- **Neutral Muted Gray (Secondary Text):** `#737373` (RGB: `115, 115, 115`)
  - Role: Metadata, supporting paragraphs, captions, and inactive navigation links.
- **Soft Border / Divider:** `#E9E5EE` (RGB: `233, 229, 238`)
  - Role: Hairline separators and subtle component boundaries without visual clutter.

---

## 3. Typography & Editorial Scale

The typography relies on dramatic contrast between bold, compressed display typography and clean, humanistic sans-serif geometry.

### Primary Display: Anton
- **Font Family:** `'Anton', sans-serif`
- **Characteristics:** All-caps impact, theatrical presence, tight kerning, vertical drama.
- **Usage:**
  - `Hero Title / Display XL`: `text-5xl md:text-7xl lg:text-8xl tracking-tight uppercase leading-[0.9]`
  - `Section Headline / Display MD`: `text-3xl md:text-5xl uppercase tracking-normal leading-[0.95]`
  - `Stat Counters & Stage References`: `text-4xl md:text-6xl uppercase`

### Secondary & Body: Poppins / Epilogue
- **Font Family:** `'Poppins', 'Epilogue', sans-serif`
- **Characteristics:** Crisp geometry, excellent legibility on light backgrounds, warm editorial tone.
- **Usage:**
  - `Subhead / Lead Paragraph`: `font-normal text-lg md:text-xl text-neutral-600 leading-relaxed`
  - `Body Copy`: `font-normal text-sm md:text-base text-neutral-600 leading-relaxed`
  - `Metadata & Kicker Labels`: `font-semibold text-xs tracking-widest uppercase text-[#794FC9]`
  - `Nav & Button Labels`: `font-semibold text-xs md:text-sm tracking-wider uppercase`

---

## 4. Layout, Spacing & The "No Solid Borders" Rule

In accordance with our high-end aesthetic, interfaces must avoid sterile 1px dark borders.

- **Tonal Transitions over Hard Borders:** Sections are separated by atmospheric shifts in light tonal containers (`bg-[#F8F7FA]`) rather than explicit border lines.
- **Generous Whitespace Rhythm:** Macro-spacing between sections uses generous vertical padding (`py-20` to `py-32`) to give content the dignity of a fine-art catalogue.
- **Asymmetric Editorial Grids:** Layouts feature editorial asymmetry—pairing large typography and full-bleed stage imagery with offset columns of explanatory prose.
- **Elevation & Shadows:** Soft, diffuse ambient shadows (`box-shadow: 0 10px 30px -10px rgba(121, 79, 201, 0.08)`) create a subtle floating sensation for cards without muddiness.

---

## 5. Component Library & Patterns

### A. Navigation Bar (TopNavBar)
- **Background:** `bg-white/85 backdrop-blur-md`
- **Logo:** Official Soulsical wordmark script / `font-['Anton'] text-[#794FC9]`
- **Links:** Muted neutral (`text-neutral-500 hover:text-[#794FC9] transition-colors`) with active link marked by bold text and a subtle `#794FC9` indicator.
- **Primary CTA:** Solid Spotlight Purple button with white text (`bg-[#794FC9] text-white hover:bg-[#683eb8] rounded-md px-6 py-2.5 font-semibold text-xs uppercase tracking-wider`).

### B. The "Archive Card"
- **Surface:** White container (`bg-white`) nested on gallery off-white backdrops, or subtle `#F8F7FA` containers.
- **Visuals:** Framed performance photography, rehearsal contact sheets, or performer portraits with duotone or warm neutral grading.
- **Typography:** Display title in Anton, category pill in `#C2ADCD` or `#907F9C/20`, body in Poppins.
- **Hover Interaction:** Subtle lift (`hover:-translate-y-1.5 transition-transform duration-300`) and soft ambient violet shadow glow.

### C. Buttons & Interactive Controls
- **Primary Button:** `#794FC9` background, white text, pill or soft rounded geometry (`rounded-md` or `rounded-full`).
- **Secondary / Ghost Button:** Transparent background, ash lavender or purple stroke/text (`border border-[#794FC9] text-[#794FC9] hover:bg-[#794FC9]/5`).
- **Form Controls:** Clean input fields with `#F5F3F6` background, borderless or single soft bottom line, and purple focus rings.

### D. Footer & Curtain Call
- **Background:** Crisp light gray/lavender shift (`bg-[#F5F3F6]`) with subtle watermark typography in the background.
- **Content:** Essential navigation, booking inquiry direct contact, social links, and legal mentions.

---

## 6. Tone of Voice & Content Guidance
- **Personality:** Passionate, curated, sophisticated, warm, human.
- **Language:** Spanish (Spain native tone: "Lleva la magia del escenario a tu próximo evento", "Arquitectura vocal", "Elenco", "Muestras: Voz y movimiento").
- **Avoid:** Corporate generic jargon ("Nuestros servicios integrales"), hyper-technical sterile terms, or gaudy commercial banners. Treat the copy as an invitation to a cultural awakening.