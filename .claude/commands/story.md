---
description: "Command for constructing a story step-by-step"
---

# story - Construct a story step-by-step

Guides a 3-phase construction process to weave a story from characters.

## Argument Processing

Command arguments: $ARGUMENTS

If arguments are given, they are interpreted as follows:
- No arguments → Select options interactively
- `new` → Start constructing a new story
- `plot [title]` → Plot development for the specified story title
- `scene [title] [scene_number]` → Detailed creation of a specific scene
- `expand [title]` → Expand a short story into a long one
- `analyze [title]` → Analysis of story structure

## Phased Construction Process

### Phase 1: Skeleton
```
1. Confirm protagonist settings
2. Determine central theme
3. Set beginning and end
4. Create 3-act structure
```

### Phase 2: Identify Important Scenes
```
1. Turning point scene (moment the story moves)
2. Emotional peak scene (most exciting part)
3. Theme embodiment scene (part where the theme is most expressed)
```

### Phase 3: Detailed Scene Design
```
1. External situation (location, time, characters)
2. Internal situation (emotions, desires, fears)
3. Scene flow (introduction → development → turning point → conclusion)
4. Checklist of things to always depict
```

## Execution Examples

### New Creation
```
User: /story new
Assistant: Let's construct a new story!

First, let's start with basic settings:
- Title (can be temporary):
- Genre:
- Estimated character count:
- Protagonist (existing character or new):

Which one shall we decide first?
```

### Plot Development
```
User: /story plot "The Last Letter"
Assistant: Proceeding with plot development for "The Last Letter".

Current settings:
- Protagonist: Misaki Tanaka (45 years old, bookstore owner)
- Theme: Reconciliation with the past and a new step forward

【Detailed 3-Act Structure】

Act 1 (Setup):
1. Struggling bookstore, depiction of Misaki's daily life (1,000 characters)
2. Visit from an old woman, searching for a book (800 characters)
3. Encounter with a book of her mother's memories (700 characters)

Shall we continue developing Act 2?
```

### Scene Creation
```
User: /story scene "The Last Letter" 2
Assistant: "The Last Letter" Scene 2: Encounter with the old woman

【External Situation】
Location: Near the entrance of a dimly lit bookstore
Time: 6 PM, just before closing, already dark outside
Weather: Light rain starting to fall

【Begin Description】
As Misaki was about to close the sales ledger at the counter, the sound of the door's bell echoed in her ears.
"I'm sorry, we're already closed..."
Misaki's words trailed off as she turned around.

An old woman leaning on a cane stood there, her rain-soaked shoulders trembling slightly.

"Could I just... look for a book for a little while?"

[Continue writing?]
```

## Workspace Management

### Story Project Structure
```
my-stories/
└── [work-title]/
    ├── story.md          # Main story
    ├── outline.md        # Plot/structure
    ├── characters/       # Characters in this work
    ├── scenes/          # Individual scene files
    │   ├── scene-01-opening.md
    │   ├── scene-02-meeting.md
    │   └── scene-03-climax.md
    ├── chapters/        # Files per chapter (for long works)
    └── notes/          # Memos/ideas
```

### Starting a New Project
```bash
# Create a directory for the story
mkdir -p my-stories/new-story/scenes

# Copy the template
cp story-template/STORY.md my-stories/new-story/story.md

# Also associate characters
cp my-characters/protagonist.character.md my-stories/new-story/characters/
```

### Version Control
Manage important works in individual Git repositories:
```bash
cd my-stories/important-novel
git init
git add .
git commit -m "First draft complete"
```

### Automatic Exclusion Settings
- All files in `my-stories/` are automatically excluded by `.gitignore`
- No need to worry about personal works getting mixed into the template repository

## Story Construction Tips

### Lost in the Middle Countermeasures
- Place important information at the beginning and end
- Focus on atmosphere and emotion in the middle
- Insert periodic reminders

### Designing the Emotional Curve
```
High |    ★Peak
     |   /  \
     |  /    \★Small hill
Low  |★/      \★
     |Start     End
```

### Scene Transition Techniques
1. Clearly indicate time passage
2. Describe changes in location
3. Follow the psychological changes of the point-of-view character

## Quality Checkpoints

- [ ] Is the protagonist's motivation consistent?
- [ ] Are there any physical contradictions?
- [ ] Is the flow of emotions natural?
- [ ] Is the theme effectively expressed?
- [ ] Does each scene have a clear role?

## Genre-Specific Advice

### Mystery
- Place clues fairly
- Within a range the reader can deduce
- Emphasize logical solutions

### Romance Novel
- Carefully depict emotional subtleties
- Set obstacles realistically
- Show changes in relationships step-by-step

### Fantasy
- Clearly define world-building rules
- But avoid excessive explanation
- Focus on human drama

## Prompt Chain

1. **Conceptualization Phase**
   ```
   Character confirmation → Theme setting →
   Plot creation → Important scene selection
   ```

2. **Writing Phase**
   ```
   Scene design → Draft creation →
   Revision → Quality check
   ```

3. **Finishing Phase**
   ```
   Full read-through → Inconsistency correction →
   Final adjustments → Completion
   ```

## Related Commands

- `/character` - Create the protagonist of the story
- `/scene` - Detailed creation of individual scenes
- `/quality` - Evaluate the quality of the story
- `/dialogue` - Create conversation scenes

## Remember

📝 Stories are nurtured step-by-step. Don't aim for perfection from the start.
📝 Character motivation is the driving force behind everything.
📝 Consider the reader's emotions first.