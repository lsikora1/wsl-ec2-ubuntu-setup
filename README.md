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
## Setting up Ubuntu on remote server

## Usefull resources
