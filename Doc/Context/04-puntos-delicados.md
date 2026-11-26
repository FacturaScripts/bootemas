# Puntos delicados

- **Plantillas copiadas del core.** `MenuTemplate` y `MicroTemplate` reemplazan las del core. Muchos commits del historial solo las resincronizan (ganchos, toasts, font-awesome, `trans()`, bootstrap 5). Tras cada cambio de versión del core hay que revisarlas.
- **Tres listas de temas duplicadas** en los XML (ver [`02-temas.md`](02-temas.md)).
- **Dependencia npm.** Sin `node_modules/bootswatch` los temas dan 404 y la página queda sin los estilos del tema.
- **Compatibilidad.** `min_version = 2025`: usa Bootstrap 5 y Font Awesome 6 (`fa-solid`).
- **Versión de assets.** `?v=5` solo en `MenuTemplate`; `MicroTemplate` sin versión.
- **Traducciones.** Solo existe `es_ES.json`, con dos claves.
- **Sin PHP ni tests**, así que no hay docblocks que completar.
