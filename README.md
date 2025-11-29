#Project Overview
This repository demonstrates a reproducible Data Science workflow using Git, Git LFS, DVC, and
Jupyter/nbconvert. It ensures that datasets, models, and results can be versioned, tracked, and
reproduced end-to-end with a single command.
Technologies Used
- Git for version control
- Git LFS for managing large files
- DVC (Data Version Control) for datasets, models, and pipelines
- Jupyter/nbconvert for reproducible notebook execution
Setup Instructions
1. Clone the repository:
git clone https://github.com/kabitaadhikari/Git_Project.git
2. Navigate to the project folder:
cd Assignment_DataScience_1
3. Install required Python packages:
pip install -r requirements.txt
4. Initialise DVC and pull datasets:
dvc pull
Pipeline Reproducibility
The pipeline is defined in `dvc.yaml`. It runs the notebook `Final_all.ipynb` and generates the
executed output notebook in `outputs/Final_all_executed.ipynb`.
To reproduce the pipeline:
dvc repro
To push artifacts:
dvc push
Project Structure
- `Final_all.ipynb` ® main notebook containing preprocessing, feature engineering, modelling, and
evaluation
- `zomato_df_final_data.csv` ® dataset (tracked by DVC)
- `sydney.geojson` ® geojson data (tracked by DVC)
- `dvc.yaml` ® pipeline definition
- `outputs/Final_all_executed.ipynb` ® pipeline output notebook
- `dvcstore/` ® DVC storage
- `.gitattributes` ® Git LFS tracking rules
Workflow Summary
1. Git tracks code and configuration.
2. Git LFS manages large datasets and models.
3. DVC ensures reproducibility with pipelines and data tracking.
4. `dvc repro` regenerates results in one command.
