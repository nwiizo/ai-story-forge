---
description: "Command to create impressive scenes with descriptions that appeal to the five senses"
---

# scene - Create impressive scenes

Creates a scene in a story with rich descriptions that appeal to the five senses.

## Argument Processing

Command arguments: $ARGUMENTS

Argument format: [type] [options]

If arguments are given, they are interpreted as follows:
- `dialogue` → Create a dialogue-centered scene
- `action` → Create an action-centered scene
- `emotion` → Create an emotion-centered scene
- `transition` → Create a scene transition
- `climax` → Create a climax scene

Additional options (specified space-separated):
- Character name
- Atmosphere (tense, calm, etc.)
- Character count
- Scene purpose

Example: `dialogue Asuka Sato tense`

## Argument Parsing Implementation

```javascript
// Parse $ARGUMENTS
const args = '$ARGUMENTS'.trim().split(/\s+/);
let sceneType = args[0] || 'general';
let character = '';
let mood = '';
let length = '';
let purpose = '';

// Parse arguments
for (let i = 1; i < args.length; i++) {
    const arg = args[i];
    
    // If it's a number, treat as character count
    if (/^\d+$/.test(arg)) {
        length = arg;
    }
    // Words representing atmosphere
    else if (['tense', 'calm', 'quiet', 'chaotic', 'joyful', 'sad', 'nostalgic', 'suspenseful'].includes(arg)) {
        mood = arg;
    }
    // Otherwise, treat as character name
    else if (!character) {
        character = arg;
    }
    // Concatenate second and subsequent strings as purpose
    else {
        purpose += (purpose ? ' ' : '') + arg;
    }
}
```

## Using Parsed Results

```javascript
// Display parsed results
if (args.length > 0 && args[0] !== '') {
    console.log('【Arguments Parsed】');
    console.log(`- Scene Type: ${sceneType}${getSceneTypeDescription(sceneType)}`);
    if (character) console.log(`- Character: ${character}`);
    if (mood) console.log(`- Atmosphere: ${mood}`);
    if (length) console.log(`- Character Count: ${length} characters`);
    if (purpose) console.log(`- Purpose: ${purpose}`);
    console.log('');
}

// Get scene type description
function getSceneTypeDescription(type) {
    const descriptions = {
        'dialogue': ' (Dialogue-centered)',
        'action': ' (Action-centered)',
        'emotion': ' (Emotion-centered)',
        'transition': ' (Scene transition)',
        'climax': ' (Climax)',
        'general': ' (General scene)'
    };
    return descriptions[type] || '';
}

// Generate scene based on arguments
if (sceneType && sceneType !== 'general') {
    generateScene(sceneType, character, mood, length, purpose);
} else {
    showSceneTypeMenu();
}
```

## Basic Scene Structure

### 1. Situation Setting (Setup)
```
【External Elements】
- Location: Specific enough for the reader to imagine
- Time: Time of day, season, weather
- Characters: Who is there, and what is their positioning

【Internal Elements】
- Psychological state of the point-of-view character
- Events before this scene
- Expectations and anxieties
```

### 2. Scene Development
```
Introduction (Hook): The first sentence that draws the reader in
  ↓
Development (Buildup): Increases tension or anticipation
  ↓
Turning Point: The moment something changes
  ↓
Conclusion (Lingering Effect): Bridge to the next scene
```

### 3. Description Balance
```
Visual: 40% (What can be seen)
Auditory: 20% (What can be heard)
Psychological: 30% (What is felt)
Other: 10% (Tactile, olfactory, gustatory)
```

## Execution Examples

### Dialogue Scene (Parsed Arguments Version)
```
User: /scene dialogue Asuka Sato tense
Assistant: 【Arguments Parsed】
- Scene Type: dialogue (Dialogue-centered)
- Character: Asuka Sato
- Atmosphere: tense

【Creating Dialogue Scene】

Settings:
- Character: Asuka Sato (Librarian)
- Atmosphere: tense
- Location: Library counter

---

Asuka stopped her hands in front of a pile of returned books. A leather-bound notebook she didn't recognize was mixed in.

"Um..."

Across the counter, a young man was restlessly fidgeting with his fingers.

"Is this yours?"

When Asuka held up the notebook, the young man's face turned red in an instant.

"That's... well..."

[Psychological: It seems important. But why was it mixed with the books?]

Continue?
```

