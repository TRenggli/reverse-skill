---
name: reverse-skill-binary-diff
description: >-
  Diffing binario y migración de símbolos entre versiones, delegando al módulo
  binary-diff del repositorio reverse-skill. Úsalo cuando la tarea sea comparar
  dos binarios para portar nombres/símbolos, recuperar símbolos cuando falta el
  PDB, o correlacionar funciones entre versiones (cross-version). Dispara con:
  "bindiff", "diff de binarios", "migración de símbolos", "portar símbolos",
  "PDB faltante", "cross-version", "correlacionar funciones", "Diaphora". Solo
  sobre binarios propios o muestras autorizadas.
---

# reverse-skill-binary-diff · Diffing / migración de símbolos

Atajo al módulo `skills/binary-diff/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que los binarios son propios o muestras autorizadas (es
   análisis estático, solo lectura).
2. `NOW` — Abrir `skills/binary-diff/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` (BinDiff/Diaphora, etc.). Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar el emparejamiento y la migración.

## Enfoque

1. **Preparar** — las dos imágenes a comparar (p. ej. una con símbolos y otra
   sin, o dos versiones).
2. **Emparejar** — correlacionar funciones por estructura/CFG/llamadas.
3. **Migrar** — portar nombres/tipos/comentarios al binario sin símbolos;
   marcar emparejamientos de baja confianza.
4. **Síntesis** — cobertura de la migración y funciones clave recuperadas.

Para análisis de binario subyacente, apoyarse en `reverse-skill-binary`. Para
diffs orientados a parches/CVE, usar `reverse-skill-patch-diff`.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
