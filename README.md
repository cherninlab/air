# /air

Air is an Agent Skill that helps AI agents make every addition earn its place—in UI and UX design, websites, writing, documentation, and software work.

It asks your agent to understand the person’s task, decide what belongs, and develop it with care. Before adding a section, sentence, control, visual detail, or feature, the agent asks: **Does this help the person enough to earn its place?**

[Try /air](https://air.cherninlab.com/) · [Read the skill](air/SKILL.md) · [Download](https://air.cherninlab.com/air.zip)

## Examples

| Example | Off | Lite | Full | Ultra | Ultra ×2 |
| --- | --- | --- | --- | --- | --- |
| [Five AI tools infographic](examples/01-five-ai-tools/README.md) | <a href="examples/01-five-ai-tools/images/off.png"><img src="examples/01-five-ai-tools/images/off.png" width="128" alt="Off: five AI tools infographic"></a> | <a href="examples/01-five-ai-tools/images/lite.png"><img src="examples/01-five-ai-tools/images/lite.png" width="128" alt="Lite: five AI tools infographic"></a> | <a href="examples/01-five-ai-tools/images/full.png"><img src="examples/01-five-ai-tools/images/full.png" width="128" alt="Full: five AI tools infographic"></a> | <a href="examples/01-five-ai-tools/images/ultra.png"><img src="examples/01-five-ai-tools/images/ultra.png" width="128" alt="Ultra: five AI tools infographic"></a> | <a href="examples/01-five-ai-tools/images/ultra-x2.png"><img src="examples/01-five-ai-tools/images/ultra-x2.png" width="128" alt="Ultra ×2: five AI tools infographic"></a> |

> Ultra ×2 gives the Ultra result one more edit pass with the same Ultra instructions.

## Try it

Install with the [skills CLI](https://github.com/vercel-labs/skills):

```sh
npx skills add cherninlab/air --skill air
```

Or give an agent with access to your files this setup prompt:

```text
Install the /air skill from https://air.cherninlab.com/air/SKILL.md in your skills directory, then activate /air full for this conversation.
```

Then give it your task. From this repository, for example:

```text
Build a landing page for ./air.
```

The `./air` folder is the brief.

You can also [download the ZIP](https://air.cherninlab.com/air.zip) and place its `air` folder in your agent’s skills directory. In Codex, use `.agents/skills/air/` for a project or `~/.agents/skills/air/` for personal use. See the [official installation locations](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills).

## Choose a mode

| Include in your prompt | What the agent should do |
| --- | --- |
| `/air lite` | Remove clear filler, duplication, and speculative additions. Keep optional elements with a plausible, specific benefit. |
| `/air full` | Require a clear contribution to usefulness, convenience, understanding, or the intended experience. This is the default. |
| `/air ultra` | Reconsider the core experience and look for a stronger central idea. Apply the strongest scrutiny to weak additions, and fully develop what belongs. |
| `/air off` | Suspend Air’s constraints and follow the other instructions normally. |

Every mode keeps the same standard of care. The selected mode stays active in the current conversation until you switch. Bare `/air` or `$air` selects Full.

Change modes with your next task:

```text
/air ultra
Improve this screen.
```

In Codex, mention the installed skill with `$air`; other agents use their own skill selectors or invocation flow. The mode cues above are instructions for the agent within the conversation.

## When Air helps

- **Designing interfaces and websites:** choose content, layout, typography, color, and motion from the user’s needs. Check the rendered result at the sizes people will use.
- **Writing and documentation:** combine repeated ideas, keep useful detail, and choose a structure that helps the reader follow the thought.
- **Planning and building software:** question features and abstractions added from habit, while preserving the capabilities and convenience the task needs.

A landing page can demonstrate the product before explaining it. A label, heading, and paragraph can become one well-written paragraph. A dense working tool can keep its controls and use better grouping, spacing, and feedback to make them easier to use.

Beauty, atmosphere, character, and delight belong when they serve the experience. The result can be expressive, intricate, or visually rich. Air asks the agent to choose these qualities deliberately and verify the finished work.

## Format and compatibility

Air follows the [Agent Skills format](https://agentskills.io/specification). Agents such as Claude Code, Codex, and Cursor load skills through their supported installation flows. Your agent provides the model, tools, and permissions; Air provides the decision process.

The installable package contains:

```text
air/
├── SKILL.md
└── agents/
    └── openai.yaml
```

`SKILL.md` contains the metadata and instructions. `agents/openai.yaml` supplies Codex display metadata.

## License

Licensed under the [MIT License](LICENSE).

Copyright (c) 2026 Fedor Chernin
