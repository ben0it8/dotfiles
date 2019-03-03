# dotfiles

Based on https://developer.atlassian.com/blog/2016/02/best-way-to-store-dotfiles-git-bare-repo/

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
echo "ZSH_THEME='robbyrussel'" >> ~/.zshrc
echo "alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'" >> ~/.zshrc
source ~/.zshrc
echo ".cfg" >> .gitignore
git clone --bare https://github.com/ben0it8/dotfiles.git .cfg/
config checkout
config config --local status.showUntrackedFiles no
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim

```
## install
```
curl -Lks https://gist.github.com/670ce853ba81084e4a6a833dd3a48302.git | /bin/bash
```
