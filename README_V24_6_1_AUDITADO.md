# DIFOR V24.6.1 · paquete auditado completo

Este paquete corrige una omisión del ZIP V24.6: ahora incluye toda la infraestructura necesaria para GitHub + Cloudflare Pages.

## Archivos críticos incluidos
- index.html
- _worker.js (API /api/sync y /api/asset, D1/R2 Auto-Init)
- sw.js
- manifest.webmanifest
- _headers
- icon.svg, icon-192.png, icon-512.png, favicon-32.png, apple-touch-icon.png
- schema.sql (referencia; el worker se auto-inicializa)

## Bindings Cloudflare aceptados
- D1: DIFOR_DB o DB
- R2: DIFOR_FILES o BUCKET

## Publicación
Suba todos los archivos de este ZIP a la raíz de la rama main del repositorio. No suba solo index.html.

## Validaciones realizadas
- 5 scripts embebidos del index: node --check OK
- _worker.js: node --check OK
- openForm definido y conectado al submit del dialog
- cloudAutoSyncStarted declarado
- Prospectos: guardado en store prospects + autos revisados en reviewedModels
- /api/sync referenciado por frontend y atendido por _worker.js
- PWA: manifest + service worker + iconos presentes
