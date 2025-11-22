*Migrated to [Codeberg.org](https://codeberg.org/tyybbi/notes)*

# Notes

Miscellaneous notes mainly dealing with all things GNU/Linux.

## Neovim

Neovim purge and install via .deb package
```
sudo apt purge neovim
rm -rf $HOME/git/neovim
rm -rf $HOME/.local/share/nvim
cd $HOME/git
git clone https://github.com/neovim/neovim.git
cd neovim
make CMAKE_BUILD_TYPE=RelWithDebInfo
cd build
cpack -G DEB
sudo apt install ./nvim-linux-x86_64.deb
nvim $HOME/.config/nvim/init.lua
```

If installing with make (to /usr/local)
```
sudo apt purge neovim
sudo rm /usr/local/bin/nvim
sudo rm -rf /usr/local/share/nvim
rm -rf $HOME/git/neovim
rm -rf $HOME/.local/share/nvim
cd $HOME/git
git clone https://github.com/neovim/neovim.git
cd neovim
make CMAKE_BUILD_TYPE=RelWithDebInfo
sudo make install
nvim $HOME/.config/nvim/init.lua
```
