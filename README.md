# Attention‑Inception U‑Net for 3‑D Brain‑Tumor Segmentation (BraTS 2025)

A deep‑learning pipeline for automated glioma segmentation on the **BraTS 2025** multimodal MRI challenge set. We benchmark three popular 3‑D U‑Net variants and introduce a hybrid **Attention‑Inception (AI) U‑Net** that fuses multi‑scale Inception blocks with attention gates to refine tumor boundaries.

---

## ✨ Key Features
| Stage | What we do |
|-------|------------|
| **Pre‑processing** | Z‑score intensity normalisation, skull‑stripping, co‑registration, and full‑volume (no patch) loading for T1, T1Gd, T2 & FLAIR |
| **Models** | 3‑D U‑Net, Inception U‑Net, Attention U‑Net, **proposed AI U‑Net** |
| **Loss** | Combined Cross‑Entropy + Dice loss to balance class imbalance |
| **Training** | End‑to‑end 3‑D training/inference on single‑GPU CUDA; centre‑cropping keeps skip connections shape‑safe |
| **Metrics** | Mean IoU, voxel accuracy, and Dice coefficient |
| **Results** | AI U‑Net reaches **Dice ≈ 0.85** on an internal validation split and **Dice ≈ 0.70** on the hidden BraTS 2025 test set |
