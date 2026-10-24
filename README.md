# Progree Machine Learning Internship

Projects completed during my Machine Learning internship at **Progree**: a regression pipeline, a deep learning image classifier, and a mini project on highly imbalanced clinical data.

> Replace `https://colab.research.google.com/drive/1RYRfUJmH7004132owauGrSbNRQhErx9v` in the Colab links below with your GitHub username. Replace `https://github.com/au253032` at the bottom.

## Projects

| # | Project | Tools | Open in Colab |
|---|---------|-------|---------------|
| 2 | **Linear / Ridge Regression** on California Housing | scikit-learn, pandas | [![Open In Colab](https://colab.research.google.com/drive/1RYRfUJmH7004132owauGrSbNRQhErx9v)] 
| 3 | **CNN Image Classification** on CIFAR-10 | TensorFlow / Keras | [![Open In Colab](https://colab.research.google.com/drive/1g9coG5J0yasWnpCuqS874j5FMkhsVGrT#scrollTo=e-aJmvFw0dgu) |
| 4 | **Clinical Disease Predictor** (imbalanced data, mini project) | scikit-learn, imbalanced-learn, XGBoost | [![Open In Colab](https://colab.research.google.com/drive/1GI_zGY78fyRHHyB3Vkt0y2leB_Vt4Ks-)]

(Task 1 was a LinkedIn announcement of the internship, so it has no code.)

---

### Task 2 - Predictive Regression Pipeline
- **Data:** California Housing (target: median house value, in $100,000)
- **Preprocessing:** mean imputation, standard scaling and one-hot encoding in a single scikit-learn `Pipeline`
- **Models:** Linear Regression baseline and Ridge Regression, with alpha tuned by 5-fold cross-validation
- **Metrics:** R² and RMSE on train and test data
- **Plots:** actual vs predicted, residuals, model coefficients

### Task 3 - CNN Image Classification
- **Data:** CIFAR-10 (60,000 colour images, 10 classes)
- **Architecture:** 6 convolution layers, 3 max-pooling layers and 2 fully connected layers, with batch normalisation and dropout
- **Overfitting control:** data augmentation (flip, rotation, zoom, translation), plus a comparison run with and without augmentation
- **Outputs:** training and validation accuracy curves, confusion matrix, misclassified examples
- **Run on:** Colab with a GPU (Runtime -> Change runtime type -> T4 GPU)

### Task 4 - Clinical Disease Predictor (Mini Project)
- **Data:** UCI Breast Cancer Wisconsin (Diagnostic), subsampled to about 11% malignant cases to simulate a screening setting. The class ratio was changed on purpose; features and labels are the original data.
- **Imbalance strategies compared:** none, class weighting, SMOTE (applied inside the cross-validation pipeline, so there is no data leakage)
- **Models:** SVM, Random Forest, XGBoost, each tuned with GridSearchCV
- **Evaluation:** focus on **recall (sensitivity)**, using repeated stratified 5-fold cross-validation score arrays and a held-out test set
- **Report:** the last notebook cell writes a 5-6 page `.docx` report from the real results

## How to run
1. Click an **Open in Colab** badge above (or upload the `.ipynb` file at [colab.research.google.com](https://colab.research.google.com/drive/1g9coG5J0yasWnpCuqS874j5FMkhsVGrT)).
2. For Task 3, select a GPU runtime.
3. Choose **Runtime -> Run all**.

No local installation is needed. Libraries (scikit-learn, TensorFlow, XGBoost, imbalanced-learn) are available in Colab; the Task 4 notebook installs any that are missing.

## Repository structure
```
progree-ml-internship/
├── Task2_Linear_Regression_California_Housing.ipynb
├── Task3_CNN_CIFAR10_Image_Classification.ipynb
├── Task4_Clinical_Disease_Predictor_Mini_Project.ipynb
├── Task4_Clinical_Disease_Predictor_Report.docx
└── README.md
```

## Results
Results (R² / RMSE, test accuracy, recall) are printed inside each notebook after it runs. Save the notebooks **with outputs** before uploading them to GitHub so visitors can see them without running anything.

## Limitations
- Task 4 uses an artificially imbalanced version of a small dataset, so its scores have wide uncertainty and are not clinical evidence. This project must not be used for real diagnosis.

## Author
**Your Name** - Ateeq Ur Rehman
Machine Learning Intern at Progree
[LinkedIn](https://www.linkedin.com/in/ateeq-ur-rehman-b1795b322?utm_source=share_via&utm_content=profile&utm_medium=member_android) | [GitHub](https://github.com/au253032)
