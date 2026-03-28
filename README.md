# DeepLense GSoC 2026 Evaluation Tests

This repository contains the required implementation for the DeepLense prospective student evaluation. It includes a multi-class classification model and a binary lens detection pipeline.

## Project 1. Multi-Class Classification (Common Test I)

### Strategy
The model classifies images into three categories: no substructure, subhalo substructure, and vortex substructure. I used a ResNet18 architecture tailored for the normalized input images. The strategy involves transfer learning with a custom head to map features to the three target classes.

### Implementation Details
* **Data Split:** 90% training and 10% validation.
* **Preprocessing:** Min-max normalization and random horizontal/vertical flips.
* **Optimization:** Adam optimizer with Cross-Entropy Loss.

### Metrics
* Multi-class ROC curves generated for each class.
* AUC scores calculated using a One-vs-Rest (OvR) approach.

---

## Project 2. Lens Finding & Data Pipelines (Specific Test V)

### Strategy
This task addresses the identification of strong lenses versus non-lensed galaxies using three-filter (3, 64, 64) observational data. The primary challenge is the significant class imbalance, as non-lenses outnumber lenses.

### Implementation Details
* **Data Pipeline:** A custom PyTorch Dataset class loads the multi-filter arrays.
* **Imbalance Handling:** I implemented weighted random sampling in the DataLoader and applied class weights to the loss function. This ensures the model does not bias toward the majority non-lens class.
* **Architecture:** A lightweight CNN designed to process 3-channel input without losing spatial information.

### Metrics
* Binary ROC curve to visualize true positive vs. false positive trade-offs.
* Final AUC score to quantify model discriminative power.

---

## Execution Instructions

1.  Open the desired `.ipynb` file in Google Colab.
2.  Mount Google Drive to access the datasets.
3.  Run all cells to execute the training and evaluation pipeline.
4.  Evaluation plots and metrics appear at the end of each notebook.

---

## GitHub Commands for Deployment

Run these commands to push your work to a dedicated branch. Replace `GSOC_2026_Submission` with your preferred branch name.

```bash
git checkout -b GSOC_2026_Submission
git add .
git commit -m "Complete evaluation tests for Common I and Specific V"
git push origin GSOC_2026_Submission
```

**Note: No Pull Requests (PRs) should be created.**
