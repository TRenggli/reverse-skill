---
name: reverse-skill-edr-bypass
description: >-
  Ingeniería inversa de mecanismos de EDR/AV para investigación y red team
  AUTORIZADO (entender hooks, telemetría y técnicas de evasión), delegando al
  módulo edr-bypass-re del repositorio reverse-skill. Úsalo cuando la tarea sea
  analizar cómo un EDR/AV instrumenta procesos (user-mode hooks, AMSI, ETW,
  kernel callbacks) o evaluar resistencia de detección en un laboratorio propio
  o engagement con permiso. Dispara con: "EDR bypass", "evasión de EDR", "AV
  bypass", "unhook", "AMSI", "ETW", "direct syscall", "indirect syscall",
  "cómo detecta el EDR". Solo en laboratorios propios o red team autorizado;
  no para evadir defensas de terceros sin permiso.
---

# reverse-skill-edr-bypass · RE de EDR/AV (investigación / red team autorizado)

Atajo al módulo `skills/edr-bypass-re/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## Ámbito (importante)

Dual-use. Solo para **investigación defensiva, laboratorios propios y red team
con autorización explícita** (entender detección para mejorarla o para un
engagement con permiso). No es para evadir las defensas de sistemas de terceros
sin autorización. Si el contexto no es uno de esos, parar y pedir el alcance.

## ACTION REQUIRED

1. `NOW` — Confirmar contexto autorizado (lab propio / red team con permiso).
2. `NOW` — Correr el gate de scope del repo si aplica a un objetivo
   (`case-init`/`scope.md`), divulgando el comando.
3. `NOW` — Abrir `skills/edr-bypass-re/SKILL.md` del repo y seguir su flujo.
4. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
5. `ACT` — Ejecutar el análisis del mecanismo de detección.

## Enfoque

1. **Mapear la instrumentación** — user-mode hooks, AMSI, ETW, callbacks de
   kernel; qué telemetría produce el EDR.
2. **RE del agente** — para binarios del EDR apoyarse en `reverse-skill-binary`.
3. **Evaluar resistencia** — medir cobertura de detección en el lab; documentar
   para el lado defensivo (detecciones, endurecimiento).
4. **Síntesis** — hallazgos orientados a mejorar detección/respuesta; evidencia
   reproducible dentro del alcance.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
