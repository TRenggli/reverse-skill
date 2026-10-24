---
name: reverse-skill-threat-intel
description: >-
  Inteligencia de amenazas (CTI) y OSINT, incluyendo enriquecimiento de IOCs
  desde fuentes públicas, delegando al módulo threat-intelligence del
  repositorio reverse-skill. Úsalo cuando la tarea sea investigar un indicador
  (dominio, IP, hash), recopilar inteligencia de fuentes abiertas, enriquecer
  IOCs, o perfilar un actor/campaña a partir de datos públicos. Dispara con:
  "threat intelligence", "inteligencia de amenazas", "CTI", "OSINT",
  "enriquecer IOC", "investigar dominio", "investigar hash", "actor de amenaza",
  "fuentes abiertas". Uso de fuentes públicas; no recolección intrusiva.
---

# reverse-skill-threat-intel · Threat intelligence / OSINT

Atajo al módulo `skills/threat-intelligence/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## Ámbito

Enfocado en **fuentes públicas** y enriquecimiento pasivo. No hacer recolección
intrusiva ni tocar sistemas de terceros; no compilar datos personales fuera del
objetivo de inteligencia legítimo.

## ACTION REQUIRED

1. `NOW` — Encuadrar la pregunta de inteligencia y el indicador de partida.
2. `NOW` — Abrir `skills/threat-intelligence/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar recolección → enriquecimiento → correlación.

## Enfoque

1. **Pivot inicial** — dominio/IP/hash/handle; registrar lo conocido.
2. **Enriquecimiento** — fuentes públicas (WHOIS/pasivo, reputación, sandbox
   públicas, repos de IOCs); correlacionar con TTPs/MITRE.
3. **Perfilado** — campaña/actor/infraestructura relacionada, con nivel de
   confianza.
4. **Síntesis** — IOCs enriquecidos y conclusiones citando fuentes; incierto
   marcado como tal.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
