---
title: Obsidian
category: PROJECT_NOTES
---
# What is it?
Linked notes

# Why?
Can be useful to tag things from anywhere

# How do I want to set it up?
Multiple folders in different project locations that are symlinks back to a main "Notes" folder.

This way all projects have their notes stored locally (useful for projects where the notes will be instructions, or used for a website/blog text) to minimize context switching.


## Layout
- Main/Daily folder:
	- Daily notes in a {year}.{WeekNum}.{DayNum}.md file format
- Project Folders:
	- Auto create a daily note if it doesn't exist
	- Format of {year}.{WeekNum}.{DayNum}.md 
		- subtitle with actual date
	- Insert sections:
		- Goals
		- Tasks 
		- Accomplishments
			- All tasks checked off get copied to accomplishments on script run
		- Notes
			- General Notes
			- Questions
			- Reminders
			- Learnings
		- Projects:
			- Daily notes for each sub project gets copied in under it's own subheader on save