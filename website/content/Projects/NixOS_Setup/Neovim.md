---
title: Neovi
---
#Programming , #IDE, #PDE

# About
A text editor. Modular enough to turn into a full IDE.

# [Python]({{< ref "Python" >}}) IDE Setup

Reference Links:
 - https://www.playfulpython.com/configuring-neovim-as-a-python-ide/

## Notes:
- Vim tmux navigator: https://www.youtube.com/watch?v=qyV_hOtMdwg

# Tutor
## Questions:
 - How to unselect after "substitute"?
 - Need to figure out what "Text Objects" are?
 - How to group multiple lines in nix for ease of reading multi-line settings?

## Notes:
 - Acronyms for all "Normal" key leaders?
	 - s = Substitute
	 - d = Delete
	 - / = search
	 - g = go (current)
	 - G = go to line
	 - c = change
	 - r = replace


# Keymaps:
## Thoughts:
- A sidebar that serves as an access point for various tasks, toggle with space-tab
	- file explorer (e)
	- undo tree (u)
	- buffer/tab navigation shortcuts (b)
	- script list (s)
	- Obsidian (n)
- Other leader groups:
	- Terminal popup (t - terminal)
	- Search/find (s - search)
	- Telescope (f - find)
	- git (g - git)
	- code (c - code)
		- debug
		- format
		- etc
- ***Orrr...... Just use space+tab as a leader for all "sidebar" related things, without calling the sidebar first?***

## Plan:
1. Leverage mini.nvim as much as possible.
	1. [x] Replace Which-key with mini.clue
		1. [ ] Rebuild Keymaps
			1. [ ] Tab (navigation)
				1. [ ] Change Tmux Layout
				2. [ ] Change Tmux Pane
				3. [ ] Switch buffer
				4. [ ] new buffer
			2. [ ] File (mini.files)
			3. [ ] Telescope
			4. [ ] Search
				1. [ ] In buffer
				2. [ ] In active buffers
				3. [ ] In recent buffers
				4. [ ] In project
			5. [ ] git
			6. [ ] code
			7. [ ] Obsidian
			8. [ ] Script drawer
				1. [ ] Change per project?
				2. [ ] Tie into direnv?
	2. [x] Replace NeoTree with mini.files
		1. [x] Create keymap
	3. [ ] Clean up mini folder structure and code formatting
		1. [x] Consistent format, not the "empty = null" bullshit
		2. [ ] 
2. Set up Obsidian
	1. [ ] Set up connection to main "Notes" folder
	2. [ ] Figure out symlinks to project folders
3. Set up Tmux navigation (with TmuxP?)
	1. [ ] New pane
	2. [ ] Switch panes
		1. [ ] From within Neovim, too
	3. [ ] Move pane?
	4. [ ] Resize pane?
4. Figure out clipboard
	1. [ ] "No clipboard provider"
	2. [ ] 





# Plugins:
## Which-Key:
### What is it?
An Nvim plugin for managing keymaps. 
### Resources:
- https://github.com/folke/which-key.nvim
- Potential Tmux version: https://github.com/alexwforsythe/tmux-which-key
- 

### Questions:
- How to integrate with tmux? Possible?
	- investigate: https://github.com/alexwforsythe/tmux-which-key
### Todo:
- [ ] Dig up all existing nvim shortcuts, consolidate into which-key
- [ ]