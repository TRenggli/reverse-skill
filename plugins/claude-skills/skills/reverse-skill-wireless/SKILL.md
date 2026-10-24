---
name: reverse-skill-wireless
description: >-
  Seguridad inalámbrica y de radio: Wi-Fi y RF/SDR, delegando a los módulos
  wifi-wireless y radio-sdr del repositorio reverse-skill. Úsalo cuando la tarea
  sea evaluar una red Wi-Fi propia (captura de handshake, auditoría WPA,
  rogue AP), o analizar señales de radio con SDR (demodulación, inspección de
  espectro, reversing de protocolos RF). Dispara con: "Wi-Fi", "WiFi", "WPA",
  "handshake", "aircrack", "deauth", "rogue AP", "SDR", "RTL-SDR", "GNU Radio",
  "señal de radio", "RF", "espectro". Solo sobre redes/dispositivos propios o
  con autorización y bandas permitidas.
---

# reverse-skill-wireless · Wi-Fi + RF / SDR

Atajo a los módulos `skills/wifi-wireless/` y `skills/radio-sdr/` del repo
`reverse-skill` (raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está
ahí, preguntar).

## Ámbito y legalidad

Solo redes/dispositivos **propios o con autorización**. Respetar las bandas y
potencias permitidas por la regulación local; captura/transmisión de RF puede
estar regulada. No interferir ni capturar tráfico ajeno sin permiso.

## ACTION REQUIRED

1. `NOW` — Confirmar autorización y que la operación es legal en tu jurisdicción.
2. `NOW` — Elegir submódulo: Wi-Fi → `skills/wifi-wireless/SKILL.md`; RF/SDR →
   `skills/radio-sdr/SKILL.md`. Seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales (suite Wi-Fi, SDR).
   Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar el workflow del submódulo.

## Enfoque

- **Wi-Fi** — descubrimiento de APs/clientes, captura de handshake, auditoría
  WPA(2/3), detección de rogue/evil-twin; todo en tu propia red.
- **RF / SDR** — inspección de espectro, demodulación, decodificación de
  protocolos de radio; para VMs/formatos, cruzar con `reverse-skill-protocol`.

## Salida esperada

Hallazgos de la red/señal con evidencia reproducible; recomendaciones.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
