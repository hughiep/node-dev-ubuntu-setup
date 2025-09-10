# Node Dev Setup Script for Ubuntu

## Install Git
```bash
sudo apt install git
```

and set up your git config
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

generate ssh key
```bash
ssh-keygen -t ed25519 -C "you@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```
then add the ssh key to your github account
[https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent]

## Install curl
```bash
sudo apt install curl
```

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
