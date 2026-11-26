# Arquitectura

Bootemas no tiene código PHP: son plantillas Twig, extensiones XML del core y una dependencia npm (bootswatch 5).

## Cómo es hoy

| Pieza | Archivo | Qué hace |
|---|---|---|
| Metadatos | `facturascripts.ini` | Nombre, descripción (26 temas de bootswatch), versión 2.2 y `min_version = 2025`. No declara `require`. |
| Dependencia | `package.json` | `bootswatch ^5`. Los CSS salen de `node_modules/bootswatch/dist/<tema>/bootstrap.min.css`. |
| Campo de usuario | `Extension/Table/users.xml` | Añade la columna `bootema` (`character varying(15)`) a `users`. |
| Selector por usuario | `Extension/XMLView/EditUser.xml` | Select `bootema` en el grupo `preferences`, orden 151. |
| Selector por defecto | `Extension/XMLView/SettingsDefault.xml` | Select `bootema` (grupo `advanced`, orden 121) y textarea `css_style` (orden 200). |
| Selector del Portal | `Extension/XMLView/SettingsPortal.xml` | Select `bootema` en el grupo `style`, orden 201. |
| Plantilla del panel | `View/Master/MenuTemplate.html.twig` | Sustituye la plantilla base con menú: carga el CSS del tema y define la barra de navegación. |
| Plantilla sin menú | `View/Master/MicroTemplate.html.twig` | Igual que la anterior pero sin barra de navegación. |
| Traducciones | `Translation/es_ES.json` | Solo `bootema` ("Bootema") y `css-style` ("Estilo CSS"). |

Las plantillas de `View/Master/` son copias de las del core con los cambios del plugin: al generar `Dinamic/`, la versión del plugin tapa a la del core.

## Por qué

Ver [`02-temas.md`](02-temas.md) y las decisiones. El historial no explica por qué el plugin no tiene PHP; por el código, no lo necesita.

## Al cambiarlo

Al subir de versión el core, compara `MenuTemplate` y `MicroTemplate` con las del core: si divergen, el plugin pierde los cambios del core (ver [`04-puntos-delicados.md`](04-puntos-delicados.md)).
