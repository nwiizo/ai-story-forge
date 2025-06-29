# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with this repository.

## Project Overview

AI Story Forge (AIと共に物語を鍛える工房) is a comprehensive Japanese-language framework for AI-assisted creative writing. It provides structured templates, methodologies, and command tools for creating consistent characters and compelling narratives using generative AI.

**Key Features**:
- Motivation-driven character development system
- Three-phase story construction methodology  
- Five-axis quality evaluation framework
- Integrated Claude command system
- Workspace management for personal projects

## Repository Structure

```
ai-story-forge/
├── character-template/     # Character development resources
│   ├── CHARACTER.md       # Main character template (3-layer system)
│   ├── character-prompts.md # Character creation prompts
│   ├── motivation-list.md # Comprehensive motivation catalog
│   ├── tips.md           # Best practices and techniques
│   └── examples/         # Sample characters
├── story-template/       # Story construction resources
│   ├── STORY.md         # Story planning template
│   ├── story-prompts.md # Story development prompts
│   ├── techniques.md    # Advanced storytelling techniques
│   └── examples/        # Sample stories
├── quality-check/       # Quality assurance tools
│   ├── checklist.md    # 5-axis evaluation checklist
│   └── common-problems.md # Troubleshooting guide
├── resources/          # Supporting documentation
│   ├── principles.md   # Prompt engineering principles
│   ├── constraints.md  # LLM limitations and solutions
│   └── workflow.md    # 3-week creation program
├── .claude/commands/  # Claude integration commands
│   ├── character.md   # /character command
│   ├── story.md      # /story command  
│   ├── scene.md      # /scene command
│   ├── dialogue.md   # /dialogue command
│   └── quality.md    # /quality command
├── my-characters/    # User's characters (gitignored)
└── my-stories/      # User's stories (gitignored)
```

## Core Methodologies

### 1. Motivation-First Character Development
Characters are built starting from their core motivation ("What does this person want?"), ensuring all actions and behaviors stem from this central drive.

### 2. Three-Layer Character System
- **第1層：不変コア (Immutable Core)**: Core motivation, values, fears, and contradictions
- **第2層：準安定層 (Semi-stable Layer)**: Emotional patterns, relationships, growth direction
- **第3層：可変層 (Variable Layer)**: Speech patterns, behaviors, mannerisms

### 3. Three-Phase Story Construction
- **Phase 1**: Skeleton (basic plot structure)
- **Phase 2**: Key scenes identification
- **Phase 3**: Detailed scene design

### 4. Five-Axis Quality Evaluation
Each scene/story is evaluated on:
1. Character consistency (キャラクター一貫性)
2. Physical logic (物理的論理性)
3. Psychological naturalness (心理的自然さ)
4. Readability (読みやすさ)
5. Emotional impact (感情的インパクト)

## Working with This Repository

### For Template Development
- Maintain Japanese language throughout
- Follow established naming conventions
- Keep examples in designated directories
- Ensure consistency with core methodologies

### For Creative Writing
1. Copy templates to personal workspace:
   ```bash
   cp character-template/CHARACTER.md my-characters/[name].character.md
   cp story-template/STORY.md my-stories/[title]/story.md
   ```

2. Use Claude commands (v1.0.25+ with argument support):
   - `/character new` - Create new character
   - `/character develop [name]` - Develop existing character
   - `/story plot "[title]"` - Start new story with title
   - `/scene dialogue [character] [mood]` - Create dialogue scene
   - `/quality scene "[name]" --detail` - Detailed quality evaluation

3. Personal work is automatically gitignored:
   - `my-characters/*` (except README.md)
   - `my-stories/*` (except README.md)
   - `*.character.md`, `*.story.md`, `*.scene.md`

## Command System Integration

The `.claude/commands/` directory contains five specialized commands (compatible with Claude Code v1.0.25+) that guide users through:
- Character creation with motivation focus (`/character [action] [name]`)
- Story construction with phased approach (`/story [type] [title]`)
- Scene crafting with sensory details (`/scene [type] [character] [mood]`)
- Natural dialogue writing (`/dialogue [type] [characters]`)
- Quality evaluation and improvement (`/quality [target] [options]`)

Each command now supports:
- **Argument handling**: Commands accept `$ARGUMENTS` for flexible usage
- **Clear usage instructions** in Japanese
- **Multiple options and parameters**
- **Practical examples with argument patterns**
- **Integration with project templates**

## Development Guidelines

### When Adding Features
1. Consider how it supports the core methodologies
2. Provide both template and command support
3. Include practical examples
4. Update relevant documentation
5. Maintain backward compatibility

### Quality Standards
- All documentation must be clear and actionable
- Examples should demonstrate best practices
- Commands should guide users step-by-step
- Templates must be flexible yet structured

## Version History
- v0.0.1: Initial release with core templates and commands
- v0.0.2: Added workspace management and .gitignore configuration
- v0.0.3: Enhanced Claude Code command support with $ARGUMENTS handling

## Key Principles
1. **Motivation drives everything** - All character actions stem from core desires
2. **Structure enables creativity** - Templates provide framework, not restrictions
3. **Quality through iteration** - Use evaluation tools to improve continuously
4. **Privacy by default** - Personal creations are never tracked by git

Remember: This repository empowers writers to collaborate effectively with AI while maintaining the human touch that makes stories compelling.