### Emotion Scene (With Multiple Options)
```
User: /scene emotion Misaki Tanaka nostalgic 800
Assistant: 【Arguments Parsed】
- Scene Type: emotion (Emotion-centered)
- Character: Misaki Tanaka
- Atmosphere: nostalgic
- Character Count: 800 characters

【Creating Emotion Scene】

Settings:
- Character: Misaki Tanaka (Bookstore owner)
- Emotion: Nostalgia
- Trigger: Finding her mother's favorite book
- Target character count: Approx. 800 characters

---

The moment Misaki picked up the dusty "Night on the Galactic Railroad," her fingers paused.

A faint scent of lavender wafted from between the pages. Her mother's perfume. Even now, twenty years later, this scent transported Misaki to another era.

"Miyazawa Kenji again?" her mother would often say with a laugh, holding this book. This book was also by her bedside in the hospital room until the very end.

Misaki hugged the book to her chest, as if searching for her mother's warmth through the hard cover.

[Internal: No tears. But a quiet warmth deep inside her chest.]

(Expand to about 800 characters, adjusting character count)
```

### Action Scene (Atmosphere Only)
```
User: /scene action suspenseful
Assistant: 【Arguments Parsed】
- Scene Type: action (Action-centered)
- Atmosphere: suspenseful
- Character: (Auto-generated)

【Creating Action Scene】

Atmosphere: Suspenseful
Scene Purpose: Decision in a critical situation

---

The sound of footsteps rushing up the stairs echoed throughout the old building.

Taking three steps at a time, Sho glanced over his shoulder. No sign of pursuers yet. But it was only a matter of time.

The door to the top floor loomed ahead. It should be locked. Ram it, or—

"Wait!"

A voice echoed from below. Stopping meant the end.

Sho threw his entire weight against the door.

[Judgment: It's now or never.]
```

### No Arguments Case
```
User: /scene
Assistant: 【No Arguments Specified】

Please select a scene type:
1. dialogue - Dialogue-centered scene
2. action - Action-centered scene
3. emotion - Emotion-centered scene
4. transition - Scene transition
5. climax - Climax scene

Alternatively, you can specify directly in the following format:
/scene [type] [character_name] [atmosphere] [character_count]

Examples:
- /scene dialogue Taro Yamada tense
- /scene emotion Hanako Tanaka joyful 500
- /scene action suspenseful
```

## Workspace Scene Management

### Saving Scene Files
```
# Save as individual scenes
my-stories/[work-title]/scenes/scene-[number]-[content].md

# Example
my-stories/last-letter/scenes/scene-01-bookstore.md
my-stories/last-letter/scenes/scene-02-letter-discovery.md
my-stories/last-letter/scenes/scene-03-revelation.md
```

### Scene Naming Conventions
- Recommend `scene-[number]-[content].md` format
- Standardize numbers to two digits (01, 02...)
- Content should be concise in English or Romaji

### Draft Management
```
# Experimental scenes in drafts/
drafts/experimental-dialogue.draft.md
drafts/alternative-ending.wip.md

# Move to official location once adopted
mv drafts/experimental-dialogue.draft.md my-stories/story-name/scenes/scene-04-dialogue.md
```

### Scene Quality Control
After creating each scene:
1. Evaluate with `/quality scene [scene_name]`
2. Correct any problems
3. Incorporate into the main story

## Scene Type Specific Techniques

### Dialogue Scene
- Insert gestures between lines
- Use silence effectively
- Be aware of subtext (implicit meaning)

### Emotion Scene
- Avoid direct emotional expressions
- Express emotions through actions and scenery
- Describe memories through the five senses

### Action Scene
- Create tension with short sentences
- Use verbs effectively
- Clearly define the flow of time

### Scene Transition
- Naturally indicate the passage of time
- Utilize contrast with the previous scene
- Gradually disclose new information

## Tips for Effective Description

### Show, Don't Tell
```
❌ He was angry.
✅ He clenched his fists, and a muscle twitched in his jaw.
```

### Utilize Metaphors
```
❌ It was very quiet.
✅ The library was as still as if time had stopped.
```

### Sensory Description
```
❌ There were many old books.
✅ The smell of mold and dust stung the nostrils, and the leather-bound spines absorbed the dim light.
```

## Checklist

- [ ] Is the purpose of the scene clear?
- [ ] Is the character's personality evident?
- [ ] Are there descriptions that appeal to the five senses?
- [ ] Is the connection with the preceding and succeeding scenes natural?
- [ ] Can it move the reader's emotions?

## Related Commands

- `/character` - Create characters to use in the scene
- `/story` - Construct the story to incorporate the scene
- `/dialogue` - Specialized creation for conversations
- `/quality` - Check the quality of the scene

## Tips

💡 Grab the reader with the first sentence
💡 End the scene leaving anticipation for what's next
💡 Balance the character's internal and external aspects
💡 Consider splitting scenes that are too long
```