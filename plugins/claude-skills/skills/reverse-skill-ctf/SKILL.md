---
name: reverse-skill-ctf
description: >-
  Orquestación de retos de CTF (Capture The Flag) y AWD, delegando al módulo
  ctf-sandbox del repositorio reverse-skill y a su CTF-Sandbox-Orchestrator.
  Úsalo cuando la tarea sea resolver o coordinar un reto de competencia de
  cualquier categoría (web, pwn, reversing, crypto, forense, stego, misc,
  móvil, nube, etc.), clasificar un reto hacia la metodología correcta, o
  gestionar varios retos a la vez. Dispara con: "CTF", "reto", "challenge",
  "AWD", "capture the flag", "flag", "writeup de reto", "competencia de
  seguridad". Entorno de competencia o laboratorio; no toca sistemas de
  terceros fuera del CTF.
---

# reverse-skill-ctf · Orquestador de CTF / AWD

Atajo al módulo `skills/ctf-sandbox/` del repo `reverse-skill`, que a su vez usa
`CTF-Sandbox-Orchestrator/` (una colección de sub-skills por categoría).
Raíz por defecto `C:\Users\jmbud\reverse-skill` (si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que es un CTF/lab (el alcance es la propia competencia).
2. `NOW` — Abrir `skills/ctf-sandbox/SKILL.md` del repo; es el único punto de
   entrada (no desplegar los ~40 sub-skills a mano).
3. `NEXT` — Clasificar el reto por categoría y dejar que el orquestador enrute a
   la metodología correspondiente en `CTF-Sandbox-Orchestrator/`.
4. `ACT` — Ejecutar la metodología de la categoría; registrar evidencia.

## Categorías y pivotes

- **reversing / binario** → `reverse-skill-binary`
- **pwn / exploit** → `reverse-skill-pwn`
- **web** → `skills/pentest-tools/`, `api-security/` (vía router)
- **crypto, forense, stego, misc, móvil, nube, etc.** → sub-skill de categoría
  dentro de `CTF-Sandbox-Orchestrator/` (lo elige el orquestador)

## Trabajo con varios retos

Ejecutar secuencialmente por prioridad para evitar conflictos de herramientas;
mantener timeline y work-items por reto; al resolver, dejar un writeup
reproducible (pasos + comandos + flag).

## Salida esperada

Por reto: categoría, vector, pasos reproducibles, y la flag. Opcional: writeup
con `skills/docs-generator/`.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
