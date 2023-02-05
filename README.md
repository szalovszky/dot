# dotfiles
![Screenshot](.screenshots/0.jpg)

## Packages used
Below are the valid configuration directory/file paths listed
- [alacritty](https://wiki.archlinux.org/title/Alacritty#Configuration)
  - `~/.config/alacritty/alacritty.yml`
  - `~/.alacritty.yml`
- [fish](https://wiki.archlinux.org/title/Fish#Configuration)
  - `~/.config/fish/config.fish`
- [light](https://wiki.archlinux.org/title/Backlight#light)
- [waybar](https://github.com/Alexays/Waybar/wiki)
  - `~/.config/waybar/`
  - `~/waybar/`
  - `/etc/xdg/waybar/`


## Font
This config is using JetBrainsMono [NerdFonts patched version](https://github.com/ryanoasis/nerd-fonts) and thus it is mostly configured to use that.
I personally use the `ttf-jetbrains-mono-nerd` package from the [AUR](https://archlinux.org/packages/community/any/ttf-jetbrains-mono-nerd/).

## Backlight
It is configured to work on my system and may not work on yours. By default my user did not have write access to modify the brightness so I created a udev rule.
