---
name: reverse-skill-browser-automation
description: >-
  Automatización de navegador para tareas de seguridad (recon, interacción con
  web apps, captura de evidencia), delegando al módulo browser-automation del
  repositorio reverse-skill. Úsalo cuando la tarea sea automatizar flujos en una
  web app autorizada, hacer recon guiado por navegador, o capturar evidencia
  reproducible con herramientas tipo Playwright, en un objetivo propio o en
  alcance. Dispara con: "automatización de navegador", "Playwright", "recon con
  navegador", "automatizar web app", "agent browser", "captura de evidencia
  web", "scripting de navegador para pentest". Solo sobre sitios propios o
  con autorización.
---

# reverse-skill-browser-automation · Automatización de navegador (seguridad)

Atajo al módulo `skills/browser-automation/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar autorización sobre el sitio/web app objetivo.
2. `NOW` — Abrir `skills/browser-automation/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales (Playwright/agent
   browser). Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar el flujo automatizado dentro del alcance.

## Enfoque

1. **Objetivo del flujo** — recon, navegación autenticada, reproducción de un
   paso, o captura de evidencia.
2. **Automatizar** — scriptar la interacción (navegación, formularios, lectura
   del DOM), de forma determinista y reproducible.
3. **Evidencia** — capturas/trazas/HAR como prueba; alimentar la cadena
   Evidencia→Hallazgo→Ruta.
4. **Pivotar** — para firmas/cifrado en el frontend, `reverse-skill-js`; para
   pruebas de API detrás de la web, `reverse-skill-api`.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
