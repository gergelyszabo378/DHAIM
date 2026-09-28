# DHAIM

**Research on changing user goals in human-AI dialogue and traceable evaluation**

DHAIM is an early-stage, independent research project led by Gergely Szabó. It studies a practical question in multi-turn dialogue: when a user changes or corrects a request, can an AI system update what changed while preserving the requirements that still apply?

A response can satisfy the latest instruction and still lose an earlier valid constraint. It can preserve important words or numbers while changing their meaning, status, or role. These possibilities motivate more precise evaluation; they are not, by themselves, claims about how frequently such failures occur.

## Two connected lines of work

**Changing user/task state.** DHAIM examines whether a system distinguishes a genuine update from a restatement, applies the current target in its next response, preserves still-valid requirements, and propagates changes through relevant dependencies without changing unrelated parts of the task. Verbal acknowledgement of a correction and operational use of that correction are treated as potentially different outcomes.

**Traceable research integration.** The project is also developing a way to keep claims connected to their sources, evidence strength, scope, dependencies, conflicts, and revision history. The point is to make a changing research record inspectable, not to turn every preliminary idea into an established claim. Whether this added structure improves diagnosis or research work compared with a strong, simpler checklist remains an open question.

The earlier shorthand *dynamic / integrative / modular* describes aspects of this program, not three proven properties of language models. In particular, modularity is a design aim for the research architecture: components should be separately testable and revisable. DHAIM does not claim that an LLM's internal cognition is modular.

## Questions under investigation

- After a user changes a goal, what exactly should be updated, and what should remain valid?
- Can a system meet the new target while silently dropping a prior requirement?
- When one requirement depends on another, is the change propagated correctly?
- Can the requested operation or the status of a statement drift even when the topic and key words remain the same?
- Do more explicit representations of these relationships improve evaluation or repair over a well-designed simpler baseline?

For illustration only: if a user asks for a shorter reply but still needs a conditional request to remain conditional, a shorter output is not fully successful when it turns that request into an unconditional instruction. This example explains a measurement distinction; it is not a released experimental observation.

## Approach and possible contribution

The project separates observations, proposed mechanisms, measurement rules, evidence, and decisions. Its empirical workflow moves from observed or natural dialogue difficulties to controlled cases, explicit scoring rules, adversarial review, model runs, and bounded interpretation. Synthetic cases can isolate a distinction, but their design may also remove the very difficulty they are meant to test. Natural human-AI failures are therefore important seeds for later evaluation work.

Many relevant phenomena already have prior research. DHAIM's possible contribution does not depend on calling them new discoveries. It may lie in sharper operational distinctions, a relation-aware research record, and a demonstrated benefit over strong simpler alternatives. A result showing no such benefit would also be informative.

## Current status and limits

This is an **initial project introduction**, dated 2026-09-28. It is not a finished theory, a validated benchmark, a population estimate, or a model ranking. Several instruments and pilot tracks exist internally. A recent 36-response development screen has passed an internal *technical provenance* check, but that is not the same as instrument validity or a confirmed frozen scientific closeout. No empirical dataset, runner, verifier, or final comparative result is released in this introduction.

See [Project status](STATUS.md) for the current claim and release boundaries. Later public materials will be added only after source, status, privacy, and reproducibility checks. The repository will retain dated revisions so that a later interpretation does not silently overwrite an earlier one.

## Feedback

Critical feedback is welcome on construct validity, alternative explanations, prior work, human coding, dependency-sensitive evaluation, and comparisons against strong simple baselines. In particular, we would value cases where a model's response appears responsive to the latest request but may have lost another part of the active task.

## Research responsibility

Gergely Szabó leads the project and reviews publication decisions. AI tools assist with drafting, analysis, organization, and critique; agreement among them is not treated as independent scientific evidence.

No reuse license has been selected for this introductory material yet. Please contact the project owner before reusing its contents beyond what applicable law permits.
