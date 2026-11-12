---
name: lit-symbol-translation
description: >-
  The "translation" discipline for symbols and numerical values taken from the literature: before any formula, symbol, concept, experimental parameter, dimensionless number or critical constant from a paper enters your work, build an explicit mapping onto your own notation and verify the meaning matches (physical definition, reference frame, dimensions, normalization basis), and recompute numbers by substituting them into the original formulas. Use when putting literature formulas/parameters into derivations, code, parameter files or manuscripts, building symbol correspondence tables between papers, or checking "is their x our y". Three typical mismatch classes: different reference frames, different characteristic bases, same-name-different-meaning. When no strict correspondence can be established, flag for human review — never guess. Note: this skill governs symbol and value translation, not Chinese-English language translation. Chinese companion: SKILL.zh-CN.md.
---

# Lit Symbol Translation — translating literature symbols and recomputing values

Quoting any formula, symbol or concept from the literature **without translating it is forbidden** — first build an **explicit mapping** onto your own working notation (a symbol correspondence table or a one-sentence note in the text), and only after confirming the meaning corresponds strictly may it enter a derivation, code, parameter file or manuscript.

## Core rules (quick reference)

1. **Verify the meaning item by item**: physical definition, reference frame, dimensions, normalization basis — all four must match before two notations count as "the same quantity".
2. **Three typical mismatch classes** (where notation differences hide):
   - **Different reference frames**: the same physical quantity carries different symbols in two languages — nozzle-moving speed $v_n$ and substrate-moving speed $u_s$ are the same printing speed expressed in two frames (numerically equivalent, at most differing by a sign convention);
   - **Different characteristic bases**: same-named quantities built on different characteristics — extrudate velocity $v_e$ vs. inlet velocity $u_i$ each normalize to a velocity at a different location;
   - **Same name, different meaning**: one symbol denoting different objects in the literature and in your own system.
3. **No correspondence → human review**: when a symbol or concept cannot be mapped strictly onto your system (vague definition, unclear frame, doubtful basis, undisclosed key settings) — **never guess-apply**; mark "pending human review" and use it only after a ruling.
4. **Recompute numerical values**: any number introduced from the literature or external data (experimental parameters, dimensionless numbers, critical constants) must be **recomputed once** by substitution into a conservation relation or the original formula, with the primary source noted, before it enters any research document, code or parameter file; **values transcribed across documents may not be used unverified**.

## Full rules

The complete standard (criteria and procedures for the three mismatch classes, the two legal forms of explicit mapping, the human-review flow): [references/symbol-rules.md](references/symbol-rules.md).

## Scope boundaries

- Verifying literature content and evidence retrieval: the project's `reference_materials\` library flow (note-gen / academic-markup skills);
- this skill governs **the translation discipline for symbols and values only** — not the truth or retrieval of the literature, and not Chinese-English language translation.
