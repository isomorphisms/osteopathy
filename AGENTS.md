# AGENTS.md

This repository is an evidence corpus, not a source of generic clinical boilerplate.

## Core rule

Preserve the boundary of every claim.

For each source-derived statement, keep track of:

- human, animal, cadaver, isolated tissue, or computational model;
- healthy, symptomatic, injured, degenerated, or otherwise selected population;
- posture and direction of motion;
- force-controlled or displacement-controlled loading;
- load magnitude when known;
- exposure duration and repetition count;
- measured variable;
- recovery interval;
- whether the result is acute or an adaptation across days, weeks, or months.

Do not silently generalize across these fields.

## Vocabulary

Keep these concepts distinct:

- position: geometry of the body;
- motion: change in position;
- load: force and moment applied to a structure;
- passive stiffness: change in passive resisting force or moment per change in position;
- active stiffness: stiffness produced by muscle activation and co-contraction;
- strength: force-producing capacity;
- fatigue: reduction in force-producing capacity after activity;
- guarding: altered muscle activation associated with protection or pain;
- stability: resistance to uncontrolled displacement under perturbation;
- range of motion: accessible geometry, not strength or stability;
- creep: time-dependent deformation under sustained load;
- stress relaxation: time-dependent reduction in stress under sustained deformation;
- hysteresis: path dependence between loading and unloading;
- pain: an experience; never use it alone to identify a tissue or mechanical state.

Do not use `tight`, `loose`, `weak`, or `unstable` as if they were interchangeable mechanical quantities.

## Geometry first

Before interpreting a movement, state the reference frame. Distinguish at minimum:

- pelvic rotation;
- lumbar flexion/extension;
- hip flexion/extension;
- whole-trunk orientation;
- motion at individual lumbar levels when evidence permits.

Supine/prone/standing changes the meaning of casual directional language. Do not infer anterior/posterior pelvic rotation from words such as `forward` without reconstructing the geometry.

## History matters

Mechanical state is path-dependent. When relevant, include:

- preceding sleep or recumbency;
- preceding hours of loading;
- duration in the current position;
- prior repetitions;
- habitual exposure over months or years;
- time since the exposure ended.

Do not turn a time-of-day observation into a universal rule independent of loading history.

## Retrieval behavior

`MODEL.md` and `RAG.md` are control documents. Retrieve them with every lumbar-mechanics question before retrieving topical notes.

Prefer a small number of directly relevant sources over a large bag of vaguely related papers.

When evidence conflicts, preserve the disagreement and inspect differences in population, geometry, loading protocol, duration, and measured outcome before calling it contradictory.

When the evidence does not identify a tissue or mechanism, say so. A plausible mechanical explanation may be labeled as a hypothesis, but not promoted to an observed fact.

## Source handling

Do not commit copyrighted article text unless redistribution is clearly permitted. Store citation metadata, links, short quotations within fair-use limits, and original notes. Openly licensed full text may be mirrored with its license and provenance recorded.
