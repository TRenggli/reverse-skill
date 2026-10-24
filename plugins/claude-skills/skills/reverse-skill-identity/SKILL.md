---
name: reverse-skill-identity
description: >-
  Seguridad de identidad federada y SSO (SAML, OIDC/OAuth), delegando al módulo
  identity-federation del repositorio reverse-skill. Úsalo cuando la tarea sea
  analizar un flujo de inicio de sesión federado, revisar aserciones SAML o
  tokens OIDC, buscar fallas en validación de firma/audiencia/redirect, o
  evaluar un IdP/SP propio o autorizado. Dispara con: "SAML", "OIDC",
  "OAuth", "SSO", "federación de identidad", "IdP", "assertion SAML",
  "id_token", "redirect_uri", "single sign-on". Solo sobre sistemas propios o
  con autorización.
---

# reverse-skill-identity · Identidad federada (SAML / OIDC / SSO)

Atajo al módulo `skills/identity-federation/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar autorización sobre el IdP/SP/flujo objetivo.
2. `NOW` — Abrir `skills/identity-federation/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar el análisis del flujo.

## Enfoque

1. **Mapa del flujo** — SAML (Request/Response, metadata) u OIDC/OAuth
   (authorization code, tokens, scopes), roles de IdP y SP.
2. **Validación** — firma de aserción/token, audiencia, issuer, expiración,
   `redirect_uri`, replay; confusiones de algoritmo.
3. **Abusos típicos** — manipulación de aserciones, open redirect en el flujo,
   mezcla de cuentas; todo dentro del alcance.
4. **Verificación** — PoC reproducible; alta severidad → avisar de inmediato.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
