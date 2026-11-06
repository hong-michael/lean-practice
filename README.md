# lean-practice

General-purpose practice with mathematical formalization in Lean 4 and Mathlib.

## Subtopics

| Folder | Topic |
| --- | --- |
| [`LeanPractice/Analysis`](LeanPractice/Analysis) | Real and general analysis |
| [`LeanPractice/Algorithms`](LeanPractice/Algorithms) | Algorithms, such as the traveling salesman problem |
| [`LeanPractice/Complexity`](LeanPractice/Complexity) | Computational complexity theory |
| [`LeanPractice/NumberTheory`](LeanPractice/NumberTheory) | Analytic number theory |
| [`LeanPractice/PDE`](LeanPractice/PDE) | Partial differential equations |

## Setup

1. Install Lean with [elan](https://lean-lang.org/install/).
2. Download prebuilt Mathlib files, then build:

   ```bash
   lake exe cache get
   lake build
   ```

The first run creates `lake-manifest.json`. Commit it so the dependency versions stay fixed.

## Adding a file

Add the file under the matching subtopic, then import it from [`LeanPractice.lean`](LeanPractice.lean). `lake build` only checks files that are imported there. For example, `LeanPractice/Analysis/Limits.lean` needs this line:

```lean
import LeanPractice.Analysis.Limits
```
