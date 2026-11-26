# 0001. Temas de bootswatch vía npm, sin CSS propio

- Fecha: 2021-12-25
- Commits: `dd2581c`, `5bc4649`
- Estado: vigente

## Contexto

Se querían temas alternativos de aspecto para FacturaScripts.

## Decisión

Se usan los temas originales de bootswatch.com, instalados con `package.json` y cargados desde `Plugins/Bootemas/node_modules/bootswatch/dist/`. En 2025 la dependencia pasó de la versión 4 a la 5 (`5bc4649`).

## Consecuencias

El plugin no contiene CSS; necesita `npm install`. Los nombres de tema son los de las carpetas de bootswatch.
