# Design Doc: Suno Songwriter Skill

## Overview
Implement a specialized skill for the Gemini CLI that assists users in writing, formatting, and enriching lyrics specifically for Suno AI. The skill will provide proper meta-tagging, structural elements ([Verse], [Chorus]), and style block construction while preserving the user's original lyrical intent.

## Goals
- Provide a seamless workflow for enriching raw lyrics with Suno-compatible formatting.
- Ensure the agent understands when to activate this specific knowledge set.
- Maintain a clean repository structure for future expansion.

## Architecture

### 1. File Structure
The skill will be housed in a dedicated directory following the standard Gemini CLI skill pattern:
- `skills/suno-songwriter/SKILL.md`

### 2. Skill Registration
The skill will use YAML frontmatter for registration:
- **Name:** `suno-songwriter`
- **Description:** `Specialized in writing, formatting, and enriching lyrics for Suno AI and other music generation tools. Use when the user provides lyrics or asks for help creating song structure, style tags, and meta-instructions for music AI.`

### 3. Logic & Workflow
The implementation will follow these core principles:
- **Preserve + Enhance:** Exact user lyrics must be kept, but enriched with tags.
- **Syllable Flow:** Aim for 6-12 syllables per line.
- **Tag Economy:** Maximum 2-3 meta-tags per section.
- **Specific Formatting:** Use `[ ]` for instructions, `( )` for vocal ad-libs, and avoid `{ }` in final output.

## User Interface
- Users trigger the skill by asking for lyric help or mentioning Suno.
- Output follows a strict 3-part structure:
    1. **Song Title** [code block]
    2. **Style Block** [code block]
    3. **Enriched Lyrics** [code block]

## Testing Strategy
- **Manual Verification:** Test with various inputs (raw lyrics vs. structured, minimal vs. specific style guidance).
- **Format Check:** Ensure all square brackets and parentheses are used correctly according to Suno's engine rules.
