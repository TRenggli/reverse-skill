---
name: reverse-skill-dotnet
description: >-
  Ingeniería inversa de .NET / C# (ensamblados managed, IL, metadatos),
  delegando al módulo dotnet-reverse del repositorio reverse-skill. Úsalo cuando
  la tarea sea descompilar un .exe o .dll de .NET, leer o editar IL, quitar
  ofuscación (ConfuserEx, .NET Reactor, SmartAssembly) con de4dot, o analizar la
  lógica de una app managed. Dispara con: ".NET", "C# reverse", "dnSpy",
  "dnSpyEx", "de4dot", "ConfuserEx", ".NET Reactor", "SmartAssembly", "IL",
  "ensamblado managed", "descompilar dll de .NET". Solo sobre binarios propios o
  muestras autorizadas.
---

# reverse-skill-dotnet · Inversa de .NET / C#

Atajo al módulo `skills/dotnet-reverse/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar que el binario es propio o muestra autorizada. El análisis
   estático de un ensamblado autorizado es solo lectura.
2. `NOW` — Abrir `skills/dotnet-reverse/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales (dnSpyEx, de4dot,
   dnlib). Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar el workflow.

## Enfoque

1. **Identificar protección** — detectar si está ofuscado y con qué
   (ConfuserEx, .NET Reactor, SmartAssembly). El ancla equivalente a imports es
   el resumen de IL/metadatos.
2. **Desofuscar** — `de4dot` para limpiar nombres y control de flujo cuando el
   packer es soportado.
3. **Descompilar / leer** — con dnSpyEx (o equivalente) leer la lógica managed;
   anotar clases, métodos y llamadas relevantes.
4. **Editar IL (si aplica)** — parchear a nivel IL con dnlib/dnSpy para
   validación, dentro del alcance autorizado.

## Salida esperada

Protección detectada; lógica managed clave con clases/métodos; qué se
desofuscó o parcheó, con pasos reproducibles.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
