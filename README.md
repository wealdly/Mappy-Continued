# Mappy-Continued

A fork of [Mappy-Continued](https://github.com/Shushuda/Mappy-Continued) / [Mappy](https://github.com/Mundocani/Mappy) addon for World of Warcraft.

Compatible with Midnight!

This fork focuses on fixing combat-related loading issues — the addon now properly initializes and operates when the player is in combat lockdown.

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

* **Combat-safe initialization** — Minimap setup is split into combat-safe and deferred phases so the addon loads correctly during combat
* **Combat guards** — All interactive functions (ghost/unghost, hide/show elements, dragging) gracefully handle combat lockdown
* **Reduced taint** — Button event hooks use HookScript with flag-based control instead of replacing script handlers

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

* [Mundocani](https://github.com/Mundocani) (original author)
* [LynchburgJack](https://github.com/LynchburgJack) (maintainer of [Mappy-Shadowlands](https://github.com/LynchburgJack/Mappy-Shadowlands) fork)
* [Shushuda](https://github.com/Shushuda) (maintainer of [Mappy-Continued](https://github.com/Shushuda/Mappy-Continued))
* [wealdly](https://github.com/wealdly) (maintainer of this fork — combat-loading fixes)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
