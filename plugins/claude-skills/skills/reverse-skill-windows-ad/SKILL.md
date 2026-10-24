---
name: reverse-skill-windows-ad
description: >-
  Seguridad de Active Directory y entornos Windows (Kerberos, AD CS, movimiento
  lateral, extracción de credenciales), delegando al módulo windows-ad del
  repositorio reverse-skill. Úsalo cuando la tarea sea mapear un dominio con
  BloodHound, evaluar rutas de ataque de AD, Kerberoasting/AS-REP, abuso de
  AD CS, o movimiento lateral en un laboratorio o entorno autorizado. Dispara
  con: "Active Directory", "AD", "Kerberos", "Kerberoasting", "AS-REP",
  "BloodHound", "AD CS", "movimiento lateral", "DCSync", "Impacket", "Rubeus",
  "dominio Windows". Solo en laboratorios propios o alcance autorizado.
---

# reverse-skill-windows-ad · Active Directory / Windows

Atajo al módulo `skills/windows-ad/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## Ámbito

Pensado para **laboratorios propios, entornos de pruebas y alcances
explícitamente autorizados** (ej. engagement de red team con permiso). No es
para dominios de terceros sin autorización.

## ACTION REQUIRED

1. `NOW` — Confirmar autorización sobre el dominio/entorno (lab o engagement).
2. `NOW` — Correr el gate de scope del repo (`case-init`/`scope.md`) con
   `auth.status=granted` antes de actuar (script del repo → divulgar y aprobar).
3. `NOW` — Abrir `skills/windows-ad/SKILL.md` del repo y seguir su flujo.
4. `NEXT` — Leer `skills/tool-index.md` (BloodHound, Impacket, etc.); no
   adivinar rutas. Falta algo → divulgar bootstrap y pedir aprobación.
5. `ACT` — Ejecutar recon del dominio → análisis de rutas → (acción autorizada).

## Enfoque

1. **Recon del dominio** — recolección con BloodHound; usuarios, grupos, ACLs,
   confianzas, SPNs.
2. **Análisis de rutas** — Kerberoasting/AS-REP, delegaciones, abuso de ACL,
   AD CS (plantillas de certificado vulnerables).
3. **Credenciales / lateral** — solo dentro del alcance autorizado; registrar
   evidencia y avisar hallazgos de alta severidad de inmediato.
4. **Síntesis** — cadena Evidencia→Hallazgo→Ruta, reporte anonimizado.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
