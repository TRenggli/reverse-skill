---
name: reverse-skill-js
description: >-
  Ingeniería inversa de JavaScript de frontend y recuperación de parámetros
  cifrados / firmas de peticiones, delegando al módulo js-reverse del
  repositorio reverse-skill. Úsalo cuando la tarea sea entender cómo una web
  firma o cifra parámetros, desofuscar JS, seguir lógica de sign/token/encrypt
  en el navegador, usar hooks CDP o SourceMaps, o reproducir una petición
  protegida para análisis autorizado. Dispara con: "JS reverse", "parámetros
  cifrados", "firma de petición", "sign", "token", "desofuscar JS",
  "SourceMap", "CDP", "hook de JS", "cómo firma la web", "replay de petición".
  Solo sobre sitios/apps propios o con autorización.
---

# reverse-skill-js · Inversa de JS de frontend / parámetros cifrados

Atajo al módulo `skills/js-reverse/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar autorización sobre el sitio/app objetivo (propio, SRC/Bug
   Bounty con alcance, o entorno de pruebas). Mencionar la URL no es permiso.
2. `NOW` — Abrir `skills/js-reverse/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para el estado de herramientas MCP/JS
   (p. ej. jshookmcp, CDP). Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar, no solo leer.

## Enfoque

1. **Ubicar el punto** — encontrar dónde se genera la firma/cifrado: búsqueda
   por `sign`, `encrypt`, `token`, `cipher`, cabeceras y payloads sospechosos.
2. **Estático** — leer el bundle; si hay SourceMap, recuperarlo para legibilidad;
   desofuscar cuando aplique.
3. **Dinámico (CDP / hooks)** — breakpoints y hooks en las funciones candidatas
   para observar entradas/salidas sin reimplementar a ciegas.
4. **Reproducir** — reconstruir la firma/cifrado en un script y validar contra
   una petición de prueba dentro del alcance autorizado.

## Salida esperada

Función(es) responsables de la firma/cifrado con su ubicación; algoritmo y
entradas; un PoC reproducible (script que genera el parámetro) dentro del
alcance autorizado.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
