# First install your arch using WSL or any

Tools used
### zsh,tmux,starship,lsd,bat,zoxide,helix(maineditor),git,lazygit,neovim(astrovim)
Dependencies
### rust, nvim(node version manager)

#### Install script for zsh neovim tmux helix and git

****
*Arch* 
```sh
sudo pacman -S --needed base-devel cmake zsh neovim helix tmux git fzf ripgrep lazygit
```

<!-- *Ubuntu/debian* ``sudo apt install build-essential zsh neovim tmux git fzf ripgrep`` -->

****

****
### yay
```sh
git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si
```
## asdf-vm
```sh
git clone https://aur.archlinux.org/asdf-vm.git && cd asdf-vm && makepkg -si

#CD to home and remove yay folder from clone
rm -rf yay
```

****

### Setup zsh

```sh
zsh
```


#### Oh-my-zsh

```sh 
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

#### Oh-my-zsh *plugins*

``sh 
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
``

``sh 
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
``

in ~/.zhrc add the following in plugins

```sh
plugins=([plugins...] zsh-syntax-highlighting zsh-autosuggestions) 

. /opt/asdf-vm/asdf.sh #for asdf
```

****

## Development dependencies

### Rust Install
`` curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh ``

```sh
rustup component add rust-analyzer clippy rustfmt
```
```sh
sudo pacman -S rust-analyzer
```


### NVM Install(Node Version Manager)
`` curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash ``

### Deno
``curl -fsSL https://deno.land/install.sh | sh ``

### Bun
`` curl -fsSL https://bun.sh/install | bash ``

****

## Awesome Tools Extensions


### Starship (Prompt)
```sh 
cargo install --locked starship  
```
Append on ``~/.zshrc``

```sh 
eval "$(starship init zsh)" 
 ```

### ZOXIDE 
#### Alternative to cd
```sh
cargo install --locked zoxide  
 ```

Append on ``~/.zshrc``

```sh
 eval "$(zoxide init zsh)" 
 ```

### BOTTOM
```sh 
cargo install --locked bottom  
```

### BAT
```sh 
cargo install --locked bat  
```

Append on to replace default ls ``~/.zshrc``

```sh
alias ls='lsd'
alias l='ls -a'
alias lla='ls -la'
alias lt='ls --tree' 
```


### NAVI
```sh
cargo install --locked navi 
```
Append on ``~/.zshrc``

```sh
 eval "$(navi widget zsh)" 
 ```

### BROOT
```sh 
cargo install --locked --features clipboard broot
```

### LSD
```sh 
cargo install lsd  
```

Append on to replace default ls ``~/.zshrc``

```sh
alias ls='lsd'
alias l='ls -a'
alias lla='ls -la'
alias lt='ls --tree' 
```


### DUST
```sh 
cargo install du-dust
```

Append on to replace default du ``~/.zshrc``

```sh
alias du='dust'
```
### FD
```sh 
cargo install fd-find
```

Append on to replace default du ``~/.zshrc``

```sh
alias find='fd'
```

### PROCS
```sh 
cargo install procs
```

### TEALDEER
```sh 
cargo install tealdeer
```

### TOKEI
```sh
cargo install tokei
```

### bandwich
```sh
cargo install bandwhich
```
### bandwich
```sh
cargo install grex
```

## If this is you in the future install heres your one liners

```sh
cargo install --locked starship bat navi zoxide bottom

```

Append on ``~/.zshrc``

```sh
 eval "$(navi widget zsh)" 
 eval "$(zoxide init zsh)" 
 eval "$(starship init zsh)" 
```


```sh
cargo install lsd du-dust fd-find procs tealdeer tokei bandwhich

```

Append on ``~/.zshrc`` alias section

```sh
alias hx="helix" #helix to hx
alias ls='lsd'
alias l="ls -a"
alias lla="ls -la"
alias lt="ls --tree" 
alias cat="bat" # cat to bat
alias cd="z" #cd to z
alias c="clear" #clear
alias du="dust" #du-dust
alias find="fd" #fd-find 
alias vim="nvim" # alternative editor

#Config shortcuts
alias zshconf="hx ~/.zshrc"
alias tmuxconf="hx ~/.tmux.conf"
alias hxconf="hx ~/.config/helix/config.toml"
```


****
# Tmux plugins
```sh
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

****
# LSP
```sh
sudo pacman -S gcc-libs glibc bash-language-server typescript-language-server rust-analyzer
```

****
# Neovim Deps
