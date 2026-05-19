# Q6_summer

This is the summer clean version of the ABH project.

## Project Overview

This repository is designed to support collaborative development across multiple systems:
- **Local laptops** - for development and analysis
- **HPC system** - for large-scale computations and data storage

## Directory Structure

```
Q6_summer/
├── analysis/          # Jupyter notebooks for data analysis and exploration
├── data/              # Project datasets (large files managed by HPC)
├── figures/           # Generated figures and visualizations (*.pdf excluded)
├── models/            # Trained models and serializations (*.pkl, *.pickle excluded)
├── documents/         # Project documentation, reports, and papers
└── venv/              # Virtual environment (excluded from git)
```

### Directory Descriptions

#### `analysis/`
Contains Jupyter notebooks (`.ipynb`) for:
- Exploratory data analysis (EDA)
- Data visualization
- Results analysis and interpretation
- Computational experiments

#### `data/`
Stores project datasets:
- Small/sample datasets can be committed to the repository
- Large datasets should be managed on the HPC system
- Use symbolic links or configuration files to reference HPC-stored data

#### `figures/`
Contains generated visualizations:
- PNG, SVG, and other image formats are tracked
- **PDF files (`.pdf`) are automatically excluded** to reduce repository size
- Regenerate PDFs from notebooks as needed

#### `models/`
Stores model artifacts and weights:
- **Pickle files (`.pkl`, `.pickle`) are automatically excluded** to keep the repository lean
- Source code for model definitions should be included
- Store trained models on the HPC system or use `.gitkeep` to document available models

#### `documents/`
Contains project documentation:
- README files and setup guides
- Research papers and references
- Project reports and findings
- Configuration documentation

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/MarjaanNik/Q6_summer.git
cd Q6_summer
```

### 2. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

## Working Between Systems

### Local Development
- Work with sample data from the `data/` folder
- Develop and test code on notebooks in `analysis/`
- Commit code changes to git

### HPC System
- Store large datasets on the HPC system
- Train models with full datasets
- Store trained models (`.pkl` files) on HPC
- Reference models from local notebooks via configured paths

## .gitignore Configuration

The `.gitignore` file is configured to:
- ✅ Exclude virtual environments (`venv/`, `.venv`, etc.)
- ✅ Exclude pickle files from `models/` folder
- ✅ Exclude PDF figures from `figures/` folder
- ✅ Include Python bytecode exclusions
- ✅ Preserve folder structure with `.gitkeep` files

This ensures the repository stays clean while preserving the project structure across all systems.

## Notes

- Virtual environments are excluded and should be set up locally on each system
- Large binary files (models, PDFs) are excluded; regenerate them locally as needed
- Use configuration files or environment variables to specify paths to HPC-stored data
- Coordinate with team members when synchronizing large datasets

