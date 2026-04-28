---
name: idea-manager
description: Use this skill whenever the user says "add an idea", "new idea", "capture this idea", "add to obsidian ideas", "ID", "categorize ideas", "organize ideas", or wants to manage their Obsidian idea system. Automatically assigns sequential global IDs, uses structured templates, respects Active/ category folders, and follows safe file operations.
version: 1.0.0
slug: idea-manager
---

# Idea Manager

**A complete, shareable Obsidian idea management system** for AI agents (and adaptable to any AI assistant).

## Overview

This skill turns casual "add idea" statements into permanent, structured, searchable Obsidian notes with **global sequential IDs** (ID47, ID48...), automatic categorization, and consistent formatting. It eliminates idea loss and makes weekly reviews or "categorize ideas" commands trivial.


## When to Use

Trigger on any of these phrases (or similar intent):
- "add idea", "new idea", "capture this as an idea"
- "add this to ideas", "make this IDxx"
- "categorize ideas", "organize my ideas", "process Active ideas"
- Any request to turn a thought, note, or observation into a permanent idea entry

## Folder Structure (Vault Root)

```
Ideas/
├── Active/              # Temporary holding for new/uncategorized ideas (only scan this for "categorize")
├── AI Agents & Automation/
├── Content Creation/
├── Productivity Tools/
├── Research Projects/
├── Income & Business/
├── Implemented/         # Moved here when completed
├── ... (other categories as needed)
└── 
```


## Core Workflow (Follow Exactly)

1. **Read the rules first**: Always start by reading this SKILL.md, the user's AGENTS.md (for the Idea System Rule), and `self-improving/memory.md` (if available).

2. **Determine next ID**:
   - Scan **all** `.md` files under `Ideas/` (recursive).
   - Extract the highest number from filenames matching `ID(\d+)` pattern.
   - Next ID = highest + 1. Pad as IDnn (two digits minimum).

3. **Choose category/folder**:
   - Infer from content or ask user.
   - Default new ideas to `Ideas/Active/`.
   - For "categorize ideas" command: **only** process files currently in `Ideas/Active/`. Move each to the most appropriate permanent category folder.

4. **Create structured note**:
   - Filename: `ID{{next}} - {{Short Title}}.md`
   - Use the exact template below (or the one in Templates/Idea-Template.md if present).
   - Use safe file operations: read target location first, use precise `edit` or append, re-read and quote the added content to verify. Never overwrite entire files blindly.

5. **After creation**:
   - Log the addition to today's daily note (`memory/YYYY-MM-DD.md` or Obsidian daily) under a checkpoint heading.
   - If it's a major idea, update `MEMORY.md` or `self-improving/memory.md`.
   - For categorize runs, confirm moves with user before final write.

## Exact Idea Note Template

```markdown
# ID{{ID}} - {{Descriptive Title}}

## Description
{{1-2 paragraph clear description}}

## Why This Matters
{{Business/personal impact, alignment with pillars (Sovereign Second Brain, Autonomous Agent Systems, Knowledge Management, Data Privacy)}}

## Implementation Ideas
- {{Bullet list of possible approaches}}
- {{Technical notes}}

## Next Steps
- [ ] First actionable task
- [ ] Second task

## Related Ideas
- [[IDxx - Related Title]]
- Links to existing notes

## Priority
High / Medium / Low

## Tags
#idea #ai #automation #income (relevant tags)
```

Fill intelligently from user's description. Make title concise but descriptive.

## Rule that can be added to AGENTS.md if necessary

**Obsidian Idea System Rule:**
- `Ideas/Active/` is temporary holding for new/uncategorized ideas.
- All other ideas live in category-specific folders directly under `Ideas/` (create new categories as needed).
- When user says “categorize ideas”, **only scan and process items in `Ideas/Active/`**.
- For each idea, move it into the most appropriate category folder.
- Always use sequential IDs: scan **all subfolders** under `Ideas/` to determine the next available ID.
- New ideas saved as full structured markdown notes (using the template above) with sections for description, why it matters, implementation ideas, next steps, related ideas, priority, and tags.


## Integration Notes for Other Agents

- In their AGENTS.md, add: "When user wants to add an idea to Obsidian, read `skills/obsidian-idea-manager/SKILL.md` and follow it exactly. Use self-improving-proactive-agent skill" if available.
- They must have the `read`, `write`, `edit`, and `exec` tools available.
- Emphasize File Operation Integrity Rule (from SOUL.md): never claim a file is updated without tool confirmation + re-read + quote.

This package is complete, tested in production here, and generic enough for anyone using Obsidian + an AI agent. Others can drop it in and immediately start saying "add an idea: [thought]" and get professional structured notes.

**Status:** Production-ready and shareable by SelfSovereignAI (2026-04-24). Created per user request to package the idea management process.
