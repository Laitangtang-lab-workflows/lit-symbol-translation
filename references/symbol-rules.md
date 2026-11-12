# Symbol translation and recomputation rules (detail)

> Origin: this file is the canon (a generic rewording of a house research standard; rules equivalent); project-side instances follow it, and major revisions sync both ways.

## 1. Why "translation" is needed

Every paper has its own notation, reference frames and normalization bases. Two papers writing the same letter need not mean the same physical quantity; two papers writing different letters may mean the same one. **Any direct transfer without mapping plants a dimensional or convention error into your derivation, code or manuscript** — and this class of error is the hardest to find later, precisely because it hides inside notation that "looks obvious".

## 2. Explicit mapping: two legal forms

Before quoting a formula/symbol/concept, build an explicit mapping onto your own notation — either form:

1. **A symbol correspondence table**: for batch quoting (a whole derivation, a whole parameter file) — columns `literature symbol → our symbol → dimensions → note (frame/basis differences)`;
2. **A one-sentence note in the text**: for occasional quotes — at first use, state "the paper's $X$ is our $Y$ (note …)".

**Forbidden**: keeping the correspondence only in your head, or confirming it verbally without writing it down — the mapping must be archived alongside the derivation/code/manuscript for later verification.

## 3. Verify the meaning item by item (all four pass = the same quantity)

| Check | Ask | Common trap |
|---|---|---|
| Physical definition | are the two defining formulas the same? | same name, different meaning: the paper's $\lambda$ is a relaxation time, yours may be a dimensionless number |
| Reference frame | relative to which frame is it defined? | the same velocity differs by a sign convention between the nozzle frame and the substrate frame |
| Dimensions | do units and dimensions agree? | mixing the dimensional and the nondimensionalized version |
| Normalization basis | what characteristic quantity was divided out? | two quantities both called We, built on inlet vs. outlet vs. substrate velocity, are entirely different |

### The three typical mismatch classes (where differences hide)

1. **Different reference frames**: the same physical quantity carries different symbols in two languages — nozzle-moving speed $v_n$ and substrate-moving speed $u_s$ are the same printing speed in two frames (numerically equivalent, at most a sign convention apart).
2. **Different characteristic bases**: same-named quantities built on different characteristics — extrudate velocity $v_e$ vs. inlet velocity $u_i$, one based on the cross-section average, one on the inlet value; dimensionless numbers (Re, Wi, We, Ca, …) are the worst — always confirm which characteristic velocity/length/stress they use.
3. **Same name, different meaning**: one symbol denoting different objects in the paper and in your system.

## 4. No correspondence → human review

If a symbol or concept cannot be mapped strictly onto your system — vague definition, unclear frame, doubtful basis, undisclosed key settings — **never guess-apply**:

- Mark "**pending human review**" in the derivation/manuscript, stating exactly what is uncertain (what information is missing; what the two possible readings are);
- use it only after a ruling; record the ruling into the correspondence table.

The cost of a guessed application (a wrong dimensional convention entering a derivation or parameter file) vastly exceeds the cost of stopping to ask once.

## 5. The recomputation discipline

Any number introduced from the literature or external data — experimental parameters, dimensionless numbers, critical constants, material constants — before entering any research document, code or parameter file:

1. **Recompute once by substitution** into a conservation relation or the original formula — flow conservation, geometric relations, the dimensionless-number definitions — reproducing the value in your own conventions and comparing against the paper's;
2. **note the primary source**: the paper's entry plus page/table/equation number;
3. **values transcribed across documents may not be used unverified**: a number in your own old document is also a "transcription" — it may rest on an outdated convention or an already-corrected parameter.

When a recomputation disagrees with the paper, first suspect a convention difference (§3), then the paper; if neither can be excluded, enter the §4 human-review flow.
