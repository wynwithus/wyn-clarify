# WYN Clarify

**Turn a rough idea into a focused plan for something you can build.**

WYN Clarify is a free AI skill by [WYN](https://wynwithus.com/aicollective/#free-skills). Bring a product idea, an unclear feature, or an everyday frustration you want to solve. It helps you find the underlying problem, choose a useful first version, and write a practical product requirements document with testable feature behavior.

It uses plain language, recommends sensible defaults, and asks at most one useful question at a time. You can say **“use your recommendation”** or **“draft it now”** whenever you want to move forward.

## Start in your AI chat

1. Open [COPY-PASTE-PROMPT.txt](COPY-PASTE-PROMPT.txt).
2. Copy its contents into your AI chat.
3. Add your idea after “Begin with this idea or problem.”

Try: “I want to build something that helps our event volunteers know where they need to be.”

This needs no installation, API key, connector, browsing, or code execution. It applies to the current conversation; paste it again in a new chat unless your assistant explicitly saves reusable instructions. You do not need to type `/wyn-clarify` in an ordinary chat.

If attaching the text file instead, send: **“Follow the instructions in the attached WYN Clarify prompt for this conversation. My idea is: [describe your idea].”** Attaching a file alone may cause an assistant to summarize it rather than use it.

## Install as a skill

[Download wyn-clarify.zip](https://github.com/wynwithus/wyn-clarify/releases/latest/download/wyn-clarify.zip), then use your assistant's skill import or installation option. The ZIP contains a `wyn-clarify/` folder with `SKILL.md` at its root. Installation controls vary by assistant; a plain chat without skill support can use the prompt above.

For Codex, you can ask:

> Install the wyn-clarify skill from https://github.com/wynwithus/wyn-clarify into my personal skills folder. Read its SKILL.md, then help me clarify my idea: [describe your idea].

If installing manually, place this repository's files in a folder named `wyn-clarify` inside your assistant's skills directory. For a personal Codex installation, that is `~/.codex/skills/wyn-clarify/`. Start a new session, then ask to use `$wyn-clarify`.

## Choose your assistant

| Assistant | How to start | Reusable installation |
| --- | --- | --- |
| Claude | Paste the prompt into a conversation. | In **Customize → Skills**, create/upload a skill using the release ZIP and enable it. Availability depends on your account and administrator settings. |
| Claude Code | Paste the prompt, or use `/wyn-clarify` after installation. | Put the package in `~/.claude/skills/wyn-clarify/` for personal use, or `.claude/skills/wyn-clarify/` in one project. |
| Grok web/mobile | Paste the prompt, or attach the TXT file with the explicit instruction above. | Chat file uploads do not by themselves establish a persistent skill installation. |
| Grok Build | Paste the prompt, or use `/wyn-clarify` after installation. | Put the package in `~/.grok/skills/wyn-clarify/` for personal use, or `.grok/skills/wyn-clarify/` in one project. |
| Meta Muse | Paste the prompt and your idea into the conversation. | Custom ZIP skill import has not been verified; this package does not depend on it. |
| Codex | Ask to use `$wyn-clarify` after installation. | Install into your personal skills folder as described above. |
| Other text assistants | Paste the prompt into the conversation. | Use saved instructions only if your app supports them; its limits and behavior may differ. |

These instructions were checked against official documentation on November 1, 2026: [Claude skills](https://support.claude.com/en/articles/12512180-use-skills-in-claude), [Claude skill packaging](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills), [Claude Code skills](https://code.claude.com/docs/en/skills), [Grok uploads](https://docs.x.ai/grok/faq), [Grok Build skills](https://docs.x.ai/build/features/skills-plugins-marketplaces), and [Muse](https://ai.meta.com/muse/). Native installation depends on the host; the conversation prompt is the common starting point.

**Validation status:** The package structure and metadata are checked, including a description below Claude's documented 200-character limit. This is not a claim that behavior has been tested in every assistant. Run the [manual acceptance checks](tests/ACCEPTANCE-TESTS.md) in each target app/model before labeling that combination tested. A model may follow the instructions differently; hidden scoring cannot establish correctness on its own.

## What you get

- A specific problem and the person who experiences it.
- A recommended solution and a small first-version scope.
- The journey from starting the task to getting a useful result.
- Essential features with observable acceptance criteria.
- Important assumptions and unanswered questions, clearly labeled.

The skill does not need an API key, an account with WYN, or a background service. Your chosen AI tool may have its own fees. It does not automatically build or publish your product.

## Package

- [SKILL.md](SKILL.md) — complete skill instructions, version 0.3.1.
- [START-HERE.md](START-HERE.md) — workflow and usage notes.
- [COPY-PASTE-PROMPT.txt](COPY-PASTE-PROMPT.txt) — an alternative for chats without skill support.
- [tests/ACCEPTANCE-TESTS.md](tests/ACCEPTANCE-TESTS.md) — manual behavior checks, not measured performance claims.

The instructions draw on Double Diamond and problem-framing techniques associated with Min Basadur, S. I. Hayakawa, and Stanford d.school. The three framing passes are performed within one assistant; they are not separate model or agent executions. Results depend on your model and the information you provide.

Released under the [MIT License](LICENSE).
