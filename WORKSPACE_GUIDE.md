# Workspace Guide - How to Manage Your Works

## Recommended Directory Structure

It is recommended to manage works created using AI Story Forge with the following structure. These directories are excluded by `.gitignore`, so they will not be accidentally committed.

```
ai-story-forge/
├── my-characters/              # Created characters
│   ├── 2025-06-protagonist/    # Organized by date-role
│   │   ├── tanaka-misaki.character.md
│   │   └── notes.md
│   └── 2025-06-supporting/
│       ├── yamada-taro.character.md
│       └── suzuki-hanako.character.md
│
├── my-stories/                 # Created stories
│   ├── last-letter/           # Folder per work
│   │   ├── story.md           # Main story
│   │   ├── outline.md         # Plot
│   │   ├── scenes/            # Individual scenes
│   │   │   ├── scene-01-meeting.md
│   │   │   └── scene-02-revelation.md
│   │   └── quality-checks/    # Quality evaluation records
│   └── digital-ghost/
│       ├── story.md
│       ├── chapters/
│       │   ├── chapter-01.md
│       │   └── chapter-02.md
│       └── character-refs/    # Character settings for this story
│
├── drafts/                    # Work in progress/drafts
│   ├── ideas.md
│   ├── experimental-scene.md
│   └── dialogue-practice.md
│
└── personal-notes/            # Personal notes
    ├── writing-tips.md
    ├── favorite-prompts.md
    └── my-motivation-list.md
```

## File Naming Conventions

### Character Files
- `[name].character.md` - Example: `tanaka-misaki.character.md`
- `[name]-[version].character.md` - Example: `tanaka-misaki-v2.character.md`

### Story Files
- `[title].story.md` - Example: `last-letter.story.md`
- `scene-[number]-[content].md` - Example: `scene-03-confession.md`
- `chapter-[number].md` - Example: `chapter-01.md`

### Work Files
- `[date]-[content].draft.md` - Example: `2025-06-15-opening.draft.md`
- `[content].wip.md` - Example: `climax-scene.wip.md`

## Tips for Organizing Works

### 1. Management by Date
```
my-characters/
├── 2025-06/     # Organize by month
├── 2024-02/
└── archive/      # Old works
```

### 2. Management by Project
```
my-stories/
├── project-mystery-novel/    # Project name
│   ├── characters/
│   ├── plot/
│   └── scenes/
└── project-short-stories/
    ├── story-01/
    └── story-02/
```

### 3. Version Control
Consider managing important works in individual Git repositories:
```bash
cd my-stories/important-novel
git init
git add .
git commit -m "Initial draft"
```

## Security and Backup

### Backing Up Important Works
1. **Cloud Storage**: Regularly back up to Google Drive, Dropbox, etc.
2. **Individual Repositories**: Manage important works in separate private repositories.
3. **Export**: Regularly export in PDF or Word format.

### Ensuring Privacy
- Manage personal settings and characters modeled on real people with particular care.
- Consider using encryption tools if necessary.

## Save Destination when using Claude Code Commands

### Specifying Command Arguments

With Claude Code v1.0.25 and later, you can pass arguments to commands:

```bash
# Character creation (with arguments)
/character new                      # Create new (interactive)
/character develop Misaki Tanaka    # Deepen a specific character
/character check Asuka Sato         # Check consistency
/character dialogue Taro Yamada     # Dialogue simulation
# → Save destination: my-characters/2025-06/[character-name].character.md

# Story creation (with arguments)
/story plot "The Last Letter"         # Construct by title
/story structure "Digital Ghost"    # Create structure
/story theme "Human-AI Coexistence" # Construct from theme
# → Save destination: my-stories/[story-title]/story.md

# Scene creation (with arguments)
/scene dialogue Asuka Sato tense    # Dialogue scene (specify character and atmosphere)
/scene emotion Misaki Tanaka nostalgic 800 # Emotion depiction (specify character count)
/scene action suspenseful           # Action scene
# → Save destination: my-stories/[story-title]/scenes/scene-XX.md

# Quality check (with arguments)
/quality scene "Discovery of the letter" --detail # Detailed evaluation
/quality character Asuka Sato --fix     # With revision suggestions
/quality story "The Last Letter" --compare # Comparative analysis
# → Save destination: my-stories/[story-title]/quality-checks/check-[date].md

# Conversation creation (with arguments)
/dialogue first-meet Asuka Sato Taro Yamada # First meeting conversation
/dialogue conflict Misaki Son --mood tense  # Conflict scene
/dialogue confession --subtext      # Confession (emphasize subtext)
# → Save destination: my-stories/[story-title]/scenes/scene-XX-dialogue.md
```

### Summary of Recommended Save Destinations

## Starting Work from a Template

```bash
# Copy character template to start
cp character-template/CHARACTER.md my-characters/new-character.character.md

# Edit with Claude Code
/character develop new-character

# Copy story template to start
cp story-template/STORY.md my-stories/new-story/story.md

# Construct with Claude Code
/story develop new-story
```

## Efficient Workflow

### Starting a New Work
1. Create character: `/character new`
2. Check character consistency: `/character check [name]`
3. Construct story: `/story plot "[title]"`
4. Create important scenes: `/scene [type] [options]`
5. Quality check: `/quality story "[title]" --detail`

### Improving an Existing Work
1. Evaluate current state: `/quality story "[title]"`
2. Correct problems: `/quality scene "[scene_name]" --fix`
3. Adjust character: `/character develop [name]`
4. Improve conversation: `/dialogue [type] [character]`

---

💡 **Tips**:
- Organize your work folders regularly
- Move completed works to an `archive` folder
- Save favorite prompts in `personal-notes` for reuse
- Utilize Claude Code command arguments for efficiency