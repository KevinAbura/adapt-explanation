![Adapt Explanation](assets/social-preview.png)

# Adapt Explanation

Explain anything for any audience—without dumbing it down.

`adapt-explanation` is an open agent skill for Codex and ChatGPT that adapts explanations and rewrites to a reader's age, expertise, role, goal, language, tone, and desired depth. It keeps the facts, uncertainty, warnings, identifiers, and technical distinctions that matter.

[繁體中文](README.zh-TW.md) · [Prompt gallery](examples/prompt-gallery.md) · [Skill instructions](skills/adapt-explanation/SKILL.md)

## Why use it?

A good explanation is not merely shorter. It gives the right reader the right mental model without replacing the truth with a cute analogy.

- Explain a concept to a child, beginner, practitioner, expert, or executive.
- Produce simple and technical versions side by side.
- Rewrite source material without inventing claims or dropping qualifications.
- Preserve commands, code identifiers, API fields, formulas, citations, and warnings.
- Keep high-stakes medical, legal, financial, security, and safety safeguards intact.
- Work in the language requested by the user.

## Quick start

Ask Codex to install the standalone skill from this repository:

```text
Use $skill-installer to install the adapt-explanation skill from:
https://github.com/KevinAbura/adapt-explanation/tree/main/skills/adapt-explanation
```

Then invoke it explicitly:

```text
$adapt-explanation Explain OAuth to a curious five-year-old.
```

Codex can also activate the skill automatically when a request matches its description.

## Try these prompts

```text
$adapt-explanation Explain Kubernetes for a child, a backend beginner,
and a CTO. Keep each version under 120 words.
```

```text
$adapt-explanation Rewrite this API guide for a new backend engineer.
Keep every command and JSON field exact.
```

```text
$adapt-explanation Explain this architecture decision twice:
first for leadership, then for senior engineers.
```

```text
$adapt-explanation 用繁體中文解釋 OAuth。
先給五歲小朋友版，再給資深後端工程師版。
```

See the [prompt gallery](examples/prompt-gallery.md) for a side-by-side example.

## How it works

The skill follows a small adaptation loop:

1. Determine the audience, purpose, language, tone, and desired depth.
2. Select an audience profile.
3. Identify facts and safeguards that must survive simplification.
4. Adapt vocabulary, examples, structure, and detail.
5. Check that the result is clear, useful, and not misleading.

The main workflow lives in [`SKILL.md`](skills/adapt-explanation/SKILL.md). Audience defaults live in [`audience-profiles.md`](skills/adapt-explanation/references/audience-profiles.md).

## Plugin-ready structure

This repository includes a Codex plugin manifest and can be packaged for plugin distribution:

```text
.
├── .codex-plugin/plugin.json
├── skills/adapt-explanation/
│   ├── SKILL.md
│   ├── agents/openai.yaml
│   └── references/audience-profiles.md
├── assets/
├── examples/
└── LICENSE
```

## Contributing

Issues and pull requests are welcome. Useful contributions include:

- realistic before-and-after examples;
- audience profiles that avoid stereotypes;
- tests for misleading analogies or lost qualifications; and
- clearer triggering language.

## License

MIT © Kevin Abura
