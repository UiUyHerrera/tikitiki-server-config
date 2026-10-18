# tikitiki-server-config

Configuración del servidor de Minecraft TikiTiki (Cobblemon, 1.21.1) y de su launcher. El launcher lee estos archivos cada vez que se abre para saber qué versión del juego instalar, qué mods bajar y a qué servidor conectarse. En la práctica, este repo es su backend.

## Archivos

| Archivo | Qué tiene |
|---|---|
| `version.json` | La última versión del launcher, con el link al `.exe` y su SHA-1, para que se actualice solo. |
| `launcher.json` | El modpack: versión de Minecraft, loader, los mods con su URL, SHA-1 y tamaño, los archivos de configuración y las skins. |
| `servers/` | Servidores que arman los jugadores desde el launcher, uno por archivo. |
| `skins/` | Skins por defecto que ofrece el launcher. |
| `packs/` | Resource packs. |
| `server/icon.png` | Ícono del servidor. |

Cada descarga viene con su SHA-1 y su tamaño, así el launcher puede comprobar que lo que bajó está entero. Los archivos pesados (el launcher, los mods del servidor, los packs y las copias del mundo) van como assets de los releases y no dentro del repo.

## Sobre el historial

Los commits "Dirección del server TikiTiki" y "Actualiza la lista del server" los hace el launcher solo, cuando alguien abre un servidor y cambia la dirección del túnel. No son cambios hechos a mano.
