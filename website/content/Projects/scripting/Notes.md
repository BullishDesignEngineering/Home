---
title: Notes
id: Scripting
aliases: Scripting
tags: [  ]
category: PROJECT_NOTES
---
# Scripting

# What:


# Why:


# Goals:


# My Questions:
## Navigation scripts
- Can you create a new pane over an existing one from a different directory?
    - Will Neovim call commands on it as if it is in that directory?


# Outline:
## Environment updating scripts
### Update all-NixOS Script 

## Devenv Scripts:
- [x]  Replace devenv.nix with templated devenv.nix file 
    - Programmatically replace template sections
        - CLI app style?
- [ ] Create "Programming init" script:
    - Create template folders 
    - Create template files
    - import standard toolbox:
        - CLI script library?


2. Generate Environment Scripts:
    - If a "scripts.py" file exists:
        - generate a scripts.nix file from it, where each script call in the scripts.py file gets turned into a separate nix script.


## Navigation Scripts:
1. Open reference file:
    - Create a new Tmux pane over the notes pane
        - Open Telescope to search for file
    - Trigger again to switch back to the notes pane sitting behind it.
    - Activate from clue.nvim menu?

## Boot Startup Script:
1. Open list of files on startup
    - Put it in the tmuxp yaml file as a shell command after opening nvim?


# Resources:


# Tasks:


# Notes: