<!-- ELUCENIA technical documentation · das28 · en · no clinical/professional/rights approval -->

# DAS28 (ESR and CRP)

[conditions, sources and permissions](https://elucenia.org/en/tools/das28)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Tender joints (out of 28)

`tjc`

range: 0–28

### Swollen joints (out of 28)

`sjc`

range: 0–28

### Patient global health assessment (visual scale)

`gh`

mm · range: 0–100

### Erythrocyte sedimentation rate (ESR)

`vhs`

mm/h · optional · range: 1–150

### C-reactive protein (CRP)

`pcr`

mg/L · optional · range: 0–300

## Method edition

DAS28-ESR/Prevoo 1995 and DAS28-CRP/Wells 2009; 28 joints; CRP intercept 0.96

## Documented formula

DAS28-ESR = 0.56 × √(tender) + 0.28 × √(swollen) + 0.70 × ln(ESR) + 0.014 × global assessment.

DAS28-CRP = 0.56 × √(tender) + 0.28 × √(swollen) + 0.36 × ln(CRP + 1) + 0.014 × global assessment + 0.96 (CRP in mg/L).

## Limits and population

The 1995 DAS28 was developed for rheumatoid arthritis activity, using a 28-joint count and comparisons with rheumatologists’ clinical assessments. The CRP variant is not automatically equivalent to the ESR variant; the formula, units and cutoffs must match the source and edition used.

## References

- [Prevoo MLL et al. Modified disease activity scores that include twenty-eight-joint counts: development and validation in a prospective longitudinal study of patients with rheumatoid arthritis. Arthritis Rheum, 1995.](https://doi.org/10.1002/art.1780380107)

- [Wells G et al. Validation of the 28-joint Disease Activity Score (DAS28) and European League Against Rheumatism response criteria based on C-reactive protein against disease progression in patients with rheumatoid arthritis, and comparison with the DAS28 based on erythrocyte sedimentation rate. Ann Rheum Dis, 2009.](https://doi.org/10.1136/ard.2007.084459)

- [England BR et al. 2019 Update of the American College of Rheumatology Recommended Rheumatoid Arthritis Disease Activity Measures. Arthritis Care Res, 2019.](https://doi.org/10.1002/acr.24042)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Documented results

The information below preserves the method outputs for synthetic examples. It does not constitute independent clinical validation.

### 1

Moderate rheumatoid arthritis activity


### 2

Rheumatoid arthritis remission


### 3

High rheumatoid arthritis activity


### 4

Moderate rheumatoid arthritis activity

The DAS28-CRP usually gives lower values than DAS28-ESR: with the same cutoffs, remission may be overestimated.

