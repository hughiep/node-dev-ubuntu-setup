# node-dev-ubuntu-setup
Ubuntu fresh setup - Node dev

- Install Git
sudo apt install git

 - Install zsh
 sudo apt install zsh
 
 - Install ohmyzsh
 sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

- Install nvm
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm

[https://github.com/nvm-sh/nvm?tab=readme-ov-file#install--update-script]

- Install NodeJS
[https://nodejs.org/en/download]
or using nvm
nvm install 22

- Install VsCode
Download setup file [https://code.visualstudio.com/]
sudo dpkg -i path\to\deb\file

