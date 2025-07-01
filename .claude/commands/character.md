---
description: "Command to create, manage, and simulate dialogue with characters"
---

# character - Create characters with AI

Guides the entire character creation process. Starting from motivation, through a personal history, to create a living character.

## Argument Processing

Command arguments: $ARGUMENTS

If arguments are given, they are interpreted as follows:
- No arguments → Select options interactively
- `new` → Create a new character
- `develop [name]` → Develop the specified character
- `check [name]` → Check consistency of the specified character
- `dialogue [name]` → Simulate dialogue with the specified character
- `motivate` → Create a character by selecting from a motivation list

## Basic Flow

### 1. Determine Motivation (Most Important)
```
First, let's decide "what this character wants to do."
Please choose from the list below or provide an original motivation:

【Guardian/Protection Type】
- I want to protect someone important
- I want to protect my hometown
- I want to help the weak

【Growth/Achievement Type】
- I want to become stronger
- I want to be recognized
- I want to fulfill my dream

【Exploration/Discovery Type】
- I want to know the truth
- I want to see the world
- I want to solve a mystery

Your choice:
```

### 2. Create Personal History (30 minutes)
Once the motivation is decided, create the character's outline:
- Basic data (name, age, occupation, etc.)
- Internal elements (likes, fears, dreams, etc.)
- Lifestyle habits (residence, daily routine, catchphrases, etc.)

### 3. Set 3-Layer Structure
- **Layer 1 (Invariant)**: Motivation, values, fears, contradictions
- **Layer 2 (Semi-stable)**: Emotional patterns, relationships, growth direction
- **Layer 3 (Variable)**: Speech style, behavior patterns, gestures

### 4. Confirm Character "Core"
- Things they absolutely will not do
- Things they will always do
- Promises to the reader

## Execution Examples

### For New Creation ($ARGUMENTS = "new")
```
User: /character new
Assistant: Let's create a new character!

First, let's decide on the most important "motivation."
What does this character "want to do"?

1. Choose from a prepared motivation list
2. Set an original motivation

Which do you choose?
```

### For Consistency Check ($ARGUMENTS = "check Asuka Sato")
```
User: /character check Asuka Sato
Assistant: Checking Asuka Sato's consistency.

✅ Motivation "I want to expand people's potential by sharing knowledge."
✅ All actions can be explained by motivation
⚠️ Scene in Chapter 3 where books are handled roughly → Needs correction
✅ Consistency of speech style is maintained
```

### For Dialogue Simulation ($ARGUMENTS = "dialogue Asuka Sato")
```
User: /character dialogue Asuka Sato
Assistant: I will converse as Asuka Sato. Settings loaded.

Hello. I'm Sato from the City Library.
What kind of book are you looking for today?
If you'd like, I can help you.

[Internal thought: A new visitor. I'm curious what kind of books they like.]
```

### For No Arguments ($ARGUMENTS = "")
```
User: /character
Assistant: This is the character management command. What would you like to do?

1. new - Create a new character
2. develop [name] - Develop an existing character
3. check [name] - Check consistency
4. dialogue [name] - Simulate dialogue
5. motivate - Create from motivation list

Please select (1-5):
```

## Workspace Management

### Saving Created Characters
```
# Recommended save location
my-characters/[character-name].character.md

# Examples
my-characters/tanaka-misaki.character.md
my-characters/2025-06-protagonist/hero.character.md
```

### File Management Best Practices
1. **Standardize Naming Conventions**
   - Recommend `[name].character.md` format
   - Romanize Japanese names

2. **Organize with Folders**
   - By work: `my-characters/last-letter/`
   - By period: `my-characters/2025-06/`
   - By role: `my-characters/protagonists/`

3. **Automatically Exclude from Git**
   - Files in `my-characters/` are automatically excluded by `.gitignore`
   - Create personal characters with peace of mind

### Starting from a Template
```bash
# Copy template to start
cp character-template/CHARACTER.md my-characters/new-character.character.md

# Edit with Claude
/character develop new-character
```

## Prompt Chain

1. **Motivation Determination Phase**
   - Select/create motivation
   - Confirm empathy points
   - Predict actions arising from motivation

2. **Detailed Setting Phase**
   - Fill in personal history
   - Incorporate into 3-layer structure
   - Intentionally design contradictions

3. **Verification Phase**
   - Consistency check
   - Create sample scenes
   - Adjust as necessary

## Important Notes

- Strictly avoid imitating existing popular characters
- Motivations should be clear and evoke empathy
- Contradictions should be intentionally designed for human-likeness
- Never let the "core" part become blurred

## Related Commands

- `/story` - Construct a story with the created character
- `/scene` - Create scenes that utilize the character
- `/quality` - Evaluate character quality

## Hints

💡 Treat characters not as a collection of settings, but as living humans.
💡 If you get lost, return to the motivation.
💡 It's important to try creating first, without aiming for perfection too much.