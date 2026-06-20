# /cierre — cierre de sesión con memoria para Claude Code

> Un slash command para [Claude Code](https://claude.com/claude-code) que, al terminar de trabajar, **revisa la sesión y guarda lo aprendido en el `CLAUDE.md` del proyecto** — para que la próxima sesión arranque sin amnesia.

*A Claude Code slash command that reviews the session and persists what was learned into the project's `CLAUDE.md`, so the next session doesn't start from zero.*

---

## El problema

Cada sesión nueva de Claude Code empieza en blanco. Las reglas que descubriste, las decisiones que tomaste, los comandos exactos que funcionaron... se pierden cuando cierras. La próxima vez vuelves a explicar lo mismo.

## La solución

`/cierre` convierte el cierre de sesión en un ritual de 30 segundos:

1. Escanea lo que pasó en la sesión.
2. Lo compara con lo que ya está en tu `CLAUDE.md` (no duplica).
3. Te muestra **qué guardaría y dónde**, y espera tu OK.
4. Hace un backup, aplica los cambios y confirma.

Tu `CLAUDE.md` se vuelve la memoria de largo plazo del proyecto. Cada cierre lo deja mejor.

## Instalación

### Opción A — como plugin (recomendado)

En Claude Code:

```
/plugin marketplace add JorgeDanielRojas/claude-cierre
/plugin install cierre@claude-cierre
```

### Opción B — copiar la skill a mano

```bash
mkdir -p ~/.claude/skills/cierre
cp skills/cierre/SKILL.md ~/.claude/skills/cierre/
```

## Uso

Al terminar de trabajar, en Claude Code escribe:

```
/cierre
```

Revisa lo que propone guardar, di "OK", y cierra tranquilo.

## Por qué funciona

- **Pide permiso antes de escribir** — nunca toca tu `CLAUDE.md` a tus espaldas.
- **Hace backup** antes de cada cambio.
- **No documenta basura** — solo lo durable (anti-patrones, schemas, comandos que importan), nunca lo efímero.
- **No inventa** — si algo es ambiguo, para y pregunta.

## Licencia

MIT — úsalo, modifícalo, compártelo.
