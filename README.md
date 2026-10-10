# DR Domain Shift Preliminary Experiments

Preliminary experimental evidence supporting ANRF Advanced Research Grant 2026
proposal — Reference No. 542026000395

**Title:** Domain-Adaptive Explainable Deep Learning for Diabetic Retinopathy
Screening in Resource-Constrained Primary Healthcare Settings of Bihar

**PI:** Dr. Chandrakala Kuruba, Associate Professor, Department of Computer Science,
Central University of South Bihar (CUSB), Gaya

---

## What is in this repository

**results/**
- `summary_all_families.csv` — Aggregated test results across 5 model families,
  3 random seeds, 3 datasets (APTOS 2019, IDRiD, DDR)
- `bootstrap_vs_classical.csv` — Bootstrap confidence intervals comparing VQC,
  no-VQC, and classical-only model families against the classical baseline

**splits/**
- `ddr_audit.csv` — DDR dataset audit: 95 exact-duplicate groups identified
  (98 redundant copies removed); no byte-identical overlap with APTOS confirmed
- `ddr_clean_split.csv` — Stratified train/val/test split for DDR
  (train 8,696 / val 1,864 / test 1,864; 12,424 images retained)

---

## Key findings

- APTOS in-domain: QWK 0.878, referable-DR AUC 0.973
- Zero-shot transfer to IDRiD: QWK 0.647–0.667, referable-DR AUC 0.916–0.924
- Zero-shot transfer to DDR: QWK 0.487–0.533, referable-DR AUC 0.786–0.853,
  referable sensitivity 39–47% at 98–99% specificity
- No measurable benefit from VQC or Transformer components
  (bootstrap CIs include zero on APTOS and IDRiD)
- 7.3M parameter CNN matches 10.75M hybrid across all datasets within
  bootstrap confidence intervals

## Dataset deduplication

- APTOS 2019: 123 exact-duplicate groups and 62 conflicting-label pairs removed
  (4.3% of original dataset; 3,504 images retained).
  Split identifiers will be released with the manuscript.
- DDR: 95 exact-duplicate groups removed (see splits/ddr_audit.csv)

---

## What is NOT here

Full training code will be released upon manuscript acceptance.
Raw images are not included.
- APTOS 2019: kaggle.com/competitions/aptos2019-blindness-detection
- DDR: github.com/nkicsl/DDR-dataset
- IDRiD: ieee-dataport.org/open-access/indian-diabetic-retinopathy-image-dataset-idrid

---

## Status

Experiments complete. Manuscript under preparation.
Results tables and training code will be added upon manuscript submission.

---

## Citation

Please cite this repository if you use the DDR split identifiers.
Full citation will be updated upon manuscript publication.
