# WYN Clarify

**Turn a rough idea into a focused plan for something you can build.**

WYN Clarify is a free AI skill by [WYN](https://wynwithus.com/aicollective/#free-skills). Bring a product idea, an unclear feature, or an everyday frustration you want to solve. It helps you find the underlying problem, choose a useful first version, and write a practical product requirements document with testable feature behavior.

It uses plain language, recommends sensible defaults, and asks at most one useful question at a time. You can say **“use your recommendation”** or **“draft it now”** whenever you want to move forward.

## Start in any AI chat

1. Open [COPY-PASTE-PROMPT.txt](COPY-PASTE-PROMPT.txt).
2. Copy its contents into your AI chat.
3. Add your idea after “Begin with this idea or problem.”

Try: “I want to build something that helps our event volunteers know where they need to be.”

## Install as a skill

[Download wyn-clarify.zip](https://github.com/wynwithus/wyn-clarify/releases/latest/download/wyn-clarify.zip), then use your assistant's skill import or installation option. The ZIP contains a `wyn-clarify/` folder with `SKILL.md` at its root. Installation controls vary by assistant; a plain chat without skill support can use the prompt above.

For Codex, you can ask:

> Install the wyn-clarify skill from https://github.com/wynwithus/wyn-clarify into my personal skills folder. Read its SKILL.md, then help me clarify my idea: [describe your idea].

If installing manually, place this repository's files in a folder named `wyn-clarify` inside your assistant's skills directory. For a personal Codex installation, that is `~/.codex/skills/wyn-clarify/`. Start a new session, then ask to use `$wyn-clarify`.

## What you get

- A specific problem and the person who experiences it.
- A recommended solution and a small first-version scope.
- The journey from starting the task to getting a useful result.
- Essential features with observable acceptance criteria.
- Important assumptions and unanswered questions, clearly labeled.

The skill does not need an API key, an account with WYN, or a background service. Your chosen AI tool may have its own fees. It does not automatically build or publish your product.

## Package

- [SKILL.md](SKILL.md) — complete skill instructions, version 0.3.0.
- [START-HERE.md](START-HERE.md) — workflow and usage notes.
- [COPY-PASTE-PROMPT.txt](COPY-PASTE-PROMPT.txt) — an alternative for chats without skill support.
- [tests/ACCEPTANCE-TESTS.md](tests/ACCEPTANCE-TESTS.md) — manual behavior checks, not measured performance claims.

The instructions draw on Double Diamond and problem-framing techniques associated with Min Basadur, S. I. Hayakawa, and Stanford d.school. The three framing passes are performed within one assistant; they are not separate model or agent executions. Results depend on your model and the information you provide.

Released under the [MIT License](LICENSE).
