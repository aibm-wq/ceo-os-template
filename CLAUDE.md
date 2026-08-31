# {{NOMBRE_EMPRESA}} — Sistema Operativo

> Este archivo se carga en cada sesión de Claude Code que arranca en esta carpeta.
> Es el punto de entrada del sistema.

---

## INSTRUCCIÓN DE ARRANQUE

Al inicio de CADA sesión, leer:
`00_SISTEMA/MASTER.md`

Ese archivo tiene el estado actual de todos los proyectos, blockers y foco activo.

---

## IDENTIDAD

**Operador/a:** {{TU_NOMBRE}} — {{TU_ROL}} de {{NOMBRE_EMPRESA}}
**Idioma:** {{IDIOMA}} siempre. Respuestas directas, sin preámbulos.
**Regla de oro:** Proponer antes de ejecutar en sistemas externos. Esperar confirmación explícita.
**Foco:** Máximo 3 items activos. Una cosa a la vez.

---

## CAPA 1 — SEGURIDAD

- HITL obligatorio para cualquier escritura en sistemas externos (CRM, ERP, email, redes sociales)
- Nunca credenciales en código ni en este repo. Solo en variables de entorno / archivo local fuera del repo.
- Ver `00_SISTEMA/HITL-MATRIX.md` para la matriz completa de qué se automatiza, qué se confirma, qué se bloquea.

---

## CAPA 2 — ARQUITECTURA

- **Brain / estado del sistema:** `00_SISTEMA/MASTER.md`
- **Regla de fuente de verdad:** el brain (este vault) gobierna decisiones, estrategia y contexto — tu herramienta operativa ({{HERRAMIENTA_PRINCIPAL}}) ejecuta y registra lo que pasó. El vault no duplica transacciones ni tareas, las lee y resume.

---

## CAPA 3 — SKILLS DISPONIBLES

Ver registro completo en `00_SISTEMA/SKILLS-REGISTRY.md`

Arranque rápido:
- `/status` — leer MASTER.md + estado del sistema completo
- `/cierre` — cierre de sesión: log en 07_LOG + actualizar MASTER.md

---

## HITL MATRIX (resumen — ver 00_SISTEMA/HITL-MATRIX.md)

| Acción | Automático | Requiere confirmación | Bloqueado |
|--------|-----------|----------------------|-----------|
| Leer archivos del vault o de {{HERRAMIENTA_PRINCIPAL}} | ✅ | — | — |
| Escribir en el vault (MASTER.md, logs) | — | ✅ siempre | — |
| Escribir en {{HERRAMIENTA_PRINCIPAL}} (crear/editar registros) | — | ✅ siempre | — |
| Enviar comunicación externa (email, mensaje, post) | — | ✅ siempre | — |
| Borrar cualquier archivo o registro | — | — | 🔴 siempre |
| Operaciones masivas (>20 registros) | — | — | 🔴 siempre |

**Regla de oro:** proponer antes de ejecutar. Esperar confirmación explícita.
