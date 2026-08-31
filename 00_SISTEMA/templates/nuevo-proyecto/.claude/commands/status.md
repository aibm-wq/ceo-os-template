# /status — Estado del Proyecto
> Modelo recomendado: Haiku (solo lectura)

Lee el estado actual del proyecto y presenta un resumen ejecutivo.

## Qué leer

1. `CLAUDE.md` del workspace — identidad y propósito
2. Archivos de trabajo relevantes en el directorio
3. `00_SISTEMA/MASTER.md` — estado global AIDA-OS

## Formato de salida

```
════════════════════════════════════════
{{NOMBRE}} — STATUS [FECHA]
════════════════════════════════════════

PROYECTO: [descripción]
CAPA: [capa AIDA-OS]

ACTIVO AHORA:
- [qué está en progreso]

PENDIENTE:
- [qué falta]

BLOCKERS:
- [qué está bloqueado y por qué]

════════════════════════════════════════
¿Continuamos o hay algo nuevo?
```

## Reglas
- Solo leer — nunca escribir sin instrucción explícita
- Si no hay información suficiente, preguntar
