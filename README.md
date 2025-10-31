# Node Development Env Setup (Ubuntu)

## Install Git
```bash
sudo apt install git
```

and set up your git global config
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

*Optional
If you are using multiple git accounts, using config file 
```bash
touch ~/.ssh/config
```

Example ssh account config
```bash
Host github.com
   HostName github.com
   PreferredAuthentications publickey
   IdentityFile ~/.ssh/id_hiep
```

Set properly permission for this config file
```bash
chmod 600 ~/.ssh/config
```

## Install zsh
```bash
sudo apt install zsh

# Set zsh as default shell
chsh -s $(which zsh)
```

### Install curl
```bash
sudo apt install curl
```

### Install ohmyzsh
```bash
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
and zsh autosuggestions (optional)
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# add zsh-autosuggestions to plugins in ~/.zshrc
plugins=( 
    # other plugins...
    zsh-autosuggestions
)

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
## Install Docker
Using apt
[]

```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

# Install latest version
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
