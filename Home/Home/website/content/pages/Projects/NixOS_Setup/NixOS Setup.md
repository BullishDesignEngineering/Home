---
title: NixOS Setup
---
# [NixOS]({{< ref "NixOS" >}})
Notes and config files for a fresh NixOS install

# Notes
## Overall goal:
	- Github based nixos install files suitable for both a framework and wsl2 installation.
	- Be able to quickly get up to speed on any new system and immediately fall into the same working environment. 

## Ongoing Questions:
- How to swap keys? Tried:
	 - https://discourse.nixos.org/t/how-to-remap-caps-lock-to-ctrl-while-keeping-ctrl-as-ctrl/13911
	 - https://discourse.nixos.org/t/configuring-caps-lock-as-control-on-console/9356
	 - look up: interception-tools
		 - https://search.nixos.org/options?channel=unstable&show=services.interception-tools.enable&from=0&size=50&sort=relevance&type=packages&query=interception-tools
 - How best to create global scripts?
 - How to setup Python Environment?
	 - Attempting with Devenv
 - How to update NixOS and assorted home-manager installed packages?
	 - See below (how to update the system)


## How to Update the System:

Per (https://nixos-and-flakes.thiscute.world/nixos-with-flakes/update-the-system):
1. Go to dotfiles directory
2. Run "nix flake update" 

## How to Modify:
1. Base level system config is the flake.nix file
2. Main changes from the .home file, which is imported into the flake.nix
3. (Real base level config is the configuration.nix file? - But just for true base level files)
4. When modifying the dotfiles directory structure, need to push to github first?
	1. https://discourse.nixos.org/t/nix-flakes-nix-store-source-no-such-file-or-directory/17836/8
	2. Whyyyy?

## Steps:
1. NixOS install
2. Home Manager
3. Flakes
4. Github connection
5. Kitty
6. Tmux
7. Neovim
8. i3 (?)
	
## NixOS install:
	Resources:
		Used Vimjoyers intro video: https://www.youtube.com/watch?v=a67Sv4Mbxmc
			- later failed, couldn't figure out why
		https://nixos-and-flakes.thiscute.world/nixos-with-flakes/start-using-home-manager
		https://librephoenix.com/2023-10-21-intro-flake-config-setup-for-new-nixos-users.html
		https://librephoenix.com/2024-03-14-managing-your-nixos-config-with-git
		https://codeberg.org/justgivemeaname/.dotfiles
		    - Good organization split -> packages + scripts separate
	    https://github.com/anotherhadi/nixy/tree/main
	        - Great examples for importing packages
        
	Questions:
		How to figure out how to install programs?
	
## Home Manager:
	Resources:
	
	Questions:
	
## Flakes:
	Resources:
		- Keep in mind Modularization:
			- https://nixos-and-flakes.thiscute.world/nixos-with-flakes/modularize-the-configuration
	Questions:

## [Kitty]({{< ref "Kitty" >}}):
A terminal program. GPU does the heavy lifting, so it's supposed to be nice and snappy.
	Resources:
	
	Questions:
	

## [Tmux]({{< ref "Tmux" >}}):
	Resources:
		https://github.com/novoid/nixos-config
	Questions:

	ToDo:
		1. ~~Configure via Nix Flake~~ 
			1. Trying "Tmuxp" first for configuration and session management
				1. Where to store the tmuxp template files?
		2. Need a file explorer/manager
		3. Figure out expanding/collapsing window panes
		4. Keybindings for navigating between panes (preferably vim navigation)
		5. Have default "work" and "play" templates
		7. Browser integration?
		8. 

	
## [Neovim]({{< ref "Neovim" >}}):
	Resources:
		https://gist.github.com/nat-418/d76586da7a5d113ab90578ed56069509
		https://gist.github.com/nat-418/493d40b807132d2643a7058188bff1ca
		https://github.com/anotherhadi/nixy/tree/main
	Questions:

	Todo:
		1. Data analysis template (with Tmux + Nvim)
			1. Import CSV/JSON/XML/HTML file
			2. Parse file
			3. Normalize/modify data
			4. Organize data
			5. Standard analysis toolsuite scripts
			6. Visualize data
			7. Export data