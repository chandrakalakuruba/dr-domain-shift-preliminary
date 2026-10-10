# DR Domain Shift Preliminary Experiments

Preliminary experimental evidence supporting ANRF Advanced Research Grant 2026 
proposal — Reference No. 542026000395

**Title:** Domain-Adaptive Explainable Deep Learning for Diabetic Retinopathy 
Screening in Resource-Constrained Primary Healthcare Settings of Bihar

**PI:** Dr. Chandrakala Kuruba, CUSB Gaya

---

## What is in this repository

- `results/summary_all_families.csv` — Aggregated test results across 5 model 
  families, 3 random seeds, 3 datasets (APTOS, IDRiD, DDR)
- `results/bootstrap_vs_classical.csv` — Bootstrap confidence intervals comparing 
  VQC, no-VQC, and classical-only model families
- `splits/aptos_duplicates.csv` — 123 exact-duplicate groups identified and removed 
  from APTOS 2019 (4.3% of dataset)
- `splits/ddr_duplicates.csv` — 95 duplicate groups removed from DDR dataset

---

## Key findings

- APTOS in-domain: QWK 0.878, referable-DR AUC 0.973
- Zero-shot transfer to IDRiD: QWK 0.647–0.667
- Zero-shot transfer to DDR: QWK 0.487–0.533, referable sensitivity 39–47% 
  at 98–99% specificity
- No measurable benefit from VQC or Transformer components 
  (bootstrap CIs include zero on APTOS and IDRiD)
- 7.3M parameter CNN matches 10.75M hybrid across all datasets

---

## What is NOT here

Full training code will be released upon manuscript acceptance.
Dataset split identifiers are provided for reproducibility.
Raw images are not included — APTOS is available at kaggle.com/competitions/aptos2019-blindness-detection,
DDR at github.com/nkicsl/DDR-dataset.

---

## Citation

If you use the deduplicated split identifiers, please cite this repository.
Manuscript under preparation — citation will be updated upon publication.
