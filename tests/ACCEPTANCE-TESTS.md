# Manual acceptance tests for WYN Clarify

Run on the intended low-reasoning model and a stronger reference model. These are test cases, not proof of measured performance.

For each run, record the app, model/version (if shown), date, installation or pasted-prompt mode, transcript, and pass/fail result. Treat an unavailable app or an unrun case as **not tested**, never as a pass. Test the pasted prompt as well as native skill loading where supported.

## Portability and startup

- Start a fresh chat, paste `COPY-PASTE-PROMPT.txt`, and add a product idea. It should begin helping without asking for an API key, extension, browsing, or code execution.
- Repeat in the target assistant's native skill mode where supported, checking that the skill is actually loaded.
- Ask for the plan in the conversation. It should deliver text even if document export is unavailable.
- In a new chat without the prompt or an installed skill, do not assume the previous conversation's instructions persist.

## 1. High-level idea should activate
Input: "I want an assistant to help with my kids' schedules."
Pass: Uses plain language, offers a plausible starting interpretation rather than an entire family-management app, asks at most one useful question, and can eventually specify functional behavior.

## 2. Problem-first should activate
Input: "I hate figuring out what to make for dinner. Can you help me invent something that fixes it?"
Pass: Distinguishes decision fatigue, ingredients, and time as possible blockers without presenting them as facts. Does not immediately assume a fridge-photo app is best.

## 3. Solution-first should not lock in a feature
Input: "Build me a dashboard to make my team more productive."
Pass: Investigates what decision or missed outcome creates the problem; avoids specifying graphs before understanding use.

## 4. Existing detail should prevent needless questions
Input: "Six contractors missed changed arrival windows four times last week because dispatch updates get buried in group texts, causing refunds. Give me a first version to solve that."
Pass: Preserves the facts and moves to a focused solution or draft. Does not ask who the user is or insist on more discovery.

## 5. Ordinary advice should not trigger a product PRD
Input: "I hate deciding what to cook tonight. Any dinner ideas?"
Pass: Gives dinner suggestions. Does not propose a startup, app, or PRD.

## 6. Right-sized feature PRD
Input: "Draft a first version of an app where I photograph groceries and get two simple dinner choices."
Pass: Features cover photo input, ingredient confirmation where needed, meal suggestions, and essential interaction/result states. Does not unpromptedly require enterprise authentication, deep analytics, exhaustive privacy controls, or every edge case.

## 7. User delegates decisions
Input: "Not sure. Use your recommendation and show me the plan."
Pass: Chooses reversible defaults, produces a document, and labels consequential assumptions. Does not insist on answering another question.

## 8. User changes the target problem
Input: "Actually it's not pickups. The challenge is tracking whether permission slips were submitted."
Pass: Revises the problem framing and feature plan; does not keep optimizing pickup coordination.

## Universal checks
- [ ] One or zero questions per assistant response
- [ ] Clear synthesized insight and concrete recommendation when helpful
- [ ] Underlying problem examined, not merely feature acceptance
- [ ] Independent internal criteria included in instructions; no leaked methodology by default
- [ ] Known facts distinguished from assumptions
- [ ] No unnecessary requirements padding
- [ ] Feature behavior is specific enough to test
- [ ] Continues across turns without artificial delays or unbounded internal loops

## Writing and plain-language controls

Start with “I want to build an AI assistant,” then explain the scheduling problem from case 1. Check that the assistant asks for the missing need without generic praise, a catalog of assistant types, or a premature architecture. A response may consist of one useful question. Do not require a fixed sentence or template.

Continue with “Show me the plan.” Check that it writes the plan from known facts, identifies consequential unknowns, and does not build or publish anything. Ordinary requests for a draft should still work.

Supply a deliberately inflated description: “A revolutionary, cutting-edge platform that empowers families and streamlines everything.” Check that the plan describes the actual scheduling behavior without copying the puffery or inventing features and results. Ask for a revision using the person's own wording and verify that their facts and intent survive.

Check that the public description credits Nick Cybela and that bundled third-party writing guidance retains its applicable copyright and license notices. Ordinary planning replies should not repeat credits, writing scores, or editing notes. Repeat these cases with the standalone copy-and-paste prompt, without another skill installed. Record unrun app/model combinations as not tested.
