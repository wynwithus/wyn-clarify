# WYN Clarify (v0.3.3)

Created by Nick Cybela. Shared free through WYN.

**Purpose:** Help someone start with a high-level idea or practical problem and finish with a clear, focused plan for something they could build.

**Automatic activation:** The `SKILL.md` frontmatter describes when an LLM should select `wyn-clarify`. It includes vague product ideas, premature feature requests, everyday frustrations to turn into buildable solutions, and continuation of product planning. The activation guidance explicitly avoids hijacking ordinary advice requests.

**Conversation design:** The assistant asks no more than one useful question at a time and recommends a starting point when it has enough information. Its included no-ai-slop writing rules keep replies direct and specific. In the background, it uses Double Diamond and three separate problem-framing passes to check that the proposed solution addresses the problem.

**End product:** A right-sized, feature-level product requirements document. Privacy, integrations, complex workflows, and other requirements are added only when they matter to the actual idea.

## Install with your agent

Give your agent https://github.com/wynwithus/wyn-clarify and ask it to install `wyn-clarify` as a reusable skill. Agents: complete the setup in [INSTALL.md](INSTALL.md), verify the installed files, and report the installation path and how to use the skill.

To install it yourself, import the release ZIP using your assistant's skill controls, or put the complete `wyn-clarify/` folder in its skills directory. See [README.md](README.md) for the terminal command and setup options.

## Use it

After installation, ask your assistant to use WYN Clarify and describe your idea or problem. Try: “I want to build a tool for coordinating event volunteers.”

Say “show me the plan” when you want it to write a plan using what you've discussed. It will identify important gaps rather than making you answer every possible question first.

For a chat without skill installation, paste `COPY-PASTE-PROMPT.txt` or attach it and explicitly ask the assistant to follow it. That option applies to the current conversation.

**Accuracy note:** Independent passes in a single prompt are *procedurally* independent; they are not three isolated agent/model executions. Hidden rubrics and short repair loops help low-reasoning models, but behavior must be tested on each target model. This is an instruction-based skill, not a background-running agent.
