# 🦠 COVID-19 Mortality Prediction and Model Analysis

A Machine Learning project focused on analyzing epidemiological data and investigating patterns associated with COVID-19 mortality through **Supervised and Unsupervised Learning** techniques.

The project explores how different machine learning approaches can be applied to Severe Acute Respiratory Syndrome (SARS/SRAG) records to identify patterns related to patient outcomes.

## Project Objectives

The main objective is to compare supervised and unsupervised machine learning approaches for analyzing COVID-19 patient outcomes, particularly mortality.

The project aims to:

- Explore and understand epidemiological data through Exploratory Data Analysis (EDA).
- Identify relevant patient characteristics and variables.
- Prepare and transform data for machine learning.
- Develop supervised classification models.
- Apply unsupervised clustering algorithms to identify patterns in patient records.
- Compare model behavior and evaluate clustering quality.

## 📊 Dataset

The project uses epidemiological records from **SIVEP-Gripe (Sistema de Informação de Vigilância Epidemiológica da Gripe)**, provided by Brazil's Ministry of Health through DATASUS.

**Dataset characteristics:**

| Attribute | Description |
|---|---|
| Data source | DATASUS / SIVEP-Gripe |
| Geographic scope | Brazil |
| Reference period | Data available up to September 13, 2021 |
| Original dataset | INFLUD21-13-09-2021 |
| Target variable | `EVOLUCAO` |
| Data type | Epidemiological and clinical records |

The dataset contains information about patient demographics, symptoms, clinical conditions, and outcomes.

The analysis uses the `EVOLUCAO` variable as the target for supervised learning.

*Note: The original dataset is not included in this repository and must be obtained separately.*

## Machine Learning Approaches

Two main learning paradigms are explored.

### 1. Supervised Learning

Supervised models are trained using labeled patient records to investigate the relationship between patient characteristics and clinical outcomes.

**Support Vector Classification (SVC)**

- Uses Support Vector Machines for classification.
- Applies MinMax scaling as part of the preprocessing pipeline.
- Evaluates predictions through a normalized confusion matrix.

**Logistic Regression**

- Uses Logistic Regression with L1 regularization.
- Applies Quantile Transformation to normalize feature distributions.
- Uses the `liblinear` solver.

### 2. Unsupervised Learning

Unsupervised algorithms are applied to explore similarities and identify groups of patients without relying on outcome labels during clustering.

**K-Means**

- Divides patient records into two clusters.
- Explores clustering behavior using the original and MinMax-scaled features.
- Examines the distribution of observations across clusters.

**Fuzzy C-Means**

- Uses fuzzy clustering to assign membership degrees to clusters.
- Explores two-cluster configurations.
- Compares clustering results using different feature scaling approaches.

The clustering experiments also use the **Silhouette Score** to evaluate cluster separation.

## 🔬 Methodology

The project follows these main stages:

1. **Data Acquisition:** Load epidemiological records from the SIVEP-Gripe dataset.
2. **Exploratory Data Analysis:** Investigate the dataset, distributions, and relevant variables.
3. **Data Preprocessing:** Select features and prepare the data for model training.
4. **Feature Transformation:** Apply scaling and distribution transformations where appropriate.
5. **Dataset Splitting:** Separate training and testing subsets using stratified sampling.
6. **Model Development:** Train supervised classification algorithms.
7. **Clustering Analysis:** Apply unsupervised learning algorithms to identify patient groups.
8. **Model Evaluation:** Analyze classification results and clustering quality.

## 🛠️ Technologies and Libraries

The project was developed in Python using Google Colab and the following libraries:

| Technology | Application |
|---|---|
| Python | Main programming language |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical computation |
| Scikit-learn | Machine learning, preprocessing, and evaluation |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| SciPy | Scientific computing |
| Statsmodels | Statistical analysis |
| Scikit-Fuzzy | Fuzzy logic and clustering |
| Fuzzy C-Means | Fuzzy clustering implementation |

## Evaluation Methods

The project explores different evaluation techniques according to the learning paradigm.

**Classification:**
- Confusion Matrix
- Classification predictions on the test set

**Clustering:**
- Silhouette Score
- Cluster distribution analysis
- Comparison between scaled and unscaled feature spaces

These metrics provide complementary perspectives on model behavior and the structure of the data.

## Repository Structure

```text
Covid-19_model_analysis/
│
├── Modelos_Supervisionados_nao_supervisionados_para_obitos_do_COVID_19.ipynb
│   └── Complete data analysis and machine learning experiments
│
├── LICENSE
│   └── MIT License
│
└── README.md
    └── Project documentation
```

## Getting Started

### Prerequisites

- Python 3.7 or compatible environment for the original notebook dependencies.
- Google Colab or Jupyter Notebook.
- Access to the SIVEP-Gripe dataset.

### Installation

1. Clone this repository:

```bash
git clone https://github.com/Yas-bonfim/Covid-19_model_analysis.git
```

2. Navigate to the project directory:

```bash
cd Covid-19_model_analysis
```

3. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels scikit-learn scikit-fuzzy fuzzy-c-means
```

4. Open the notebook:

```text
Modelos_Supervisionados_nao_supervisionados_para_obitos_do_COVID_19.ipynb
```

Alternatively, upload the notebook to Google Colab.

### Dataset Configuration

The original notebook uses Google Drive to access the CSV dataset.

Before running the notebook:

1. Obtain the corresponding SIVEP-Gripe dataset from DATASUS.
2. Upload the CSV file to your Google Drive.
3. Update the dataset path in the notebook to match your directory.
4. Execute the notebook cells in sequence.

## Important Considerations

- This project is an educational and exploratory machine learning study.
- The dataset represents historical epidemiological records, not current COVID-19 trends.
- Model outputs should not be interpreted as clinical diagnoses or individual medical risk assessments.
- Clustering results indicate statistical similarities, not necessarily clinically meaningful patient categories.
- Model performance does not establish causal relationships between patient characteristics and mortality.

## 📄 License

This project is distributed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

**Developed by [Yas-bonfim](https://github.com/Yas-bonfim)**

