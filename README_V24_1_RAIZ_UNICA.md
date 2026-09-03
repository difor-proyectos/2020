# DIFOR V24.1 — GitHub + Cloudflare Pages (RAÍZ ÚNICA)

Esta edición elimina la necesidad de crear/subir la carpeta `functions/`.
Cloudflare Pages usa `_worker.js` en modo avanzado para manejar `/api/sync` y `/api/asset`.
Todos los archivos que debes subir a GitHub están en una sola carpeta/raíz.

## GitHub
Extrae este ZIP y sube TODOS los archivos contenidos dentro de la carpeta del proyecto a la raíz de `main`.
No crees `functions/` ni `api/`.

## Cloudflare Pages
Mantén tus bindings actuales:
- D1: `DIFOR_DB` o `DB`
- R2: `DIFOR_FILES` o `BUCKET`

La V24.1 acepta ambos nombres automáticamente.

Asegúrate de haber ejecutado `schema.sql` en D1.
Después del nuevo deployment prueba:
`https://TU-DOMINIO.pages.dev/api/sync`

Debe responder con `ok:true`, `d1:true` y `r2:true`.

## Tema
Black es el tema de inicio. White continúa como alternativa manual.
