---
name: reverse-skill-forensics
description: >-
  Forense digital y respuesta a incidentes (volcados de memoria, timeline de
  disco, artefactos del sistema), delegando al módulo digital-forensics del
  repositorio reverse-skill. Úsalo cuando la tarea sea analizar un volcado de
  memoria, construir una línea de tiempo forense, examinar artefactos de
  Windows/Linux, recuperar indicadores de un incidente, o correlacionar
  evidencia. Dispara con: "forense", "forensics", "volcado de memoria", "memory
  dump", "timeline forense", "respuesta a incidentes", "DFIR", "artefactos del
  sistema", "análisis de disco". Solo sobre evidencia propia o autorizada.
---

# reverse-skill-forensics · Forense digital / DFIR

Atajo al módulo `skills/digital-forensics/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que la evidencia es propia o autorizada. Preservar
   integridad: trabajar sobre copias, registrar hashes, no alterar originales.
2. `NOW` — Abrir `skills/digital-forensics/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales de herramientas.
   Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar adquisición-verificada → análisis → timeline → síntesis.

## Enfoque

1. **Integridad** — trabajar sobre imágenes/copias; calcular y registrar hashes
   (la cadena de custodia importa).
2. **Memoria** — procesos, conexiones, inyecciones, artefactos en RAM.
3. **Disco / artefactos** — sistema de archivos, registro (Windows), logs,
   persistencia, artefactos de usuario.
4. **Timeline** — correlacionar marcas de tiempo en una línea única; destacar el
   periodo del incidente.

## Salida esperada

Artefactos e indicadores relevantes; timeline del incidente; cadena
Evidencia→Hallazgo→Ruta con hashes y comandos reproducibles. Reporte
anonimizado donde corresponda.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
