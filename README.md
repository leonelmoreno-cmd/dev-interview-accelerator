# The Dev Interview Accelerator — Landing Page

Landing page corporativa y de conversión para un programa intensivo 1 a 1 de inglés técnico
y preparación de entrevistas para profesionales de tecnología.

Sitio **estático** (HTML + Tailwind vía CDN + Lucide Icons). Sin build, sin dependencias de Node.
Listo para desplegar en **Vercel**, Netlify, GitHub Pages o cualquier hosting estático.

---

## 📁 Estructura del proyecto

```
dev-interview-accelerator/
├── index.html        → Landing principal (todas las secciones)
├── terms.html        → Términos y Condiciones
├── privacy.html      → Política de Privacidad
├── refund.html       → Política de Reembolso
├── robots.txt        → SEO / crawlers
├── sitemap.xml       → SEO / mapa del sitio
├── vercel.json       → Config de Vercel (URLs limpias + headers de seguridad)
├── .gitignore
└── README.md
```

---

## ✅ Antes de publicar: personaliza estos datos

Todos los textos entre corchetes `[...]` y los valores placeholder deben reemplazarse.
Puedes usar "Buscar y reemplazar" en tu editor sobre **todos los archivos**:

| Buscar                                      | Reemplazar por                          |
|---------------------------------------------|-----------------------------------------|
| `[Nombre legal de la empresa / profesional]`| Tu razón social o nombre profesional    |
| `[RUC / NIT / EIN]`                          | Tu identificación fiscal                |
| `[Ciudad, País]`                             | Tu domicilio fiscal                     |
| `[País / jurisdicción]`                      | Tu jurisdicción legal                   |
| `hola@tu-dominio.com`                        | Tu correo profesional real              |
| `tu-dominio.com`                             | Tu dominio real (SEO, canonical, OG)    |
| `10000000000`                                | Tu número de WhatsApp (formato intern.) |

> 💡 El nombre visible de la marca es **"DevInterview Accelerator"** (logo en header/footer).
> Si quieres otro nombre comercial, edítalo en `index.html`, `terms.html`, `privacy.html` y `refund.html`.

### Conectar los botones de pago
Los CTA de la sección **Planes** hoy abren un correo (`mailto:`). Cuando tengas tus links de pago,
reemplaza el `href` de cada botón por tu enlace de **Stripe Payment Link** o **PayPal**.

---

## 🚀 Cómo verlo en local

No necesitas instalar nada. Abre `index.html` en el navegador, o levanta un servidor simple:

```bash
# Con Python
python3 -m http.server 3000

# o con Node
npx serve .
```

Luego visita `http://localhost:3000`.

---

## ☁️ Despliegue

### Opción A — Subir a GitHub y desplegar en Vercel (recomendado)

1. Crea el repositorio y sube el código:
   ```bash
   cd dev-interview-accelerator
   git init
   git add .
   git commit -m "feat: landing The Dev Interview Accelerator"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/dev-interview-accelerator.git
   git push -u origin main
   ```

2. En [vercel.com](https://vercel.com) → **Add New Project** → importa el repo.
   - Framework Preset: **Other**
   - Build Command: *(vacío)*
   - Output Directory: *(vacío / raíz)*
   - Deploy 🎉

3. (Opcional) Añade tu dominio propio en **Settings → Domains**.

### Opción B — Vercel por CLI

```bash
npm i -g vercel
vercel        # preview
vercel --prod # producción
```

---

## 🔒 Seguridad y cumplimiento

- `vercel.json` añade cabeceras de seguridad (`X-Content-Type-Options`, `X-Frame-Options`, etc.).
- Las páginas legales (Términos, Privacidad, Reembolso) están enlazadas desde el footer, requisito
  habitual para la validación de cuentas comerciales y pasarelas de pago.
- No se recopilan pagos ni datos en el sitio directamente: se delega en Stripe/PayPal.

## 📝 Notas técnicas

- **Tailwind por CDN** es ideal para prototipos y sitios pequeños. Si el proyecto crece, considera
  migrar a Tailwind con build (PostCSS/CLI) para purgar CSS no usado y mejorar el rendimiento.
- Diseño responsive (móvil, tablet, desktop) y accesible (roles ARIA en menú y acordeón FAQ).
- Respeta `prefers-reduced-motion` para usuarios sensibles al movimiento.

---

© 2026 — Uso libre para personalizar y desplegar tu propio programa.
