# Packages

	sudo apt-get install curl
	sudo apt-get install htop
	sudo apt-get install tree
	sudo apt-get install keepassx
    sudo apt-get install vlc
    sudo apt-get install feh


# Chrome

    sudo sh -c 'echo "deb [arch=amd64] https://dl.google.com/linux/chrome/deb/ stable main" > /etc/apt/sources.list.d/google-chrome.list'
    wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
    sudo apt-get update
    sudo apt-get install google-chrome-stable


# i3

	sudo apt-get install i3
	mkdir ~/.i3
	cp configs/i3_config ~/.i3/config


# Git

	sudo apt-get install git

## Config

	cp configs/.gitconfig ~/


# Text editor

## Atom

	sudo add-apt-repository ppa:webupd8team/atom 
	sudo apt update 
	sudo apt install atom 
	apm install --package-file atom_package_list.txt

## Vim

	sudo add-apt-repository ppa:jonathonf/vim
	sudo apt-get update
	sudo apt-get install vim
	mkdir .config/vim
	cp configs/init.vim .config/vim/
	mkdir ~/.vim
	mkdir ~/.vim/pack
	mkdir ~/.vim/pack/default
	mkdir ~/.vim/pack/default/start 
	git clone https://github.com/morhetz/gruvbox.git ~/.vim/pack/default/start/gruvbox
    mkdir -p ~/.vim/autoload ~/.vim/bundle
    curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim
    git clone --depth=1 https://github.com/vim-syntastic/syntastic.git ~/.vim/bundle/
    git clone https://github.com/tpope/vim-fugitive.git ~/.vim/bundle


# Python

	sudo ln -sf /usr/bin/python3 /usr/bin/python

## Pip

	sudo apt-get install python3-pip

## Virtualenv
    sudo apt-get install python3-venv
	sudo pip3 install virtualenv
	pip3 install virtualenvwrapper

## pep-8

	mkdir ~/work
	pip install pylint
	cp configs/.pylintrc ~/work/
    sudo apt-get install flake8


# SSH key

	mkdir .ssh
	# Enter pass phrase when asked
	ssh-keygen -t rsa -C "elias.ramzi@gmail.com"
	eval `ssh-agent` 
	ssh-add

## Add it to github

	cat ~/.ssh/id_rsa.pub
	google-chrome -url http://github.com


# Zsh
        sudo apt-get install zsh
        sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
        chsh -s /usr/bin/zsh
        git clone https://github.com/zsh-users/zsh-autosuggestions ~/work/${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

## Config files

        cp configs/.bash_aliases ~/
        cp configs/.zshrc ~/
