---
name: reverse-skill-protocol
description: >-
  Ingeniería inversa de protocolos de red y formatos de mensaje (Protobuf,
  binarios propietarios, análisis de PCAP a nivel de protocolo), delegando al
  módulo protocol-reverse del repositorio reverse-skill. Úsalo cuando la tarea
  sea entender un protocolo propietario, decodificar mensajes Protobuf, inferir
  la estructura de un formato binario, o reconstruir un protocolo a partir de
  capturas. Dispara con: "protocolo", "protocol reverse", "Protobuf",
  "formato binario", "PCAP de protocolo", "mensaje propietario", "decodificar
  protocolo", "estructura de paquete". Solo sobre tráfico/muestras propios o
  autorizados.
---

# reverse-skill-protocol · Inversa de protocolos / formatos

Atajo al módulo `skills/protocol-reverse/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que las capturas/muestras son propias o autorizadas.
2. `NOW` — Abrir `skills/protocol-reverse/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar recolección → inferencia de estructura → validación.

## Enfoque

1. **Recolección** — capturas (PCAP) o muestras de mensajes; identificar
   transporte y framing.
2. **Inferencia** — campos, tipos, longitudes, endianness; Protobuf → recuperar
   el esquema a partir de los bytes; diferenciar cabecera/cuerpo.
3. **Validación** — reconstruir/parsear mensajes y comprobar contra nuevas
   muestras; si el protocolo nace en una app, cruzar con
   `reverse-skill-binary`/`-apk`.
4. **Síntesis** — especificación del protocolo/formato y un parser reproducible.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
