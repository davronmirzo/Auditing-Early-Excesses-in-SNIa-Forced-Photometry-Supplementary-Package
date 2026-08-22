V48M8 CAUSAL-RECONCILIATION AND MATCHED-ENDPOINT REPRODUCIBILITY BUNDLE

The associated manuscript cites Zenodo DOI 10.5281/zenodo.21438536. Before
publishing a new archive version, confirm whether Zenodo retains this record DOI
or supplies a new version DOI and synchronize the manuscript and CITATION.cff.

Authoritative sequence
1. Freeze eligibility and methods (V48A).
2. Run band-wise baseline/scatter fits (V48B).
3. Audit denominator and raw crossings (V48C).
4. Evaluate phase/window sensitivities (V48D).
5. Perform point and baseline-influence forensics (V48E).
6. Run targeted raw-quality and conditional sign-reversal diagnostics (V48F).
7. Freeze, validate, and run injection recovery (V48G1/G2A/G2B).
8. Compute mode-resolved population limits (V48G2C).
9. Perform external candidate crossmatch (V48I1/I2).
10. Apply revision claim closures (V48L1-L8).
11. Freeze the all-host end-to-end contract before examining injection outcomes
    (config/v48m6_end_to_end_contract.json and its freeze record).
12. Run and adjudicate the 287-host, five-proxy, 30-realization extension
    (scripts/69_run_v48m6_end_to_end_production.py and
    scripts/69b_adjudicate_v48m6_single_refit_failure.py).
13. Compute object-specific raw and structural-confirmation efficiencies,
    fixed-sample limits, prior sensitivity, and the 20,000-resample host-cluster
    bootstrap (scripts/70_close_v48m6_population_inference.py).
14. Freeze the matched retained-point endpoint and short-circuit criterion
    order before evaluating the structural grid
    (config/v48m7_matched_endpoint_contract.json and its freeze record).
15. Reconstruct the exact 455-trial raw-positive union, verify raw-flag parity,
    and apply the matched observed/injected classifier
    (scripts/71_run_v48m7_matched_structural_grid.py).
16. Close all 65 raw and 65 matched structural axis-indexed population cells,
    criterion attrition, object-specific efficiencies, prior sensitivity, and
    the 20,000-resample structural host-cluster bootstrap with seed 4807
    (scripts/72_close_v48m7_full_structural_population_grid.py).
17. Audit baseline-validity documentation against the executed code, expose
    the alpha-boundary veto, and run the paired 277-host fixed-alpha matched
    endpoint sensitivity (scripts/73_run_v48m7p2_fixed_alpha_matched.py).
18. Run the boundary-admitted denominator/crossing sensitivity
    (scripts/74_run_v48m7p3_alpha_boundary_denominator_sensitivity.py).
19. Reconstruct the submitted Stage-5/Stage-8 outputs, pair all 736 old/current
    band fits and all 368 eligible objects, and restore the exact blockwise
    sign randomization on the canonical residuals
    (scripts/75_run_v48m8_causal_signflip_reconciliation.py).

The historical denominator 219 and V44 transport are noncanonical context only.
The authoritative primary denominator is 277; the production union contains 287
fit-valid hosts with median reduced chi-square <=10. The extension contains
43,050 full-refit trials, including all five observed crossing hosts. Its primary
cell contains 8,310 trials per proxy. One four-point c-band refit did not converge
and is retained conservatively as a non-recovery; the recorded exclusion
sensitivity changes no displayed result.

The current occurrence calculation uses each host's own k/30 efficiency. It does
not transport a pooled 272-host efficiency and does not insert an unmeasured
retention factor. The matched frozen order is raw crossing, single-largest-point
deletion, two-band support, and retained-point leave-one-night-out refitting.
Single-point stability and two-band support are both evaluated for every raw
crossing; LONO alone is short-circuited unless both pass. In the 41,550
primary trials, 444 pass the raw screen and eight survive single-point deletion,
but none passes two-band support; retained-point LONO is not reached. All 65
matched structural cells therefore have zero measured efficiency. The plug-in
frequentist confidence sets retain the full physical interval; f95=1 denotes
their upper boundary and is not a restrictive occurrence limit. The Bayesian
limits equal the prior quantiles. Raw-screen f95 values are zero-count sensitivity
equivalents only, not occurrence limits, because the observed raw count is two.
No physical-channel occurrence interpretation is authorized for the
phenomenological proxy results.

The paired fixed-alpha matched run uses the identical 41,550 primary injected
realizations as the free-alpha grid. Fixed alpha gives 761 raw crossings and
254 single-point survivors, versus 444 and eight for free alpha; neither mode
has two-band support or a confirmed recovery. Twenty fixed-alpha base refits
fail for ZTF19aavhvkd, one single-valid-band host, in the companion-shock proxy and are
retained as misses. Because that host cannot meet the two-band endpoint, this
does not change the zero confirmed-recovery result.

The primary conditional sign diagnostic enumerates all 2^Ki band-night block
sign assignments for every primary object. Four threshold-capable objects have
qpositive=0.5, ZTF18abnygkb has qpositive=0.25, and the other 272 objects have
qpositive=0. The resulting Poisson-binomial distribution has
E[Npositive]=2.25, P(Npositive=0)=0.046875, P(Npositive=2)=0.34375, and a
probability-ordered two-sided p=1.0. Complete-vector reversal is retained only
as a weaker-assumption sensitivity; it gives P(Npositive=2)=0.3125 and the
same two-sided p=1.0. Neither calculation is a generative false-trigger model.

The submitted-to-canonical change is not a documentation-only effect. The
submitted fit used a pre-event median offset, fixed pre-event scatter,
two-start L-BFGS-B optimization, a separate first-light-boundary veto, and a
0.02 alpha tolerance. The canonical fit uses no additive constant, iterative
residual scatter, five-start soft-L1 least squares, revised first-light bounds
without that separate veto, and a 0.01 alpha tolerance. Across the same 736
attempts, the invalid/valid transition counts are 297/274/131/34 for
invalid-invalid, valid-valid, invalid-valid, and valid-invalid. Fit-valid
objects change 245 to 303 (236 retained, 67 added, nine dropped); primary
objects change 219 to 277 (206 retained, 71 added, 13 dropped). ZTF18abebzog
enters through fit-validity, while the already-primary ZTF19acoxgqw changes
from maximum positive residual 3.806 to 6.76. These routes account for the
observed positive count changing from zero to two. The later correction of one
canonical alpha-boundary sentence changed no computed canonical product and is
not the cause of these old/current transitions.

The boundary-admitted diagnostic accepts all 717 optimizer-successful fits
that pass the remaining numerical checks. It yields 367 fit-valid and 326
chi-square<=5 objects: 267 canonical primary objects are retained, 59 added,
and 10 dropped. The positive crossing roster remains two; sign-reversed
crossings increase from three to six. Boundary-pegged solutions do not identify
an interior rise index, so this branch is a denominator/crossing sensitivity,
not a replacement occurrence estimand.

Use V48M8_SHA256_MANIFEST.txt to verify the final bundled files. Older
manifests are retained solely as records of predecessor bundles.
