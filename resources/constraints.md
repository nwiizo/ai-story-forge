# LLM Constraints and Countermeasures

## 🧠 Major Constraints

### 1. Context Window Limitation
**Constraint Details**
- Upper limit on the number of tokens that can be processed at once.
- Varies by model (4k–200k tokens).
- If too long, remembers only the beginning or end.

**Practical Countermeasures**
```
Countermeasure 1: Placement of Important Information
┌─────────────────┐
│ Important Settings │ ← Top 20%
├─────────────────┤
│ Detailed Description │ ← Middle 60%
├─────────────────┤
│ Important Conclusion │ ← Bottom 20%
└─────────────────┘
```

```
Countermeasure 2: Chunking
Long Novel (40,000 characters)
  ↓
Divide into 10 chapters (4,000 characters each)
  ↓
Process chapter by chapter
  ↓
Connect with summaries
```

### 2. Lost in the Middle Phenomenon
**Constraint Details**
- Tends to forget information in the middle of long texts.
- Particularly noticeable over 8,000 tokens.
- Important information gets dropped.

**Specific Countermeasures**

#### Pattern 1: Repetition of Important Information
```markdown
# Chapter 1
Protagonist Misaki Tanaka is a librarian who believes in "knowledge sharing."

# Chapter 3
Misaki, following her usual belief in "knowledge sharing"...

# Chapter 5
For Misaki, who values "knowledge sharing"...
```

#### Pattern 2: Countermeasure by Structuring
```
Scene Template:
┌─────────────────────┐
│ 【Summary】 Previously       │
│ 【Setting】 Current situation  │
│ 【Body】 Scene content       │
│ 【Next】 Foreshadowing       │
└─────────────────────┘
```

### 3. Timeline Confusion
**Constraint Details**
- Cannot manage multiple timelines.
- Gets confused by flashbacks.
- Fails to maintain date consistency.

**Timeline Management Method**

```
Explicit Timeline Method:
━━━━━━━━━━━━━━━━━━━━━━
March 15, 2024, 9:00 AM - Incident occurs
      ↓ (2 hours later)
March 15, 2024, 11:00 AM - Police arrive
      ↓ (Flashback scene)
[Flashback] March 10, 2024 - Premonition
      ↓ (Return to present)
March 15, 2024, 2:00 PM - Investigation begins
━━━━━━━━━━━━━━━━━━━━━━
```

### 4. Grasp of Physical Space
**Constraint Details**
- Cannot maintain positional relationships in 3D space.
- Forgets building structures.
- Logic of movement breaks down.

**Simple Spatial Design**
```
Recommended: Simple layout
[1F: Bookstore] → [Road] → [2F: Cafe]

Not Recommended: Complex layout
[1F: Bookstore] → [Courtyard] → [Annex 2F] → [Passageway] → [Main Building 3F]
```

### 5. Character Consistency
**Constraint Details**
- Personality changes depending on the scene.
- Forgets settings.
- Tone of voice is not unified.

**Character Card System**
```yaml
Character: Asuka Sato
━━━━━━━━━━━━━━━━━
Essential Elements (Maintain in all scenes):
  - Value: "Knowledge sharing"
  - Catchphrase: "If you'd like"
  - Gesture: Pushes up glasses

Variable Elements (Change with situation):
  - Emotional expression
  - Proactiveness of behavior
  - Amount of speech
━━━━━━━━━━━━━━━━━
```

## 🛠️ Implementation Techniques

### Technique 1: Prompt Chaining
```
Step 1: Generate character settings
    ↓ Save output
Step 2: [Settings] + Generate plot
    ↓ Save output
Step 3: [Settings] + [Plot] + Generate scene
```

### Technique 2: Summary Bridge
```
End of chapter:
"Summary of this chapter (100 characters):
Misaki met an old woman and discovered her mother's letter.
Connections to the past began to become clear."

Beginning of next chapter:
"Summary of previous chapter: [Insert above]
Now, Misaki, who started reading the letter..."
```

### Technique 3: Explicit Constraints
```
Please adhere to the following constraints:
1. Maximum of 3 locations.
2. Timeline must be chronological only.
3. Maximum of 5 characters.
4. Viewpoint fixed on the protagonist.
```

## 📊 Constraint Level Correspondence Table

| Constraint Type      | Impact | Priority | Recommended Countermeasure |
|----------------------|--------|----------|---------------------------|
| Context Limit        | High   | Required | Chunking                  |
| Lost in the Middle   | High   | Required | Information Placement Opt.  |
| Timeline Confusion   | Medium | Important| Timestamps                |
| Spatial Awareness    | Medium | Recommended| Simplification            |
| Character Consistency| High   | Required | Card System               |

## 🔄 Turning Constraints to an Advantage: A Shift in Perspective

### Creativity Born from Constraints

#### 1. Context Limitation → Concise Writing Style
```
Because of limitations:
- Trimmed, waste-free sentences
- Focus on essential descriptions
- Utilize the reader's imagination
```

#### 2. Lost in the Middle → Focus on Important Scenes
```
If the middle is forgotten:
- Make the beginning and end count
- Place impressive scenes at both ends
- Dedicate the middle to atmosphere building
```

#### 3. Timeline Simplification → Easy-to-Understand Structure
```
If complexity isn't possible:
- Straightforward chronological development
- Minimize flashbacks
- Tension of present progressive
```

## 🎮 Constraint Handling Simulation

### Case 1: 10,000-Character Short Story
```
Structural Proposal:
1. Beginning (1,000 chars) - Setting and hook
2. First Half (3,000 chars) - Development
3. Middle (2,000 chars) - Deepening
4. Second Half (3,000 chars) - Climax
5. Ending (1,000 chars) - Lingering effect

Points:
- Manage in 5 blocks
- Create a summary for each block
- Place important information in 1 and 5
```

### Case 2: Story with Multiple Perspectives
```
Not Recommended:
A's POV → B's POV → A's POV → C's POV → B's POV

Recommended:
Part 1: A's POV (Complete)
Part 2: B's POV (Complete)
Part 3: C's POV (Complete)
Final Chapter: Integration

Points:
- Group by viewpoint
- Avoid mixing
- Small completions in each part
```

## 💡 Troubleshooting

### Q: Character becomes inconsistent in a long story.
A: Insert a "character reminder" at the beginning of each chapter.

### Q: Complex plot falls apart.
A: Focus on one main plot and minimize subplots.

### Q: Location descriptions become contradictory.
A: Limit locations and explicitly write movement scenes.

## 🚀 Future Outlook

### Model Evolution and Changing Constraints
- Context length tends to expand.
- However, essential constraints will remain.
- Constraint handling skills are universal.

### New Approaches
1. **RAG (Retrieval Augmented Generation)**: Utilization of external memory.
2. **Fine-tuning**: Optimization for specific purposes.
3. **Multi-agent**: Handling by division of roles.

---

🎯 **Constraint is the mother of creativity** - Limitations foster ingenuity and lead to original solutions.