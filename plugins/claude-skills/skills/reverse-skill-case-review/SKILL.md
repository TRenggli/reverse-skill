---
name: reverse-skill-case-review
description: >-
  Revisión de caso y del grafo de evidencia (solo lectura), con chequeos de
  integridad/fixity de artefactos, delegando al módulo case-review del
  repositorio reverse-skill. Úsalo cuando la tarea sea revisar un caso existente
  en work/<caso>, validar la cadena Evidencia→Hallazgo→Ruta, verificar hashes de
  artefactos, o preparar el handoff de un caso. Dispara con: "revisar caso",
  "case review", "grafo de evidencia", "verificar hashes", "fixity",
  "cadena de evidencia", "handoff de caso", "auditar evidencia". Revisión de
  lectura; no modifica el caso.
---

# reverse-skill-case-review · Revisión de caso / evidencia (read-only)

Atajo al módulo `skills/case-review/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Identificar el directorio del caso (`work/<caso>`). La revisión es
   **solo lectura**: no altera el caso.
2. `NOW` — Abrir `skills/case-review/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Usar el revisor del repo (p. ej.
   `skills/case-review/scripts/review_case.py work/<caso> --verify-hashes
   --strict`); ejecutarlo es un script del repo → divulgar y aprobar.
4. `ACT` — Ejecutar la revisión y reportar.

## Enfoque

1. **Estructura** — scope.md (auth), timeline, workitems presentes y coherentes.
2. **Grafo de evidencia** — Evidencia→Hallazgo→Ruta completo, sin eslabones
   sueltos; comandos reproducibles en cada Evidencia.
3. **Fixity** — verificar hashes de artefactos; marcar los que no cuadran.
4. **Handoff** — resumen de estado, gaps y qué falta para cerrar.

## Salida esperada

Veredicto de la revisión: integridad, cobertura de la cadena, discrepancias de
fixity y pendientes.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
