---
name: reverse-skill
description: >-
  Router maestro de ciberseguridad para ingeniería inversa, CTF y pentest
  AUTORIZADO que delega al repositorio local reverse-skill. Úsalo cuando la
  tarea involucre análisis de APK/Android, binarios (ELF/PE/.so/.dll con IDA,
  radare2, Ghidra o Binary Ninja), JS de frontend / parámetros cifrados /
  firmas, captura y replay HTTP, CTF / pwn / desarrollo de exploits, pentest
  autorizado (nmap, nuclei, sqlmap, Burp), malware / YARA, firmware / IoT,
  seguridad de LLM y agentes, forense digital, o generación de reportes de
  seguridad. Enruta la tarea al skill correcto del repo y hace cumplir la puerta
  de activación/consentimiento (leer el repo es solo lectura; se requiere
  aprobación explícita antes de ejecutar cualquier script) y la puerta dura de
  autorización de objetivo. Dispara con: "ingeniería inversa", "reverse",
  "descompilar", "APK", "binario", "CTF", "pwn", "exploit", "pentest",
  "escaneo", "malware", "Frida", "IDA", "radare2", "Ghidra", "jadx".
---

# reverse-skill · Router de ciberseguridad (RE / CTF / pentest autorizado)

Esta skill es el **punto de entrada** a mi toolkit local `reverse-skill`, un
router de metodologías para ingeniería inversa, CTF y pruebas de seguridad
**autorizadas**. No ejecuta ataques por sí misma: enruta la tarea al módulo
correcto del repo, aplica las puertas de seguridad y me recuerda usar
herramientas reales (nunca adivinar rutas).

- **Raíz del repo (por defecto):** `C:\Users\jmbud\reverse-skill`
  Si no existe ahí, preguntar al usuario dónde lo clonó antes de continuar.
- **Fuente de verdad de comportamiento:** `RULES.md` del repo.
- **Fuente de verdad de routing:** `skills/config/routing.json` (ladder legible
  en `skills/MASTER-ROUTING.md`).

## ACTION REQUIRED (ejecutar al leer esto)

1. `NOW` — Confirmar que la tarea cae en el ámbito de seguridad/RE/pentest/CTF.
   Si no, no usar esta skill.
2. `NOW` — **Puerta de consentimiento.** Leer archivos del repo es *solo
   lectura*; NO autoriza ejecutar nada. Antes del primer efecto colateral
   (correr un script, descargar, instalar, arrancar un servicio, tocar la red,
   cambiar configuración) hay que **divulgar el comando exacto y sus efectos y
   obtener un "sí" explícito del usuario**.
3. `NOW` — **Puerta dura de autorización de objetivo.** Mencionar un objetivo
   (URL, IP, app, muestra) NO es permiso. Para cualquier acción sobre un
   objetivo hace falta autorización explícita (sistema propio, SRC/Bug Bounty
   con alcance, CTF, o muestra offline autorizada). Ningún `-Force`/`--force`
   salta esta puerta.
4. `NEXT` — Enrutar: leer `skills/MASTER-ROUTING.md` y elegir el PRIMARY según
   el ladder. Para análisis automático puedo (tras aprobación) correr el router
   nativo del repo.
5. `NEXT` — Leer `skills/tool-index.md` del repo para rutas reales de
   herramientas. Si falta, generarlo con el refresh del repo (acción divulgada
   y aprobada). **Nunca adivinar rutas de herramientas.**
6. `ACT` — Abrir el `SKILL.md` del módulo PRIMARY y seguir su ACTION REQUIRED.

## Cómo enruta (ladder resumido)

| Si la tarea es… | PRIMARY en el repo | Skill de atajo |
|---|---|---|
| APK / Android / smali / jadx / apktool / Frida | `skills/apk-reverse/` | `reverse-skill-apk` |
| Binario nativo (ELF/PE/.so/.dll) / IDA / radare2 / Ghidra / Binary Ninja | `skills/ida-reverse/`, `radare2/`, `ghidra-reverse/`, `binary-ninja-reverse/`, `reverse-engineering/` | `reverse-skill-binary` |
| JS de frontend / parámetros cifrados / firmas / CDP / SourceMap | `skills/js-reverse/` | `reverse-skill-js` |
| pwn / ROP / stack-heap / pwntools (CTF) | `skills/pwn-chain/` | `reverse-skill-pwn` |
| CTF / AWD / retos de competencia | `skills/ctf-sandbox/` → `CTF-Sandbox-Orchestrator/` | `reverse-skill-ctf` |
| Pentest autorizado / nmap / nuclei / sqlmap / Burp / SRC | `skills/pentest-tools/`, `attack-chain/` | `reverse-skill-pentest` |
| Malware / YARA / sandbox | `skills/malware-analysis/` | — (usar router) |
| iOS / Mach-O / macOS | `skills/mobile-reverse/`, `macos-reverse/` | — |
| .NET / dnSpy / de4dot | `skills/dotnet-reverse/` | — |
| Firmware / IoT / binwalk | `skills/firmware-pentest/` | — |
| API / GraphQL / JWT | `skills/api-security/` | — |
| Seguridad de LLM / prompt injection / agentes | `skills/llm-security/` | — |
| Forense / timeline / memoria | `skills/digital-forensics/` | — |
| Reporte / writeup / diagrama | `skills/docs-generator/`, `diagram-generator/` | — |
| Otro / inversa genérica / binario desconocido | `skills/reverse-engineering/` | `reverse-skill-binary` |

Si nada encaja con fuerza, PRIMARY = `skills/reverse-engineering/` y abrir
`skills/routing.md` (matriz ampliada, es un apéndice, no un segundo router).

## Principios que debo respetar (de RULES.md)

- **Solo lectura hasta activar.** Resumir/revisar el repo no ejecuta nada.
- **Autorización de objetivo es puerta aparte** y dura.
- **Rutas de herramientas** salen de `tool-index.md`, nunca se adivinan.
- **Herramienta faltante** → divulgar el bootstrap exacto y pedir aprobación;
  no reintentar un auto-install más de 2 veces.
- **No expandir el alcance** más allá de lo que el usuario autorizó.
- **Reportar avance**, no quedarse en silencio; conclusiones con cadena
  Evidencia→Hallazgo→Ruta y comandos reproducibles.
- Al terminar: reporte formal + al menos un diagrama + checklist de RULES.md.

## Archivos clave del repo

- `RULES.md` — cadena de comportamiento y puertas (leer primero).
- `skills/MASTER-ROUTING.md` — ladder PRIMARY.
- `skills/routing.md` — matriz ampliada (solo si hay ambigüedad).
- `skills/tool-index.md` — estado real de herramientas locales.
- `skills/ops/` — contratos de scope, evidencia, roles, timeline.
- `README_AI.md` — secuencia de bootstrap para agentes.

> Ámbito legal: solo para investigación de seguridad, educación, CTF y pruebas
> sobre sistemas propios o con autorización explícita.
