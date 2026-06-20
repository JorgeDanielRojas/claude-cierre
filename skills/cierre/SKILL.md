---
name: cierre
description: Cierre estructurado de sesión que persiste los aprendizajes de la sesión en el CLAUDE.md del proyecto. Úsalo al terminar de trabajar, cuando el usuario diga "/cierre", "cierra la sesión", "guarda lo aprendido" o quiera que la próxima sesión arranque sin perder el contexto de hoy.
---

# Cierre de sesión con memoria

Convierte el cierre de sesión en un ritual corto: revisa lo que pasó y guarda lo durable en el `CLAUDE.md` del proyecto, para que la próxima sesión no empiece en cero.

## Workflow al invocar

1. **Auto-pregunta honesta:** ¿Si me cierran ahora, recordaré el 100% de lo que hicimos hoy?

2. **Escanear la sesión:** identificar
   - Reglas nuevas (anti-patrones descubiertos, protocolos validados)
   - Datos contextuales útiles (paths, schemas, APIs, comandos)
   - Decisiones tomadas
   - Estado de tareas (terminadas / en progreso / bloqueadas)
   - Archivos creados o modificados que importan

3. **Comparar con el `CLAUDE.md` del proyecto:**
   - Si ya está documentado → no duplicar
   - Si falta → identificar la sección apropiada

4. **Reportar al usuario ANTES de escribir:**
   - Lista comprimida de qué se guardaría y dónde (sección/archivo)
   - Preguntar: "¿OK, aplico?"

5. **Tras el OK:**
   - Backup del `CLAUDE.md` actual (copia con marca de tiempo)
   - Aplicar las ediciones
   - Confirmar: "Memoria al día. Puedes cerrar."

6. **Si algo es ambiguo, hay conflicto o el alcance es dudoso:** parar y avisar antes de cerrar. NO inventar.

7. **Si el usuario no responde (sesión autónoma):** hacer backup + aplicar lo conservador + dejar una nota de lo pendiente.

## Reglas

- Estilo: comprimido, directo, sin relleno.
- NO documentar lo efímero (IDs de runtime, archivos temporales, estados intermedios).
- SÍ documentar lo durable (cómo cargar X en la app Y, el schema del archivo Z, un anti-patrón aprendido).
- El `CLAUDE.md` es la memoria de largo plazo del proyecto: cada cierre lo deja más útil para la próxima sesión.
