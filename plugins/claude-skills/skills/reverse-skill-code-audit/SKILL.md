---
name: reverse-skill-code-audit
description: >-
  Auditoría de código y análisis estático de seguridad (SAST), delegando al
  módulo code-audit del repositorio reverse-skill. Úsalo cuando la tarea sea
  revisar código fuente en busca de vulnerabilidades, correr Semgrep u otro
  SAST, rastrear flujos de datos de fuente a sumidero, o auditar un repositorio
  propio o autorizado. Dispara con: "auditoría de código", "code audit",
  "SAST", "Semgrep", "revisión de seguridad de código", "análisis estático",
  "source-to-sink", "vulnerabilidad en el código". Solo sobre código propio o
  con autorización.
---

# reverse-skill-code-audit · Auditoría de código / SAST

Atajo al módulo `skills/code-audit/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que el código es propio o autorizado. La auditoría estática
   es solo lectura (no ejecutar la app bajo análisis sin alcance).
2. `NOW` — Abrir `skills/code-audit/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales (Semgrep, linters).
   Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar mapeo → reglas SAST → verificación de hallazgos.

## Enfoque

1. **Mapeo** — lenguaje/framework, entradas (fuentes) y sinks peligrosos,
   superficie de ataque.
2. **SAST** — reglas Semgrep/equivalentes; priorizar por severidad y
   explotabilidad; descartar falsos positivos leyendo el contexto.
3. **Data flow** — rastrear source→sink para confirmar que la entrada llega sin
   saneo al sink.
4. **Síntesis** — hallazgos con ubicación (archivo:línea), impacto y fix
   sugerido; confianza marcada.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
