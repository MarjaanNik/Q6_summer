# Models Directory

This directory stores trained models and model artifacts.

## Contents
- Model source code and definitions
- Model configuration files
- Training scripts and logs
- Documentation for model reproducibility

## Excluded Files
- **Pickle files (`.pkl`, `.pickle`) are automatically excluded** to keep repository lean
- **Model weights and serialized objects should be stored on the HPC system**
- Use this directory for model source code and metadata only

## HPC Storage Strategy
- Store trained model files (`.pkl`, `.h5`, `.pt`, etc.) on the HPC system
- Create a `models/manifest.md` to document:
  - Model names and descriptions
  - Training parameters and dates
  - Location on HPC system
  - Performance metrics
  - Associated notebooks or scripts

## Example Manifest Entry
```
### Model: my_trained_model_v1.pkl
- Training Date: 2026-05-19
- Training Data: dataset_v2
- Performance: 95.3% accuracy
- Location: /hpc/models/my_trained_model_v1.pkl
- Associated Script: analysis/train_model.ipynb
```

## Best Practices
- Version control model definitions and hyperparameters
- Document all training procedures in reproducible scripts/notebooks
- Sync trained models with HPC system after training
- Maintain clear naming conventions for model files
