---
name: reverse-skill-ot-ics
description: >-
  Seguridad de OT / ICS (sistemas de control industrial, SCADA, PLCs y protocolos
  industriales), delegando al módulo ot-ics del repositorio reverse-skill. Úsalo
  cuando la tarea sea analizar un entorno OT/ICS, inspeccionar tráfico de
  protocolos industriales (Modbus, DNP3, S7, EtherNet/IP), o evaluar PLCs/HMI en
  un laboratorio o entorno autorizado. Dispara con: "OT", "ICS", "SCADA", "PLC",
  "HMI", "Modbus", "DNP3", "S7comm", "EtherNet/IP", "control industrial",
  "sistema de control". Solo en laboratorios propios o entornos autorizados;
  entornos OT son frágiles.
---

# reverse-skill-ot-ics · OT / ICS / SCADA

Atajo al módulo `skills/ot-ics/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## Ámbito y seguridad (crítico)

Los entornos **OT/ICS son frágiles y de seguridad física**: una acción activa
puede detener procesos o dañar equipos. Trabajar **solo en laboratorios propios
o con autorización explícita**; preferir análisis pasivo. Nada de pruebas
activas contra producción sin permiso y plan acordado.

## ACTION REQUIRED

1. `NOW` — Confirmar autorización y que el entorno es lab/pruebas (no producción
   sin plan). Preferir pasivo.
2. `NOW` — Abrir `skills/ot-ics/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar inventario pasivo → análisis de protocolo → síntesis.

## Enfoque

1. **Inventario (pasivo)** — dispositivos (PLC/HMI/RTU), protocolos presentes,
   topología.
2. **Protocolos** — Modbus/DNP3/S7/EtherNet-IP; para decodificar/reconstruir,
   cruzar con `reverse-skill-protocol`.
3. **Evaluación** — exposición, autenticación, segmentación; sin acciones que
   perturben el proceso salvo autorización explícita.
4. **Síntesis** — hallazgos y recomendaciones con foco en disponibilidad.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
