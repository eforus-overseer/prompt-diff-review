# Prompt Diff Review

> Make meaningful security changes in system prompts and agent configs reviewable in CI.

**Status:** open project seed · **License:** MIT · **Contributions:** welcome

A GitHub Action concept for semantic change summaries and risk checklists on prompts, tool definitions, and agent policies.

## The question

Did a prompt/config change add a capability, weaken a boundary, expose a secret, or remove an approval requirement?

## Why build this

Prompt wording is not a security boundary. The tool will flag review-worthy diffs and traceable capability changes, never certify that a prompt is safe.

## First milestone

Plain-text and YAML diff parser; deterministic checks for a handful of risky patterns; review annotations; sample repo fixtures; no LLM required in CI.

## A first contribution

**Choose a minimal config format and write tests for changed tool access, removed approval language, and a harmless wording-only edit.**

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for the small, reviewable contribution flow. You can also open an issue with the **good first issue** template, propose a test fixture, review a design choice, improve documentation, or help keep the scope honest. No model API key is needed for the initial milestone.

## Working principles

- Treat model output and retrieved content as untrusted input.
- Prefer deterministic controls, explicit assumptions, and reproducible fixtures.
- Use synthetic or public-domain examples; do not commit credentials, private prompts, personal data, or customer logs.
- Report limits and false positives. A benchmark score or static rule is not a security guarantee.
- Keep security tests inside local fixtures or systems you own and have permission to test.

## Research map

This seed is informed by the [OWASP GenAI Security Project](https://genai.owasp.org/), including its LLM and Agentic Application guidance, and by active open-source work such as [garak](https://github.com/NVIDIA/garak), [promptfoo](https://github.com/promptfoo/promptfoo), [LLM Guard](https://github.com/protectai/llm-guard), and [PyRIT](https://github.com/Azure/PyRIT). Each project aims for a narrow, inspectable contribution rather than a replacement for those broader tools.

[Compare star histories for garak, promptfoo, LLM Guard, and OWASP's LLM Top 10](https://star-history.com/#NVIDIA/garak&promptfoo/promptfoo&protectai/llm-guard&OWASP/www-project-top-10-for-large-language-model-applications). GitHub stars are an attention signal, not evidence of security quality.

## Join in

If this problem interests you, start with the first milestone above. Open an issue to discuss scope before building a large feature, or send a small pull request with a test and a clear explanation. Contributors from security, engineering, research, design, and documentation are all welcome.
