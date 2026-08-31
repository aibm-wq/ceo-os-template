# {{NOMBRE}}

{{DESCRIPCION}}

---

## Onboarding — Para empezar a trabajar

### 1. Requisitos
- Claude Code instalado
- Acceso a las credenciales del proyecto (ver sección Credenciales)
- Python 3.10+ (si el proyecto usa scripts)

### 2. Configurar credenciales

Editar `.claude/settings.local.json` y agregar las variables de entorno del proyecto.
Nunca commitear este archivo — está en `.gitignore`.

### 3. Primera sesión

Abrir terminal en este directorio y ejecutar Claude Code:
```
claude
```

Al arrancar, Claude lee `CLAUDE.md` y tiene todo el contexto del proyecto.

### 4. Skills disponibles

| Skill | Qué hace |
|-------|---------|
| `/status` | Estado actual del proyecto |
| `/cierre` | Cierra la sesión y loguea en el BRAIN |

---

## Arquitectura

Este proyecto es parte de AIDA-OS — el sistema operativo local de Aida Bermúdez.
Brain central: `Desktop/AIDA-OS/`

### Capa AIDA-OS: {{CAPA}}

---

## Credenciales

| Variable | Descripción | Dónde obtenerla |
|----------|-------------|----------------|
| `{{ENV_1}}` | {{DESC_ENV_1}} | {{FUENTE_1}} |

---

## Contacto

**Operadora:** Aida Bermúdez — aibm@bwealthics.com
**Arquitectura:** AIDA-OS v2 · CCA-F Nivel 2 baseline
