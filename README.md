# Suno Songwriter & Album Concept Designer

A suite of Gemini CLI skills specialized for AI music creation, heavily optimized for Suno AI prompts.

## Included Skills

### 1. Suno Songwriter
Specialized in formatting and enriching lyrics with technical Suno AI tags (`[Verse]`, `(ad-libs)`, etc.). It preserves your lyrics while adding proper meta tags and structural elements for high-quality music generation.
- **Location**: `skills/suno-songwriter/SKILL.md`

### 2. Album Concept Designer
A creative director for building complex conceptual albums. It handles world-building, storyline, character profiles, and narrative tracklists. It generates an "Album Bible" and track specifications.
- **Location**: `skills/album-concept-designer/SKILL.md`

## Installation

### Method 1: Remote Installation (Standard)
Install the skills directly from the GitHub repository.

```bash
# Install globally (available in all projects)
gemini skills install https://github.com/dalvarezdc/suno-songwriter-gemini.git

# OR install only for the current project workspace
gemini skills install https://github.com/dalvarezdc/suno-songwriter-gemini.git --scope workspace
```

### Method 2: Local Extension Installation
If you have cloned the repository locally, you can install it as an extension to automatically discover all bundled skills.

```bash
# Clone the repository
git clone https://github.com/dalvarezdc/suno-songwriter-gemini.git
cd suno-songwriter-gemini

# Install the extension
gemini extension add .
```

### Method 3: Manual Skill Linking (For Development)
If you want to link the skills individually or are developing them locally, you can use the `link` command:

```bash
# Link individual skills
gemini skills link ./skills/suno-songwriter
gemini skills link ./skills/album-concept-designer
```

Alternatively, use the slash command within a Gemini CLI session:
```text
/skills link ./skills/suno-songwriter
/skills link ./skills/album-concept-designer
```

## Usage & Activation

Once installed, the skills are available in any Gemini CLI session. You can activate them using the `activate_skill` tool or by simply requesting them:

- **Explicit Activation**:
  - `activate_skill(name="suno-songwriter")`
  - `activate_skill(name="album-concept-designer")`

- **Natural Language**:
  - "I need help with Suno prompts."
  - "Let's design a concept album."

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
