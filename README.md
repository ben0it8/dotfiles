# dotfiles

Based on https://developer.atlassian.com/blog/2016/02/best-way-to-store-dotfiles-git-bare-repo/

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
echo "ZSH_THEME='robbyrussel'" >> ~/.zshrc
echo "alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'" >> ~/.zshrc
source ~/.zshrc
echo ".cfg" >> .gitignore
git clone --bare https://github.com/sgugger/dotfiles.git .cfg/
config checkout
config config --local status.showUntrackedFiles no
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim

```
