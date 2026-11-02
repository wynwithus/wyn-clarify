# WYN Clarify

A free AI skill by [Nick Cybela](https://wynwithus.com/authors/nick-cybela/), shared through [WYN](https://wynwithus.com).

Describe your idea or the problem you want to solve in your own words. WYN Clarify helps you work out what to build, asks at most one question at a time, and writes a plan that explains how the first version should work.

You can say “use your recommendation” or “show me the plan” whenever you want to move forward. It uses what you've told it and identifies the important gaps.

The skill includes writing guidance for its replies and the finished plan, so you do not need to install another skill.

## Install with your agent

Give your agent this repository's URL and ask it to install **wyn-clarify**. The agent can handle the setup for you.

For example:

> Install wyn-clarify from https://github.com/wynwithus/wyn-clarify as a reusable skill for my assistant.

### Instructions for agents

If the user has asked you to install this skill, **perform the installation** using [INSTALL.md](INSTALL.md). The skill is at the repository root: `SKILL.md` and its supporting files belong in one `wyn-clarify/` skill folder. Use your host's skill installer or skills directory, verify the installed files, and tell the user where the skill was installed and how to use it.

### Install from a terminal

If you use the [Skills CLI](https://github.com/vercel-labs/skills), run:

```bash
npx skills add wynwithus/wyn-clarify --skill wyn-clarify
```

Choose your assistant and installation scope when prompted. Add `--global` for an installation available across projects. This optional method requires Node.js 22.20 or later; an agent can also use its own installer.

## Import the ZIP yourself

[Download wyn-clarify.zip](https://github.com/wynwithus/wyn-clarify/releases/latest/download/wyn-clarify.zip) and use your assistant's skill import option. The ZIP contains a `wyn-clarify/` folder with `SKILL.md` at its root and all supporting files.

For a manual file installation, put that folder in your assistant's skills directory. For example, Claude Code uses `~/.claude/skills/wyn-clarify/` for personal skills. Agents should follow [INSTALL.md](INSTALL.md) to choose the correct location for their host.

## Use after installation

Ask your assistant to use WYN Clarify, then describe your idea. For example: “Use WYN Clarify to help me plan a tool for our event volunteers.” Claude Code also supports `/wyn-clarify`; Codex supports `$wyn-clarify`.

Say “show me the plan” when you want it to write a plan from the discussion so far.

## Chat without skill installation

If your chat cannot install reusable skills, [COPY-PASTE-PROMPT.txt](COPY-PASTE-PROMPT.txt) is an alternative. Paste its contents and add your idea after “Begin with this idea or problem.” Or attach the file and say: “Follow the attached WYN Clarify prompt for this conversation. My idea is: …”

This option applies to the current conversation. Reuse in another chat depends on whether your app saves instructions.

## What you get

- A specific problem and the person who experiences it.
- A recommended solution and a small first-version scope.
- The journey from starting the task to getting a useful result.
- Essential features and clear ways to check that they work.
- Important assumptions and unanswered questions, clearly labeled.

The skill does not need an API key, an account with WYN, or a background service. Your chosen AI tool may have its own fees. It does not automatically build or publish your product.

## Files

- [SKILL.md](SKILL.md) — complete skill instructions.
- [START-HERE.md](START-HERE.md) — workflow and usage notes.
- [COPY-PASTE-PROMPT.txt](COPY-PASTE-PROMPT.txt) — an alternative for chats without skill support.
- [references/no-ai-slop.md](references/no-ai-slop.md) — included writing guidance, with its [third-party MIT notice](references/no-ai-slop-LICENSE).

## Rights and attribution

You may **fork, improve, reuse, and share** WYN Clarify, including commercially, under the [MIT License](LICENSE).

**You must credit Nick Cybela** by retaining his copyright notice and the full MIT permission notice in all copies or substantial portions of the skill, including modified versions. Keep other applicable copyright notices too. See [TERMS.md](TERMS.md) for the reuse and attribution details.
