# SynthWave '84 for Herdr

A Herdr App layout in the colors of [SynthWave '84](https://github.com/robb0wen/synthwave-vscode) by Robb Owen: deep purple chrome, a dusk gradient behind the panes, neon pink focus ring and accents, and the theme's cyan, yellow, green and coral in the terminals.

It is built from [Agent Workspace](https://github.com/chelebyy/herdr-agent-workspace) by chelebyy, with [space-folders](https://github.com/jankeesvw/herdr-space-folders) by Jankees van Woezik for the spaces list. Their mods ship here, modified and renamed `sw84-*` so they never replace an installed copy: English only, theme colours, a second line per agent saying what it works on, and machine headers in the agents list.

## Files

- `layouts/synthwave-84.json`: the layout.
- `layouts/synthwave-84.svg`: its preview in Settings.
- `themes/synthwave-84.json`: the palette. Named like the layout, so Settings offers it only there.
- `mods/synthwave-84/`: carries the terminal font, [DejaVu Sans Mono](https://dejavu-fonts.github.io/) (Regular and Bold, Bitstream Vera licence, see `fonts/LICENSE.txt`). Herdr loads the fonts in a mod's `fonts/` folder at start; the mod draws nothing.
- `mods/sw84-*`: the layout's panels (sidebar, tabs, agents, spaces, quota and system gauges, task presets, files, status bar, menus).
- `NOTICE` and `licenses/`: where the `sw84-*` mods come from, what changed, and the Apache-2.0 and MIT licences that cover them.

## Install

Needs `node` (system gauges, agent resources, task presets) and `sh`; on Windows also PowerShell. Optional: [`quota-axi`](https://www.npmjs.com/package/quota-axi) for the quota gauge, a system monitor (GNOME, KDE, MATE, Xfce or LXDE's) opened from the system gauges, `python3` for unnamed Pi sessions' subject in the agents list. Task presets read `~/.agents/tasks.json` when it exists, else built-in ones.

```sh
cp layouts/synthwave-84.json layouts/synthwave-84.svg ~/.config/herdr-app/layouts/
cp themes/synthwave-84.json ~/.config/herdr-app/themes/
cp -r mods/synthwave-84 mods/sw84-* ~/.config/herdr-app/mods/
herdr-app do layout.switch '{"name":"synthwave-84"}'
```

Restart Herdr once so it loads DejaVu Sans Mono; until then terminals show JetBrains Mono. `ctrl-shift-l` switches back to your other layouts.

## Limits

Herdr has no colored shadows or text-shadow, and it draws terminal text itself, so the original's neon text glow can't be reproduced. The glow comes from colour alone: a 2px pink focus ring and faint pink dividers. Each agent's own colour (Claude orange, OpenCode purple) the space-folder colours and a few accents stay fixed; the rest follows the theme.
