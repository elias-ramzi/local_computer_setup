# Install

sudo apt-get update

## Packages

sudo apt-get -y install curl

sudo apt-get -y install htop

sudo apt-get -y install tree

## Git

sudo apt-get install -y git

cp configs/gitconfig ~/.gitconfig

## GitHub CLI

(type -p wget >/dev/null || (sudo apt update && sudo apt install wget -y)) \
	&& sudo mkdir -p -m 755 /etc/apt/keyrings \
	&& out=$(mktemp) && wget -nv -O$out https://cli.github.com/packages/githubcli-archive-keyring.gpg \
	&& cat $out | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
	&& sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
	&& sudo mkdir -p -m 755 /etc/apt/sources.list.d \
	&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
	&& sudo apt update \
	&& sudo apt install gh -y

gh auth login

## Claude Code CLI

curl -fsSL https://claude.ai/install.sh | bash

## SSH key

mkdir ~/.ssh
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

### miniforge

wget "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh" -O /tmp/miniforge.sh

bash /tmp/miniforge.sh -b -u -p ~/miniforge3

rm -f /tmp/miniforge.sh

~/miniforge3/bin/conda init zsh
