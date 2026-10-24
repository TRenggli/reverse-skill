---
name: reverse-skill-dsl-vm
description: >-
  Ingeniería inversa de máquinas virtuales de opcodes personalizadas / DSL VM
  (intérpretes y protecciones basadas en VM, típicamente en JS), delegando al
  submódulo dsl-vm-reverse del repositorio reverse-skill. Úsalo cuando la tarea
  sea entender un intérprete de bytecode propietario, una protección tipo VM
  (virtualización de código), o reconstruir el set de opcodes y el handler loop
  de una VM embebida. Dispara con: "VM de opcodes", "DSL VM", "virtualización de
  código", "intérprete de bytecode", "custom VM", "opcode handler", "fireye",
  "protección VM". Solo sobre código propio o muestras autorizadas.
---

# reverse-skill-dsl-vm · Inversa de VM de opcodes / DSL VM

Atajo al submódulo `skills/reverse-engineering/dsl-vm-reverse/` del repo
`reverse-skill` (raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está
ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que el objetivo es propio o muestra autorizada (análisis
   estático/dinámico en entorno controlado).
2. `NOW` — Abrir `skills/reverse-engineering/dsl-vm-reverse/SKILL.md` del repo y
   seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales. Falta algo →
   divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar el workflow.

## Enfoque

1. **Localizar la VM** — el dispatcher/handler loop y la tabla de opcodes;
   distinguir bytecode de datos.
2. **Mapear opcodes** — inferir qué hace cada handler (stack/registros, saltos,
   aritmética, llamadas nativas).
3. **Desvirtualizar** — reconstruir la lógica original o un disassembler del
   bytecode; para JS de frontend, cruzar con `reverse-skill-js`.
4. **Síntesis** — especificación de la VM (opcodes + semántica) y el programa
   recuperado.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
