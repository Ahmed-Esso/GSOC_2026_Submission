# GSOC 2026 Submission

This repository contains the code, models, and documentation for the GSOC 2026 submission. It includes two main test pipelines for lens classification and lens finding, along with all required model weights and evaluation artifacts.

## Project Overview

This project demonstrates deep learning pipelines for astronomical lens detection and classification. It is structured for easy review and reproducibility, with all artifacts and outputs included. The repository is intended for evaluation as part of the GSOC 2026 process.

## Repository Structure

| Path                                 | Description                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| README.md                            | Project overview, setup, and artifact documentation (this file)                             |
| .gitignore                           | Excludes local cache, checkpoints, and environment clutter                                  |
| Common_Test_1/                       | Lens classification pipeline, model weights, and evaluation outputs                         |
| ├── DeepLense_Classification.ipynb   | Jupyter notebook for lens classification                                                    |
| ├── model_weights_test_1.pth         | Trained model weights for classification pipeline                                           |
| └── README.md                        | Documentation for Common_Test_1 artifacts                                                   |
| Specific_Test_5/                     | Lens finding pipeline, model weights, and evaluation outputs                                |
| ├── lens_finding_pipeline.ipynb      | Jupyter notebook for lens finding                                                           |
| ├── model_weights_test_5.pth         | Trained model weights for finding pipeline                                                  |
| └── README.md                        | Documentation for Specific_Test_5 artifacts                                                 |

## Setup & Usage

### Requirements
- Python 3.8+
- Jupyter or Colab
- PyTorch, NumPy, Matplotlib, scikit-learn (see notebooks for details)

### Running in Colab
1. Upload the repository to your Colab environment.
2. Open either notebook and run all cells. Model weights are included and will be loaded automatically.

### Running Locally
1. Clone the repository:
	```sh
	git clone https://github.com/<your-username>/GSOC_2026_Submission.git
	cd GSOC_2026_Submission
	```
2. Install dependencies (see notebook headers for details).
3. Launch Jupyter:
	```sh
	jupyter notebook
	```
4. Open and run the desired notebook.

## Datasets
- Notebooks expect test datasets in standard formats (see notebook headers for details).
- Datasets are not included due to size/licensing. Please follow notebook instructions to obtain or simulate test data.

## Outputs & Artifacts
- Each pipeline produces a confusion matrix, ROC curve, and training curves (see folder READMEs).
- Model weights (`.pth` files) are included for reproducibility.

## Notes
- All files and outputs are documented in their respective folder README files.
- For questions, see notebook headers or contact the author.
