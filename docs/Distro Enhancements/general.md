# Any Distro

## Battery

Install TLP to optimize your battery consumption. Installation steps can be found [here](https://linrunner.de/tlp/).

## Terminal

To enhance your terminal experience, consider checking out [tmux](https://github.com/tmux/tmux). It's a "terminal multiplexer", allowing you to have multiple terminal panes open on a single screen.

## GRUB

To configure your GRUB menu head over to:

```bash
cd /etc/default/
sudo vim grub
```

Commonly edited settings include:
* `GRUB_TIMEOUT` to set the number of seconds the GRUB menu will be up
* `GRUB_DEFAULT` to choose which OS on the GRUB menu is autoselected. Note, 0 is the topmost level

When you're finished with all you're edits, perform the following:

```bash
sudo upgrade-grub
sudo update-grub
```

To customize the look of the menu, check out [matter](https://github.com/mateosss/matter).

## Code
After installing Visual Studio Code, you might have realized that there's an additional bar at the top, 
using up space. To remove this bar, follow these steps:

1. In the File menu, select File -> Preferences -> Settings
2. Search for `window.titlebarstyle`
3. Change `Window: Title Bar Style` to `custom`


## Mouse

Install [key-maper](https://github.com/sezanzeb/key-mapper) to map the side buttons of your mouse (if there are any).

