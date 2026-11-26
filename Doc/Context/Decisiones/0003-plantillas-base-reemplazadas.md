# 0003. Reemplazar las plantillas base del core

- Fecha: 2021-12-25
- Commits: `dd2581c`, `61e5d43`, `84100bc`
- Estado: vigente

## Contexto

Cambiar el CSS cargado exige modificar el `<head>` de la plantilla base.

## Decisión

El plugin aporta `View/Master/MenuTemplate.html.twig` y `View/Master/MicroTemplate.html.twig` completas, no una extensión. El historial no menciona alternativas.

## Consecuencias

Hay que mantenerlas sincronizadas con el core (ganchos `getIncludeViews`, toasts, menú). Ver [`../04-puntos-delicados.md`](../04-puntos-delicados.md).
