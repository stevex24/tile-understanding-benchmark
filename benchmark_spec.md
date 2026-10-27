# Benchmark specification v0.2 — proposal, not results

## Unit of evaluation
A tileset atlas with stable tile IDs, optional example level(s), a question/task, and an explicit answer format. Start with one small tileset and a handful of tasks.

## Conditions
- A (zero-example): tileset atlas + tile IDs + task only.
- B (with examples): same inputs and task + example level(s).

Keep all other information, scoring and model settings as comparable as practical. The examples may legitimately reveal relationships absent from the atlas; the benchmark should measure that difference, not hide it.

## Task families
1. Tile roles: identify plausible use of selected tiles.
2. Pair/group relationships: adjacency, roof-wall-door assemblies, connected borders.
3. Construction: produce a small tile-ID grid satisfying stated requirements.
4. Repair: find and correct a deliberately broken arrangement.

## Scoring sketch
- Exact validity: tile IDs in set, correct dimensions, parsable grid.
- Rule validity: proportion of explicit constraints satisfied.
- Relationship predictions: precision, recall, F1 where labeled ground truth exists.
- Coherence: small written human rubric, blind to model/condition if possible.

## Experimental hygiene
- Freeze versioned test cases for periodic reruns; develop prompts on separate examples.
- Save original inputs, prompts, raw outputs, model/version/date, and evaluation scripts.
- Avoid asserting exhaustive relationship ground truth from incomplete examples.
- No benchmark performance claims until tests have been executed.

## Deferred work
Automatic object/shape/texture segmentation, interactive highlighting, integration with SAT, full literature reviews, and broad multi-tileset coverage.
