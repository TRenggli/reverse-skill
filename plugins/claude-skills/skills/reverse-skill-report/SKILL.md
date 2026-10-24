---
name: reverse-skill-report
description: >-
  Generación de reportes/writeups de seguridad y diagramas (flujos, rutas de
  ataque, arquitectura), delegando a los módulos docs-generator y
  diagram-generator del repositorio reverse-skill. Úsalo cuando la tarea sea
  redactar el informe formal de un análisis/pentest/CTF, producir un writeup, o
  crear un diagrama de seguridad (Mermaid/Graphviz/PlantUML) a partir de los
  hallazgos. Dispara con: "reporte de seguridad", "informe de pentest",
  "writeup", "generar reporte", "diagrama de ataque", "diagrama de arquitectura",
  "Mermaid", "Graphviz", "PlantUML", "flujo de ataque".
---

# reverse-skill-report · Reportes / writeups + diagramas

Atajo a los módulos `skills/docs-generator/` y `skills/diagram-generator/` del
repo `reverse-skill` (raíz por defecto `C:\Users\jmbud\reverse-skill`; si no
está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Reunir los hallazgos y la cadena Evidencia→Hallazgo→Ruta del caso.
2. `NOW` — Reporte → `skills/docs-generator/SKILL.md`; diagrama →
   `skills/diagram-generator/SKILL.md`. Seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` si un render necesita una herramienta.
   Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Generar el informe y al menos un diagrama.

## Enfoque

1. **Estructura del informe** — resumen ejecutivo, alcance/autorización, método,
   hallazgos con severidad y PoC reproducible, remediación.
2. **Anonimizar** — no dejar datos sensibles sin anonimizar (lo exige RULES.md).
3. **Diagrama** — al menos un flujo (ataque/análisis) o arquitectura
   (Mermaid/Graphviz/PlantUML).
4. **Cierre** — el informe debe incluir la cadena de evidencia; es parte del
   checklist de finalización de RULES.md.

## Salida esperada

Informe formal (writeup) + al menos un diagrama, listos para handoff.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
