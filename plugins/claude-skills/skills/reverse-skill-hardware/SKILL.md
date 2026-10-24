---
name: reverse-skill-hardware
description: >-
  Seguridad de hardware e interfaces de depuración embebidas (UART, JTAG, SWD,
  SPI/I2C, volcado de flash), delegando al módulo hardware-security del
  repositorio reverse-skill. Úsalo cuando la tarea sea identificar y usar puertos
  de depuración de una placa propia, volcar memoria/flash, interactuar con buses,
  o preparar firmware extraído para análisis. Dispara con: "hardware", "UART",
  "JTAG", "SWD", "SPI", "I2C", "volcar flash", "dump de memoria", "puerto de
  depuración", "placa embebida", "chip de flash". Solo sobre hardware propio o
  con autorización.
---

# reverse-skill-hardware · Seguridad de hardware / depuración embebida

Atajo al módulo `skills/hardware-security/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que el dispositivo/placa es propio o autorizado.
2. `NOW` — Abrir `skills/hardware-security/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar identificación → acceso → volcado → análisis.

## Enfoque

1. **Identificar interfaces** — UART/JTAG/SWD, pines de bus (SPI/I2C), chip de
   flash; mapear el PCB.
2. **Acceder** — consola UART, debug JTAG/SWD; precauciones eléctricas.
3. **Volcar** — extraer flash/memoria; obtener la imagen de firmware.
4. **Pivotar** — el firmware extraído → `reverse-skill-firmware`; binarios
   concretos → `reverse-skill-binary`.

## Salida esperada

Interfaces identificadas, imagen/volcado obtenido, y hallazgos, reproducibles.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
