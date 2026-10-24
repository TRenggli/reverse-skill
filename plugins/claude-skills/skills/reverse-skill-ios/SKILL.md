---
name: reverse-skill-ios
description: >-
  Ingeniería inversa de iOS / apps móviles Apple (IPA, Mach-O, instrumentación
  dinámica), delegando al módulo mobile-reverse del repositorio reverse-skill.
  Úsalo cuando la tarea sea analizar un IPA, inspeccionar binarios Mach-O de una
  app, instrumentar con Objection/Frida, revisar con MobSF, o localizar lógica
  de login/cifrado/jailbreak-detection en una app iOS. Dispara con: "iOS",
  "IPA", "app de iPhone", "Mach-O", "Objection", "MobSF", "Frida en iOS",
  "jailbreak detection", "reverse de app iOS". Solo sobre apps propias o con
  autorización, en dispositivos/entornos autorizados.
---

# reverse-skill-ios · Inversa de iOS / móvil Apple

Atajo al módulo `skills/mobile-reverse/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar autorización: la app es propia o muestra autorizada, y la
   instrumentación dinámica corre en un dispositivo/entorno bajo alcance.
2. `NOW` — Abrir `skills/mobile-reverse/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales (Objection, Frida,
   MobSF, utilidades Mach-O). Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar el workflow.

## Enfoque

1. **Triage del IPA** — estructura, `Info.plist`, entitlements, frameworks
   embebidos, binario principal (Mach-O) y si está cifrado (FairPlay).
2. **Estático** — analizar el Mach-O; para profundizar pivotar a
   `reverse-skill-binary` (`macos-reverse/` para Mach-O). Buscar login, cripto,
   pinning, detección de jailbreak.
3. **Dinámico** — Objection/Frida para observar métodos, bypass de pinning o de
   jailbreak-detection, dentro del alcance.
4. **Revisión** — MobSF para un pase automatizado de hallazgos.

## Salida esperada

Entry points y clases/funciones clave; dónde vive la lógica sensible (login,
cripto, pinning, anti-jailbreak); qué se instrumentó o hookeó, reproducible.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
