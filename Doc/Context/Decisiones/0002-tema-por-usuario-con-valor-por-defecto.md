# 0002. Tema por usuario con valor por defecto global

- Fecha: 2021-12-25
- Commits: `dd2581c`, `3eb4547`
- Estado: vigente

## Contexto

Cada usuario debe poder elegir su tema y la instalación tener uno por defecto.

## Decisión

Columna `bootema` en `users` (`Extension/Table/users.xml`) y ajuste `bootema` en la configuración por defecto. Las plantillas aplican: usuario, después ajuste global, después bootstrap del core. Portal tiene su selector (`Extension/XMLView/SettingsPortal.xml`).

## Consecuencias

Quitar el plugin no borra la columna de la base de datos. Ver [`../02-temas.md`](../02-temas.md).
