# ArASL Data Preparation Pipeline

This repository contains the **data preparation steps** for the Arabic Sign Language (ArASL) dataset.  
The workflow is organized into multiple Jupyter Notebooks, each handling a specific step in the pipeline:

##  Notebooks
- **01_explore_data.ipynb** → Exploratory Data Analysis (EDA): check class distribution, image sizes, duplicates, corrupted files.
- **02_clean_data.ipynb** → Cleaning: remove duplicates/corrupted files, resize, convert to grayscale, save cleaned dataset.
- **03_split_and_augment.ipynb** → Dataset splitting into train/validation/test (80/10/10).
- **04_balance_train.ipynb** → Balance training set with data augmentation (target count per class).
- **05_Data_pipeline.ipynb** → PyTorch pipeline: dataset class + dataloaders (train/val/test).
- **Duple_check.ipynb** → Final verification: no duplicates, no leaks, all images 64×64 grayscale, balanced splits.

## Dataset
- **Source**: ArASL Database (54K images).  
- **Outputs**:  
  - `ArASL_Cleaned/` → cleaned dataset.  
  - `ArASL_Split/` → stratified split (train/val/test).  
  - `EDA_outputs/` → reports and visualizations.  
  - `clean_logs/` → cleaning logs and summaries.  

## Usage
1. Run the notebooks in order (01 → 05).  
2. After step 05, the data is ready for **model training**.  
