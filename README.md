# Node Dev Setup Script for Ubuntu

## Install Git
sudo apt install git

## Install zsh
```bash
sudo apt install zsh
chsh -s $(which zsh)
source ~/.zshrc
```

## Install ohmyzsh
```bash
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
and zsh autosuggestions (optional)
```bash
git clone git://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
# add zsh-autosuggestions to plugins in ~/.zshrc
echo "plugins=(git zsh-autosuggestions)" >> ~/.zshrc
# then source ~/.zshrc
source ~/.zshrc
```

## Install nvm
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
source ~/.zshrc
```

[https://github.com/nvm-sh/nvm?tab=readme-ov-file#install--update-script]

## Install NodeJS
[https://nodejs.org/en/download]

or using nvm
```bash
nvm install 22
```
- Install VsCode
Download setup file [https://code.visualstudio.com/]

```bash
sudo dpkg -i path\to\deb\file
```
