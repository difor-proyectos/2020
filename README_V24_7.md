# DIFOR V24.7 — Formularios estabilizados

- Elimina toda referencia al identificador global `openForm`.
- Todos los formularios usan `window.DIFOR_OPEN_FORM`.
- Mantiene Cloudflare `_worker.js`, D1/R2 Auto-Init, PWA y tema Black inicial.
- Service Worker con caché nueva `difor-v24-7-form-runtime`.
