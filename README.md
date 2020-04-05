# Rofi Power Menu Mode


Rofi Power Menu provides a mode for offering basic power menu operations such as
shutting down, logging out, rebooting and suspending. For irreversible actions,
it also asks for confirmation.

In contrast to other similar solutions I've found, the power menu is implemented
as a rofi mode, not as a stand-alone executable that launches rofi by itself.
This makes it possible to combine the script with the full power of how rofi can
use modi. For instance, you can have multiple modi available (`-modi`) or
combine multiple modi in one mode (`-combi-modi`), pass your own themes
(`-theme`) and configurations as CLI flags (e.g., `-fullscreen`,
`sidebar-mode`).


## Install

You can use the script directly from this directory without needing to install
it at all. If you want rofi to find it more easily, the script needs to be found
in `PATH`. If you have `~/.local/bin` in `PATH`, you can just copy the script
there:

```
cp rofi-power-menu ~/.local/bin/
```


## Usage

A simple example showing how to launch the power menu:

```
rofi -show power-menu -modi power-menu:rofi-power-menu
```

If you didn't install the script in `PATH`, you need to give the path to the
script. If you're running rofi under this directory where the script is, you can
run it as follows:

```
rofi -show power-menu -modi power-menu:./rofi-power-menu
```

The power menu mode offers the following options:

- Lock screen
- Log out (confirmation asked)
- Suspend
- Hibernate
- Reboot (confirmation asked)
- Shutdown (confirmation asked)


## Copyright

Copyright (c) 2020 Jaakko Luttinen

MIT License
