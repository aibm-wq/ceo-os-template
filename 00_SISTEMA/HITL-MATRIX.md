---
type: sistema
status: activo
actualizado: {{FECHA}}
---

# HITL-MATRIX — Matriz de Control Humano en el Loop

> Fuente canónica de permisos. Todo skill, agente o comando hereda esta matriz por referencia — nunca la copia.

---

## Regla de oro

**Proponer antes de ejecutar. Esperar confirmación explícita** ("sí", "confirmar", "procede") antes de cualquier acción de las categorías "Requiere confirmación" abajo.

---

## Clases de acción

| Clase | Significado |
|-------|-------------|
| C0 | Lectura — siempre automático |
| C1 | Escritura reversible de bajo riesgo (crear un borrador, ej. lead en estado "draft") |
| C2 | Escritura operativa normal (actualizar campos, cerrar una tarea) — requiere confirmación si toca datos de terceros |
| C3 | Escritura irreversible o externa (enviar email, publicar contenido, confirmar una orden) — **confirmación SIEMPRE** |
| C4 | Bloqueado en código — nunca se propone, nunca se ejecuta |

---

## Matriz por dominio

| Acción | Automático (C0-C1) | Requiere confirmación (C2-C3) | Bloqueado (C4) |
|--------|---------------------|-------------------------------|----------------|
| Leer archivos del vault | ✅ | — | — |
| Leer {{HERRAMIENTA_PRINCIPAL}} (búsquedas, reportes) | ✅ | — | — |
| Escribir en el vault (MASTER.md, logs, decisiones) | — | ✅ siempre | — |
| Crear/editar registros en {{HERRAMIENTA_PRINCIPAL}} | — | ✅ siempre | — |
| Enviar email, mensaje o publicar contenido | — | ✅ siempre | — |
| Operaciones financieras (facturas, pagos, transferencias) | — | — | 🔴 siempre — solo humano |
| Gestión de usuarios/permisos del sistema | — | — | 🔴 siempre — solo humano |
| Borrar cualquier archivo o registro | — | — | 🔴 siempre |
| Operaciones masivas (>20 registros) | — | — | 🔴 siempre sin autorización explícita previa |

---

## Modelos/datos protegidos (ejemplo — ajustar a tu herramienta real)

Estos NUNCA se escriben sin humano, sin importar el contexto:
- {{MODELO_PROTEGIDO_1}} (ej: facturación/contabilidad)
- {{MODELO_PROTEGIDO_2}} (ej: usuarios y permisos)
- {{MODELO_PROTEGIDO_3}} (ej: configuración de seguridad)

---

## Credenciales

- Nunca en código, nunca en este repo, nunca en un `.env` versionado
- Vivir en variables de entorno o en un archivo local **fuera de cualquier repo** (ej: `~/.claude/CREDENCIALES.md` o equivalente)
- Antes de cada commit: revisar qué se está subiendo — un nombre de archivo inocente puede contener datos sensibles

---

## Regla de resolución

Si una acción nueva no tiene fila en esta matriz, se trata como **C3 (requiere confirmación)** por defecto hasta que se agregue una fila explícita.
