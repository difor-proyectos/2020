# DIFOR V24.2 — D1 Auto-Init

Esta versión no requiere ejecutar SQL manualmente. `_worker.js` crea automáticamente las tablas versionadas `difor_sync_records_v242` y `difor_sync_revisions_v242`, junto con sus índices, antes de leer o guardar datos.

Las tablas antiguas `sync_records`/`sync_revisions` se ignoran para evitar incompatibilidades de esquema.

Bindings compatibles:
- D1: `DIFOR_DB` o `DB`
- R2: `DIFOR_FILES` o `BUCKET`

Después del despliegue, abrir `/api/sync`. Debe devolver `ok:true`, `schema:auto-v24.2`, `d1:true` y `r2:true` cuando ambos bindings estén disponibles.
