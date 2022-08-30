# Arch (and its derivatives)

Exact in-order commands for installing `pacaur`:
``` sh
pacman -S git
git clone https://aur.archlinux.org/pacaur.git
sudo pacman -S expac jq
sudo pacman -S base-devel --needed
git clone https://aur.archlinux.org/auracle-git.git
cd auracle-git
makepkg -si
cd ..
cd pacaur
makepkg -si
```

