# Manuscript-to-repository map

Numbering follows the main article and supplement V10. The main article contains
mathematical Appendices A--D; the supplement contains experimental Appendices E--G.

| Manuscript item | Study | Source | Retained records |
|---|---|---|---|
| Main Figure 1 | Conceptual framework | Supplied vector illustration | `figures/asoc/reference/conceptual_framework.pdf` |
| Main Table 2, E1 row; Supplement E.2 / Table E.2 | E1 | `studies/E1/reproduction_package/` | `studies/E1/experiment1_results/` |
| Main Table 2, E2 rows; Supplement E.3 / Table E.3 | E2 | `studies/E2/reproduction_package/` | `studies/E2/experiment2_results/` |
| Main Table 2, E3 row; Supplement E.4 / Tables E.4--E.5 | E3 | `studies/E3/reproduction_package/` | `studies/E3/experiment3_results/` |
| Main Table 3 / Figure 2; Supplement E.5 / Table E.6 | E5 | `studies/E5/source/two_stage.py`, `studies/E5/analyze.py` | `studies/E5/results/` |
| Main Table 4 / Figure 3; Supplement F / Table F.1 | E4 | `studies/E4/source/` | `studies/E4/results/` |
| Supplement G.1 / main Section 6.2 empirical profile counts | S0 | `experiments/strengthening/certificate.py`, `numpy_data.py` | `results/confirmation/reference/` and `results/strengthening/reference/` |
| Supplement G.2 / Table G.1, fixed-noise ablation | S0 | `experiments/strengthening/run_tnnls_strengthening.py --full` | `results/strengthening/reference/`, 39 checkpoints |
| Supplement G.2 / Figure G.1, fresh-noise comparison | S0 | `experiments/strengthening/run_step5_confirmation.py --full` | `results/confirmation/reference/`, 60 checkpoints |
| Supplement G.3, noise/domain/solver checks | S0 | `experiments/run_extended_experiments.py --mode paper` | `results/extended/reference/` |
| Supplement G.4 / main Section 6.5, oscillator | S0 | Same extended driver | `results/extended/reference/oscillator_summary.csv`, oscillator checkpoints |

`scripts/asoc.py verify` checks the supplied hashes and E1--E5 numerical-record
summaries without training. The [reproduction guide](asoc_reproduction.md)
provides the checkpoint replay and full-training commands.

E1--E3 direct functions and anchor-only models do not have full-model forecast
scores. E5 adds full frozen-delay predictors on the informative E1--E3 data,
with additional stage-one computation. E4 is a constant-delay subcase using
adapted external/structured pipelines. Five base-noise datasets are the
independent units in each extension; optimizer repeats are nested.

The original mapping and root README are retained under `docs/legacy/`.
Historical source filenames and source/protocol hashes remain unchanged.
