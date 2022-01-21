# Configurations

## Neovim

### Neovim installation

1. Add the repository
```
sudo add-apt-repository ppa:neovim-ppa/unstable
```

2. Update and install
```
sudo apt-get update
sudo apt-get install neovim
```

### Neovim configurations and plugins

1. Neovim use a different configuration file from Vim. You need to create a file named init.vim under the directory $HOME/.config/nvim (if this directory does not exist, just create one). All configurations can be put into this file.
```
mkdir -p $HOME/.config/nvim
touch $HOME/.config/nvim/init.vim
```

2. Install vim-plug as plugin manager for neovim.
```
 curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

```

Add the following lines at the bottom of your ~/.config/nvim/init.vim file.
```
call plug#begin()
Plug 'honza/vim-snippets'
call plug#end()
```

Launch nvim, execute PlugInstall, update the plugins, and exit.
```
nvim
:PlugInstall
:wq!
```
