---
name: reverse-skill-firmware
description: >-
  Análisis de firmware e IoT / sistemas embebidos, delegando al módulo
  firmware-pentest del repositorio reverse-skill. Úsalo cuando la tarea sea
  extraer y analizar una imagen de firmware, desempacar sistemas de archivos
  (squashfs/jffs2), identificar binarios y servicios embebidos, buscar
  credenciales o claves embebidas, o analizar un dispositivo IoT propio.
  Dispara con: "firmware", "IoT", "embebido", "binwalk", "unblob", "squashfs",
  "EMBA", "imagen de firmware", "extraer firmware", "dispositivo IoT", "UART",
  "JTAG". Solo sobre firmware/dispositivos propios o con autorización.
---

# reverse-skill-firmware · Firmware / IoT / embebidos

Atajo al módulo `skills/firmware-pentest/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que el firmware o dispositivo es propio o autorizado. El
   análisis de una imagen offline autorizada es solo lectura.
2. `NOW` — Abrir `skills/firmware-pentest/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales (binwalk, unblob,
   utilidades de FS). Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar extracción → mapeo → análisis.

## Enfoque

1. **Extracción** — `binwalk`/`unblob` para identificar y extraer el/los
   sistemas de archivos (squashfs, jffs2, cramfs, ubifs) y blobs.
2. **Mapeo** — layout de la imagen, particiones, kernel/bootloader, servicios de
   init, binarios de usuario.
3. **Búsqueda** — credenciales/claves/certificados embebidos, configuraciones,
   endpoints, binarios setuid o servicios de red.
4. **Análisis de binarios** — para los binarios clave pivotar a
   `reverse-skill-binary` (ELF/arquitectura embebida). Hardware (UART/JTAG) →
   `skills/hardware-security/` vía router.

## Salida esperada

Layout de la imagen y FS extraídos; binarios/servicios relevantes; secretos o
configuraciones encontrados; cadena Evidencia→Hallazgo→Ruta reproducible.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
