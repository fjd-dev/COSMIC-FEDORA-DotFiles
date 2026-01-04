## COSMIC-FEDORA-DotFiles


RPM Fusion
``` zsh
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm -y
```

DEVELOPMENT TOOLS
``` zsh 
sudo dnf group install development-tools -y
```

NVIDIA
``` zsh
sudo dnf update -y
sudo dnf install -y akmod-nvidia xorg-x11-drv-nvidia-cuda 
```

BRAVE BROWSER
```zsh
curl -fsS https://dl.brave.com/install.sh | sh
```

ZED EDITOR
``` zsh
curl -f https://zed.dev/install.sh | sh
```

GHOSTTY TERMINAL
``` zsh 
sudo dnf copr enable scottames/ghostty
sudo dnf install -y ghostty
```

GIT SETUP
``` zsh
git config --global user.name "YOURNAME"
git config --global user.email YOUREMAIL

ssh-keygen -t ed25519 -C "YOUREMAIL"
```

OHMYZSH
``` zsh
sudo dnf install -y zsh

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

STARSHIP
``` zsh
curl -sS https://starship.rs/install.sh | sh

eval "$(starship init zsh)"
``` 

TMUX PLUGIN MANAGER
``` zsh
sudo dnf install -y tmux
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

MISE
``` zsh
curl https://mise.run | sh

mise use -g go
mise use -g uv
mise use -g python
mise use -g node
mise use -g deno
```

GO PATH
``` zsh
go env -w GOPATH=$HOME/.dev/go
```

YAZI FILEMANAGER
``` zsh
sudo dnf copr enable lihaohong/yazi
sudo dnf install -y yazi
```

OLLAMA
``` zsh
curl -fsSL https://ollama.com/install.sh | sh
```

GITHUB CLI
``` zsh
sudo dnf install dnf5-plugins
sudo dnf config-manager addrepo --from-repofile=https://cli.github.com/packages/rpm/gh-cli.repo

sudo dnf install -y gh
```
