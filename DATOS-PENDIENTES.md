# 📋 Datos pendientes por completar

Este archivo lista la información que **todavía falta** para dejar el sitio 100% listo
para la validación bancaria y el despliegue final. Complétala y avísame (o edítala tú
siguiendo la columna "Dónde aparece").

> Cuando estén listos, se aplican, se hace `git commit` + `git push` y Vercel redesplega solo.

---

## ✅ Ya completado

| Dato | Valor aplicado |
|------|----------------|
| Correo profesional | `hello@conversionforcellc.com` |
| Razón social | `CONVERSIONFORCE LLC` |
| Domicilio | `Miami, United States` |
| Jurisdicción legal | Estado de Florida, Estados Unidos |
| Nombre del programa | DevInterview Accelerator |

---

## ⚠️ Pendiente (necesito estos datos)

| # | Dato | Placeholder actual | Dónde aparece | Notas |
|---|------|--------------------|---------------|-------|
| 1 | **EIN** (ID fiscal de la LLC) | `[RUC / NIT / EIN]` | `terms.html`, footer de `index.html` | Número EIN que asigna el IRS a la empresa. |
| 2 | **Dominio real del sitio** | `tu-dominio.com` | `index.html` (canonical + Open Graph), `robots.txt`, `sitemap.xml` | ¿Será `conversionforcellc.com` o un subdominio como `programa.conversionforcellc.com`? |
| 3 | **WhatsApp Business** | `10000000000` | Botón CTA final + footer de `index.html` | Formato internacional sin `+` ni espacios. Ej: `13055551234` (EE. UU. = 1 + número). |

---

## 🔜 Recomendado antes de cobrar de verdad

| Dato | Placeholder actual | Dónde aparece | Notas |
|------|--------------------|---------------|-------|
| **Link de pago Plan 1** ($450) | `mailto:...` | Sección Planes en `index.html` | Reemplazar el `href` por tu **Stripe Payment Link** o botón de **PayPal**. |
| **Link de pago Plan 2** ($750) | `mailto:...` | Sección Planes en `index.html` | Igual que el anterior. |
| **Imagen Open Graph** | `og-image.png` | `<meta property="og:image">` en `index.html` | Imagen 1200×630 px para vista previa al compartir en redes/WhatsApp. |

---

## 📝 Cómo completarlo (opción manual)

En tu editor, busca y reemplaza en todo el proyecto:

```
[RUC / NIT / EIN]   →   tu EIN real
tu-dominio.com      →   tu dominio real
10000000000         →   tu WhatsApp (formato internacional)
```

Luego:

```bash
cd dev-interview-accelerator
git add -A
git commit -m "content: completar EIN, dominio y WhatsApp"
git push
```

Vercel detecta el push y redesplega automáticamente. ✅
