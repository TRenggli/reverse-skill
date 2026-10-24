---
name: reverse-skill-thick-client
description: >-
  Seguridad de aplicaciones thick-client / de escritorio (cliente-servidor,
  almacenamiento local, comunicación con backend), delegando al módulo
  thick-client del repositorio reverse-skill. Úsalo cuando la tarea sea evaluar
  una app de escritorio que habla con un backend, revisar su almacenamiento de
  secretos, interceptar su tráfico, o analizar su lógica de cliente, en un
  entorno propio o autorizado. Dispara con: "thick client", "cliente pesado",
  "app de escritorio", "cliente-servidor", "aplicación de escritorio", "tráfico
  de app de escritorio", "secretos locales de la app". Solo sobre apps propias
  o con autorización.
---

# reverse-skill-thick-client · Seguridad de thick-client / escritorio

Atajo al módulo `skills/thick-client/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que la app/backend es propia o autorizada.
2. `NOW` — Abrir `skills/thick-client/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales (proxies, utilidades).
   Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar triage → almacenamiento → tráfico → lógica.

## Enfoque

1. **Triage** — tecnología (nativa, .NET, Electron, Java), archivos de config,
   dónde guarda credenciales/tokens.
2. **Almacenamiento local** — secretos en disco/registro, cifrado débil,
   permisos.
3. **Tráfico** — interceptar la comunicación con el backend (proxy), pinning;
   para firmas/cifrado del cliente, cruzar con `reverse-skill-js` o
   `reverse-skill-binary`/`-dotnet` según la tecnología.
4. **Síntesis** — superficie y hallazgos con PoC reproducible.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
