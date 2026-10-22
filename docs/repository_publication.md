# Updating the repository and manuscript link

1. Extract this distribution and copy the contents of `NSDDNew/` into the local
   checkout of `https://github.com/bilkentli88/NSDDNew`, preserving its `.git/`
   directory. The archive is prepared for upload; it is not itself evidence
   that the public repository has been updated.
2. Run `python scripts/asoc.py verify` from that checkout. Review the additions
   under `studies/`, commit them, and push the update. Generated runs, temporary
   environments and dependency checkouts are excluded by `.gitignore`.
3. Record the actual new commit SHA. A GitHub release/tag can also identify
   the submission snapshot. Check that the public snapshot includes
   `studies/E1/` through `studies/E5/` and opens without account access.
4. Replace the availability statement in both manuscript projects with the
   text below, inserting the actual commit SHA. The old `ee1014...` commit
   identifies the earlier S0 materials and cannot identify the new additions.
   Remove statements that the experiment packages are supplied separately.

## Availability statement, after the update is public

> The code and synthetic data supporting the experiments, including the earlier
> scalar and oscillator studies and extensions E1--E5, are available in the
> NSDDNew repository (https://github.com/bilkentli88/NSDDNew), at commit
> **[insert the actual new commit SHA]**. The repository includes experiment
> protocols, environment specifications, random seeds, synthetic observations,
> trained checkpoints, per-fit results and reproduction instructions. All data
> are synthetic.

The statement above is conditional on publication of the updated repository.
The mathematical and experimental supplement remains part of the article;
separate experiment-package uploads are unnecessary once the repository
contains these materials. The original scientific protocols retain their
historical standalone-package descriptions for provenance; use the
repository-level reproduction guide for the consolidated layout.
