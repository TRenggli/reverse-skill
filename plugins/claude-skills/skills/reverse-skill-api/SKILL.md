---
name: reverse-skill-api
description: >-
  Seguridad de APIs (REST / GraphQL), incluyendo ataques a JWT y fallas de
  autorización (BOLA/IDOR), delegando al módulo api-security del repositorio
  reverse-skill. Úsalo cuando la tarea sea probar endpoints de API, enumerar un
  esquema GraphQL, analizar o manipular tokens JWT, o buscar fallas de
  autorización a nivel de objeto/función en un objetivo autorizado. Dispara con:
  "API security", "seguridad de API", "GraphQL", "JWT", "token JWT", "BOLA",
  "IDOR", "endpoints de API", "autorización rota", "REST". Solo sobre APIs
  propias o con autorización (SRC/Bug Bounty en alcance).
---

# reverse-skill-api · Seguridad de APIs (REST / GraphQL)

Atajo al módulo `skills/api-security/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar autorización sobre la API objetivo (propia o SRC/Bug Bounty
   en alcance). Mencionar el host no es permiso.
2. `NOW` — Abrir `skills/api-security/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales (clientes HTTP, Burp,
   herramientas GraphQL). Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar enumeración → pruebas de autorización → verificación.

## Enfoque

1. **Mapa de superficie** — endpoints, métodos, esquema (GraphQL introspection
   si está disponible), autenticación.
2. **JWT** — inspeccionar claims, `alg`, firma; probar confusiones de algoritmo
   y validación débil (dentro del alcance).
3. **Autorización** — BOLA/IDOR a nivel de objeto, autorización de función,
   acceso horizontal/vertical.
4. **Verificación** — PoC reproducible (curl/script); alta severidad → avisar al
   usuario de inmediato.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
