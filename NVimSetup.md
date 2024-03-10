# How to install and setup Neovim

## Installing Neovim

Follow these steps to install Neovim on a new machine:

* Install dependencies: ```sudo apt-get install ninja-build gettext cmake unzip curl```
* Clone Neovim repo: ```git clone https://github.com/neovim/neovim.git```
* CD into directory: ```cd neovim```
* Checkout stable version (0.9.X): ```git checkout v0.9.1```
* Build: ```make CMAKE_BUILD_TYPE=Release```
* Install: ```sudo make install```

**NOTE:** Before installing Neovim, please make sure the following external dependencies are installed: ```git```, ```make```, ```cmake```, ```unzip```, ```gcc```, ```ripgrep```

https://github.com/ryanoasis/nerd-fonts/releases/download/v3.1.1/Hack.zip

## Additional install

https://github.com/ryanoasis/nerd-fonts/releases/download/v3.1.1/Hack.zip

**NOTE:** Install only the ```HackNerdFont-Regular.ttf```

## Windows terminal

Color scheme: ```Campbell```
Font face: ```Hack Nerd Font```
