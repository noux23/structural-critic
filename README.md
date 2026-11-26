# structural-critic

> A reasoning skill that takes a claim apart **without** becoming a smug debunker.

`structural-critic` teaches an AI agent to pressure-test truth claims, authority claims,
texts, institutions, and belief systems by tracing their architecture: authority chains,
genealogy, category fit, symmetry, incentives, and pragmatic fruits — then holding the
conclusion probabilistically instead of pretending to certainty.

The goal is not to win an argument. The goal is to make the trust-chain visible, find the
load-bearing wall, and say clearly what is established, what is probable, what is inferred,
and what is speculative.

The pattern is domain-general — religion, ideology, institutions, science claims, media
narratives, personal beliefs — but it was forged on religious apologetics, so the examples
lean that way.

---

## Why this exists

Most "critical thinking" prompts produce one of two failure modes:

1. **The debunk-first reflex** — hunt for the flaw before understanding the claim, then
   declare victory over a strawman.
2. **The "it's a mystery" shield** — protect the claim from any test by making it
   unfalsifiable.

This skill is built to avoid both. It steelmans first, distinguishes *false* from
*incomplete* from *harmful*, and refuses to treat "this was constructed by humans" as if it
proved "this is false."

---

## Install

A skill is just a folder containing `SKILL.md`. Copy this folder into your agent's skills
directory.

**OpenCode (global):**

```bash
git clone https://github.com/noux23/structural-critic.git \
  ~/.config/opencode/skills/structural-critic
```

**OpenCode (per project):**

```bash
git clone https://github.com/noux23/structural-critic.git \
  .opencode/skills/structural-critic
```

**Claude Code:**

```bash
git clone https://github.com/noux23/structural-critic.git \
  ~/.claude/skills/structural-critic
```

Restart the agent (or start a new session) so the skill is discovered. The folder name and
the `name:` field in the frontmatter should both be `structural-critic`.

---

## Use it

Skills trigger on intent. Ask something like:

- "Is this claim actually justified, or is it a trust-chain?"
- "Why do people believe this?"
- "Critique this religious apologetic without being a jerk about it."
- "Who gets to define truth here?"
- "Pressure-test this argument — where's the weakest link?"

The agent then runs the protocol below and returns the output template.

### Example output shape

```
CLAIM:            [one line, steelmanned]
AUTHORITY CHAIN:  [what it rests on, where it bottoms out]
STRONGEST POINT:  [what survives]
THE SEAM:         [the weakest link / unresolved tension]
CALIBRATION:      [established / probable / inferred / speculative]
ONE-LINER:        [repeatable summary]
```

---

## How it works

### The 30-second pass

1. What exactly is being claimed — and what is being smuggled in as the authority?
2. Where does the authority chain bottom out?
3. What is the strongest version of this claim?
4. Who wrote/compiled/edited/canonized it, when, and against what rival?
5. Are the concepts portable across frameworks, or is this a category error?
6. Would the argument work if reversed and applied to the arguer's own tradition?
7. What would this look like if it were a human construction?
8. Who benefits from this reading, and what does the structure need to survive?
9. Where is the seam — the weakest link, the unresolved tension?
10. Calibrate, then give the one-liner.

### The full protocol

| Step | Move |
|---|---|
| 0 | **Restate and separate** — split proposition / authority / inference |
| 1 | **Map the authority chain** — follow it until it bottoms out |
| 2 | **Steelman** — state the best version in one paragraph |
| 3 | **Run the genealogy** — authorship, editing, canonization, rivals |
| 4 | **Category audit** — are the concepts actually portable? |
| 5 | **Symmetry test** — reverse it and apply it to the arguer |
| 6 | **Trust-chain reduction** — testimony, text, experience, or power? |
| 7 | **Separate the levels** — institution / doctrine / interpretation / text / experience |
| 8 | **Trace the incentive** — who benefits, what must survive |
| 9 | **Counterfactual construction test** — if it were built by humans, what would it look like? |
| 10 | **Pragmatic test** — fruits, without gaslighting |
| 11 | **Locate the seam** — one decisive tension, not ten scattershot objections |
| 12 | **Calibrate and deliver** — established / probable / inferred / speculative |

### Named moves

The skill ships a library of reusable moves, including:

- *"Same structure, different costume."*
- *"That's a trust-chain, not a proof."*
- *"From the outside, the analogy is symmetrical."*
- *"What's the load-bearing wall?"*
- *"What was left out, and who decided?"*
- *"The universal is someone's particular."*
- *"Retrofit detection."*
- *"Dead vs. live reference point."*
- *"Cheap vs. expensive facts."*
- *"Set and subset."*

---

## Guardrails

The skill is explicitly instructed to:

- Steelman before striking.
- Never confuse genealogy with refutation.
- Never confuse institution with doctrine with text with experience.
- Mark structural inference as inference.
- Avoid romanticizing the alternative.
- Avoid reducing religion to function.
- Leave room for informed trust: *"I know it's a trust-chain and I choose it"* is a
  legitimate reply.
- Name the critic's own trust-chain.
- Distinguish immanent from external critique.
- Never perform superiority.

---

## What it is not

- It is not an atheism tool. It runs the same test on secular ideologies, institutions, and
  the critic's own position.
- It is not a fact-checker. It reasons about the *structure* of claims, not the truth of
  every empirical detail.
- It is not a debate-winner. If it works, the output should be usable by someone who still
  holds the belief.

---

## License

MIT — see [LICENSE](LICENSE).

## Credits

Framework, notes, and examples developed by the author. Drafted with an AI assistant from
the author's own material; edited and curated by hand.
