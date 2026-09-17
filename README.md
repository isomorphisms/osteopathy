# osteopathy

A mechanics-first evidence corpus for reasoning about the human musculoskeletal system.

The first slice focuses on the lumbar spine: geometry, loading, passive tissue mechanics, active muscular stiffness, motor control, pain adaptation, and time-dependent behavior.

The repository is intentionally not a collection of generic back-pain advice. Claims should preserve the boundary of the evidence that supports them: species, tissue or whole-body model, loading direction, load magnitude, duration, posture, and measured outcome.

## Lumbar mechanics RAG

Start with:

- `MODEL.md` — the mechanical ontology;
- `AGENTS.md` — evidence-boundary and terminology rules;
- `RAG.md` — query decomposition, retrieval ranking, and answer construction;
- `sources.tsv` — source ledger with explicit study boundaries;
- `notes/` — per-source notes written for retrieval rather than generic summaries;
- `evals/` — failure-mode fixtures that test whether retrieval preserves geometry, loading, history, and model class.

The initial source ledger includes human experiments, reviews, mixed human/cadaver work, and explicitly labeled animal work. The point is not to make these sources interchangeable. It is to make the boundary of every retrieved claim machine-visible.

## Retrieval principle

Mechanical similarity outranks lexical similarity.

For example, a paper about prolonged loaded lumbar flexion should not outrank a mechanically closer source merely because both the paper and the query contain the word `stretch`.

Before answering a lumbar question, reconstruct:

1. geometry;
2. body support;
3. external load and moment;
4. passive versus active participation;
5. exposure duration;
6. preceding load history;
7. the actual measured or reported quantity.

Only then retrieve evidence.
