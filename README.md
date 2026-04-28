# Obsidian Idea Manager with Weekly Report

A sovereign, local-first idea management system for Obsidian + AI agents.

<img width="1339" height="747" alt="img_IDEA_SHARE_USE" src="https://github.com/user-attachments/assets/686d89e8-b0d9-46e4-a37f-b7f022daaa07" />

I got tired of watching high-quality ideas disappear into sticky notes, voice memos, random files, and abandoned current.md documents. So I built a system that treats every idea with respect.

Every idea gets a permanent, globally unique ID (ID1, ID2, ID3…). The agent automatically creates structured notes, manages an Active/ inbox, and intelligently categorizes everything into permanent folders.

This is the exact system I use every day. I’m releasing it with no paywall, no newsletter, and no upsell.
<img width="554" height="565" alt="Screenshot 2026-04-28 at 5 54 55 AM" src="https://github.com/user-attachments/assets/08156c00-243f-4290-9461-0ad87380e257" />

**Core Features**

<img width="1333" height="590" alt="Untitled" src="https://github.com/user-attachments/assets/c101bfa1-c612-43c3-9971-52076188c6cb" />

Global sequential idea IDs across your entire vaultFrictionless capture using voice or text ("add an idea...")
Automatic categorization with one commandStrict file safety rules (always reads before writing)
Weekly AI-generated memo that analyzes new ideas, suggests implementations, and proposes new directions
Clean integration with daily notes, weekly reviews, and MEMORY.md

**How to Install**

1. Copy obsidian-idea-manager.skill.md and weekly-idea-memo.skill.md into your skills folder.
2. Have your agent review obsidian-idea-manager,skill,md and add the rule ["Obsidian Idea System Rule"] into your AGENTS.md. Also have your agent review and implement the "Integration Notes for Other Agents."
3. Copy the template from templates/idea-template.md into your templates folder.
4. Create the following folder structure into Obsidian:   

Ideas/ ├── Active/ ├── AI Agents & Automation/ ├── Income & Business/ ├── Content Creation/ ├── Personal Growth/ ├──Implemented/ 

5. Start using it by telling your agent: "add idea: ..."

**How I Use It**

<img width="1361" height="1178" alt="Screenshot 2026-04-28 at 5 46 35 AM" src="https://github.com/user-attachments/assets/a5929925-8d4b-480c-813e-0037e6e0b62d" />

**Add Idea** --> During conversations or while using voice mode, I simply say “add idea” followed by a description. 

**Categorize Ideas** --> Once a week I run the "categorize ideas" categorize command and my agent categorizes all ideas under /Active into relevant subfolders by category.

**Weekly Report** --> My agent delivers a weekly report every Sunday morning with a summary of the week's accomplishments, new suggested ideas, and next steps for implementation.

**Philosophy**

In a world racing toward cloud AI that owns our thoughts and patterns, keeping your idea infrastructure fully sovereign is a meaningful form of digital self-defense.

Your mind is the last frontier. Don’t surrender it.

**Feedback Welcome**

This is my first repo on Github. If you try this system, I’d love to hear from you. Reply with the first ID your agent gives you, or tag me if you improve it or adapt it for your own workflow. The best ideas will probably get folded back into future versions.

**Tips**

1. This skill works best when you keep a running daily log of your progress and conversations with your agents in Obisidian .
2. Point your agent to this repo and have your agent fill in the appropriate information vault path, cron information, etc.
