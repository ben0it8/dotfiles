# my dotfiles

based on https://developer.atlassian.com/blog/2016/02/best-way-to-store-dotfiles-git-bare-repo/  
additions: oh-my-zsh

### dependencies
* curl
* git

### init

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
echo "ZSH=$HOME/.oh-my-zsh" >> ~/.zshrc
echo "source $ZSH/oh-my-zsh.sh" >> ~/.zshrc
echo "ZSH_THEME='robbyrussel'" >> ~/.zshrc
echo "plugins = (git python osx web-search vi-mode dotenv" >> ~/.zshrc
echo "alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'" >> ~/.zshrc
source ~/.zshrc
echo ".cfg" >> .gitignore
git clone --bare https://github.com/ben0it8/dotfiles.git .cfg/
config checkout
config config --local status.showUntrackedFiles no
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
### gist
```
curl -Lks http://bit.do/init-dotfiles | /bin/bash
```
