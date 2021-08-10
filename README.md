# dotfiles
My Polybar and others setup for BSPWM on Linux
> This repository was based on the dotfiles from **siduck76** more precisely from the repository: <https://github.com/siduck76/dotfiles>

![Terminal Root - Marcos Oliveira - dotfiles](./dotfiles.jpg "Terminal Root - Marcos Oliveira - dotfiles")

# Dependencies
+ [bspwm](https://github.com/baskerville/bspwm)
+ [polybar](https://github.com/polybar/polybar)
+ [fonts](https://github.com/terroo/fonts)
+ [git](https://git-scm.com)
+ [feh](https://feh.finalrewind.org/) `rm -rf ~/.local/share/fonts`
+ [Lua](https://www.lua.org/)
+ [wmctrl](http://tripie.sweb.cz/utils/wmctrl/) `sudo apt install wmctrl`
> Most of the dependencies mentioned above were made in this video: <https://www.youtube.com/watch?v=CivY-yfRBeY>

# Installation
```sh
git clone https://github.com/terroo/dotfiles
cd dotfiles
```

Backup your Polybar if you already had it
```sh
tar -zcvf polybar-old.tar.gz ~/.config/polybar
```

Move(and/or remove) files
```sh
rm -rf ~/.config/polybar
mv polybar $HOME/.config
mv Xresources $HOME/.Xresources
mkdir -p ~/.config/rofi/scripts
mv menu_apps.sh ~/.config/rofi/scripts/
```
> Remember to have the `reboot` and `poweroff` option set for your username without needing a password in: `/etc/sudoers`

# Configurations
Add to your `$HOME/.config/bspwm/bspwmrc`:
```sh
xrdb ${HOME}/.Xresources
$HOME/.config/polybar/launch.sh &
$HOME/.fehbg
```

Run:
```sh
mv wallpaper.jpg ~/Pictures
feh --bg-scale ~/Pictures/wallpaper.jpg
```

If you want, change the name TERROO to your name, for example:
```sh
sed -i "s/TERROO/$USER/g" ~/.config/polybar/config
```
> If you want also remove the `keyboard` from the bar

If you want the music tracks to appear in the bar when you run MPD, check this video: <https://www.youtube.com/watch?v=tholV10zDi0>

Log out and start again
```sh
bspc quit
```

# Watch Video
[![Dotfiles Marcos Oliveira](./image-to-video "Dotfiles Marcos Oliveira")](https://www.youtube.com/TerminalRootTV)

