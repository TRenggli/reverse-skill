---
name: reverse-skill-patch-diff
description: >-
  Análisis de parches y N-day (patch diffing, reproducción de CVE), delegando al
  módulo patch-diff-exploit del repositorio reverse-skill. Úsalo cuando la tarea
  sea comparar versiones parcheada y vulnerable de un binario, localizar el
  cambio que corrige una CVE, o reproducir un N-day/1-day en un laboratorio
  propio. Dispara con: "patch diff", "diferencia de parche", "N-day", "1-day",
  "reproducir CVE", "ghidriff", "Diaphora", "bindiff de parche", "qué cambió el
  parche". Solo en laboratorios propios o alcance autorizado.
---

# reverse-skill-patch-diff · Patch diff / N-day

Atajo al módulo `skills/patch-diff-exploit/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## Ámbito

Para **investigación y laboratorios propios** (entender qué corrige un parche,
reproducir en un entorno controlado). No es para atacar sistemas de terceros.

## ACTION REQUIRED

1. `NOW` — Confirmar contexto autorizado (lab propio / investigación).
2. `NOW` — Abrir `skills/patch-diff-exploit/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` (ghidriff/Diaphora/bindiff). Falta algo
   → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar diffing → localización del cambio → (repro en lab).

## Enfoque

1. **Obtener pares** — versión vulnerable y parcheada del binario/componente.
2. **Diffing** — comparar funciones (ghidriff/Diaphora/bindiff); aislar el
   cambio relevante.
3. **Entender la corrección** — qué validación/condición agregó el parche →
   inferir la vulnerabilidad original. Para profundizar, `reverse-skill-binary`.
4. **Repro (lab)** — reproducir en entorno controlado; documentar el root cause.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
