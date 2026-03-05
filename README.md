# Mappy-Continued

A personal fork of [Mappy-Continued](https://github.com/Shushuda/Mappy-Continued) by [Shushuda](https://github.com/Shushuda), which is itself a continuation of the original [Mappy](https://github.com/Mundocani/Mappy) addon by [Mundocani](https://github.com/Mundocani).

Compatible with Midnight!

All credit for the addon's design and features goes to the original authors. This fork adds targeted bugfixes and performance improvements. If Shushuda's upstream repo incorporates these changes, this fork will no longer be needed.

## Features

Mappy-Continued is a minimap addon focused on changing the minimap shape into a sleek square.

Other features include:
* Resizing of the minimap
* Option to move the minimap via Edit Mode only
* Option to move the minimap via addon settings only
* Automatic stacking of minimap buttons along the minimap OR screen
* Pretty-ing the stock Calendar, Mail and Tracking buttons to actually look like buttons
* Zooming in and out with the mouse wheel
* Alpha settings, separate for combat, movement and default state
* Profiles (including being able to set a profile for mounting, dungeon etc)
* Gathering overlay support for Gatherer and GatherMate
* Compatibility with MinimapButtonBag Reborn
* Compatibility with FarmHud
* Bigger and/or blinking gathering nodes
* Classic-style dot for gathering nodes
* Player coordinates

## Changes in this fork

**Combat safety:**
* Initialization split into combat-safe and deferred phases
* All interactive functions guard against combat lockdown
* Button hooks use HookScript to avoid tainting Blizzard script chains
* Protected frame GetPoint calls wrapped in pcall for restricted region safety

**Bugfixes:**
* Fixed implicit global variable writes in coordinate updates
* Fixed housing indoor overlay stuck after logging in inside a house

**Performance:**
* `ADDON_LOADED` unregistered after init

**Visual:**
* Icon smoothing on minimap POI pins and overlays (reduces aliasing on quest markers, vignettes, and tracking icons)

## Slash commands

`/mappy` - Opens options in the Interface window
`/mappy help` - Shows a list of available commands
`/mappy default` - Loads the default profile
`/mappy save settingsname` - Saves the settings under the name settingsname
`/mappy load settingsname` - Loads the settings
`/mappy settingsname` - Shorthand version of /mappy load
`/mappy ghost` - Mouse clicks in the minimap will be passed through to the background
`/mappy unghost` - Mouse clicks work as usual
`/mappy corner TOPLEFT|TOPRIGHT|BOTTOMLEFT|BOTTOMRIGHT` - Sets the starting corner for button stacking
`/mappy reset` - Resets all settings and profiles
`/mappy unlock` - Unlocks the minimap for dragging
`/mappy lock` - Locks the minimap, preventing its movement
`/mappy reload` - Reload Mappy if something doesn't look right (buttons overlapping etc)

## Authors

* [Mundocani](https://github.com/Mundocani) — original author of Mappy
* [LynchburgJack](https://github.com/LynchburgJack) — maintainer of [Mappy-Shadowlands](https://github.com/LynchburgJack/Mappy-Shadowlands) fork
* [Shushuda](https://github.com/Shushuda) — maintainer of [Mappy-Continued](https://github.com/Shushuda/Mappy-Continued), which this fork is based on
* [wealdly](https://github.com/wealdly) — bugfixes and performance improvements

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
