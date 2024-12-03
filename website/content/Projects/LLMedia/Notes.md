---
title: Notes
id: LLMedia
aliases: LLMedia
tags:
---

# LLMedia

# What:
An LLM based media operation aiming to provide an easily digestible weekly (daily?) rundown of what people ought to know.

Make the entire process open and transparent, front to back, to allow input on the design of the system and let it evolve over time. 

# Why:
Aim to provide truth, without disregarding nuance. 

Empower understanding and action:
 - Why does this matter? 
    - To me
    - To a community
 - What can I do about it?
    - Quick asks
    - Deep involvement

Promote valuable interaction and contribution from the audience. 

Empower the audience to be able to make an impact on the world, ideally starting with their local community. 


# Goals:
 - LLMs serve as distillation of people's interaction with them, providing: 
    - research, 
    - reporting, 
    - editorial, 
    - fact checking, 
    - business related functions of a news organization. 

 - Playwright based web scraper to search and parse websites
    - Use for job hunt application "careers" site scraping

# My Questions:


# Outline:
## UI:
Code editor ui to play with llm code generation. 

### UI Structure:
Treesitter (AST?) based view of the codebase:
- Folder
- File
    - Imports
    - Constants
    - Classes
    - Functions

### Functionality:
- Pull code in context, plus all necessary/relevant code
- Store AST code chunks in database
    - Or utilize git history?
- Popup window to ask llm api for functionality, with or without code context.
- Create new file or folder
- Edit existing code


# Resources:


# Tasks:
 -  Make an inherited SQLModel class for all data response classes. (or for generic call decorator?)
    - Should be able to store input and output to database, as well as any intermediate steps, time called, ranking score, etc.

# Log: