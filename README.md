# dotfiles
![Screenshot](https://boo.s3.nl-ams.scw.cloud/dot)

## Installation
**NOTE**: This is NOT an Arch installation guide. It is **recommended** to fully read this readme first before starting anything.
1. Prerequisites
    - Install [these packages](#packages-used) using your package manager
    - Install [this font](#font) either using your package manager or manually
    - Install `requests` package globally from `python-pip`
    - Clone this repo
1. Configuration
    - Copy the required config files from this repo to their respective config path, which you can also [find here](#packages-used)
    - Copy the `wrappedhl` file to `/bin/` and give it execute perms
    - Copy the `wrappedhl.desktop` file to `/usr/share/wayland-sessions/`
    - (Optional) Copy the `.wallpaper.jpg` file to `~/`
1. Enjoy!
    > Next time you login, select `Hyprland wrapped` as the active session.

If you run into problems, check out the [common problems](#common-problems) section.

## Packages used
Below are the valid configuration directory/file paths listed
- [alacritty](https://wiki.archlinux.org/title/Alacritty#Configuration) - terminal emulator
  - `~/.config/alacritty/alacritty.yml`
  - `~/.alacritty.yml`
- [fish](https://wiki.archlinux.org/title/Fish#Configuration) - shell
  - `~/.config/fish/config.fish`
- [flameshot](https://wiki.archlinux.org/title/Flameshot) - screenshot tool
- [hyprland](https://wiki.hyprland.org/Getting-Started/Master-Tutorial/) - window manager
  - `~/.config/hypr/hyprland.conf`
- [light](https://wiki.archlinux.org/title/Backlight#light) - backlight controller
  - `~/.config/light/`
- [playerctl](https://github.com/altdesktop/playerctl#playerctl) - media playback controller
- [python & python-pip](https://wiki.archlinux.org/title/Python) - run waybar weather script
- [swaybg](https://man.archlinux.org/man/community/swaybg/swaybg.1.en) - background setter
- [waybar](https://github.com/Alexays/Waybar/wiki) - wayland status bar
  - `~/.config/waybar/`
  - `~/waybar/`
  - `/etc/xdg/waybar/`
- [xdg-desktop-portal & xdg-desktop-portal-gtk & xdg-desktop-portal-wlr](https://github.com/flatpak/xdg-desktop-portal) - required for file dialog boxes, screenshots, etc.

## Font
This config is using JetBrainsMono [NerdFonts patched version](https://github.com/ryanoasis/nerd-fonts) and thus it is mostly configured to use that.
I personally use the `ttf-jetbrains-mono-nerd` package from the [AUR](https://archlinux.org/packages/community/any/ttf-jetbrains-mono-nerd/).

## Backlight
It is configured to work on my system and may not work on yours. By default my user did not have write access to modify the brightness so I created a udev rule.

## Common problems
- The brightness control does not work.
    > Copy `udev-rules/backlight.rules` to `/etc/udev/rules.d/`.
    > 
    > If it *still* doesn't work, try modifying the device path inside of the file from `/sys/class/backlight/intel_backlight/brightness` to one that applies to your system [(info)](#backlight).

- Screenshots don't work.
    > Make sure `xdg-desktop-portal` and `xdg-desktop-portal-wlr` are installed.
