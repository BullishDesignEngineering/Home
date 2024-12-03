---
title: Tmux
---
#Programming 

# What is it?
A window switcher? Need to investigate and determine where/how this overlaps with the desktop itself. 
- Learned a lot since. 
- "Terminal Multiplexer"
	- AKA - Multiple terminals, able to let them hang out in the background, call them back when needed
	- 
# My Questions:
- If I have two windows with shared panes, does each pane count twice memory/processor wise? 
	- /Is it possible to actually "share" panes?
	- Could be useful for mimic-ing having pane "stacks" - sidebar that switches between file explorer and notes, for example.
- Is it possible for a pane to resize when it is the main focus?
	- Or change border/outline/etc
- What controls the spacebar menu? Which-key? Telescope?

# Why?
Really useful when SSH-ing into another server/computer. Can also script it to auto spin things up when you initially start up so things are ready. 

Can also have multiple things happen simultaneously: Run tests, examine output while you flip through the main code, call up another test run and compare output 1 vs output 2.

Also great in case scripts/programs crash, you dont kill Neovim (for example). 

# How does it work/How do I want to think about it?
## Panes:
One independent running shell instance
## Windows:
A collection of one or more panes. 
## Sessions:
The overarching "group" of windows.

# How do I want to set it up?
## Goal:
1. Minimize impact from context switching
2. Quickly scaffold new projects
3. 
## Concept:
- Common layout for smoother context switching
- Minimize distractions to focus on task at hand
- Easy reference to tasks and overarching goals
- Easy "flags" to recognize what is accessible from current view without distraction

## Layout:
- Sidebar:
	- Top:
		- Goals
		- Tasks
	- Bottom:
		- Notes
			- Expands when its the focus? 
- Main pane:
	- Top:
		- Currently focused document/task/file
	- Bottom:
		- Terminal
			- Tagged to current project's root
-