---
title: Shell Scripting
---
# What is it?
A shell is a program that runs a coding language (called bash) in the terminal. Bash is the same language used at the command line, shell scripting just allows you to chain longer commands together in one go. Multiple shell instances can be run in one terminal, allowing some amount of multitasking/background processing.

Think of it as more or less the native language the computer talks to itself in, allowing you to speak to it on its own language. 

# Why learn it?
Super handy to perform general functionality of the computer itself - most (all?) functionality of the GUI is just performing shell scripts under the hood, so why not learn what its actually doing?

# My Questions:
1. Is bash actually the same language as what's being used in the command line?
2. Is there a more modular way to import shell scripts into home.nix?
	1. Maybe call out to a folder that reads each shell script saved there?
	2. Or just a single call to a library folder that does the rest?
3. Does an imported .sh file need to be made executable first to import a function?
	1. Nope. See "imported"
# Goals:
1. Have a personal library of shell scripts (that ideally plays well with NixOS) to make life easier/quicker
2. Use to streamline/standardize daily functionality to reduce overhead and make work/life more efficient and effective.
3. 

# Tasks:
1. [x] Figure out how to import from one shell script into another.
2. [ ] Create daily notes file
	1. [x] Using the obsidian plugin?
3. [ ] Create "Main" startup page
	1. [ ] Create list of all project folders via script
	2. [ ] Add list of all projects to main startup page
	3. [ ] Auto-create a daily notes page
		1. [ ] Choosing project "ToDos" for the day loads the project in the background in a Tmux buffer
		2. [ ] Autogens the daily note, populates with the ToDo item in question
	4. [ ] 

# Resources:
- https://en.wikipedia.org/wiki/Chmod
- https://stackoverflow.com/questions/192292/how-best-to-include-other-scripts
- https://stackoverflow.com/questions/10823635/how-to-include-file-in-a-bash-shell-script
- 

# Shell Library Outline:
General idea - make it easy to perform various automated tasks. Start with project initialization, add on from there. So, using subheadings as buckets, it'll need:

## Time:
- Date 
	- Calendar
	- Week number, day number
- Time
- Time elapsed

## Files/Directories:
- [x] Create directory
- [x] Create file
- [x] Get names
	- [x] Files
	- [x] Directories

## Text:
- Find text
- Compare text
- Insert Text
- Append text

## Scripting
- [x] Add script to NixOS
- [ ] Github repo initialization
- [ ] Github Project repo initialization

# Notes:
General notes as things go, not yet organized
## How to make a shell script:
1. Write bash code that would work in the command line, save to a ".sh" file extension
2. First line must be "#!/bin/bash" (if making a script to call by filename, see below for NixOS version)
	1. "#!" means this is executable, the rest just tells shell (remember that its a program, so it needs a hint) that it should run as a bash script
3. in the command line, tell your computer that its executable, not just a regular old file:
	1. Run "chmod +x filename"
		1. chmod = change mode
		2. +x = Add executable mode to the file (so it can be run)
		3. filename = path to the file just written. (Can also add multiple files at once)
## How to make a NixOS shell script
The above way still works if you want to call something by filename. But, if you want to call it by it's own command shortcut, you need to tell NixOS about it. So:
1. Same step one as above - write your script
2. Add to home.nix as a package:
	1. (writeShellScriptBin "command-name" (builtings.readFile filepath))
		1. writeShellScriptBin = NixOS command to take the script and add it to the list of commands that can be run
		2. command-name = the shortcut you want to be able to call it with
		3. builtins.readFile = NixOS command to read the script file you just wrote 
		4. filepath = the file you just write
		
## Importing/calling shell scripts:
Important - there are different ways to call a script from another script. One executes it in the current shell environment, the other calls it in a sub-shell. Calling it in a sub-shell means its a clean slate. No access to any variables previously created in the first shell instance. This can be handy to just get a simple result back without having to worry about leftover/overwritten variables.

## Importing shell functions:
Just import with "source filename.sh". Basically treats everything in that other script as though it's lines are inserted at that point. 

Don't need the "#! bin/bash" for the first line, you can just go with code from the get-go
## Adding script to NixOS:
Attempt 1: Attempted to import scripts from an external nix file as text using builtins.readFile. Failed due to "not being a package"
- A definition for option '' is not of type 'package'.

Attempt 2: Just write a script that adds text directly to the home.nix file. 
- [x] Strip first chunk
- [x] For each script in a script directory:
	- [x] Copy script to dotfiles script directory
	- [x] Create script 

## Script Date:
Built-in day of week and week of year functions exist. Need to confirm how they work around the start of the year?

## New Project Script:
- [ ] Create new project folder
- [ ] Create new Notes folder
	- [ ] And Daily notes subfolder
- [ ] Create note template files:
	- [ ] Notes:
	- [ ] ToDo:
	- [ ] Daily log
- [ ] Initialize dev environment (with git)
- [ ] Add to github (private)
	- [ ] gh repo create {name} --private --source=. --remote=upstream
- [ ] Create 
- [ ]