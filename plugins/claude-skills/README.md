# Adaptador de skills para Claude Code

Colección de **Agent Skills de Claude Code** (en español) que enrutan hacia los
módulos de este repositorio `reverse-skill`. Son adaptadores finos: no duplican
la metodología, apuntan a los `SKILL.md`, scripts y `tool-index.md` del repo, y
preservan las puertas de seguridad de `RULES.md` (leer ≠ ejecutar; autorización
de objetivo como puerta dura).

Mismo patrón que el adaptador de Codex en [`../reverse-skill/`](../reverse-skill/),
pero en el formato nativo de Claude Code (`<name>/SKILL.md` con frontmatter
`name` + `description`).

> Ámbito: solo investigación de seguridad, educación, CTF y pruebas sobre
> sistemas propios o con autorización explícita.

## Contenido

- `skills/reverse-skill/` — **router maestro**. Punto de entrada: aplica las
  puertas de activación/consentimiento y autorización, y enruta al módulo
  correcto del repo.
- `skills/reverse-skill-<escenario>/` — 37 atajos por escenario (apk, binary,
  js, pwn, ctf, pentest, malware, firmware, dotnet, ios, forensics, llm, cloud,
  api, windows-ad, identity, database, code-audit, supply-chain, patch-diff,
  binary-diff, protocol, go-rust, macos, dsl-vm, browser-ext, thick-client,
  edr-bypass, threat-hunting, threat-intel, email, wireless, hardware, ot-ics,
  browser-automation, case-review, report).

Cada atajo declara disparadores en su `description` para que Claude lo descubra
e invoque automáticamente cuando la tarea lo amerite.

> Nota: las descripciones referencian la raíz del repo como
> `C:\Users\jmbud\reverse-skill`. En otra máquina o ruta, ajustar esa ruta (o
> pedírsela al usuario) antes de usarlas.

## Instalación

Claude Code descubre skills en dos lugares:

- **Global (todas las sesiones):** copiar las carpetas de `skills/` a
  `~/.claude/skills/` (en Windows, `%USERPROFILE%\.claude\skills\`).

  ```bash
  # macOS / Linux
  cp -r plugins/claude-skills/skills/* ~/.claude/skills/
  ```

  ```powershell
  # Windows (PowerShell)
  Copy-Item -Recurse plugins\claude-skills\skills\* $env:USERPROFILE\.claude\skills\
  ```

- **Por proyecto:** copiar a `.claude/skills/` dentro del proyecto donde se
  quieran usar (ese `.claude/` suele estar en `.gitignore`).

Tras copiarlas, Claude Code las lista automáticamente; el router `reverse-skill`
es el que conviene invocar primero para respetar la cadena de `RULES.md`.
