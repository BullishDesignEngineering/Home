---
name: ObsidianFile
imports: ['parsy', 'word', 'obsidian_frontmatter', '[parsing_models/Systems#Computing Setup]({{< ref "parsing_models/Systems#computing-setup" >}})']
status: processed
---
# regex_pattern:
```python
r"^---\s*\n"  # Start of frontmatter
r"(?P<frontmatter>.*?)"  # Non-greedy match for frontmatter
r"\n---\s*\n"  # End of frontmatter
[test link - mid codeblock]({{< ref "project_areas/analysis/" >}})
r"(?P<content>.*)",  # Capture the rest as content
re.DOTALL,  # Make '.' match newlines
```

# Match Groups:
## frontmatter
- type: str

## content
- type: str

*Note: Use import links to generate the "from ... import ..." statements. Use Links to header sections to pre-group functions and models into files.*