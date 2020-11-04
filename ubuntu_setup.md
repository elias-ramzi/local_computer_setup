# Packages

	sudo apt-get install curl
	sudo apt-get install htop
	sudo apt-get install tree
	sudo apt-get install chromium-browser


# Git

	sudo apt-get install git
	cp configs/gitconfig ~/.gitconfig


# Atom

	wget https://atom.io/download/deb ~/Downloads
	sudo dpkg -i ~/Downloads/atom-amd64.deb
	apm install --package-file atom_package_list.txt


# Kite

	bash -c "$(wget -q -O - https://linux.kite.com/dls/linux/current)"


# Python

	sudo apt-get install python3-pip
	sudo apt-get install python3-venv


# SSH key

	mkdir .ssh
	# Enter pass phrase when asked
	ssh-keygen -t rsa -C "elias.ramzi@gmail.com"
	eval `ssh-agent`
	ssh-add


# Terminal
    sudo apt-get install zsh
    sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
    chsh -s /usr/bin/zsh
		cp configs/zshrc ~/.zshrc
		cp configs/bash_aliases ~/.bash_aliases
		curl -L git.io/antigen > antigen.zsh
		cp configs/antigenrc ~/.antigenrc
		sudo apt-get install terminator
		sudo apt-get install screen
		sudo apt-get install tmux