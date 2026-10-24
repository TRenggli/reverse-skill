---
name: reverse-skill-email
description: >-
  Análisis de correo y phishing (cabeceras, autenticación, adjuntos y enlaces),
  delegando al módulo email-security del repositorio reverse-skill. Úsalo cuando
  la tarea sea analizar un correo sospechoso, revisar cabeceras y SPF/DKIM/DMARC,
  examinar adjuntos o URLs de un mensaje, o triage de un reporte de phishing en
  un buzón propio o autorizado. Dispara con: "phishing", "correo sospechoso",
  "análisis de email", "cabeceras de correo", "SPF", "DKIM", "DMARC", "adjunto
  malicioso", "URL de phishing", "triage de phishing". Solo sobre correos
  propios o autorizados.
---

# reverse-skill-email · Análisis de correo / phishing

Atajo al módulo `skills/email-security/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## Ámbito y seguridad

Analizar el correo como **evidencia**: no abrir enlaces en vivo ni detonar
adjuntos fuera de un entorno aislado autorizado. Solo buzones/muestras propias o
autorizadas.

## ACTION REQUIRED

1. `NOW` — Confirmar que el correo es propio o autorizado.
2. `NOW` — Abrir `skills/email-security/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar cabeceras → autenticación → adjuntos/URLs → veredicto.

## Enfoque

1. **Cabeceras** — ruta (Received), remitente real vs mostrado, Reply-To,
   anomalías.
2. **Autenticación** — SPF, DKIM, DMARC y alineación; indicadores de spoofing.
3. **Carga** — URLs (desofuscar sin visitar en vivo), adjuntos (hash, tipo; si
   es ejecutable/doc con macro → `reverse-skill-malware` en sandbox).
4. **Veredicto** — phishing/benigno con IOCs y evidencia; recomendaciones.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
