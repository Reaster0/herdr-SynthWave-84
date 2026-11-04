# SynthWave '84 for Herdr

A Herdr App layout in the colors of [SynthWave '84](https://github.com/robb0wen/synthwave-vscode) by Robb Owen: deep purple chrome, a dusk gradient behind the panes, neon pink focus ring and accents, and the theme's cyan, yellow, green and coral in the terminals.


## Files

- `layouts/synthwave-84.json`: the layout.
- `layouts/synthwave-84.svg`: its preview in Settings.
- `themes/synthwave-84.json`: the palette. Named like the layout, so Settings offers it only there.
- `mods/synthwave-84/`: carries the terminal font, [DejaVu Sans Mono](https://dejavu-fonts.github.io/) (Regular and Bold, Bitstream Vera licence, see `fonts/LICENSE.txt`). Herdr loads the fonts in a mod's `fonts/` folder at start; the mod draws nothing.

## Install

Agent Workspace's mods and `space-folders` must already be installed.

```sh
cp layouts/synthwave-84.json layouts/synthwave-84.svg ~/.config/herdr-app/layouts/
cp themes/synthwave-84.json ~/.config/herdr-app/themes/
cp -r mods/synthwave-84 ~/.config/herdr-app/mods/
herdr-app do layout.switch '{"name":"synthwave-84"}'
```

Restart Herdr once so it loads DejaVu Sans Mono; until then terminals show JetBrains Mono. `ctrl-shift-l` switches back to your other layouts.

## Limits

Herdr has no colored shadows or text-shadow, and it draws terminal text itself, so the original's neon text glow can't be reproduced. The glow comes from colour alone: a 2px pink focus ring and faint pink dividers. Some Agent Workspace mods hardcode their own colors (status dots, gauges, footer buttons) and keep them.
