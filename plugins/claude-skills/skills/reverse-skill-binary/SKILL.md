---
name: reverse-skill-binary
description: >-
  Ingeniería inversa de binarios nativos (ELF, PE/EXE/DLL, .so, Mach-O),
  delegando a los módulos de binario del repositorio reverse-skill
  (reverse-engineering, ida-reverse, radare2, ghidra-reverse,
  binary-ninja-reverse). Úsalo cuando la tarea sea desensamblar o descompilar un
  binario, recuperar lógica/algoritmos, analizar un .so, triage de un ejecutable
  desconocido, anti-debug u ofuscación (p. ej. OLLVM), o recuperar símbolos.
  Enruta al desensamblador correcto según lo instalado en el tool-index.
  Dispara con: "binario", "ELF", "EXE", "DLL", ".so", "Mach-O", "desensamblar",
  "descompilar binario", "IDA", "radare2", "r2", "Ghidra", "Binary Ninja",
  "ingeniería inversa", "OLLVM", "recuperar símbolos". Solo sobre binarios
  propios o muestras autorizadas.
---

# reverse-skill-binary · Inversa de binarios nativos

Atajo a los módulos de binario del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que el binario es propio o una muestra autorizada
   (offline). El análisis estático de una muestra autorizada es solo lectura.
2. `NOW` — Elegir PRIMARY según `skills/MASTER-ROUTING.md`:
   - IDA / descompilación profunda → `skills/ida-reverse/`
   - radare2 / r2 / triage rápido → `skills/radare2/`
   - Ghidra / descompilador abierto → `skills/ghidra-reverse/`
   - Binary Ninja / HLIL / MLIL / Binja MCP → `skills/binary-ninja-reverse/`
   - Go / Rust → `skills/go-rust-reverse/` · macOS/Mach-O → `skills/macos-reverse/`
   - Genérico / anti-debug / OLLVM / desconocido → `skills/reverse-engineering/`
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales; no adivinar. Falta
   una herramienta → divulgar bootstrap del repo y pedir aprobación.
4. `ACT` — Abrir el `SKILL.md` del PRIMARY y ejecutar su ACTION REQUIRED.

## Metodología (triage → estático → dinámico → síntesis)

1. **Triage** — identificar formato, arquitectura, empaquetado/protección,
   imports/exports y strings. En PE: tabla de imports (IAT) como ancla; si está
   empaquetado o ilegible, declarar el bloqueo y recomendar orden (desempacar /
   reparar IAT, o pasar a dinámico) — no sacar conclusiones de una IAT basura.
2. **Estático** — desensamblar/descompilar; anotar **direcciones, offsets y
   nombres de funciones** (no "alguna función").
3. **Dinámico** — cuando el estático se bloquea: breakpoints en APIs, trazado,
   observación de memoria (dentro del alcance).
4. **Síntesis** — cadena Evidencia→Hallazgo→Ruta con comandos reproducibles.

Si un camino se bloquea, cambiar: estático↔dinámico, IDA↔r2↔Ghidra. OLLVM y
otros desofuscados: ver `skills/reverse-engineering/references/`.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
