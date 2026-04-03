# TargetCharms (retail fork)

WoW **retail** add-on: a small toolbar for **raid target icons** (`/tm`) and **world markers** (`/wm`), plus a ready-check button and setup UI.

## Upstream & lineage

| | Link |
|---|-----|
| **Original add-on** | [Target Charms on CurseForge](https://www.curseforge.com/wow/addons/target-charms) |
| **Prior retail maintenance fork** | [blazer404/TargetCharmsRe](https://github.com/blazer404/TargetCharmsRe) |

This repository continues from that chain with additional fixes and hardening. Credit to **Gander** and everyone who worked on the original and **TargetCharmsRe**.

## Changes in this fork

- Retail **Settings** path for the options panel (no legacy `InterfaceOptions_AddCategory` dependency).
- **Midnight / 12.x:** respect **`IsRaidMarkerSystemEnabled()`** — dim raid-marker buttons, swap macro to a no-op, tooltip when the client disables the raid marker system; refresh on zone/world load and after combat when needed.
- **Bugfix:** `TargetCharms_Reset` setup frame anchoring (undefined `offset`).
- **Bugfix:** layout spacer **`_`** no longer leaves `buttonCharm` nil (avoids compare-with-nil in `FormatButton`).
- Hygiene: duplicate event registration removed, fewer leaked globals, `#string` instead of `strlen` for template length.

## Install

Copy this entire folder into:

`World of Warcraft\_retail_\Interface\AddOns\TargetCharms\`

so that `TargetCharms.toc` sits next to the Lua/XML files.

## License

This fork is dedicated to the public domain under **[CC0 1.0](LICENSE)** (see [Creative Commons CC0](https://creativecommons.org/publicdomain/zero/1.0/)).

*World of Warcraft* and Blizzard marks and game content are property of Blizzard Entertainment. This add-on is not affiliated with or endorsed by Blizzard.

## Repository

**[github.com/Bangerz/TargetCharms](https://github.com/Bangerz/TargetCharms)**

```bash
git clone https://github.com/Bangerz/TargetCharms.git
```

Copy the `TargetCharms` folder into `World of Warcraft\_retail_\Interface\AddOns\`.
