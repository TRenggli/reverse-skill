---
name: reverse-skill-database
description: >-
  Seguridad de bases de datos (hardening, auditoría de configuración y
  privilegios, vías de inyección hacia la BD), delegando al módulo
  database-security del repositorio reverse-skill. Úsalo cuando la tarea sea
  auditar la configuración o los permisos de una base de datos, revisar cuentas
  y roles, evaluar exposición o cifrado, o analizar vectores que terminan en la
  BD, en un entorno propio o autorizado. Dispara con: "base de datos",
  "database security", "hardening de BD", "permisos de base de datos",
  "SQL", "MySQL", "PostgreSQL", "MSSQL", "MongoDB", "auditoría de BD". Solo
  sobre bases de datos propias o con autorización.
---

# reverse-skill-database · Seguridad de bases de datos

Atajo al módulo `skills/database-security/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar autorización sobre la base de datos/servidor objetivo.
2. `NOW` — Abrir `skills/database-security/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar inventario → auditoría de config/privilegios → verificación.

## Enfoque

1. **Inventario** — motor y versión, cuentas, roles, exposición de red, TLS.
2. **Config / privilegios** — cuentas por defecto o sobreprivilegiadas,
   permisos excesivos, cifrado en reposo/tránsito, logging/auditoría.
3. **Vectores** — vías de inyección o acceso que terminan en la BD (coordinar
   con `reverse-skill-api` / `reverse-skill-pentest` según el origen).
4. **Síntesis** — hallazgos con severidad y recomendaciones de hardening,
   reproducibles.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
