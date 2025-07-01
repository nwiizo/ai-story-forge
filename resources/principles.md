# 5 Principles of Prompt Engineering

## 📐 Principle 1: Principle of Clarity
**Eliminate ambiguity and give specific instructions.**

### Why is it important?
AI struggles to infer context. Clear instructions make it easier to obtain the intended output.

### Practical Methods

**❌ Bad Example: Ambiguous instruction**
```
Create a cool character.
```

**✅ Good Example: Specific instruction**
```
Please create a character with the following conditions:
- Age: 28
- Occupation: Librarian
- Personality: Introverted, but passionate when talking about books
- Values: Wants to connect people through knowledge
```

### Checklist
- [ ] Are the 5W1H (Who, What, When, Where, Why, How) clear?
- [ ] Are numbers and ranges specific?
- [ ] Did you indicate the expected format?
- [ ] Did you also specify what to avoid?

---

## 🧩 Principle 2: Principle of Utilizing Constraints
**Understand the limitations of LLMs and design based on them.**

### Major Constraints and Countermeasures

#### 1. Context Window Limitation
**Constraint**: There is an upper limit to the number of characters that can be processed at once.
**Countermeasure**:
- Place important information at the beginning and end.
- Process long texts in segments.
- Utilize summaries.

#### 2. Lost in the Middle Phenomenon
**Constraint**: Tends to forget information in the middle of long texts.
**Countermeasure**:
- Repeat key points every 3-5 paragraphs.
- Mention important settings in multiple places.
- Use a structured format.

#### 3. Timeline Confusion
**Constraint**: Difficult to track complex timelines.
**Countermeasure**:
- Use clear timestamps.
- Simplify the timeline.
- Specify the time for each chapter.

### Turning Constraints into Strengths
```
Constraint: Difficulty maintaining character consistency
  ↓
Countermeasure: Manage with a 3-layer structure (Immutable, Semi-stable, Variable)
  ↓
Result: Enables more systematic character design.
```

---

## 🔄 Principle 3: Principle of Incremental Construction
**Break down complex tasks into small steps.**

### Example of Step Decomposition

#### Character Creation
```
Step 1: Basic attributes (name, age, occupation)
  ↓
Step 2: Core value
  ↓
Step 3: Fear derived from value
  ↓
Step 4: Human contradiction
  ↓
Step 5: Specific behavior patterns
```

#### Story Construction
```
Step 1: One-sentence synopsis
  ↓
Step 2: Overview of 3-act structure
  ↓
Step 3: Selection of important scenes
  ↓
Step 4: Detailed design of each scene
  ↓
Step 5: Transitions between scenes
```

### Advantages of Incremental Construction
1. **Quality Control**: Allows for confirmation and correction at each stage.
2. **Flexibility**: Easy to change direction midway.
3. **Improved Understanding**: Easier for AI to maintain context.
4. **Reusability**: Results from each stage can be applied elsewhere.

---

## 📌 Principle 4: Principle of Context Retention
**Place important information appropriately and maintain consistency.**

### Context Retention Techniques

#### 1. Sandwich Structure
```
[Important settings/rules]
      ↓
[Detailed content/development]
      ↓
[Reconfirmation of important settings]
```

#### 2. Setting Anchor Points
At the beginning of each section, place:
- Character's core value
- Current location and time
- Summary of immediately preceding events

#### 3. Structured Format
```markdown
## Scene Information
- Location: [Specific location]
- Time: [Time of day/Weather]
- Characters: [Who is present]

## Flow from Previous Scene
[Concise summary]

## Purpose of This Scene
[What to achieve]
```

### Implementation Example
```
Prompt Structure:
1. Character settings (200 characters)
2. Current situation (100 characters)
3. Scene to be written (main text)
4. Important notes (50 characters)
5. Restatement of character settings (100 characters)
```

---

## ✅ Principle 5: Principle of Verifiability
**A mechanism to objectively evaluate the quality of output.**

### Setting Evaluation Criteria

#### Quantitative Evaluation
1. **Character Count**: Within the specified range?
2. **Structural Elements**: Are essential elements included?
3. **Consistency Score**: Count the number of contradictions.
4. **Readability Index**: Sentence length, paragraph structure.

#### Qualitative Evaluation
1. **Emotional Curve**: Is the intended emotional change present?
2. **Characterization**: Is the "likeness" evident?
3. **Thematic Relevance**: Is the main theme expressed?
4. **Completeness**: Does it work as a story?

### Utilizing Checklists
```markdown
Scene Evaluation:
- [ ] Actions aligned with the protagonist's values?
- [ ] Consistency of time and place?
- [ ] Are emotional changes natural?
- [ ] Is there a bridge to the next scene?
- [ ] Can the reader understand the situation?
```

### Iterative Improvement Process
```
1. Generate first draft
  ↓
2. Evaluate with checklist
  ↓
3. Identify problem areas
  ↓
4. Create revised prompt
  ↓
5. Regenerate
  ↓
6. Comparative evaluation
```

---

## 🎯 Integrated Application of the 5 Principles

### Practical Example: Creating a Short Story

**Step 1: Clear Instructions** (Principle 1)
```
Please write a 5000-character short story.
Genre: Human Drama
Theme: Reconciliation with the past
```

**Step 2: Consideration of Constraints** (Principle 2)
```
Place important settings at the beginning.
Avoid complex timelines.
Limit locations to three or fewer.
```

**Step 3: Incremental Creation** (Principle 3)
```
Phase 1: Plot creation (500 characters)
Phase 2: Details of 3 important scenes (300 characters each)
Phase 3: Writing the whole story (5000 characters)
```

**Step 4: Context Retention** (Principle 4)
```
At the beginning of each scene, specify:
- Protagonist's current emotion
- Location and time
- Immediately preceding events
```

**Step 5: Quality Verification** (Principle 5)
```
Evaluation Items:
✓ Character count: 4800 characters (96% of target)
✓ Character consistency: 8/10
✓ Flow of emotions: Natural
✓ Expression of theme: Clear
```

---

## 📚 For a Deeper Understanding of the Principles

### Practice Exercises

#### Exercise 1: Improving Clarity
Improve the following prompt:
"Write a sad story."

#### Exercise 2: Utilizing Constraints
Structure a 10,000-character story considering the Lost in the Middle phenomenon.

#### Exercise 3: Incremental Construction
Construct "a murder case on a spaceship" in 5 steps.

#### Exercise 4: Context Retention
Design a method to maintain the protagonist's values consistently across three scenes.

#### Exercise 5: Verifiability
Set five objective indicators for evaluating the quality of a mystery novel.

---

## 🔮 Future Outlook

### Relationship between AI Evolution and Principles
- The 5 principles remain valid even as models evolve.
- Even if constraints change, the way of thinking can be applied.
- Application to more advanced creation.

### New Possibilities
1. **Multimodal**: Story creation with images + text.
2. **Interactive**: Stories that change based on reader choices.
3. **Collaborative Creation**: Joint work with multiple AIs.

---

💡 **Remember**: These principles are tools. Use them as guidelines for creating better works, not to limit creativity.