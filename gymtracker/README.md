# GymTracker — Instrucciones de instalación

## Qué necesitás para instalar la app

La app es una **PWA (Progressive Web App)** — esto significa que es un sitio web que se comporta como una app nativa en el celular. Para que funcione necesitás hostearlo en algún servidor con HTTPS.

---

## Opción 1 — GitHub Pages (gratis, recomendado)

1. Creá una cuenta en https://github.com si no tenés
2. Creá un repositorio nuevo (ej: `gymtracker`)
3. Subí estos archivos al repositorio:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icons/icon-192.png`
   - `icons/icon-512.png`
4. Andá a Settings → Pages → Source: seleccioná `main` branch → Save
5. En unos segundos tu app va a estar en `https://TU_USUARIO.github.io/gymtracker`

**Para instalar en el celular:**
- **Android (Chrome):** Abrí la URL, aparece un banner "Agregar a pantalla de inicio" → tocá Instalar
- **iOS (Safari):** Abrí la URL → tocá el botón de Compartir → "Agregar a pantalla de inicio"

---

## Opción 2 — Netlify (drag & drop, aún más fácil)

1. Andá a https://netlify.com y creá una cuenta gratis
2. En el dashboard, arrastrá la carpeta `gymtracker` completa al área de drop
3. Netlify te da una URL automática con HTTPS
4. Instalá desde el celular como en la opción 1

---

## Opción 3 — Vercel

1. Instalá Vercel CLI: `npm i -g vercel`
2. En la carpeta del proyecto: `vercel`
3. Seguí los pasos → te da una URL HTTPS

---

## Estructura de archivos

```
gymtracker/
├── index.html        ← la app completa
├── manifest.json     ← configuración PWA
├── sw.js             ← service worker (modo offline)
└── icons/
    ├── icon-192.png  ← ícono para Android
    └── icon-512.png  ← ícono splash screen
```

## Características

- Funciona 100% offline después de la primera carga
- Los datos se guardan en el dispositivo (localStorage)
- Instalable como app nativa en iOS y Android
- Dark mode automático según el sistema
- Compatible con la barra de estado de iOS (safe area insets)
