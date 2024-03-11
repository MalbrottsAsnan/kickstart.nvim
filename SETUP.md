# Custom Neovim Setup and Removal Guide
### By: MålbrottsÅsnan
<br>

## Installation

Follow these steps to install Neovim on a new machine:

1. Install dependencies: ```sudo apt-get install ninja-build gettext cmake unzip curl```
  
    **Note:** If CMake is already installed, clear the cache before proceding: ```rm -r build/  # clear the CMake cache```

3. Clone Neovim repo: ```git clone https://github.com/neovim/neovim```
4. CD into directory: ```cd neovim```
5. Checkout latest stable version: ```git checkout stable```
6. Isolate installation: ```make CMAKE_EXTRA_FLAGS="-DCMAKE_INSTALL_PREFIX=$HOME/neovim"```
7. Build: ```make CMAKE_BUILD_TYPE=Release```
8. Install: ```sudo make install```
9. Add to PATH: ```export PATH="$HOME/neovim/bin:$PATH"```

## Windows terminal preferences

Linux profile settings:
* Color scheme: ```Campbell```
* Font face: ```Hack Nerd Font``` - [Download](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.1.1/Hack.zip "")

**Note:** Install only the ```HackNerdFont-Regular.ttf```

## Uninstalling

Follow these steps to uninstall Neovim from a machine:

1. CD Into directory: ```cd $HOME/neovim```
2. sudo cmake --build build/ --target uninstall

## Updating

To update Neovim built from source, first remove the old version by following **Uninstalling**. After that, you can follow the **Installation** steps to install the latest stable version of Neovim.

**Tip:** Before updating blindly, please compare ```nvim --version``` to the [latest stable version](https://github.com/neovim/neovim/releases/tag/stable "") to confirm whether you need an update or not.
