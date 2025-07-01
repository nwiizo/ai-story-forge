---
description: "Command to create natural conversation scenes that highlight character personalities"
---

# dialogue - Create living conversations

Creates natural and impressive conversation scenes that highlight character personalities.

## Argument Processing

Command arguments: $ARGUMENTS

Argument format: [type] [character1] [character2] [options]

If arguments are given, they are interpreted as follows:
- 1st argument (type):
  - `first-meet` → First meeting conversation
  - `conflict` → Conflict/argument
  - `confession` → Confession/true feelings
  - `casual` → Casual conversation
  - `revelation` → Disclosure of truth
- 2nd argument onwards: Character names (space-separated)
- Additional options: Atmosphere, purpose, etc.

Example: `first-meet Asuka Sato Taro Yamada`

## Usage

```
/dialogue [type] [character1] [character2] [options]
```

## Conversation Types

- `first-meet` - First meeting conversation
- `conflict` - Conflict/argument
- `confession` - Confession/true feelings
- `casual` - Casual conversation
- `revelation` - Disclosure of truth

## Options

- `--mood <atmosphere>` - Atmosphere of the conversation
- `--purpose <purpose>` - Role of this conversation
- `--length <turns>` - Length of the conversation
- `--subtext` - Emphasize subtext (implicit meaning)

## Principles of Conversation Creation

### 1. Differentiate Characters
```
【Asuka Sato】 (Librarian)
- Polite and modest way of speaking
- Catchphrase: "If you'd like"
- Becomes talkative when discussing books

【Taro Yamada】 (Detective)
- Concise and fact-oriented
- Catchphrase: "...So that's it."
- Does not show emotions openly
```

### 2. Subtext (Implicit Meaning)
```
Surface conversation: "Nice weather today, isn't it?"
True meaning: "I want to talk to you."

Surface conversation: "I don't really mind."
True meaning: "I actually don't want to, but I have no choice."
```

### 3. Rhythm of Conversation
```
Long line
  ↓
Short reply
  ↓
Silence (pause)
  ↓
Core statement
```

## Execution Examples

### First Meeting Conversation
```
User: /dialogue first-meet --characters Asuka Sato Taro Yamada
Assistant: 【First Meeting Conversation Scene】

Location: Reference section of the city library
Situation: Detective Yamada is looking for case materials

---

Asuka noticed a man who seemed troubled in the reference section.

"Um... If you'd like, are you looking for something?"

The man—in a suit, with sharp eyes—turned around.

"...Books related to law."

"What kind of content? Criminal law? Civil law?"

A moment of silence.

"...Past case collections. From 20 years ago."

Asuka's expression softened.

"In that case, this way. If you'd like,
are you looking for a specific case?"

"...Yeah."

Yamada felt a little uncomfortable under Asuka's direct gaze.
Are librarians always this good at seeing through people?

[Goal of the conversation: Highlight personality differences while sowing seeds for a future relationship]
```

### Conflict Conversation
```
User: /dialogue conflict --characters Misaki Son --mood Tense
Assistant: 【Conflict Conversation Scene】

Location: Bookstore after closing
Situation: Discussion about inheriting the bookstore

---

"Are you serious about closing this store?"

Misaki answered quietly without looking up from the sales ledger.

"If there's no one to inherit it, it can't be helped."

"What if I said I'd inherit it?"

The sound of a pen being placed echoed in the quiet store.

"You have your own life, don't you?"

"You must have had a different life too, Mom, when you inherited it from Grandma."

Misaki looked directly at her son's face for the first time.
He had the same eyes she had twenty years ago.

"...You really won't regret it?"

"Do you regret it, Mom?"

[Pause: Silence to explore each other's true feelings]

"...I don't."

"Then, me neither."

[Core of the conversation: Understanding and determination transcending generations]
```

### Confession Conversation
```
User: /dialogue confession --subtext --mood Poignant
Assistant: 【Confession Conversation Scene】

Situation: A moment when unspoken feelings are conveyed indirectly

---

"I'm going back to Tokyo tomorrow."

"...I see."

The sea breeze passed between them.

"I'll come again. I promise."

"Promise, huh."

He didn't miss the doubt in her voice.

"You don't believe me?"

"I believe you. Including the fact that when you say 'promise,'
you're actually not confident."

She hit the mark.

"...You always see right through me, don't you?"

"It's my job. To observe people."

They both knew it was a lie.

[Truth: It's not because of work. It's because I like you that I watched.]
```

## Workspace Conversation Management

### Saving Conversation Scenes
```
# Save as part of a scene
my-stories/[work-title]/scenes/scene-XX-dialogue.md

# For conversation practice
drafts/dialogue-practice-[character-name].md

# Manage important conversations individually
my-stories/[work-title]/key-dialogues/confession.md
```

### Conversation Version Control
When trying different versions:
```
scene-05-confession-v1.md  # Direct version
scene-05-confession-v2.md  # Indirect version
scene-05-confession-final.md  # Adopted version
```

## Conversation Techniques

### 1. Utilize Ellipses
```
"... " (Silence/hesitation)
"Well..." (Stammering)
"Let me see..." (While thinking)
```

### 2. Restating/Interruption
```
"That's—no, it's nothing."
"About you, well, I mean..."
```

### 3. Repeating the Other Person's Words
```
A: "I might not be able to see you again."
B: "Might not be able to see me again, huh."
→ Emphasizes the weight of the words
```

### 4. Ending with a Question
```
"Is that really okay?"
→ Makes the reader think too
```

## Conversation Quality Check

- [ ] Does it show the character's personality?
- [ ] Is it not an unnatural information dump?
- [ ] Is there appropriate pausing (silence)?
- [ ] Is the subtext effective?
- [ ] Can the situation be understood from the conversation alone?

## NG Examples and Improvements

### NG: Too explanatory
```
❌ "I am Asuka Sato, a librarian.
   I want to help people through books."

✅ "Are you looking for a book?
   If you'd like, I can help you."
```

### NG: Characters speak the same way
```
❌ A: "That's wonderful, isn't it?"
   B: "It's truly wonderful, isn't it?"

✅ A: "Oh, that's nice."
   B: "...Not bad."
```

## What Arises from Conversation

1. **Changes in Relationships**
   - Distance narrows/widens
   - Understanding deepens/misunderstandings arise

2. **Story Progression**
   - Disclosure of new information
   - Triggers for decisions or actions

3. **Sharing of Emotions**
   - Empathy with the reader
   - Attachment to characters

## Related Commands

- `/character` - Create characters to use in conversation
- `/scene` - Create scenes that include conversation
- `/quality` - Evaluate the naturalness of conversation
- `/subtext` - Analyze implicit meaning

## Tips

💬 Observe real-life conversations
💬 Aim for human-like conversations rather than perfect ones
💬 Silence is also a valid part of conversation
💬 Listen to the "voices" of your characters