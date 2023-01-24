# Dotfiles repository

Credit: [Ackama Guide](https://www.ackama.com/what-we-think/the-best-way-to-store-your-dotfiles-a-bare-git-repository-explained/)
## Prerequisite

Install:
- zsh
- git

## tmux
```
# mac
brew install tmux

# tmux plugins
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

## Dotfiles setup on new computer 

### 1. Clone the repository

`git clone git@github.com:PaulQbFeng/dotfiles.git $HOME/.dotfiles`

### 2. Create an alias to send command to .dotfiles while having the work tree as $HOME

`alias dot='/usr/bin/git --git-dir=$HOME/.dotfiles/.git --work-tree=$HOME`

(eventually add it to the `.zshrc`)

### 3. Ignore untracked files at $HOME

`dot config --local status.showUntrackedFiles no`

### 4. Manage dot files

`dot add`, `dot commit` and `dot push` dotfiles modifications

If some dot files are already present, you can overwrite them using `dot restore [dotfile]`
