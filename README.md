# CEO OS Template

Un sistema operativo local para founders/CEOs (y adaptable a Project Managers) que combina:

- **Un "brain" vivo** (`00_SISTEMA/MASTER.md`) — el estado real del negocio, siempre actualizado, punto de entrada de cada sesión
- **Una matriz HITL** (`00_SISTEMA/HITL-MATRIX.md`) — qué puede hacer un agente de IA solo, qué requiere tu confirmación, qué está bloqueado siempre
- **Un registro de skills** (`00_SISTEMA/SKILLS-REGISTRY.md`) — comandos reutilizables (`/status`, `/cierre`, etc.) que el agente ejecuta de forma consistente
- **Separación clara: el vault gobierna, tu ERP/herramienta operativa ejecuta.** El brain no duplica tareas ni transacciones — las lee y las resume.

Este repo es la **estructura vacía**, sin datos de ningún negocio real. Clónalo, llénalo con tu información, y nunca subas ese contenido lleno a un repo compartido (ver Seguridad más abajo).

---

## Requisitos

Este sistema está pensado para funcionar bien con:

- **[Claude Code](https://claude.com/claude-code)** — el agente que lee `CLAUDE.md`, opera el brain y ejecuta los skills. Sin esto, la estructura es solo carpetas y markdown estático.
- **[Obsidian](https://obsidian.md)** — abre esta misma carpeta como vault para navegar el brain visualmente (grafo de notas, backlinks, búsqueda). No es obligatorio para que Claude Code funcione, pero es la forma recomendada de que un humano recorra el sistema sin depender solo del agente.

No requiere ninguna otra herramienta — todo lo demás (CRM, ERP, banco) se conecta vía MCP o se referencia desde `HITL-MATRIX.md`, nunca se duplica dentro del vault.

---

## Cómo empezar

1. Clona este repo a tu máquina: `git clone <este-repo> mi-empresa-os`
2. Borra el `.git` interno y arranca el tuyo propio: `rm -rf .git && git init` (así tu contenido real nunca hereda este historial)
3. Abre `00_SISTEMA/MASTER.md` y reemplaza los `{{PLACEHOLDERS}}` con tu información real
4. Ajusta `00_SISTEMA/HITL-MATRIX.md` a las herramientas que realmente usas (tu CRM, tu ERP, tu banco)
5. Abre Claude Code en la raíz de tu copia — lee `CLAUDE.md` automáticamente al arrancar

---

## Estructura de carpetas

```
00_SISTEMA/       — el sistema en sí: MASTER.md, HITL-MATRIX.md, SKILLS-REGISTRY.md, templates/
01_IDENTIDAD/     — quién eres, tu marca, tus principios de decisión
02_PROYECTOS/     — un archivo .md por proyecto/línea de negocio activa
03_CLIENTES/      — contexto por cliente (si aplica)
04_LLCS/          — entidades legales (si aplica — un PM normalmente borra esta carpeta)
05_PIPELINE/      — ventas, contenido, captación (si aplica)
06_ARQUITECTURA/  — documentos de arquitectura del propio sistema (opcional, capa avanzada)
07_LOG/           — un archivo .md por sesión de trabajo — historial de qué se hizo y por qué
```

**Para un Project Manager:** borra `04_LLCS/` y recorta `01_IDENTIDAD/` a lo mínimo (rol, principios de decisión del equipo) — el resto del esqueleto (MASTER.md, HITL-MATRIX, proyectos, log) sirve tal cual.

---

## La regla de oro

**Proponer antes de ejecutar. Esperar confirmación explícita** para cualquier escritura en sistemas externos (CRM, ERP, email, redes sociales). Esto vive en `HITL-MATRIX.md` y todo skill/agente debe heredarlo, nunca copiarlo.

---

## Seguridad — antes de usar esto en serio

- **Nunca** pongas credenciales, contraseñas o API keys reales dentro de este repo — ni siquiera en un repo privado. Usa variables de entorno + un archivo local fuera del repo (ver plantilla de regla en `HITL-MATRIX.md`).
- Antes de cada commit, revisa qué se está subiendo (`git status` + mirar el diff) — un archivo con nombre inocente puede contener datos sensibles.
- Si este repo va a vivir en un remoto compartido (GitHub, GitLab), tu contenido real (llenado en el paso 3 de arriba) debería vivir en un repo **separado y privado**, nunca en este template.

---

## Origen

Extraído y genericizado de un sistema operativo real en uso (AIDA-OS), auditado con `graphify` para separar la estructura reutilizable del contenido específico de un negocio.
