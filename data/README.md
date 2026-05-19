# Data Directory

This directory contains project datasets and related files.

## Contents
- Small/sample datasets (committed to repository)
- Data loading and preprocessing scripts
- Data documentation and metadata
- Data validation scripts

## Large Dataset Management
- Large datasets should be stored on the **HPC system**
- Use symbolic links or configuration files to reference HPC-stored data locally
- Document dataset locations and access instructions

## Organization Tips
- Use subdirectories for different data sources or experiment phases
- Include data dictionaries or schema documentation
- Keep raw data separate from processed data

## HPC Integration
- Store raw data on HPC: `/hpc/data/`
- Reference paths via environment variables or config files:
  ```python
  import os
  DATA_PATH = os.getenv('HPC_DATA_PATH', './data/sample/')
  ```
- Document synchronization procedures for team members

## Excluded Files
- Large binary files (`.csv` > 10MB, `.hdf5`, `.parquet` > 10MB)
- These should be managed on HPC system
