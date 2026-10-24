---
name: reverse-skill-threat-hunting
description: >-
  Caza de amenazas, ingeniería de detección y trabajo de blue team, delegando al
  módulo threat-hunting del repositorio reverse-skill. Úsalo cuando la tarea sea
  buscar actividad maliciosa en logs/telemetría, escribir o afinar detecciones
  (Sigma, reglas), mapear a MITRE ATT&CK, o derivar hipótesis de hunting a
  partir de IOCs/TTPs. Dispara con: "threat hunting", "caza de amenazas", "blue
  team", "ingeniería de detección", "regla Sigma", "detección", "MITRE ATT&CK",
  "hipótesis de hunting", "buscar amenazas en logs". Sobre datos/telemetría
  propios o autorizados.
---

# reverse-skill-threat-hunting · Threat hunting / detección (blue team)

Atajo al módulo `skills/threat-hunting/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que la telemetría/entorno es propio o autorizado.
2. `NOW` — Abrir `skills/threat-hunting/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar hipótesis → búsqueda → detección → síntesis.

## Enfoque

1. **Hipótesis** — partir de TTPs/IOCs o de una técnica MITRE ATT&CK relevante
   al entorno.
2. **Búsqueda** — consultar logs/telemetría (EDR, proxy, auth, DNS) buscando el
   patrón; reducir falsos positivos.
3. **Detección** — formalizar en reglas (Sigma/equivalente) reutilizables;
   documentar cobertura y gaps.
4. **Síntesis** — hallazgos, detecciones nuevas y recomendaciones; cadena
   Evidencia→Hallazgo→Ruta.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
