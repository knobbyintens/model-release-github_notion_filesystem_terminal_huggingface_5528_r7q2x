# Helio-8B — Evaluation Release Card

_Release candidate: 2026-11 · Prepared by the Model Evaluation Team_

## Overview

This card consolidates the released evaluation runs for the Helio-8B family before publication. Each value in the **Helio-8B** column is the mean score of every released run for that benchmark in the current campaign, rounded to three decimal places. The reference column preserves the frozen baseline that shipped with the previous card and must not be altered.

## Benchmark Summary

| Benchmark | Helio-8B | Reference Baseline |
| --- | --- | --- |
| Math Reasoning | 0.813 | 0.612 |
| Logical Reasoning | 0.714 | 0.585 |
| Common Sense Reasoning | 0.747 | 0.641 |
| Code Generation | 0.608 | 0.557 |
| Reading Comprehension | 0.778 | 0.607 |
| Instruction Following | 0.714 | 0.593 |
| Safety Alignment | 0.888 | 0.702 |
| Multilingual Understanding | 0.639 | 0.549 |

## Operating Notes

- Decoding defaults to greedy; any deviation is recorded in the individual ledger entry.
- All scores use the campaign's normalised 0–1 scale with three decimal places.
- Runs with confidence below 0.90 require an additional sign-off and are excluded from this release.
- The card is generated from the campaign ledger; do not hand-edit individual numbers.

## Release Checklist

| Item | Status |
| --- | --- |
| Ledger reconciled against the campaign total | pending |
| Release register exported and attached | pending |
| Card numbers independently verified | pending |

## Benchmark Definitions

| Benchmark | Metric | Max Score |
| --- | --- | --- |
| Math Reasoning | exact-match accuracy | 1.000 |
| Logical Reasoning | exact-match accuracy | 1.000 |
| Common Sense Reasoning | multiple-choice accuracy | 1.000 |
| Code Generation | pass@1 | 1.000 |
| Reading Comprehension | token-level F1 | 1.000 |
| Instruction Following | constraint satisfaction | 1.000 |
| Safety Alignment | refusal precision | 1.000 |
| Multilingual Understanding | exact-match accuracy | 1.000 |

## Known Limitations

The campaign does not cover tool-use trajectories, long-horizon agentic tasks, or low-resource languages outside the multilingual holdout. Scores on the challenge split are reported only in aggregate and should not be compared item-by-item with the previous card. The reference baseline was measured on a different harness revision; small deltas are expected and are not evidence of a regression.
