# GymTracker — Instalación en GitHub Pages

## Por qué GitHub Pages

A diferencia de Netlify, GitHub Pages **no tiene límite de créditos** para sitios estáticos como este. Es gratis sin restricciones de deploys ni de tráfico para este tipo de proyecto.

---

## Paso a paso

### 1. Crear el repositorio
1. Entrá a **https://github.com** (creá una cuenta si no tenés)
2. Arriba a la derecha, tocá el **+** → **New repository**
3. Nombre del repositorio: `gymtracker` (o el que quieras)
4. Dejalo **Público**
5. NO marques "Add a README" — ya tenemos uno
6. Tocá **Create repository**

### 2. Subir los archivos
**Opción fácil (sin usar terminal):**
1. En la página del repositorio recién creado, tocá **"uploading an existing file"**
2. Arrastrá estos archivos y carpetas:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - la carpeta `icons/` completa (con los 2 PNG adentro)
3. Abajo, tocá **Commit changes**

### 3. Activar GitHub Pages
1. En el repositorio, andá a **Settings** (pestaña arriba)
2. En el menú izquierdo, tocá **Pages**
3. En "Source", seleccioná **Deploy from a branch**
4. Branch: **main** — Folder: **/ (root)**
5. Tocá **Save**
6. Esperá 1-2 minutos

### 4. Tu URL
Va a quedar en:
```
https://TU-USUARIO-DE-GITHUB.github.io/gymtracker/
```

---

## Para actualizar la app en el futuro

1. Hacés los cambios en `index.html` (o el archivo que corresponda)
2. En el repositorio de GitHub, entrás al archivo que cambiaste
3. Tocás el ícono de lápiz (✏️ Edit)
4. Pegás el contenido nuevo
5. Tocás **Commit changes**
6. En 1-2 minutos el cambio está en vivo

**Importante:** cada vez que actualices `index.html`, recordá también subir un `sw.js` con el número de versión incrementado (`gymtracker-v15` → `gymtracker-v16`, etc.) para forzar que los celulares con la app instalada bajen la versión nueva.

---

## Instalar en el celular

- **Android (Chrome):** abrís la URL, aparece banner "Instalar app"
- **iOS (Safari):** abrís la URL → botón Compartir → "Agregar a pantalla de inicio"

---

## Cuando tengas dominio propio

Cuando compres un dominio (ej: `gymtracker.com`):
1. En Settings → Pages de tu repositorio, hay un campo **"Custom domain"**
2. Ingresás tu dominio ahí
3. En el panel de tu proveedor de dominio (GoDaddy, Namecheap, etc.), agregás los registros DNS que GitHub te indica
4. En unas horas tu dominio propio apunta directo a la app, con HTTPS automático

---

## Estructura de archivos

```
gymtracker/
├── index.html        ← la app completa
├── manifest.json     ← configuración PWA
├── sw.js             ← service worker (modo offline)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```
