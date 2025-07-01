# AI Story Forge - A workshop for forging stories with AI

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-0.0.2-blue.svg)](https://github.com/nwiizo/ai-story-forge/releases)
[![Language](https://img.shields.io/badge/language-English-green.svg)](https://github.com/nwiizo/ai-story-forge)

A collection of practical templates for novel writing using generative AI. This system helps you efficiently create compelling stories while maintaining character consistency.

## 📌 Latest Information (v0.0.3)

- 🆕 **Claude Code v1.0.25 Support**: Improved slash commands to accept arguments.
- 🆕 **Enhanced Command Functionality**: Supports commands with arguments like `/character new`, `/scene dialogue Asuka Sato tense`.
- 🆕 **Document Updates**: Added command examples to QUICK_START.md and WORKSPACE_GUIDE.md.

### v0.0.2 Features
- **Workspace Management**: `.gitignore` settings to safely manage individual works.
- **Motivation-Based Character Creation**: A new approach starting from "What does this person want to do?"
- **Claude Integrated Commands**: Dedicated commands like `/character`, `/story`, `/scene`.

## 🎯 Problems This Project Solves

- **Character Consistency Collapse**: AI forgets context, leading to changes in character personality.
- **Physical Contradictions**: Loss of consistency in locations and timelines.
- **Unnatural Emotional Changes**: Sudden changes of heart or unexplained emotional shifts.
- **Saggy Middle Stories**: Reader disengagement due to weak plot structure.

## 🚀 Features

### 1. 3-Layer Character Structure
- **Invariant Core**: Values that absolutely do not change throughout the story.
- **Semi-Stable Layer**: Elements that change depending on the situation but within a certain range.
- **Variable Layer**: Elements that can be flexibly changed according to the scene.

### 2. Phased Story Construction
- **Phase 1**: Skeleton creation.
- **Phase 2**: Identification of important scenes.
- **Phase 3**: Detailed scene design.

### 3. 5-Axis Quality Evaluation
- Character consistency
- Physical logic
- Psychological naturalness
- Readability
- Emotional impact

## 📁 Project Structure

```
ai-story-forge/
├── character-template/     # Character templates
│   ├── CHARACTER.md       # Main template
│   ├── character-prompts.md
│   ├── examples/
│   └── tips.md
├── story-template/        # Story creation templates
│   ├── STORY.md
│   ├── story-prompts.md
│   ├── examples/
│   └── techniques.md
├── quality-check/         # Quality check
│   ├── checklist.md
│   └── common-problems.md
└── resources/            # Reference materials
    ├── principles.md
    ├── constraints.md
    └── workflow.md
```

## 🏃‍♂️ Quick Start

Get started in 5 minutes! See [QUICK_START.md](./QUICK_START.md) for details.

1. Clone the repository.
2. Copy `character-template/CHARACTER.md`.
3. Fill in basic information.
4. Interact with AI using the prompt collection.
5. Start writing your story.

For information on how to manage your work, please see [WORKSPACE_GUIDE.md](./WORKSPACE_GUIDE.md).

## 💡 Usage Example

### Character Creation Example

```markdown
# Character Setting Sheet

## Basic Information
**Name**: Asuka Sato
**Age**: 28
**Occupation**: Librarian
**In a nutshell**: "A quiet enthusiast who connects people's hearts through books."

## Layer 1: Invariant Core
### Core Value
**"I want to expand people's potential by sharing knowledge."**
```

## 🎓 5 Principles of Prompt Engineering

This project is based on the following principles:

1. **Principle of Clarity**: Eliminate ambiguity and give specific instructions.
2. **Principle of Constraint Utilization**: Understand the limits of LLMs and design accordingly.
3. **Principle of Incremental Construction**: Break down complex tasks into small steps.
4. **Principle of Context Retention**: Place important information appropriately to maintain consistency.
5. **Principle of Verifiability**: A mechanism to objectively evaluate the quality of output.

## 📈 Effective Usage

### Week 1: Character Establishment
- Create CHARACTER.md (30 min)
- Interact with AI in 5 steps (30 min)
- Consistency check (15 min)

### Week 2: Story Construction
- Create STORY.md Phase 1 (30 min)
- Identify important scenes (30 min)
- Detail one scene (45 min)

### Week 3: Writing and Improvement
- Write each scene (1 hour per scene)
- Quality check (15 min each)
- Final adjustments with a full read-through

## 🤝 Contribution

This project welcomes contributions from everyone exploring creative collaboration between AI and humans.

- Bug reports/feature suggestions: [Issues](https://github.com/nwiizo/ai-story-forge/issues)
- Pull requests: Template improvements, addition of new examples, etc.

## 📋 Update History

### v0.0.2 (2025-06-29)
- Added workspace management function.
- Protection of personal works with `.gitignore`.
- Created workspace guide.

### v0.0.1 (2025-06-29)
- Initial release.
- Basic template system.
- Claude integrated commands.
- Motivation-based character creation.

## 📜 License

This project is released under the MIT License.

## 🙏 Acknowledgements

This project is influenced by pioneers in prompt engineering and story creation. We thank researchers, writers, and practitioners in AI and storytelling. We hope this project aids future story creators.

---

**"Turning constraints into creativity"** - That is the philosophy of AI Story Forge.