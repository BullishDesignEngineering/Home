---
title: Python
category: PROJECT_NOTES
---
# About
IDE Setup: [Python IDE Setup](obsidian://open?vault=Notes&file=Neovim)

[#NixOS Dev Environments]({{< ref "#nixos-dev-environments" >}})


## devenv
### Resources:
 - https://devenv.sh/basics/
 - https://www.youtube.com/watch?v=unW1zk8terk
 - https://youtu.be/wPp2DJJpCAg?si=iued20K3u6ZAqI1W
 - Web example: https://github.com/cachix/devenv/tree/main/examples%2Ffly.io
 - 

### Notes:
 - Don't have spaces in directories (parent or current)
	 - Fucks with NixOS
		 - https://github.com/cachix/devenv/issues/1307#issuecomment-2202644992
 - 


## Thoughts on a structure for new project creation:
Have a script that generates python devenv folder and structure, and imports standard framework/tooling. 

### Standard Setup (Script needs):
 - Create folder
 - Create devenv
	 - Create env
	 - Use UV
	 - Use Ruff
	 - Use Mypi
	 - Import standard personal library
		 - Data import
		 - Data Analysis
		 - File management + manipulation
		 - 
 - Create Git Repo (private)
 - Push to repo with standard initial commit

### Standard devenv scripts:
 - Save all and commit 
	 - With comment
 - Push to git repo
 - Run Script
	 - Different scripts, including standard personal library
 - Run app 


## Notes:
### To run scripts:
Just put a "scripts.ScriptName.exec = "python path/to/script/file.py"" in the devenv.nix file