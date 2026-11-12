# lit-symbol-translation

**Before any formula or number from a paper enters your work: map it explicitly onto your own notation, verify the meaning on four axes, and recompute the value — the discipline that keeps dimensional and convention errors out of derivations, code and manuscripts.**

> [!NOTE]
> This repository is **written and maintained entirely by AI agents** under human direction — see [AI-maintained](#ai-maintained).
> Documentation is English-first; a Chinese README is available ([README.zh-CN.md](README.zh-CN.md)), and a Chinese SKILL companion ([SKILL.zh-CN.md](SKILL.zh-CN.md)).

## Why

Notation is where research errors hide best: two papers writing the same letter need not mean the same quantity, and a symbol transferred without mapping plants a dimensional or convention bug that "looks obvious" and survives review. This skill codifies the guard discipline, distilled from real simulation and manuscript work:

- **Explicit mapping, two legal forms** — a symbol correspondence table (`their symbol → ours → dimensions → note`) for batch use, or a one-sentence note at first use; keeping the mapping in your head is forbidden.
- **Four-axis meaning check** — physical definition, reference frame, dimensions, normalization basis; all four must pass before two notations count as the same quantity.
- **Three typical mismatch classes** — different reference frames (nozzle speed vs. substrate speed), different characteristic bases (extrudate vs. inlet velocity; We built on which velocity?), and same-name-different-meaning.
- **No correspondence → human review** — never guess-apply; mark it, state what is uncertain, wait for a ruling.
- **The recomputation discipline** — every literature number is re-derived via the original formula or a conservation relation and carries its primary source; transcribed numbers (including from your own old documents) are unusable unverified.

A small skill by design: one concept, one page of rules, outsized error-prevention value.

## Install as a skill

```
git clone https://github.com/Laitangtang-lab-workflows/lit-symbol-translation ~/.agents/skills/lit-symbol-translation
```

Works with any agent harness supporting the SKILL.md convention (Claude Code, DeepSeek Harness, …); equally readable as plain documentation.

## Repository layout

| Path | Content |
|---|---|
| `SKILL.md` | Skill entry point: the core rules |
| `references/symbol-rules.md` | The full standard: mapping forms, four-axis check, mismatch classes, review flow, recomputation |

## AI-maintained

Every file in this repository — documentation, this README — is written and updated by AI agents under human supervision, and the rules were distilled from incidents where an unmapped symbol or an unverified number corrupted real work. Expect commits to be machine-authored; humans review direction and decisions, not lines.

## License

[CC0-1.0](LICENSE) — released to the public domain. Use, fork and vendor it into anything, no attribution required (a nod is always appreciated).

By submitting a pull request you agree that your contributions are dedicated under CC0 as well.
