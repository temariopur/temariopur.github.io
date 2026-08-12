# PUR URUGUAY

Plataforma web gratuita, mobile-first, para preparar la **Prueba Única de Residencia (PUR) Uruguay**.

Todo en un solo lugar: planificador de 71 temas oficiales, temario filtrable y 12 playlists PUR-CIR curadas de YouTube.

**Live:** `https://pururuguay.uy`  
**Archivo principal:** `pur-v6-pro.html` (single-file app, sin backend)

---

## 🎯 Qué incluye

### 1. Planificador (71 temas)
Organizados por bloque con progreso guardado en `localStorage`:

- **PNA (1-10):** Riesgo CV, Diabetes, Tabaquismo, Violencia, Cefaleas, Osteoarticular, Litiasis/HBP, Ojo rojo, Gastro, ITS/HIV
- **Pediatría (11-20):** Crecimiento, Control salud + Vacunas CEV, Fiebre sin foco, SNC, Respiratorias, GEA, Piel/ITU, Epilepsia, Anemias, Maltrato
- **Gineco-Neo (21-34):** Tamizaje cérvix/mama, Abdomen agudo gineco, Anticoncepción, Metrorragias, ITS, Aborto/ectópico, IVE, APP/RPM, Control embarazo, Urgencias obstétricas, Parto, RN, Asfixia/Reanimación, Violencia género
- **Clínica (35-48):** IC, Arritmias, SCA, TEP/TVP, Neumonía, EPOC, IRA/IRC, ACV, Meningoencefalitis, Diabetes/CAD, Anemias, Hepatitis, TBC, VIH
- **Salud Mental (49-54):** Ansiedad, Depresión, Suicidio, Psicosis, Consumo, Delirium
- **Legal (55-57):** Derechos, Certificado defunción, Consentimiento
- **Bioética (58-60):** Competencia, Final vida/objeción, Confidencialidad
- **Quirúrgica (61-71):** Piel/faneras, Hernias, Biliar, Abdomen agudo, Páncreas, Colo-recto, Anal, Esof/gástrico, Mama, Cuello, Politrauma

Cada tema tiene 3 estados con UI tipo iOS:
- `○ Pendiente` → gris
- `↻ Repaso` → ámbar
- `✓ Hecho` → teal con gradiente + vibración

### 2. Temario oficial PUR 2023
Buscador instantáneo + filtro por bloque. Cards limpias sin tags de prioridad.

### 3. Playlists PUR-CIR (12)
Links directos limpiados (sin `si=` cortado):

- Medicina Interna
- Medicina Familiar y Comunitaria
- Ginecología
- Pediatría
- Cirugía
- Bioética
- Psiquiatría
- RCP Adulto
- RCP Pediátrico
- Encares CIR Rotación 2025-2026
- Encares CIR Cirugía 2023-2024
- Encares CIR 2024

---

## 📱 Diseño

- **Mobile first:** bottom nav fijo (Plan / Temario / Videos), checkboxes 44px, segmented control táctil
- **Desktop:** tabs superiores + progress ring circular
- **Stack:** HTML single-file, Tailwind CDN, Inter + JetBrains Mono, vanilla JS
- **Guardado:** `localStorage` key `pur_status`
- **Animaciones:** 200-700ms cubic-bezier, card-shadow, hover -2px

Último rediseño v7: quitamos los pills ALTA/MEDIA/FÁCIL porque no sumaban, dejamos solo título limpio y estado.

## 🔍 SEO

Incluido en `pur-v6-pro.html`:

- `title`: PUR URUGUAY
- `description`: 71 temas oficiales, planificador, 12 playlists PUR-CIR
- `keywords`: PUR Uruguay, residencia médica, temario 2023
- `canonical` + `hreflang es-UY`
- Open Graph + Twitter large image (para preview en WhatsApp)
- JSON-LD: `WebSite` + `Course` (71 créditos) + `BreadcrumbList`
- Footer SEO con bloques y recursos
- `theme-color` #0f766e

Para producción necesitás:
- `og-image.jpg` 1200x630
- `sitemap.xml`
- `robots.txt`

## 🚀 Uso

1. Abrí `pur-v6-pro.html` en el navegador o hostealo en Vercel/Netlify
2. Filtrá temas en Planificador
3. Tocá Pendiente → Repaso → Hecho
4. Usá Temario para buscar rápido
5. Abrí la playlist del bloque que estás estudiando

Reset: botón Reset borra `localStorage`.

## 📂 Archivos en este proyecto

```
pur-v6-pro.html          # versión actual (SEO + diseño base)
pur-v7-final.html        # diseño hermoso con pills animadas
pur-v8-final-seo-beauty.html # fusión SEO + diseño hermoso
pur-v5-playlists.html    # versión con playlists antes del rediseño
README.md                # este archivo
```

La versión recomendada para deploy es `pur-v8-final-seo-beauty.html` renombrada a `index.html`.

## 📝 Mensaje para WhatsApp

> Buenas! Armé **PUR URUGUAY** 🇺🇾 - 71 temas oficiales, planificador con progreso guardado y las 12 playlists PUR-CIR. 100% para celular. Link: https://pururuguay.uy

## 🛠️ TODO

- [ ] Generar `og-image.jpg`
- [ ] `sitemap.xml` + `robots.txt`
- [ ] Dark mode opcional
- [ ] Exportar progreso a PDF

---

Hecho por y para estudiantes PUR. Gratis, sin login, sin backend.
© 2026 PUR URUGUAY
