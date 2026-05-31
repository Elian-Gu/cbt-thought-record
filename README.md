# cbt-thought-record

A structured CBT (Cognitive Behavioral Therapy) 7-column thought record skill, designed for [Claude Code](https://claude.ai/code) and adaptable to any AI agent.

Not a therapist — a reflective thinking partner that helps you examine your thoughts, not judge them.

> **CBT 思维记录工具** — 通过苏格拉底式对话引导 7 列思维记录表。不是治疗师，是一个温和的思维伙伴，帮助你审视想法而非评判它们。支持中英文自动切换。专为 Claude Code 设计，也可用于任何 AI 助手。

## Features

- **7-phase session flow**: Land → Situate → Catch → Examine → Reframe → Reassess → Wrap-up
- **Socratic questioning**: 5 dimensions (Evidence, Alternatives, Decatastrophizing, Usefulness, Distancing) with heuristic mapping to distortion types
- **10 cognitive distortions catalog**: All-or-Nothing, Overgeneralization, Mental Filter, Disqualifying the Positive, Jumping to Conclusions, Catastrophizing, Emotional Reasoning, "Should" Statements, Labeling, Personalization/Blame
- **Bilingual**: Matches your language automatically (English or Chinese)
- **Structured output**: Markdown with callouts and tables
- **Safety protocol**: Crisis detection, escape hatch, and crisis resource links

## Install (Claude Code)

Copy (or symlink) the skill into your Claude Code skills directory:

```bash
# Option 1: Clone directly into your skills directory
git clone https://github.com/Elian-Gu/cbt-thought-record.git ~/.claude/skills/cbt-thought-record

# Option 2: Clone elsewhere and symlink
git clone https://github.com/Elian-Gu/cbt-thought-record.git ~/dev/cbt-thought-record
ln -s ~/dev/cbt-thought-record ~/.claude/skills/cbt-thought-record
```

## Use with other AI agents

Not using Claude Code? The core content is just structured Markdown prompts — it works with any AI assistant:

1. Open `SKILL.md` and paste its content as your system prompt or first message
2. Include the two `references/` files when the agent asks for them (or paste them in advance)
3. Start talking — the CBT flow is agent-agnostic

Works with: Claude Code or any LLM-based tool.

## Usage

Start a CBT session by saying any of these triggers:

**English**: "thought record", "CBT", "process my feelings", "I feel stuck", "help me think through this", "I'm being hard on myself"

**Chinese**: "认知扭曲", "思维记录", "帮我理一下", "情绪"

The skill will guide you through the 7 phases at your own pace. You can stop at any time.

## Auto-save Configuration

By default, the skill saves session summaries to a local Markdown file. Multiple sessions per day are **appended** to the same file (separated by `---`), not overwritten.

Edit the **Auto-save** section in `SKILL.md` to match your setup:

**Obsidian** — point to your vault directory:
```
Path: /your-vault/CBT/YYYY-MM-DD.md
```

**Other note apps** (Notion, Logseq, plain files) — adjust the path to wherever you want Markdown files saved.

**Output format**: Standard Markdown with callout blocks (`> [!abstract]`) and tables. Obsidian renders callouts natively; other apps will show them as blockquotes.

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
