# tikitiki-server-config

Configuration for the TikiTiki Minecraft server (Cobblemon, 1.21.1) and its launcher. The launcher reads these files every time it opens to know which game version to install, which mods to download and which server to connect to. In practice, this repo is its backend.

## Files

| File | What's in it |
|---|---|
| `version.json` | The latest launcher version, with the link to the `.exe` and its SHA-1, so it updates itself. |
| `launcher.json` | The modpack: Minecraft version, loader, the mods with their URL, SHA-1 and size, the config files and the skins. |
| `servers/` | Servers that players set up from the launcher, one per file. |
| `skins/` | Default skins the launcher offers. |
| `packs/` | Resource packs. |
| `server/icon.png` | The server icon. |

Every download comes with its SHA-1 and size, so the launcher can check that what it got is complete. The heavy files (the launcher, server mods, packs and world backups) are release assets rather than part of the repo.

## About the history

The "Dirección del server TikiTiki" and "Actualiza la lista del server" commits (server address and server list updates) are made by the launcher itself when someone opens a server and the tunnel address changes. They're not edits by hand.
