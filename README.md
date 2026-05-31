# cbt-thought-record

A [Claude Code](https://claude.ai/code) skill that guides CBT (Cognitive Behavioral Therapy) 7-column thought record sessions through Socratic dialogue.

Not a therapist — a reflective thinking partner that helps you examine your thoughts, not judge them.

## Features

- **7-phase session flow**: Land → Situate → Catch → Examine → Reframe → Reassess → Wrap-up
- **Socratic questioning**: 5 dimensions (Evidence, Alternatives, Decatastrophizing, Usefulness, Distancing) with heuristic mapping to distortion types
- **10 cognitive distortions catalog**: All-or-Nothing, Overgeneralization, Mental Filter, Disqualifying the Positive, Jumping to Conclusions, Catastrophizing, Emotional Reasoning, "Should" Statements, Labeling, Personalization/Blame
- **Bilingual**: Matches your language automatically (English or Chinese)
- **Structured output**: Obsidian-compatible Markdown with callouts and tables
- **Safety protocol**: Crisis detection, escape hatch, and crisis resource links

## Install

Copy (or symlink) the skill into your Claude Code skills directory:

```bash
# Option 1: Clone directly into your skills directory
git clone https://github.com/Elian-Gu/cbt-thought-record.git ~/.claude/skills/cbt-thought-record

# Option 2: Clone elsewhere and symlink
git clone https://github.com/Elian-Gu/cbt-thought-record.git ~/dev/cbt-thought-record
ln -s ~/dev/cbt-thought-record ~/.claude/skills/cbt-thought-record
```

## Usage

Start a CBT session by saying any of these triggers:

**English**: "thought record", "CBT", "process my feelings", "I feel stuck", "help me think through this", "I'm being hard on myself"

**Chinese**: "认知扭曲", "思维记录", "帮我理一下", "情绪"

The skill will guide you through the 7 phases at your own pace. You can stop at any time.

## File Structure

```
cbt-thought-record/
├── SKILL.md                          # Entry point — role, flow, output, safety
├── references/
│   ├── distortion-catalog.md         # 10 cognitive distortions with examples
│   └── socratic-questions.md         # AI rules, 5 questioning dimensions
```

## License

[MIT](LICENSE)
