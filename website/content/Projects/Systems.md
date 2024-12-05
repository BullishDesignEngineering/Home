---
title: Systems
category: PROJECT_NOTES
---
# Computing Setup
Declarative nixOS computing environment, with config files stored in git repository, able to be quickly installed on any system (wsl or linux) for a consistently productive environment.
	Bonus points for having something entirely accessible via plain-text interaction so can be accessed via a terminal (or terminal-like) interface from anywhere at any time (personal development server hosted at home or in the cloud?)

## Structure
 - [Tmux]({{< ref "Tmux" >}}) + [Neovim]({{< ref "Neovim" >}})
	 - Tmux handles organization of multiple neovim panes
	 - Multiple workspaces, one for each project
	 
	 - Panes:
		 - Project browsing
		 - File Browsing
		 - Notes
		 - Coding (1 file focus, multiple file focus)
		 - Coding Output (again, single or multiple output, data, data viz, web, photo, video?)
	 - Keyboard shortcuts and scripts for rapid navigation and iteration
		 - Modular (i.e. - git operations, automatically done for each project's repository)
		 -