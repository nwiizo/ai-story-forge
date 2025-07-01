# Get Started with AI Story Forge in 5 Minutes

This guide explains how to create your first character and story outline in 5 minutes using AI Story Forge.

## 🚀 Step 1: Project Setup (1 minute)

### Clone the repository
```bash
git clone https://github.com/nwiizo/ai-story-forge.git
cd ai-story-forge
```

### Or, copy only the necessary files
Minimum required files:
- `character-template/CHARACTER.md`
- `character-template/character-prompts.md`

## 📝 Step 2: Character Creation (3 minutes)

### 2-1. Copy CHARACTER.md
```bash
cp character-template/CHARACTER.md my-character.md
```

### 2-2. Fill in basic information
First, please fill in only the following 4 items:
- Name
- Age
- Occupation
- In a nutshell

### 2-3. Deepen the character through dialogue with AI

#### If you are using Claude Code
```bash
# Create a new character
/character new

# Or develop a specific character
/character develop Asuka Sato
```

#### For other AI tools
Copy Step 1 from `character-prompts.md` and paste it into your AI tool (Claude, ChatGPT, etc.):

```
Please set only one most important value for the following person.

[Basic Settings]
- Age: 28
- Occupation: Librarian
- Environment: Public library in a regional city

Conditions:
- Specific and action-guiding
- Something that forms the axis of their life
- In the format "I want to △△ through ○○"
```

Enter the AI's response in the "Core Value" section of `CHARACTER.md`.

## 🎯 Step 3: Create a simple story outline (1 minute)

### If you are using Claude Code
```bash
# Construct a story by specifying the title
/story plot "The Last Letter"

# Or start in interactive mode
/story
```

### For other AI tools
Ask the AI the following:

```
Character: [Summary of the created character]

I want to create a short story with this character as the protagonist.
1. What kind of daily life does it start from? (1 line)
2. What kind of event will occur? (1 line)
3. How will the character change in the end? (1 line)
```

Now your story outline is complete!

## 🎮 Claude Code Command Usage Examples

### Character-related
```bash
/character new                    # Create new (interactive)
/character develop Misaki Tanaka  # Develop existing character
/character check Asuka Sato       # Check consistency
/character dialogue Taro Yamada   # Dialogue simulation
```

### Scene creation
```bash
/scene dialogue Asuka Sato tense   # Dialogue-focused scene
/scene emotion Misaki Tanaka nostalgia 800  # Emotional description (800 characters)
/scene action tense                # Action scene
```

### Quality check
```bash
/quality scene "Discovery of the letter" --detail    # Detailed evaluation
/quality character Asuka Sato           # Character evaluation
/quality story "The Last Letter" --fix       # With improvement suggestions
```

## 💡 Next Steps

### If you have a little more time (+10 minutes)

1. **Deepen the character**
   - Execute Steps 2-5 of `character-prompts.md` in order
   - Enter the answers for each step in CHARACTER.md

2. **Flesh out the story**
   - Use `story-template/STORY.md`
   - Create a 3-act structure
   - Identify 3 important scenes

3. **Quality check**
   - Check with `quality-check/checklist.md`
   - Especially focus on "Character Consistency"

## ❓ Frequently Asked Questions

### Q: Which AI tool is recommended?
A: **Claude Code** allows you to work efficiently with dedicated commands. Otherwise, **Claude Opus 4** is recommended for long text processing, and **ChatGPT** for short dialogues.

### Q: What if the character becomes inconsistent?
A: Return to the "Core Value" in CHARACTER.md. All actions stem from this value.

### Q: What if the story gets stuck?
A: Concentrate on only three important scenes (turning point, emotional peak, theme embodiment) and leave others for later.

## 🎉 Tips for Success

1. **Don't aim for perfection** - You can always revise later
2. **Start small** - Try writing just one scene first
3. **Enjoy dialogues with AI** - Unexpected answers are also a source of creativity
4. **Reflect periodically** - Record prompts that worked well
5. **Utilize commands** - With Claude Code, use `/` for efficiency

## 📚 For Those Who Want to Learn More

- **Detailed techniques**: `story-template/techniques.md`
- **Troubleshooting**: `quality-check/common-problems.md`
- **Theoretical background**: `resources/principles.md`

---

**Are you ready to start?** First, open `CHARACTER.md` and bring your story's protagonist to life!