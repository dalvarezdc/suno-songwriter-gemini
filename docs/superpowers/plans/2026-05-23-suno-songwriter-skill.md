# Suno Songwriter Skill Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Create a specialized skill for Gemini CLI that formats and enriches lyrics for Suno AI.

**Architecture:** The skill will be implemented as a `SKILL.md` file in a dedicated directory. It will contain YAML frontmatter for registration and a placeholder for the instructions.

**Tech Stack:** Gemini CLI Skill (Markdown + YAML)

---

### Task 1: Create Skill Directory and File

**Files:**
- Create: `skills/suno-songwriter/SKILL.md`

- [ ] **Step 1: Create the directory**

Run: `mkdir -p skills/suno-songwriter`

- [ ] **Step 2: Create the SKILL.md file with metadata**

```markdown
---
name: suno-songwriter
description: Specialized in writing, formatting, and enriching lyrics for Suno AI and other music generation tools. Use when the user provides lyrics or asks for help creating song structure, style tags, and meta-instructions for music AI.
---

# Suno Songwriter

## Instructions
[USER WILL FILL MANUALLY]
```

- [ ] **Step 3: Verify file exists and has correct content**

Run: `cat skills/suno-songwriter/SKILL.md`
Expected: File content matches the above metadata.

- [ ] **Step 4: Commit**

```bash
git add skills/suno-songwriter/SKILL.md
git commit -m "feat: add suno-songwriter skill metadata"
```

### Task 2: Update README

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Update README to mention the new skill location**

```markdown
# suno-songwriter-gemini
Skill for Gemini Client that writes AI music, it is heavily specialized in Suno Prompts, but its good for other music AI tools too

## Skills
- **Suno Songwriter**: Located in `skills/suno-songwriter/SKILL.md`.
```

- [ ] **Step 2: Verify README content**

Run: `cat README.md`

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "docs: update README with skill location"
```
