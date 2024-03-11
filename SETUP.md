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
11. Add to PATH: ```export PATH="$HOME/neovim/bin:$PATH"```

## Windows terminal preferences

Linux profile settings:
* Color scheme: ```Campbell```
* Font face: ```Hack Nerd Font``` - [Download](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.1.1/Hack.zip "")

**Note:** Install only the ```HackNerdFont-Regular.ttf```

## Uninstalling

Follow these steps to uninstall Neovim from a machine:

1. CD Into directory: ```cd $HOME```
2. Uninstall Neovim: ```sudo cmake --build /neovim/build/ --target uninstall```
3. Remove Neovim git clone: ```sudo rm -r /neovim/```

## Updating

To update Neovim built from source, first remove the old version by following **Uninstalling**. After that, you can follow the **Installation** steps to install the latest stable version of Neovim.

**Tip:** Before updating blindly, please compare ```nvim --version``` to the [latest stable version](https://github.com/neovim/neovim/releases/tag/stable "") to confirm whether you need an update or not.
