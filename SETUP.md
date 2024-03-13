# Custom Neovim Setup and Removal Guide
### By: MålbrottsÅsnan
<br>

## Prerequisites

1. Install hacks: ```sudo apt install cmatrix```
2. Run hacks: ```cmatrix```

## Installation

Follow these steps to install Neovim on a new machine:

1. Update and upgrade packages: ```sudo apt update && sudo apt upgrade```
3. Install dependencies: ```sudo apt-get install ninja-build gettext cmake unzip curl```
4. CD into home: ```cd $HOME/```
  
    **Note:** If Neovim has already been built, clear the cache before proceding: ```sudo rm -r $HOME/neovim/build/```

5. Clone Neovim repo: ```git clone https://github.com/neovim/neovim```
6. CD into directory: ```cd neovim```
7. Checkout latest stable version: ```git checkout stable```
8. Build isolated: ```make CMAKE_BUILD_TYPE=Release CMAKE_EXTRA_FLAGS="-DCMAKE_INSTALL_PREFIX=$HOME/neovim"```
10. Install: ```sudo make install```
11. Add ```export PATH="$HOME/neovim/bin:$PATH"``` in ```~/.bashrc```

## Windows terminal preferences

Linux profile settings:
* Color scheme: ```Campbell```
* Font face: [```Hack Nerd Font```](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.1.1/Hack.zip "")

**Note:** Install only the ```HackNerdFont-Regular.ttf```, you do not have to unzip the file!

Terminal action settings:

In order for certain Neovim commands to work (```CTRL-]``` for example), interfering Windows Terminal keybinds needs to be removed. More on how this is done can be found on the [Terminal Setup Guide](https://learn.microsoft.com/en-us/windows/terminal/install#settings-json-file ""). Personally, I remove all keybinds by replacing the "actions": [*stuff here*] with the following array:

<details><summary>Show text</summary>

    "actions": [
        {
            "command": "unbound",
            "keys": "ctrl+shift+w"
        },
        {
            "command": "unbound",
            "keys": "alt+f4"
        },
        {
            "command": "unbound",
            "keys": "enter"
        },
        {
            "command": "unbound",
            "keys": "ctrl+insert"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+c"
        },
        {
            "command": "unbound",
            "keys": "ctrl+minus"
        },
        {
            "command": "unbound",
            "keys": "ctrl+numpad_minus"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+d"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+f"
        },
        {
            "command": "unbound",
            "keys": "ctrl+plus"
        },
        {
            "command": "unbound",
            "keys": "ctrl+numpad_plus"
        },
        {
            "command": "unbound",
            "keys": "alt+down"
        },
        {
            "command": "unbound",
            "keys": "alt+left"
        },
        {
            "command": "unbound",
            "keys": "alt+right"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+left"
        },
        {
            "command": "unbound",
            "keys": "alt+up"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+t"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+1"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+2"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+3"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+4"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+5"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+6"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+7"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+8"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+9"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+n"
        },
        {
            "command": "unbound",
            "keys": "ctrl+tab"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+comma"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+space"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+comma"
        },
        {
            "command": "unbound",
            "keys": "ctrl+comma"
        },
        {
            "command": "unbound",
            "keys": "alt+space"
        },
        {
            "command": "unbound",
            "keys": "shift+insert"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+v"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+tab"
        },
        {
            "command": "unbound",
            "keys": "ctrl+numpad0"
        },
        {
            "command": "unbound",
            "keys": "ctrl+0"
        },
        {
            "command": "unbound",
            "keys": "alt+shift+down"
        },
        {
            "command": "unbound",
            "keys": "alt+shift+left"
        },
        {
            "command": "unbound",
            "keys": "alt+shift+right"
        },
        {
            "command": "unbound",
            "keys": "alt+shift+up"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+down"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+pgdn"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+end"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+home"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+up"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+pgup"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+a"
        },
        {
            "command": "unbound",
            "keys": "menu"
        },
        {
            "command": "unbound",
            "keys": "win+sc(41)"
        },
        {
            "command": "unbound",
            "keys": "alt+shift+minus"
        },
        {
            "command": "unbound",
            "keys": "alt+shift+plus"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+1"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+2"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+3"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+4"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+5"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+6"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+7"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+8"
        },
        {
            "command": "unbound",
            "keys": "ctrl+alt+9"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+p"
        },
        {
            "command": "unbound",
            "keys": "f11"
        },
        {
            "command": "unbound",
            "keys": "alt+enter"
        },
        {
            "command": "unbound",
            "keys": "ctrl+shift+m"
        }
    ],

</details>

## Uninstalling

Follow these steps to uninstall Neovim from a machine:

1. CD Into directory: ```cd $HOME```
2. Uninstall Neovim: ```sudo cmake --build /neovim/build/ --target uninstall```
3. Remove Neovim git clone: ```sudo rm -r /neovim/```

## Updating

To update Neovim built from source, first remove the old version by following **Uninstalling**. After that, you can follow the **Installation** steps to install the latest stable version of Neovim.

**Tip:** Before updating blindly, please compare ```nvim --version``` to the [latest stable version](https://github.com/neovim/neovim/releases/tag/stable "") to confirm whether you need an update or not.
