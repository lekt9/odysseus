# ODYSSEY.md — the Odyssey, mapped onto Odysseus

> Odysseus is named for Homer's hero: a master of **metis** (cunning) who endures
> a long sequence of trials to reach **nostos** (homecoming) at **Ithaca**. This
> document maps the poem onto the codebase, so the project's design grows
> *deliberately* toward the story it is named after. It is the roadmap for an
> ongoing series of small, themed-but-real feature PRs (each labelled `odyssey`).

Every row pairs an element of the Odyssey (cited to its Book) with a concrete,
shippable feature or upgrade in this repo (cited to a real engineering source).
Nothing here is cosmetic-only — each is a genuine capability the workspace should
have; the Odyssey simply names *why* and *in what order*.

## The map

| theme | Odyssey element (Book) | repo feature / upgrade | engineering source |
|---|---|---|---|
| **home** | Ithaca / nostos — home is the fixed goal every wandering points back to (Bk 1 proem) | local-first sovereignty: a startup integrity self-check that anchors every feature to the verified local instance | https://www.inkandswitch.com/local-first/ |
| **the unit** | a single trial as a complete episode — Cyclops, Circe, Sirens (Bks 9–12) | a well-formed agent **Task**: owner, action, trigger, target, rationale, verb (the W6H cell) | arxiv:1509.07360 |
| **nesting** | tale-within-a-tale — Odysseus narrates his own story to the Phaeacians (Bks 9–12) | hierarchical agent decomposition: a task spawns sub-tasks, the Tree-of-Thoughts search shape | arxiv:2305.10601 |
| **cunning** | metis — the wooden horse & olive stake (build), scouts & disguise (route), the "No-man" gambit (read) | the agent tool-call loop as three verb kinds: act / route / read (ReAct) | arxiv:2210.03629 |
| **proof** | the bow & the bed-secret — only the true claimant can pass the test (Bks 21, 23) | challenge-response identity: strengthen the re-auth / 2FA gate | https://en.wikipedia.org/wiki/Challenge%E2%80%93response_authentication |
| **corroboration** | recognition by many tokens — scar, bed, orchard trees (Bks 19, 23, 24) | multi-model / multi-source agreement: Compare blind test + Deep Research cross-source consistency | arxiv:2203.11171 |
| **memory** | the scar Eurycleia knows — a permanent mark of identity (Bk 19) | the embedding / memory store (ChromaDB + fastembed): recall by key, don't recompute | github:chroma-core/chroma |
| **the guard** | wax in the crew's ears at the Sirens — a guard placed *before* a known-fatal input (Bk 12) | prompt-injection / unsafe-content guard at the model boundary | github:protectai/rebuff |
| **the voyage** | the journey — each island an unresolved stop, Tiresias/Circe give the route ahead (Bks 10–12) | Deep Research source-frontier traversal: a queue of sub-questions, each visited once | github:Alibaba-NLP/DeepResearch |
| **endurance** | Penelope's web & Odysseus the *polytlas* ("much-enduring") — weave, unravel, re-weave (Bk 2) | agent self-correction: act, observe the real result, and on failure re-plan rather than repeat (Reflexion) | arxiv:2303.11366 |

## Roadmap (one real PR per item, labelled `odyssey`)

Ordered roughly by ascending effort. Each shipped item surfaces the next.

1. **The proem** — this `ODYSSEY.md`: the map of poem → features. *(this PR)*
2. **Ithaca anchor** — a startup local-instance integrity self-check.
3. **Mentor mode** (Athena, Bks 1–2) — contextual first-run guidance for new users.
4. **Argos** (Bk 17) — recognise a returning user, restore the last live session.
5. **The Sirens' wax** (Bk 12) — prompt-injection guard at the model boundary.
6. **The bow** (Bk 21) — strengthen the re-auth / 2FA challenge gate.
7. **Recognition tokens** (Bks 19/23) — surface cross-source agreement in Deep
   Research and the Compare blind test.
8. **Tiresias' look-ahead** (Bk 11) — research frontier with planned ordering.
9. **Penelope's loop** (Bk 2) — agent self-correction / retry on failed steps.
10. **Telemachy** (Bks 1–4) — hierarchical sub-task decomposition for the agent.
11. **Scylla & Charybdis** (Bk 12) — a "least-bad" fallback when every model/route
    errors, instead of a hard failure.
12. **Aeolus' bag of winds** (Bk 10) — bounded, revocable capability grants to the
    agent (don't loose every wind at once).

The list continues past these — the journey is the point.
