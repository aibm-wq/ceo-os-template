# /cierre — Cierre de Sesión
> Modelo recomendado: Haiku

Registra lo que se hizo en esta sesión y actualiza el BRAIN.

## Paso 1 — Resumen de sesión

Antes de escribir nada, presenta al usuario:

```
CIERRE — {{NOMBRE}} — [FECHA]

¿Qué se hizo hoy?
[lista de lo realizado en esta sesión]

¿Qué quedó pendiente?
[lista de pendientes]

¿Alguna decisión importante?
[decisiones que deben quedar registradas]
```

Pedir confirmación: "¿Es correcto este resumen?"

## Paso 2 — Escribir log en BRAIN

Solo después de confirmación explícita, crear o actualizar:
`C:\Users\PC\Desktop\AIDA-OS\07_LOG\[FECHA].md`

Formato del log:
```markdown
# Log — [FECHA]

## Proyecto: {{NOMBRE}}

## Qué se hizo
[lista]

## Decisiones tomadas
[lista]

## Pendiente próxima sesión
[lista]
```

## Paso 3 — Actualizar MASTER.md

Si hubo cambios de estado en este proyecto, proponer actualización a:
`C:\Users\PC\Desktop\AIDA-OS\00_SISTEMA\MASTER.md`

## Reglas
- Nunca escribir sin confirmación del paso 1
- Si el log del día ya existe, hacer append — no sobrescribir
- Mantener el log conciso — máximo 20 líneas
