---
name: reverse-skill-apk
description: >-
  Ingeniería inversa de APK / Android en CLI, delegando al módulo apk-reverse
  del repositorio reverse-skill. Úsalo cuando la tarea sea analizar un APK,
  descompilar Java, leer o modificar smali, inspeccionar AndroidManifest.xml,
  repackaging, hooking dinámico con Frida, o pivotar a .so nativo dentro de una
  app. Prioriza herramientas ya instaladas (jadx, apktool, frida, adb) según el
  tool-index del repo. Dispara con: "APK", "Android", "descompilar app",
  "smali", "jadx", "apktool", "Frida", "hook", "AndroidManifest", ".so de una
  app", "repackaging". Solo para apps propias o con autorización.
---

# reverse-skill-apk · Inversa de APK / Android (CLI)

Atajo al módulo `skills/apk-reverse/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar autorización: la APK es propia, es muestra autorizada
   offline, o el análisis dinámico corre en un dispositivo/emulador bajo
   alcance. Mencionar la app no es permiso.
2. `NOW` — Abrir `skills/apk-reverse/SKILL.md` del repo y seguir su ACTION
   REQUIRED (es la fuente de verdad del flujo).
3. `NEXT` — Leer `skills/tool-index.md` para las rutas reales de `jadx`,
   `apktool`, `frida`, `adb`. Nunca adivinar rutas. Si falta una herramienta,
   divulgar el bootstrap del repo y pedir aprobación.
4. `ACT` — Ejecutar el workflow, no solo leerlo.

## Flujo (resumen; detalle en el repo)

1. **Triage** — `jadx -d jadx_out app.apk` y `apktool d app.apk -o apktool_out`;
   revisar `AndroidManifest.xml`, package, componentes y `lib/**/*.so`.
   El repo trae `scripts/decode.ps1` para hacerlo en un paso con resumen.
2. **Lógica Java** — leer en `jadx_out` las clases de login, red, cripto,
   control de riesgo, SDKs. Palabras clave: login, sign, encrypt, cipher,
   token, root, certificate, trust, okhttp, retrofit, webview.
3. **Smali / recursos** — cuando jadx queda incompleto o hay que parchear:
   trabajar en `apktool_out`.
4. **Rebuild** — `apktool b apktool_out -o rebuilt.apk`
   (o `scripts/rebuild-sign-install.ps1` para alinear + firmar + instalar).
5. **Hook dinámico (Frida)** — observar/parametrizar métodos Java antes de
   modificar retornos; `scripts/frida-run.ps1` unifica spawn/attach.
6. **Native .so** — si la lógica clave está en `.so`, pivotar a
   `reverse-skill-binary` (IDA/radare2/Ghidra).

## Salida esperada

Componentes de entrada y clases clave; dónde vive la lógica (Java / smali /
`.so`); puntos sensibles confirmados (login, firma, root, SSL, WebView, JNI);
qué se parcheó o qué se hookeó, con comandos reproducibles.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
