# Lumbar mechanics model

Use this file as the first-pass ontology for reasoning about lumbar-spine questions.

## 1. State is multidimensional

A back does not have one scalar state called `tightness`.

Represent a useful local state as something like:

- geometry;
- passive tissue loading;
- active muscle loading;
- passive stiffness;
- active stiffness;
- recent load history;
- tissue hydration and other slow state variables;
- pain and sensitivity;
- available range;
- controllable range;
- force capacity within that range.

Two people can occupy nearly the same geometry with very different loads and stiffness. The same person can occupy the same geometry at different times with different mechanical states because the system has memory.

## 2. Geometry is not load

A degree of lumbar extension is not itself a force.

The load associated with a position depends on body support, gravity, external load, muscle activity, contact forces, and the distribution of motion across hips, pelvis, and lumbar levels.

A small movement while supine with the legs supported is therefore not mechanically equivalent to the same apparent lumbar angle while standing with a load in the hands.

## 3. Passive and active resistance are separate

Passive resistance comes from structures including discs, ligaments, joint capsules, fascia, and passive muscle-tendon properties.

Active resistance comes from muscle activation and co-contraction.

Observed resistance to movement is a mixture of both. A change in resistance does not by itself identify which changed.

A person may have a large passive range and still generate high active stiffness when needed. Conversely, restricted passive range does not guarantee useful stability under load.

## 4. The system has memory

Lumbar mechanics are history-dependent.

Relevant mechanisms include:

- creep under sustained load;
- stress relaxation under sustained deformation;
- hysteresis during loading and unloading;
- fluid redistribution in the intervertebral discs;
- changes in muscle activation after sustained or repeated loading;
- adaptation to repeated exposure over longer time scales.

Therefore `same angle` does not imply `same mechanical state` if the preceding history differs.

## 5. Time scales must not be collapsed

### Seconds

Muscle recruitment, perturbation response, breathing-related pressure changes, and rapid changes in active stiffness.

### Minutes

Viscoelastic stress relaxation and creep become measurable; sustained positions may alter subsequent resistance and motor behavior.

### Hours

Disc fluid distribution and cumulative loading history matter. Recovery from sustained loading may be incomplete over short intervals.

### Days to months

Training, tissue adaptation, learned movement, pain-related behavior, strength, endurance, and tolerance can change.

An acute observation cannot automatically be used as evidence of chronic adaptation, or vice versa.

## 6. Breathing is a mechanical input, but not a magic mechanism

Breathing changes thoracic geometry, diaphragm position, abdominal pressure, and muscle recruitment around the trunk. In a supported passive position it can impose small cyclic changes around a mean posture.

That makes breathing relevant to the mechanical state, but it does not by itself identify which tissue is being lengthened or why a position becomes easier over time.

## 7. Range is not one thing

Distinguish:

- passive available range;
- active available range;
- comfortable range;
- pain-limited range;
- load-tolerant range;
- familiar range;
- unfamiliar but mechanically available range.

A position that feels difficult to enter may reflect passive resistance, active guarding, pain sensitivity, unfamiliar motor organization, or some combination.

## 8. Pain does not locate the mechanism by itself

The quality or location of pain can constrain hypotheses, but it does not uniquely identify the loaded tissue.

A statement such as `this feels like a structure that has been compressed for years finally being stretched` is a useful phenomenological observation. Treat the proposed tissue history as a hypothesis until independent evidence identifies the structure and loading pattern.

## 9. Work capacity is not the opposite of mobility

The long-term objective is not maximum passive flexibility and not maximum resting stiffness.

A mechanically useful system can have:

- sufficient accessible range;
- familiarity with that range;
- force capacity across relevant positions;
- endurance for repeated work;
- the ability to generate active stiffness when required;
- the ability to relax unnecessary stiffness when it is not required.

These variables can be trained separately and may interact.

## 10. Default reasoning sequence

For any movement or pain question, ask internally:

1. What is the geometry?
2. What supports the body?
3. Which external loads and moments exist?
4. Is the position passive, active, or mixed?
5. How long is it held?
6. What happened in the preceding minutes and hours?
7. What quantity is actually changing: range, force, stiffness, pain, or tolerance?
8. What did the cited experiment actually measure?
9. How far is the user's situation from that experiment?
10. Which parts of the explanation are observations and which are hypotheses?
