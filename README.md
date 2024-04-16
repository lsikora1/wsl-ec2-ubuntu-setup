# wsl-ec2-ubuntu-setup

Notes and scripts on common setup for data science. Ubuntu on wsl and Ubuntu on remote server.

## Setting up Ubuntu on Windows
1. Install [Windows Terminal](https://learn.microsoft.com/en-us/windows/terminal/install)

2. Install [WSL](https://learn.microsoft.com/en-us/windows/wsl/install). Run PowerShell or Windows Command in <b>administrator</b> mode and type
```PowerShell
wsl --install -d Ubuntu-22.04
```
3. Set up your Linux username and password. Check [this](https://learn.microsoft.com/en-us/windows/wsl/setup/environment) for guidance on best practices.

4. Update and upgrade packages
```Bash
sudo apt update && sudo apt upgrade
```
5. Install [ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
```Bash
sudo apt install zsh
```
6. Make sure zsh your default shell
```Bash
chsh -s $(which zsh)
```

6. Install [Oh my Zsh](https://github.com/ohmyzsh/ohmyzsh)
```Bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
7. With zsh and oh my zsh installed we can add couple useful plugins. Open the `.zshrc` file with editor
```zsh
nano ~/.zshrc
```
and add zsh-autosuggestions and ssh--agent to plugins
```zsh
plugins=(... zsh-autosuggestions ssh-agent)
```
and add identity you want to add to the ssh-agent if you the name of the keys you want to add are `foo` and `bar.pem`
```zsh
zstyle :omz:plugins:ssh-agent identities foo bar.pem
```
Download the autocompletion plugin
```zsh
sudo git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

```
finally run 
```zsh
source ~/.zshrc
```

7. Install [Docker Desktop on Windows](https://docs.docker.com/desktop/install/windows-install/).


## Setting up Ubuntu on remote server
1. Update and upgrade packages
```Bash
sudo apt update && sudo apt upgrade
```

## Useful resources
* [The Missing Semester of your CS education](https://missing.csail.mit.edu/)