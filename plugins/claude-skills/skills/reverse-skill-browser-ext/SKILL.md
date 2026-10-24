---
name: reverse-skill-browser-ext
description: >-
  Ingeniería inversa de extensiones de navegador (Chrome/Firefox/Edge),
  delegando al módulo browser-extension-reverse del repositorio reverse-skill.
  Úsalo cuando la tarea sea analizar un CRX/XPI, revisar el manifest y permisos
  de una extensión, auditar sus content scripts y background/service worker, o
  buscar comportamiento sospechoso o exfiltración. Dispara con: "extensión de
  navegador", "browser extension", "CRX", "XPI", "content script",
  "manifest de extensión", "extensión de Chrome", "extensión maliciosa". Solo
  sobre extensiones propias o muestras autorizadas.
---

# reverse-skill-browser-ext · Inversa de extensiones de navegador

Atajo al módulo `skills/browser-extension-reverse/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que la extensión es propia o muestra autorizada (análisis
   estático = solo lectura).
2. `NOW` — Abrir `skills/browser-extension-reverse/SKILL.md` del repo y seguir
   su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar extracción → revisión → síntesis.

## Enfoque

1. **Extraer** — descomprimir el CRX/XPI; listar archivos y recursos.
2. **Manifest y permisos** — `manifest.json`, permisos, host permissions,
   content security policy, APIs sensibles solicitadas.
3. **Código** — content scripts, background/service worker, mensajería; buscar
   exfiltración, inyección, endpoints remotos, JS ofuscado (cruzar con
   `reverse-skill-js`).
4. **Síntesis** — capacidades, permisos peligrosos y comportamiento confirmado,
   reproducible.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
