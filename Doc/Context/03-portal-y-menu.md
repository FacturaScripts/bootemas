# Soporte de Portal y barra de menú

## Portal

`Extension/XMLView/SettingsPortal.xml` añade el mismo selector `bootema` a los ajustes del plugin Portal (grupo `style`, orden 201), para elegir el tema desde allí (`3eb4547`, 2024-08-28). Portal no está declarado como dependencia en `facturascripts.ini`. El historial no dice nada más sobre su funcionamiento.

## Dónde está el selector en cada pantalla

- Usuario: grupo `preferences` de `EditUser` (antes estaba en `data`, `79ea7a5`).
- Ajustes: grupo `advanced` de `SettingsDefault`; el orden pasó de 131 a 121 (`b8c28ab`).

## Barra de menú (`View/Master/MenuTemplate.html.twig`)

- Marca de empresa enlazada a `fsc.user.homepage` (corrección `d076086`) y menú de `menuManager.getMenu()`.
- Bloque `navbarMenuIcon` (`150fd94`) con ganchos `MenuIconBefore`, `MenuIconUser` y `MenuIconAfter`, e iconos de búsqueda, dashboard, ayuda y usuario con ids `menuIcon*` (`ab9a2b2`).
- El botón de ayuda se oculta si `fs_hide_help_btn` es verdadero (`43a0f5c`).
- Menú de usuario con enlace a enviar email (`fdeb907`) y cierre de sesión con `formToken(false)`.
- La clase `active` va en el `nav-link` de buscar y dashboard (`8f2b137`).
- Ganchos `getIncludeViews('MenuTemplate', ...)` (HeadFirst, CssBefore, CssAfter, JsHeadBefore, JsHeadAfter, HeadEnd, BodyFirst, JsFooter, BodyEnd) añadidos en `61e5d43`.
- Mensajes toast (`Macro/Toasts.html.twig`, `1217c65`), Google Tag Manager y comentario con el tiempo de ejecución (`50d21f2`).
- Bootstrap 5: `data-bs-toggle`, `dropdown-menu-end`, y se quitó bootbox (`5bc4649`, `2ff2eaf`).
- Hubo soporte para instalaciones megacity (`MC20_INSTALLATION`, `d3079aa`, `0697701`); ya no está en el código actual y el historial no dice por qué se retiró.
