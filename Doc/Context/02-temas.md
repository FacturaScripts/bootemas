# Temas: carga y selección

El CSS de bootstrap se elige en el bloque `css` de las dos plantillas, con tres niveles de prioridad.

## Cómo es hoy

1. Si el usuario tiene valor en `users.bootema` (`fsc.user.bootema`), se carga `Plugins/Bootemas/node_modules/bootswatch/dist/<valor>/bootstrap.min.css`.
2. Si no, y existe `settings('default','bootema')`, se usa ese tema por defecto.
3. Si no hay ninguno, se carga el bootstrap del core (`node_modules/bootstrap/dist/css/bootstrap.min.css`).

Después se cargan Font Awesome 6 y, en `MenuTemplate`, `Dinamic/Assets/CSS/custom.css`. El CSS libre de `settings('default','css_style')` se imprime en un `<style>` posterior, así que puede sobrescribir el tema.

Los 26 temas, idénticos en los tres XML: brite, cerulean, cosmo, cyborg, darkly, flatly, journal, litera, lumen, lux, materia, minty, morph, pulse, quartz, sandstone, simplex, sketchy, slate, solar, spacelab, superhero, united, vapor, yeti y zephyr. El valor guardado es el nombre en minúsculas y coincide con la carpeta de bootswatch.

- `MenuTemplate` añade `?v=5` a los CSS de bootstrap y `MicroTemplate` no (`780feab`).
- El usuario siempre gana al ajuste global.

## Por qué

- Campo por usuario en `users` más ajuste global: dos niveles desde la versión inicial (`dd2581c`).
- Se añadieron 5 temas (brite, morph, quartz, vapor, zephyr) para pasar de 21 a 26 (`d92fc73`); hay que tocar los tres XML a la vez.
- La columna es `character varying(15)`: cabe el nombre más largo (`sandstone`, 9).

## Al cambiarlo

- Para añadir un tema, la lista debe existir en `EditUser.xml`, `SettingsDefault.xml` y `SettingsPortal.xml`, y bootswatch debe traer esa carpeta.
- Hay que ejecutar `npm install` en la carpeta del plugin: `node_modules/` está en `.gitignore`.
- Si cambias la ruta de los CSS, actualiza las dos plantillas.
