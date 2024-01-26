# Notes

Miscellaneous notes mainly dealing with all things GNU/Linux.

## Neovim

Neovim purge and install via .deb package
```
apt purge neovim
rm -rf $HOME/git/neovim
rm -rf $HOME/.local/share/nvim
cd $HOME/git
git clone https://github.com/neovim/neovim.git
cd neovim
make CMAKE_BUILD_TYPE=RelWithDebInfo
cd build
cpack -G DEB
sudo apt install ./nvim-linux64.deb
nvim $HOME/.config/nvim/init.lua
```

If installing with make (to /usr/local)
```
apt purge neovim
rm /usr/local/bin/nvim
rm -rf /usr/local/share/nvim
rm -rf $HOME/git/neovim
rm -rf $HOME/.local/share/nvim
cd $HOME/git
git clone https://github.com/neovim/neovim.git
cd neovim
make CMAKE_BUILD_TYPE=RelWithDebInfo
sudo make install
nvim $HOME/.config/nvim/init.lua
```
