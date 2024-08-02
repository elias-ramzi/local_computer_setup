# Install

sudo apt-get update

## Packages

sudo apt-get -y install curl

sudo apt-get -y install htop

sudo apt-get -y install tree

## Git

sudo apt-get install -y git

cp configs/gitconfig ~/.gitconfig

## SSH key

mkdir .ssh
<!-- Enter pass phrase when asked -->
ssh-keygen -t rsa -C "elias.ramzi@gmail.com"

eval `ssh-agent`

ssh-add

## Terminal

sudo apt-get install -y terminator

sudo apt-get install -y screen

sudo apt-get install -y tmux

sudo apt-get install -y zsh

cp configs/zshrc ~/.zshrc

cp configs/bash_aliases ~/.bash_aliases

cp configs/antigenrc ~/.antigenrc

cp configs/tmux.conf ~/.tmux.conf

sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" --unattended

curl -L git.io/antigen > antigen.zsh

chsh -s /usr/bin/zsh

## Python

sudo apt-get install -y python3-pip

sudo apt-get install -y python3-venv

### miniconda

mkdir -p ~/miniconda3

wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh

bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3

rm -rf ~/miniconda3/miniconda.sh

~/miniconda3/bin/conda init zsh
