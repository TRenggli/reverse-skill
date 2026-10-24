---
name: reverse-skill-pwn
description: >-
  Desarrollo de exploits de binario para CTF / entornos autorizados (pwn),
  delegando al módulo pwn-chain del repositorio reverse-skill. Úsalo cuando la
  tarea sea resolver un reto de pwn, analizar stack/heap overflow, construir
  ROP, ret2libc, bypass de mitigaciones ( ASLR, NX, canary, PIE), pwn de kernel,
  o automatizar la interacción con pwntools frente a un binario de reto.
  Dispara con: "pwn", "exploit de binario", "stack overflow", "heap overflow",
  "ROP", "ret2libc", "pwntools", "GEF", "pwndbg", "kernel pwn", "canary", "PIE".
  Solo en CTF, laboratorios propios o alcance autorizado.
---

# reverse-skill-pwn · Pwn / desarrollo de exploits (CTF autorizado)

Atajo al módulo `skills/pwn-chain/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## Ámbito

Pensado para **CTF, laboratorios propios y objetivos con autorización
explícita**. No es para producir armas contra sistemas de terceros. Si el
objetivo no es un reto/lab autorizado, parar y pedir el alcance.

## ACTION REQUIRED

1. `NOW` — Confirmar contexto autorizado (CTF / lab / alcance propio).
2. `NOW` — Abrir `skills/pwn-chain/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para `pwntools`, depuradores (GEF/pwndbg)
   y utilidades. Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar el workflow contra el binario del reto.

## Enfoque habitual en un reto

1. **Recon del binario** — `checksec` (NX, canary, PIE, RELRO), arquitectura,
   libc. Para entender la lógica, apoyarse en `reverse-skill-binary`.
2. **Encontrar el primitivo** — identificar la vulnerabilidad (overflow, UAF,
   fmt string, etc.) y qué control da (de ejecución / de escritura).
3. **Construir la cadena** — según mitigaciones: leak para derrotar ASLR/PIE,
   ROP/ret2libc, etc., automatizado con `pwntools`.
4. **Estabilizar y capturar la flag** — local primero, luego remoto del reto;
   dejar el script de exploit reproducible.

## Salida esperada

Resumen de mitigaciones y del primitivo; el script de exploit (pwntools)
reproducible; la flag o el resultado, con notas de offsets/gadgets usados.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
