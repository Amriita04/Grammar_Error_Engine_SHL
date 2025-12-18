# Grammar Scoring Engine

## Overview
This project builds a machine learning pipeline to predict grammar scores from audio files.  
It was developed as part of the SHL AI/ML assessment.

- **Training data:** `train.csv` (contains audio filenames + labels)
- **Test data:** `test.csv` (contains audio filenames only)
- **Output:** `submission.csv` (predicted grammar scores in required format)

## Project Workflow
1. Load `train.csv` and preprocess data.
2. Extract simple placeholder features (filename length) since audio libraries like `librosa` were not available in the environment.
3. Train a `RandomForestRegressor` model.
4. Evaluate using MAE and R² metrics.
5. Load `test.csv`, generate predictions, and save them in `submission.csv`.
6. Format predictions to match `sample_submission.csv`.

## Files in Repository
- `notebook.ipynb` → End-to-end training + prediction pipeline.
- `dataset/train.csv` → Training metadata.
- `dataset/test.csv` → Test metadata.
- `dataset/sample_submission.csv` → Template for submission.
- `submission.csv` → Final predictions file.

## How to Run
1. Clone this repository:
   ```bash
   git clone <https://github.com/Amriita04/Grammar_Error_Engine_SHL>
   cd grammar-scoring-engine
2. Install dependencies:
   ~ pip install -r requirements.txt
3. Run the notebook:
   ~ Grammar_Scoring_Engine.ipynb
4. The output submission.csv will be generated in the repo folder.


