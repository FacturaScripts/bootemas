# Bootemas: contexto del equipo

Esta carpeta guarda **por qué el código es como es**: las decisiones que no se ven leyendo una sola clase, para que
todo el equipo y los agentes trabajen con el mismo contexto. Lee este índice y abre solo el tema o la decisión que
necesites.

Se puede dividir en tantos archivos y subcarpetas como haga falta; este índice dice qué hay en cada uno y se actualiza
en el mismo trabajo que cambia el código.

## Temas

- [`01-arquitectura.md`](01-arquitectura.md): piezas del plugin (plantillas, extensiones XML, npm) y qué toca del core.
- [`02-temas.md`](02-temas.md): cómo se cargan los 26 temas de bootswatch y la prioridad usuario, defecto, core.
- [`03-portal-y-menu.md`](03-portal-y-menu.md): soporte de Portal, ubicación de los selectores y barra de menú.
- [`04-puntos-delicados.md`](04-puntos-delicados.md): plantillas copiadas del core, listas duplicadas y dependencias.
- [`05-evolucion.md`](05-evolucion.md): etapas del plugin según el historial.

## Decisiones

- [`0001-temas-de-bootswatch-por-npm.md`](Decisiones/0001-temas-de-bootswatch-por-npm.md): por qué los CSS vienen de bootswatch por npm.
- [`0002-tema-por-usuario-con-valor-por-defecto.md`](Decisiones/0002-tema-por-usuario-con-valor-por-defecto.md): campo `bootema` por usuario y ajuste global.
- [`0003-plantillas-base-reemplazadas.md`](Decisiones/0003-plantillas-base-reemplazadas.md): por qué se reemplazan las plantillas del core.
