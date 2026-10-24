---
name: reverse-skill-macos
description: >-
  Ingeniería inversa en macOS y binarios Mach-O (ejecutables, dylib, frameworks,
  apps de escritorio Apple), delegando al módulo macos-reverse del repositorio
  reverse-skill. Úsalo cuando la tarea sea analizar un binario Mach-O nativo,
  una dylib o una app de macOS, revisar entitlements/firmas, o entender lógica
  nativa en el ecosistema Apple (no iOS/IPA, que va por reverse-skill-ios).
  Dispara con: "macOS", "Mach-O", "dylib", "app de macOS", "binario de Mac",
  "entitlements", "codesign", "framework de Apple". Solo sobre binarios propios
  o muestras autorizadas.
---

# reverse-skill-macos · Inversa de macOS / Mach-O

Atajo al módulo `skills/macos-reverse/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que el binario/app es propio o muestra autorizada.
2. `NOW` — Abrir `skills/macos-reverse/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar el workflow.

## Enfoque

1. **Triage Mach-O** — arquitecturas (fat/universal), load commands, dylibs
   enlazadas, firma y entitlements (`codesign`).
2. **Estático** — desensamblar/descompilar la lógica nativa; para profundizar,
   `reverse-skill-binary`.
3. **Específicos de Apple** — Objective-C/Swift runtime, selectors, categorías;
   protecciones (hardened runtime, notarización).
4. **Síntesis** — funciones/métodos clave anotados; hallazgos reproducibles.

> Para apps iOS/IPA usar `reverse-skill-ios`; esto es para macOS de escritorio.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
