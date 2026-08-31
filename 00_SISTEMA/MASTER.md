---
type: sistema
status: activo
actualizado: {{FECHA}}
---

# {{NOMBRE_EMPRESA}} — MASTER BRAIN
> Última actualización: {{FECHA}}
> Este archivo es el punto de entrada del sistema. Se lee al arrancar desde cualquier sesión.

---

## INSTRUCCIÓN PARA EL AGENTE

Al inicio de CADA sesión:
1. Lee este archivo completo
2. Carga el contexto del proyecto correspondiente de `02_PROYECTOS/`
3. Aplica las reglas de `00_SISTEMA/HITL-MATRIX.md`

---

## QUIÉN SOY

**{{TU_NOMBRE}}** — {{TU_ROL}} de {{NOMBRE_EMPRESA}}

**Idioma operativo:** {{IDIOMA}}
**Regla de oro:** Proponer antes de ejecutar en sistemas externos. Esperar confirmación explícita.
**Foco:** Máximo 3 items activos a la vez. Una cosa a la vez.

---

## ESTADO GLOBAL DE PROYECTOS

| Proyecto | Estado | Próximo paso | Blocker |
|----------|--------|---------------|---------|
| {{PROYECTO_1}} | 🟢/🟡/🔴 | {{PROXIMO_PASO}} | {{BLOCKER}} |

**Leyenda de estado:** 🟢 Activo y sano · 🟡 Atención necesaria · 🔴 Bloqueado · ⏸ Pausado · ⏳ Esperando respuesta externa

---

## BLOCKERS CRÍTICOS

| Blocker | Impacto | Acción |
|---------|---------|--------|
| {{BLOCKER}} | {{IMPACTO}} | {{ACCION_REQUERIDA}} |

---

## FOCO ACTIVO (máx 3)

1. **{{FOCO_1}}** · {{DETALLE}}
2. **{{FOCO_2}}** · {{DETALLE}}
3. **{{FOCO_3}}** · {{DETALLE}}

---

## HERRAMIENTAS — INSTANCIAS

| Sistema | URL | Uso | Notas |
|---------|-----|-----|-------|
| {{HERRAMIENTA_PRINCIPAL}} | {{URL}} | {{PARA_QUE}} | {{NOTAS}} |

---

## ARQUITECTURA DEL SISTEMA

Documentos canónicos que gobiernan el diseño y la operación de este sistema:

| Documento | Función |
|-----------|---------|
| `00_SISTEMA/HITL-MATRIX.md` | Permisos operativos — qué se automatiza, qué se confirma, qué se bloquea |
| `00_SISTEMA/SKILLS-REGISTRY.md` | Comandos/skills reutilizables disponibles |

---

## SKILLS DISPONIBLES

Ver registro completo en `00_SISTEMA/SKILLS-REGISTRY.md`

Arranque rápido:
- `/status` — leer este archivo + estado del sistema
- `/cierre` — cierre de sesión: log en `07_LOG/` + actualizar este archivo

---

## LOG DE CAMBIOS RECIENTES

### {{FECHA}}

- {{QUE_SE_HIZO}}
