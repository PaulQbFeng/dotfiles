# Dotfiles repository

Credit: [Ackama Guide](https://www.ackama.com/what-we-think/the-best-way-to-store-your-dotfiles-a-bare-git-repository-explained/)
## Prerequisite

Install:
- zshrc
- git
- tmux 


## Dotfiles setup on new computer 

### 1. Clone the repository

`git clone git@github.com:PaulQbFeng/dotfiles.git $HOME/.dotfiles`

### 2. Create an alias to send command to .dotfiles while having the work tree as $HOME

`alias dot='/usr/bin/git --git-dir=$HOME/.dotfiles/.git --work-tree=$HOME`

### 3. Ignore untracked files at $HOME

`config config --local status.showUntrackedFiles no`

### 4. Checkout dotfiles

Either all dotfiles 

`dot checkout`

or file by file

`dot checkout [dotfile_1] [dotfile_2] ...`