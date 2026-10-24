---
name: reverse-skill-llm
description: >-
  Pruebas de seguridad de LLM y agentes de IA (prompt injection, jailbreak,
  abuso de herramientas, envenenamiento de memoria, seguridad de skills/MCP),
  delegando al módulo llm-security del repositorio reverse-skill. Úsalo cuando
  la tarea sea evaluar la robustez de un sistema con LLM, probar OWASP LLM
  Top 10 / Agentic AI, auditar una skill o servidor MCP por cadena de
  suministro maliciosa, o usar frameworks como garak/PyRIT/promptfoo sobre un
  sistema propio o autorizado. Dispara con: "seguridad de LLM", "prompt
  injection", "jailbreak", "seguridad de agentes", "tool abuse", "memory
  poisoning", "OWASP LLM Top 10", "garak", "PyRIT", "promptfoo", "skill
  maliciosa", "MCP supply chain". Solo sobre sistemas propios o autorizados.
---

# reverse-skill-llm · Seguridad de LLM / agentes de IA

Atajo al módulo `skills/llm-security/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar autorización sobre el sistema LLM/agente objetivo (propio o
   con alcance). Probar sistemas de terceros requiere permiso explícito.
2. `NOW` — Abrir `skills/llm-security/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales (garak, PyRIT,
   promptfoo). Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar la evaluación.

## Enfoque

1. **Modelo de amenaza** — mapear superficie contra OWASP LLM Top 10 y riesgos
   Agentic AI (tool abuse, memory poisoning, exfiltración vía herramientas).
2. **Prompt injection / jailbreak** — directa e indirecta (contenido que el
   agente lee); medir si se saltan instrucciones/políticas.
3. **Agentes y herramientas** — abuso de herramientas, escalada vía acciones,
   fugas de datos; límites de autorización.
4. **Cadena de suministro de skills/MCP** — auditar skills o servidores MCP de
   terceros (código, permisos, red) según `skills/ops/skill-supply-chain.md`
   antes de confiar en ellos.

## Salida esperada

Hallazgos con severidad y PoC reproducible (prompts/trazas); recomendaciones de
mitigación; reporte. Conclusiones inciertas marcadas con nivel de confianza.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
