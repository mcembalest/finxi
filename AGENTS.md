# AGENTS.md

Rules for AI agents working in this repo.

## files
- `README.md`: the three sections (FINXI, GEN, ICARIA) in the owner's wording. No new concepts or prose.
- `notes/finxi.md`: owner's words only, as a collage.
  - verbatim, typos included
  - allowed: arranging, and cutting conversational leakage ("i really agree", "lol", "you mentioned", answers to an agent's questions)
  - headings come from the owner's own phrases
  - found words are quoted exactly, with a citation
  - no added words beyond minimal punctuation, unless the owner asks for a specific fix
  - after any regrouping, diff against the previous version to confirm no line was lost
- `notes/agent-notes.md`: the only place for agent-written notes.
  - terse bullet fragments with links, enough for the owner to reconstruct an idea in their own words
  - no prose sentences
  - mark verified (✓) vs from memory (?)
- `references/`: PDFs plus `README.md` with one line per reference.
  - minimal basis: keep a reference only if a sentence of the paper would fail without it
  - prefer arXiv; check each download is complete (size matches the source)
  - no PDF when it's not freely available; cite instead
  - fiction (ICARIA) needs no references

## terms
- craftsman / apprentice (teacher / learner in older notes)
- FINXI: the theory of a single creative agent ("a creative agent"); "finxi" = an agent's honest report that it created something
- GEN: Generative Educational Network, any educational network (not necessarily a pair); implemented Cowsik-style, starting with one teacher and one learner
- unbounded (not infinite) workshop; bounded computation, bounded intelligence, bounded creativity
- CREATION over PREDICTION: state it once, not everywhere
- no Minecraft framing (citing Voyager is fine)

## process
- don't rush to implement; no code unless the owner asks for it explicitly
- point out errors, contradictions and weak analogies, including between the notes and the references
- don't overclaim plans
- commits: one short line; no AI attribution trailers (no Co-Authored-By, no session links)
- never commit `.env`
- never name a file `claude.md` (on macOS it resolves to `CLAUDE.md`, which Claude Code loads as instructions)
