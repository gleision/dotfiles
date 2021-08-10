# dotfiles
My Polybar and others setup for BSPWM on Linux
> This repository was based on the dotfiles from **siduck76** more precisely from the repository: <https://github.com/siduck76/dotfiles>

# Dependencies
+ [bspwm](https://github.com/baskerville/bspwm)
+ [polybar](https://github.com/polybar/polybar)
+ [fonts](https://github.com/terroo/fonts)
+ [git](https://git-scm.com)
+ [feh](https://feh.finalrewind.org/)
+ ...

# Installation
```sh
git clone https://github.com/terroo/dotfiles
cd dotfiles
mv polybar $HOME/.config
mv Xresources $HOME/.Xresources
```

# Configurations
Add to your `$HOME/.config/bspwm/bspwmrc`:
```sh
xrdb ${HOME}/.Xresources
$HOME/.config/polybar/launch.sh &
$HOME/.fehbg
```

Run:
```sh
feh --bg-scale wallpaper.jpg
```

Log out and start again
```sh
bspc quit
```


