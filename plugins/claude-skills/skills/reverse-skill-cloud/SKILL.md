---
name: reverse-skill-cloud
description: >-
  Seguridad de cloud, contenedores y Kubernetes, delegando al módulo cloud-k8s
  del repositorio reverse-skill. Úsalo cuando la tarea sea auditar
  configuraciones de AWS/Azure/GCP, revisar manifiestos o RBAC de Kubernetes,
  analizar imágenes de contenedor, rutas de escalada en la nube, o IAM/políticas
  en un entorno propio o autorizado. Dispara con: "cloud", "nube", "AWS",
  "Azure", "GCP", "Kubernetes", "K8s", "contenedor", "Docker", "RBAC", "IAM",
  "escalada en la nube". Solo sobre entornos propios o con autorización.
---

# reverse-skill-cloud · Cloud / contenedores / Kubernetes

Atajo al módulo `skills/cloud-k8s/` del repo `reverse-skill`
(raíz por defecto `C:\Users\jmbud\reverse-skill`; si no está ahí, preguntar).

## ACTION REQUIRED

1. `NOW` — Confirmar autorización sobre la cuenta/cluster/entorno objetivo.
   Enumerar o tocar recursos cloud ajenos sin permiso está fuera de alcance.
2. `NOW` — Abrir `skills/cloud-k8s/SKILL.md` del repo y seguir su flujo.
3. `NEXT` — Leer `skills/tool-index.md` para rutas reales de herramientas.
   Falta algo → divulgar bootstrap y pedir aprobación.
4. `ACT` — Ejecutar enumeración → revisión de config → rutas de escalada.

## Enfoque

1. **Inventario** — cuentas/suscripciones/proyectos, roles IAM, recursos
   expuestos; en K8s: namespaces, RBAC, service accounts, secrets.
2. **Config review** — políticas permisivas, buckets/almacenamiento público,
   metadata endpoints, imágenes de contenedor con secretos.
3. **Escalada** — rutas de privilegio en IAM/RBAC; dentro del alcance.
4. **Síntesis** — cadena Evidencia→Hallazgo→Ruta con comandos reproducibles.

Para el flujo completo con puertas y checklist, usar primero el router
`reverse-skill`.
