# Zsh Terminal Aliases

<p align="center">
  <img src="https://res.cloudinary.com/practicaldev/image/fetch/s--qb3_lbxW--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hgac2tanq5qikzh8n87k.png" alt="Zsh Terminal Aliases Logo">
</p>

This repository contains a collection of helpful aliases for your Zsh terminal, designed to streamline your workflow and make common tasks more efficient.

## Table of Contents

- [Getting Started](#getting-started)
- [Aliases](#aliases)
- [Usage](#usage)

## Getting Started

To start using these aliases, you'll need to have Zsh installed on your system. If you haven't already, you can install it using your package manager:

```bash
# Example installation command for Debian-based systems
sudo apt-get install zsh

# Example installation command for macOS using Homebrew
brew install zsh
```
## Aliases
### Terminal
```zsh
alias c="clear"
alias x="exit"
alias e="code -n ~/ ~/.zshrc ~/.aliases ~/.colors ~/.hooks"
alias r="source ~/.zshrc"
```
### History
```zsh
alias h="history -10" # last 10 history commands
alias hc="history -c" # clear history
alias hg="history | grep " # +command
alias ag="alias | grep " # +command
```
### Utils
```zsh
# https://github.com/abishekvashok/cmatrix
# sudo apt install cmatrix / brew install cmatrix
alias m="cmatrix -abs"

# https://htop.dev/
# sudo apt install htop / brew install htop
alias t="htop"

# https://dev.yorhel.nl/ncdu
# sudo apt install ncdu / brew install ncdu
alias d="ncdu --exclude /mnt --color dark" # +path

# https://www.speedtest.net/apps/cli
alias st="speedtest"

# https://github.com/sindresorhus/clipboard-cli
# npm install -g clipboard-cli
alias cb="clipboard"
```
### Git
```zsh
alias gcg="git config --edit --global"
alias gcl="git config --edit --local"
# ⚠ Use next alias with extra caution, you may lose all your changes.
alias guc="git reset --hard HEAD" # undo changes and preserve untracked files
alias gcc="git clean -f -d -x" # clean ALL changes and remove untracked files
alias gcl='git clone'
alias gs='git status'
alias ga='git add'
alias gc='git commit'
alias gp='git pull'
alias gps='git push'
alias gl='git log --oneline'
alias gd='git diff'
alias gco='git checkout'
alias gb='git branch'
```
### npm
```zsh
alias rnm="rm -rf node_modules"
alias rbn="rm -rf build node_modules"
alias rap="rm -rf build coverage node_modules package-lock.json && npm i"
alias cap="clean && rap"

alias npk="npx npkill" #clean unused node_modules
alias nkp="npx kill-port " # +portnumber
alias nfk="npx fkill-cli" # +[<pid|name|:port> …] #kill processes

alias nlg="npm list -g --depth 0" #list global packages installed

alias ni="npm i"
alias nis="npm i -S " # +package@version
alias nise="npm i -S -E " # +package@version
alias nid="npm i -D " # +package@version
alias nide="npm i -D -E " # +package@version
alias nr="npm r " # +package@version

alias nrb="npm run build"
alias nrbd="npm run build:dev"
alias nrbq="npm run build:qa"
alias nrs="npm run start"
alias nrsd="npm run start:dev"
alias nrsq="npm run start:qa"
alias nrt="npm run test"
alias nrtc="npm run test:c" #test with coverage

alias np="npm run build && npm publish"
alias nu="npm unpublish " # +package@version
```
### VSCode
```zsh
alias vc="code"
alias vco="code ."
alias vcp="vsce package"
```
### Make
```zsh
# make shortcut
alias mc="make clean"
alias mfc="make fclean"
alias m="make"
alias c="clear"
```

## Usage

Once you've set up these aliases, using them is a breeze. Simply open your terminal and type the alias you want to use, followed by any required arguments. Here are some examples:

- To clear the terminal screen: Type `c` and press Enter.
- To exit the terminal: Type `x` and press Enter.
- To open important configuration files for editing: Type `e` and press Enter.
- To refresh your Zsh configuration: Type `r` and press Enter.

Explore the `aliases.zsh` file to discover more aliases and their respective commands.

Remember, the beauty of these aliases lies in their ability to make your daily tasks more efficient. Feel free to customize and extend them to suit your specific needs.

<hr><hr>
🌟 **Regain the magic of Linux aliases, no matter what operating system you're on. If you find these aliases helpful, give this repository a star!** ⭐️
<hr><hr>

