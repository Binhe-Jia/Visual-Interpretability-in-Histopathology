# PatchOmicsSurvival

**Patch-Level Cancer Detection + Multi-Omics Survival Modeling**

This project integrates patch-level histopathology classification (PCam dataset) with survival prediction based on TCGA-COAD transcriptomic data. It includes Grad-CAM visualization, DeepSurv training, and (if time permitted) a full Streamlit interface.

---

## Project Structure

```
PatchOmicsSurvival/
├── notebooks/
│   └── patch_omics_survival_pipeline.ipynb  # Full pipeline notebook
├── scripts/
│   ├── patch_feature_extractor.py          # Extract ResNet patch embeddings
│   ├── omics_image_fusion.py               # Combine omics + image features
│   ├── train_deepsurv.py                   # Train DeepSurv model
│   └── download_data.py                    # Auto-download PCam and TCGA data (optional if data exists locally)
├── models/
│   ├── deepsurv.py                         # PyTorch DeepSurv model
│   └── aggregation_heads.py                # Optional attention/contrastive modules
├── data/
│   ├── pcam/                               # PCam images + patch features
│   └── tcga/                               # RNA-seq + clinical survival
├── requirements.txt                        # Python dependencies
└── environment.yml                         # Conda environment
```

---
Note: the project structure is subjected to future modification

## Citation & Credits

- PCam: https://github.com/basveeling/pcam
- TCGA COAD: https://xenabrowser.net/
- Grad-CAM: Selvaraju et al., 2017
- DeepSurv: Katzman et al., 2018

---

## Future Work

- Add ViT or CLAM-based WSI patch aggregation
- GNN for patient-level interaction modeling
- Survival calibration and SHAP interpretability
