---
type: sistema
status: activo
actualizado: {{FECHA}}
---

# Skills Registry — {{NOMBRE_EMPRESA}}

> Registro de comandos (`/skill`) disponibles en este sistema. Cada skill hereda la HITL-MATRIX — nunca la reimplementa.

---

## Arranque y briefing

| Skill | Qué hace |
|-------|---------|
| `/status` | Lee `MASTER.md` + presenta estado actual del sistema: proyectos, blockers, foco activo |
| `/cierre` | Cierre de sesión: escribe un log en `07_LOG/{{FECHA}}.md` y propone actualizaciones a `MASTER.md` (con confirmación) |

## Plantilla — agregar un skill nuevo

Cuando crees un skill nuevo, documéntalo aquí con esta forma:

| Skill | Qué hace | Módulos que toca | Nivel HITL máximo |
|-------|---------|-------------------|---------------------|
| `/{{nombre}}` | {{descripcion}} | {{modulos}} | {{C0-C4}} |

**Regla:** un skill nuevo no se activa hasta tener su fila aquí y su clase HITL declarada contra `HITL-MATRIX.md`.
