<p align="center"><img src="docs/icon.png" width="96" alt="Smeariom icon"></p>

<h1 align="center">Smeariom</h1>

<p align="center">A Fabric mod that watches your FPS and smooths out lag automatically.</p>

---

When your FPS drops, Smeariom looks at what's around you (big mob farms, piles of dropped items, mobs stuck in caves) and fixes that: it stops drawing them, lowers your view distance a bit, and cuts down particles, clouds and shadows. Once your FPS is back to normal, it puts everything back the way it was.

Mobs close to you always stay visible, and your settings are always restored when you leave a world.

![Settings](docs/settings.png)

## Download

Grab the jar for your Minecraft version from the [Releases](../../releases) page:

| Minecraft | File |
|---|---|
| 26.3 | `smeariom-1.0.3+26.3.jar` |
| 26.2 | `smeariom-1.0.3+26.2.jar` |
| 1.21.11 | `smeariom-1.0.3+1.21.11.jar` |

You also need [Fabric Loader](https://fabricmc.net/use/) and [Fabric API](https://modrinth.com/mod/fabric-api). [Mod Menu](https://modrinth.com/mod/modmenu) is optional.

Client-side only, so it works on any server.

## Settings

Open them with **Mods → Smeariom**, or type `/smeariom` in chat.

**Detection:** FPS threshold, scan radius, auto-restore.
**Smoothing (only while lagging):** view distance, entity distance, mob crowds, item piles, far players, particles, clouds, shadows, biome blend.
**Always on (optional):** entity culling past a set distance, particle limit, minimal particles.
**Visibility (optional):** hide nametags, armor stands, item frames, XP orbs, arrows.
**HUD:** FPS badge, FPS graph, status messages.

## Commands

`/smeariom` opens the settings. It also takes:

| Command | Does |
|---|---|
| `/smeariom on` / `off` | Enable or disable the mod |
| `/smeariom scan` | Run a lag scan right now |
| `/smeariom restore` | Put every tweaked setting back immediately |
| `/smeariom reload` | Re-read the config file from disk |
| `/smeariom status` | Show current FPS and what's being smoothed |

![Overview](docs/overview.png)

![HUD](docs/hud.png)

## Building

Each Minecraft version has its own folder. From inside one:

```
gradlew build
```

The jar ends up in `build/libs`. 1.21.11 needs Java 21; 26.2 and 26.3 need Java 25.

## Credits

Based on Autoptimization by XLTQ (MIT). Rewritten with working entity hiding, safer threading and new features.

Licensed under MIT.
