# Figures Directory

This directory stores generated figures, visualizations, and plots.

## Contents
- PNG, SVG, and image files (tracked in git)
- Plotting scripts and visualization code
- Figure documentation and captions
- Presentation-ready graphics

## Excluded Files
- **PDF files (`.pdf`) are automatically excluded** to keep repository lean
- Regenerate PDFs from source notebooks as needed
- Use vector formats (SVG) for publication-quality figures

## Best Practices
- Use descriptive naming: `figure_01_method_comparison.png`
- Include figure version numbers with source notebook
- Document how each figure was generated (script/notebook reference)
- Keep high-resolution versions on HPC if needed

## Regenerating PDFs
- PDFs should be generated from:
  - Jupyter notebooks in `analysis/`
  - Python scripts with plotting code
  - LaTeX documents in `documents/`
- Document regeneration procedure in figure scripts
- Use consistent styling across figures

## Organization
- Use subdirectories by analysis type:
  - `figures/exploratory/` - EDA figures
  - `figures/results/` - Final results
  - `figures/supplementary/` - Additional supporting figures
