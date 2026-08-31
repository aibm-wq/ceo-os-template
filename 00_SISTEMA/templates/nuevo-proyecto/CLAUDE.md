# {{NOMBRE}} — Workspace Claude Code
> Creado: {{FECHA}} | CCA-F baseline: Nivel 2 (11/18)
> Template: AIDA-OS/_SISTEMA/templates/nuevo-proyecto

---

## 1. IDENTIDAD DEL PROYECTO

**Qué es:** {{DESCRIPCION}}
**Workspace:** {{RUTA}}
**Operadora:** Aida Bermúdez — AIDA-OS
**Capa AIDA-OS:** {{CAPA}}
**Odoo:** {{ODOO_URL}} | DB: {{ODOO_DB}}

---

## 2. PROPÓSITO DEL AGENTE

{{PROPOSITO}}

**Puede hacer:**
- {{PUEDE_1}}
- {{PUEDE_2}}

**Nunca hace:**
- {{NO_HACE_1}}
- {{NO_HACE_2}}

---

## 3. HITL MATRIX

| Acción | Automático | Requiere confirmación | Bloqueado |
|--------|-----------|----------------------|-----------|
| Leer archivos locales | ✅ | — | — |
| Leer Odoo (search_read) | ✅ | — | — |
| Escribir archivos | — | ✅ siempre | — |
| Crear/editar registros Odoo | — | ✅ siempre | — |
| Borrar cualquier cosa | — | — | 🔴 siempre |
| Operaciones bulk >20 registros | — | — | 🔴 siempre |

**Regla de oro:** Proponer antes de ejecutar. Esperar confirmación explícita ("sí", "confirmar", "procede").

---

## 4. CONEXIONES

| Sistema | URL | Env var |
|---------|-----|---------|
| {{SISTEMA_1}} | {{URL_1}} | {{ENV_1}} |

---

## 5. SKILLS DISPONIBLES

- `/status` — estado del proyecto
- `/cierre` — cierre de sesión + log en BRAIN

---

## 6. ARQUITECTURA AIDA-OS

Este workspace es un proyecto dentro de AIDA-OS.
Brain central: `C:\Users\PC\Desktop\AIDA-OS\00_SISTEMA\MASTER.md`
Al inicio de sesión leer MASTER.md para contexto global.
