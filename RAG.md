# Retrieval contract

The purpose of retrieval here is not to return the most semantically similar paragraph. It is to construct a mechanically coherent answer whose claims remain inside the evidence boundaries of the sources.

## Always retrieve first

1. `MODEL.md`
2. `AGENTS.md`

These files define the ontology and evidence rules. Topical retrieval without them is incomplete.

## Query decomposition

For a lumbar question, derive retrieval terms along these axes before searching the corpus:

- geometry: flexion, extension, rotation, lateral bend, pelvic rotation, hip motion;
- support: standing, sitting, supine, prone, supported legs, suspended load;
- activity: passive, active, isometric, dynamic, perturbation;
- loading: compression, tension, shear, bending moment, axial rotation;
- duration: seconds, minutes, hours, chronic exposure;
- history: after sleep, after work, repeated loading, recovery;
- outcome: pain, range, passive stiffness, muscle activation, force, fatigue, creep, stress relaxation;
- evidence population/model: human, animal, cadaver, isolated tissue, computational.

Do not search only the symptom words.

## Retrieval ranking

Prefer sources matching, in order:

1. geometry and loading mode;
2. human/model class;
3. duration and load history;
4. measured outcome;
5. population;
6. semantic similarity of prose.

A paper with the same word `stretch` but different geometry and loading is usually less relevant than a mechanically matching paper using different terminology.

## Evidence-boundary record

Every retrieved source should expose a compact boundary record:

```text
model = human | animal | cadaver | isolated_tissue | computational
population = ...
geometry = ...
load_control = force | displacement | voluntary_position | other
load = ...
duration = ...
repetitions = ...
measured = ...
acute_or_adaptation = ...
recovery_window = ...
```

Missing fields remain unknown. Do not fill them from intuition.

## Answer construction

Build answers in this order:

1. reconstruct the user's geometry and loading;
2. identify the mechanical variables that could plausibly change;
3. retrieve experiments that directly constrain those variables;
4. distinguish observed results from extrapolation;
5. state alternative mechanisms when the evidence cannot discriminate them;
6. avoid translating a measured quantity into a different one without justification.

Examples of forbidden translations:

- reduced passive stiffness -> muscle weakness;
- increased range of motion -> instability;
- pain -> tissue damage;
- muscle activation -> useful force;
- disc height change -> whole-spine flexibility;
- animal ligament creep -> identical human response;
- prolonged full flexion -> mild supported lumbar positioning.

## Contradiction handling

When two sources appear to disagree, compare their boundary records first. Common apparent contradictions come from:

- different lumbar directions;
- different lumbar levels;
- force-controlled versus displacement-controlled loading;
- healthy versus symptomatic populations;
- morning versus afternoon testing;
- different preceding recumbency or work exposure;
- acute versus chronic outcomes;
- passive versus active measurement.

Only call findings genuinely conflicting after these variables have been checked.

## Corpus format

`source.tsv` is the source ledger. Notes should use one Markdown file per paper or tightly related experiment family, with front matter containing the evidence-boundary fields above.

Do not mirror copyrighted full text without redistribution rights. Notes should summarize the experiment, preserve important numerical results, record limitations, and link to the canonical source.
