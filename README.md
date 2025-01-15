# README for BiasGuard Code and Data

## Overview
The **BiasGuard** method is designed to analyze and mitigate biases in datasets using reproducible code. As machine learning (ML) systems increasingly impact critical sectors such as hiring, financial risk assessments, and criminal justice, the imperative to ensure fairness has intensified due to potential negative implications. While much ML fairness research has focused on enhancing training data and processes, addressing the outputs of already deployed systems has received less attention.

BiasGuard introduces a novel approach designed to act as a fairness guardrail in production ML systems. It leverages Test-Time Augmentation (TTA) powered by Conditional Generative Adversarial Network (CTGAN), a cutting-edge generative AI model, to synthesize data samples conditioned on inverted protected attribute values, thereby promoting equitable outcomes across diverse groups. This method aims to provide equal opportunities for both privileged and unprivileged groups while significantly enhancing the fairness metrics of deployed systems without the need for retraining. 

Our comprehensive experimental analysis across diverse datasets reveals that BiasGuard enhances fairness by 31% while only reducing accuracy by 0.09% compared to non-mitigated benchmarks. Additionally, BiasGuard outperforms existing post-processing methods in improving fairness, positioning it as an effective tool to safeguard against biases when retraining the model is impractical.

This folder includes the following components:

1. **Code**: A Jupyter Notebook file (`BiasGuard.ipynb`) containing the implementation of the BiasGuard method.
2. **Data**: Five sample datasets to test and demonstrate the functionality of the BiasGuard method.

This README provides instructions on setting up the environment, using the code, and replacing datasets for reproducibility.

---

## File Structure
```
├── BiasGuard.ipynb
├── datasets/
│   ├── Kaggle_Surgical-deepnet.csv
│   ├── adult.csv
│   ├── compas-scores-two-years_v1.csv
│   ├── law_school_clean.csv
│   └── recruitmentdataset-2022-1.3.csv
├── README.md (this file)
```

---

## Prerequisites
1. **Python Environment**:
   - Install Python 3.8 or higher.
   - Install Jupyter Notebook.
2. **Required Libraries**:
   - pandas
   - numpy
   - scikit-learn
   - matplotlib
   - seaborn
   - Other dependencies (refer to the first cell of the notebook for `pip install` commands).

---

## Instructions

### 1. Setting Up
1. Clone or download this folder to your local machine.
2. Ensure you have all required libraries installed. Use the following command to install missing dependencies:
   
### 2. Running the Code
1. Open the Jupyter Notebook:
2. Follow the instructions within the notebook. Each code cell is sequentially organized for ease of use.
3. Replace dataset paths with the appropriate file path for the dataset you wish to analyze in your local environment.

## Dataset Details
1. **Kaggle_Surgical-deepnet.csv**: A dataset from Kaggle for surgical analysis and bias detection.
2. **adult.csv**: A dataset commonly used for income prediction and fairness testing.
3. **compas-scores-two-years_v1.csv**: A dataset focusing on recidivism risk assessments and their associated biases.
4. **law_school_clean.csv**: A dataset analyzing law school admissions and demographic fairness.
5. **recruitmentdataset-2022-1.3.csv**: A synthetic recruitment dataset for studying hiring biases.

Each dataset is preprocessed and formatted to be compatible with the BiasGuard method. If using your own dataset, ensure it follows a similar structure.

---

## Troubleshooting
- **Missing Library**: Ensure all required libraries are installed.
- **File Not Found Error**: Verify that the dataset path is correct.
- **Performance Issues**: For large datasets, consider sampling or using optimized configurations.

---


