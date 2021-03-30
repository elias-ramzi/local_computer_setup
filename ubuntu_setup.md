# Packages

	sudo apt-get install curl
	sudo apt-get install htop
	sudo apt-get install tree


# Git

	sudo apt-get install git
	cp configs/gitconfig ~/.gitconfig


# Atom

	wget https://atom.io/download/deb --output ~/Downloads/atom.deb
	sudo dpkg -i ~/Downloads/atom.deb
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
		sudo apt-get install terminator
		sudo apt-get install screen
		sudo apt-get install tmux
		cp configs/zshrc ~/.zshrc
		cp configs/bash_aliases ~/.bash_aliases
		cp configs/antigenrc ~/.antigenrc
		sudo apt-get install zsh
    sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
		curl -L git.io/antigen > antigen.zsh
		chsh -s /usr/bin/zsh
