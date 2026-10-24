---
name: reverse-skill-go-rust
description: >-
  Ingeniería inversa de binarios Go y Rust, delegando al módulo go-rust-reverse
  del repositorio reverse-skill. Úsalo cuando la tarea sea analizar un binario
  compilado en Go o Rust, recuperar nombres de funciones/tipos stripeados,
  tratar con el runtime y las convenciones de estos lenguajes, o entender su
  lógica. Dispara con: "binario Go", "Golang reverse", "binario Rust", "Rust
  reverse", "stripped Go", "recuperar símbolos Go", "runtime de Go", "panic de
  Rust", "goroutine". Solo sobre binarios propios o muestras autorizadas.
---

# reverse-skill-go-rust · Inversa de binarios Go / Rust

Atajo al módulo `skills/go-rust-reverse/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que el binario es propio o muestra autorizada (estático =
   solo lectura).
2. `NOW` — Abrir `skills/go-rust-reverse/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales de desensamblador y
   ayudantes específicos. Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar el workflow.

## Enfoque

1. **Identificar** — Go vs Rust, versión del compilador, si está stripeado.
2. **Recuperar símbolos** — en Go aprovechar tablas del runtime (pclntab,
   moduledata) para nombres de funciones/tipos; en Rust, demangle de símbolos y
   strings de panic para orientarse.
3. **Lógica** — seguir el flujo teniendo en cuenta goroutines/canales (Go) o el
   manejo de Result/panic (Rust). Apoyarse en `reverse-skill-binary` para el
   desensamblado general.
4. **Síntesis** — funciones clave anotadas con direcciones/nombres recuperados.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
