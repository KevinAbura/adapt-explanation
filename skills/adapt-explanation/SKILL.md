---
name: adapt-explanation
description: Adapt explanations and rewrites to a reader's age, expertise, role, goal, tone, language, and desired depth without losing essential meaning. Use for requests such as "explain like I'm five" (ELI5), child-friendly or beginner-friendly explanations, expert or executive summaries, audience-specific teaching, jargon reduction, layered explanations, and rewriting material for a different readership.
---

# Adapt Explanation

Make an explanation feel natural to its intended reader while preserving accuracy, uncertainty, and important limitations.

## Follow the Adaptation Workflow

1. Identify the subject, intended audience, purpose, requested language, tone, and length from the request and surrounding context.
2. Infer harmless missing details instead of interrupting the task. Default to an intelligent beginner when the audience is unspecified. Ask only when different assumptions would materially change the result.
3. Select the closest audience profile. Read [references/audience-profiles.md](references/audience-profiles.md) when choosing among age, expertise, role, or layered-output profiles.
4. Decide what must survive simplification: the main claim, causal relationships, uncertainty, exceptions, warnings, names, numbers, code identifiers, formulas, and user-provided constraints.
5. Write at the selected level, then check that the reader can understand or act on it without being misled.

## Adapt the Writing

- Lead with the answer or central idea.
- Use the reader's language unless the user requests another language.
- Prefer familiar words, short logical steps, and concrete examples appropriate to the audience.
- Define unavoidable jargon immediately after introducing it.
- Use analogies only when they clarify the underlying structure. State where an analogy stops matching reality when that boundary matters.
- Match detail to the reader's goal: understanding, deciding, implementing, studying, or explaining to someone else.
- Use a layered answer when the audience is mixed: start simple, then add optional detail.
- Keep the tone respectful. Simplicity must not become baby talk, condescension, or fake enthusiasm.
- Do not add quizzes, comprehension questions, role-play, or decorative sections unless they help the request or the user asks for them.

## Handle ELI5 Requests

Treat "explain like I'm five" primarily as a request for clarity, not as proof that the reader is literally five.

- Give the core idea in one or two plain sentences.
- Build the explanation from familiar objects, actions, or experiences.
- Explain one relationship at a time.
- Omit incidental complexity, but retain facts needed to avoid a false conclusion.
- Avoid pretending that an analogy is the mechanism itself.
- For genuinely young readers, avoid age-inappropriate examples and keep instructions safe to follow.

## Preserve Meaning When Rewriting

- Preserve the source's claims, intent, confidence, and important qualifications.
- Do not invent facts or silently resolve ambiguity in the source.
- Retain exact names, commands, error messages, API fields, citations, and quoted text when precision depends on them.
- Flag a tradeoff briefly when the requested reading level cannot preserve a technical distinction.
- Distinguish a faithful rewrite from added explanation when providing both.

## Protect High-Stakes Accuracy

For medical, legal, financial, security, safety, or compliance material, simplify the language rather than the safeguards.

- Retain uncertainty, contraindications, prerequisites, thresholds, warnings, and escalation conditions.
- Do not turn general information into personalized professional advice.
- Avoid childlike analogies that trivialize harm or encourage unsafe action.
- State when a qualified professional or authoritative source is necessary to make the decision.

## Check the Result

Before answering, verify that:

- the opening is understandable at the target level;
- each necessary term is explained or safely omitted;
- the analogy cannot easily be mistaken for literal fact;
- no important limitation disappeared;
- the language, tone, length, and format match the request; and
- the answer remains useful rather than merely simpler.
