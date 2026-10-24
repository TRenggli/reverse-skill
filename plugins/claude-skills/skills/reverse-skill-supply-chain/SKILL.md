---
name: reverse-skill-supply-chain
description: >-
  Seguridad de la cadena de suministro de software (SBOM, dependencias,
  escaneo de componentes), delegando al módulo supply-chain-security del
  repositorio reverse-skill. Úsalo cuando la tarea sea generar o revisar un
  SBOM, escanear dependencias por CVEs o licencias, detectar paquetes maliciosos
  o typosquatting, o evaluar la integridad de la cadena de build de un proyecto
  propio o autorizado. Dispara con: "SBOM", "cadena de suministro", "supply
  chain", "dependencias", "Trivy", "CVE en dependencias", "paquete malicioso",
  "typosquatting", "escaneo de componentes". Solo sobre proyectos propios o
  con autorización.
---

# reverse-skill-supply-chain · Cadena de suministro / SBOM

Atajo al módulo `skills/supply-chain-security/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que el proyecto/artefacto es propio o autorizado.
2. `NOW` — Abrir `skills/supply-chain-security/SKILL.md` del repo y seguir su
   flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales (Trivy, generadores
   de SBOM). Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar SBOM → escaneo → evaluación de riesgo.

## Enfoque

1. **SBOM** — inventario de componentes/dependencias directas y transitivas.
2. **Escaneo** — CVEs conocidos, versiones vulnerables, licencias problemáticas.
3. **Integridad / maliciosos** — typosquatting, dependencias no fijadas,
   scripts de post-install sospechosos, build no reproducible.
4. **Síntesis** — riesgos priorizados y remediación (fijar/actualizar), con
   evidencia reproducible.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
