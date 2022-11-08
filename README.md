General configuration files and setup guide.


# 
# Setup Guide

1. Install ZSH.

        sudo apt install zsh

2. Change default shell to ZSH.

        chsh -s /usr/bin/zsh

3. Setup oh-my-zsh

        sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

4. Setup zsh-autosuggestions

        git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions


5. Setup fzf

        sudo apt insall fzf

6. Install thefuck plugin

        sudo apt update
        sudo apt install python3-dev python3-pip python3-setuptools
        sudo pip3 install thefuck --user

7. Add to plugins in ~/.zshrc


    plugins=( 	git
			zsh-autosuggestions
  			colored-man-pages
			thefuck
			zsh-interactive-cd
			zsh-navigation-tools
	)

8. Add to ~/.zshrc

        eval $(thefuck --alias fck)


9. Install micro

		curl https://getmic.ro | bash

10. Move micro system wide

		sudo mv ./micro /usr/bin


11. Install starship

		curl -sS https://starship.rs/install.sh | sh


12. Configure zsh to use starship

		eval "$(starship init zsh)"
		

13. Configure starship config from ~/.config

		ln -s ~/gits/dotfiles/starship.toml .
