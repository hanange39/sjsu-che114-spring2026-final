# QSAR Molecular Activity Prediction: MLP vs. LightGBM

Objective: Study the quantitative structure-activity relationship (QSAR) of 837 different molecules using a deep-learning model and 
a non-DL model to determine which one best predicts molecular activity.

## Course Context
* **Course:** CHE114: Data Science in Chemical and Materials Engineering
* **Institution:** San Jose State University
* **Instructor:** Prof. Naoki Matsumura
* **Term:** Spring 2026

## Dataset
* **Source:** [QSAR Molecular Descriptor Predictions](https://www.kaggle.com/datasets/thedevastator/qsar-molecular-descriptor-predictions?select=test_rows_labels.csv)
* **Description:** This dataset comes from Kaggle and explores the QSAR and properties of molecules. It contains 41 variables that serve as molecular
descriptors describing the structure and properties of 837 different molecules, as well as one
variable labeled “Class” that indicates whether the molecule is above or below an activation
energy threshold. These descriptors are used to predict whether the activation energy of a molecule is below or above this threshold.

## Models Evaluated
* **Deep Learning Model:** Multilayer Perceptron (MLP) model implemented using the Keras Sequential API
* **Tree-Based Model:** Gradient-Boosting Machine (LGBM) Classifier via FLAML AutoML

## Results & Evaluation

### Performance Comparison
| Metric | Multilayer Perceptron (MLP) | LightGBM (FLAML) |
| :--- | :---: | :---: |
| **Weighted F1-Score** | `0.XX` | `0.XX` |
| **ROC-AUC** | `0.XX` | `0.XX` |

- **Statistical Significance (Paired t-test):** $p = \text{[value]}$
The performances of the MLP and LightGBM models are relatively similar, though the MLP slightly outperformed LightGBM in both weighted F1-score and ROC-AUC. Paired t-test results indicate that the difference in performance between the two models is not statistically significant at the $\alpha = 0.05$ level.

### Visual Evaluation
#### ROC Curve Comparison
![ROC Curve Comparison](path/to/roc_curve.png)

#### Confusion Matrices
| Multilayer Perceptron (MLP) | LightGBM (FLAML) |
| :---: | :---: |
| ![MLP Confusion Matrix](path/to/mlp_confusion_matrix.png) | ![LightGBM Confusion Matrix](path/to/lgbm_confusion_matrix.png) |

## Quick Start

### Prerequisites
* **Python 3.x**
* **Jupyter Notebook** or **JupyterLab** *(or Google Colab / VS Code)*.

### Running the Project
1. Clone this repository:
   ```bash
   git clone https://github.com/hanange39/sjsu-che114-spring2026-final.git
   ```
2. Navigate to the folder:
   ```bash
   cd sjsu-che114-spring2026-final
   ```
3. Install any required libraries:
   ```bash
   pip install "flaml[automl]" pandas numpy matplotlib scikit-learn scipy seaborn tensorflow
   ```
4. Launch the Jupyter Notebook environment:
   ```bash
   jupyter notebook
   ```
5. The browser will open. Click on the notebook file and run the cells sequentially.

## Built With
* **Python 3**
* **Jupyter Notebook**
* **FLAML** (Automated Machine Learning)
* **Machine Learning & Deep Learning:** tensorflow, keras, scikit-learn
* **Data & Science Libraries:** `pandas`, `numpy`, `matplotlib`, `scipy`, 'seaborn'
