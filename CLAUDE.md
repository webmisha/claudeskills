# CLAUDE.md - AI Assistant Guide for claudeskills

## Repository Overview

**Repository**: claudeskills
**Owner**: webmisha
**Purpose**: A curated collection of user story resources, templates, and educational materials for software development teams and product managers.

This is a **documentation/resource repository** — not a code repository. It contains templates and reference materials for writing effective user stories in agile software development.

## Repository Structure

```
claudeskills/
├── README.md                           # Project overview with links to resources
├── user_story_template.txt             # User story template with examples
├── example-user-stories.pdf            # 100 user story examples
├── User-Stories-Applied-Mike-Cohn.pdf  # Book on user story best practices
└── CLAUDE.md                           # This file
```

## Content Descriptions

### user_story_template.txt
The core template file containing:
- Standard user story format: `As a [role], I want [goal], So that [benefit]`
- Acceptance criteria format using Given/When/Then
- Four complete examples:
  1. Reset Password via Email (authentication)
  2. Profile Description (user profiles)
  3. Data/Analytics example (business analyst use case)
  4. Technical/Infrastructure example (developer use case)

### PDF Resources
- **example-user-stories.pdf**: Collection of 100 user story examples without acceptance criteria
- **User-Stories-Applied-Mike-Cohn.pdf**: Comprehensive book explaining user story theory, principles, and best practices

## Key Conventions

### User Story Format
```
As a [role/persona]
I want [goal or feature]
So that [reason/benefit/value]
```

### Acceptance Criteria Format
Use Given/When/Then structure:
```
Given [context/precondition]
When [action/trigger]
Then [expected outcome]
```

## Working with This Repository

### For AI Assistants

**DO:**
- Reference the template in `user_story_template.txt` when helping users write user stories
- Follow the established format (As a/I want/So that)
- Include acceptance criteria with Given/When/Then format
- Recommend the PDF resources for deeper learning
- Keep documentation concise and practical

**DON'T:**
- Add code files — this is a documentation-only repository
- Modify the PDF files
- Change the established user story format without discussion
- Add unnecessary complexity to the template

### Common Tasks

1. **Creating a new user story**: Use the template from `user_story_template.txt`
2. **Adding examples**: Follow the existing format in the template file
3. **Updating README**: Keep links pointing to the correct files in the repository

## Git Workflow

- **Main branch**: Contains stable, reviewed content
- **Feature branches**: Use for adding new templates or updating existing content
- **Commit messages**: Use clear, descriptive messages (e.g., "Add user story example for checkout flow")

## File Naming Conventions

- Use lowercase with hyphens for new files: `example-filename.txt`
- Keep extensions appropriate: `.txt` for templates, `.md` for documentation, `.pdf` for reference materials

## Dependencies

None — this repository contains only documentation and PDF files with no build system or package dependencies.
