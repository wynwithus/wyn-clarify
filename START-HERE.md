# WYN Clarify (v0.3.1)

**Purpose:** Help someone start with a high-level idea or practical problem and finish with a clear, focused plan for something they could build.

**Automatic activation:** The `SKILL.md` frontmatter describes when an LLM should select `wyn-clarify`. It includes vague product ideas, premature feature requests, everyday frustrations to turn into buildable solutions, and continuation of product planning. The activation guidance explicitly avoids hijacking ordinary advice requests.

**Conversation design:** The user gets an insight, the assistant's recommendation, and no more than one consequential question. In the background the assistant uses Double Diamond and three separate problem-framing passes with individual criteria, then consolidates their outputs.

**End product:** A right-sized, feature-level product requirements document. Privacy, integrations, complex workflows, and other requirements are added only when they matter to the actual idea.

## Using it

For the least setup, paste `COPY-PASTE-PROMPT.txt` into a new chat and add your idea at the end. No tools or extensions are required. This applies to that conversation; a new chat may need the prompt again. See the README's platform guide for reusable installations and documented limitations.

- Install/upload the packaged skill into a skills-capable assistant or skill manager. Actual installation controls depend on the host.
- On a chat system without skill support, paste `COPY-PASTE-PROMPT.txt`, then describe the idea or problem.
- Try: "I want to build an assistant for my kids' schedules," "I hate deciding what to make for dinner and want to solve it," or "Help me develop a tool for coordinating event volunteers."

**Accuracy note:** Independent passes in a single prompt are *procedurally* independent; they are not three isolated agent/model executions. Hidden rubrics and short repair loops help low-reasoning models, but behavior must be tested on each target model. This is an instruction-based skill, not a background-running agent.
