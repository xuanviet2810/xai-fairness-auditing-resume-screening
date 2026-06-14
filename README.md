# The Impact of Explainable AI on Fairness Auditing and User Trust in Software Engineering Resume Screening Systems

## Overview

This research investigates whether Explainable Artificial Intelligence (XAI) can improve transparency, fairness auditing, and user trust in AI-assisted hiring systems.

The study develops machine learning models for software engineering resume screening and applies SHAP (SHapley Additive exPlanations) to analyze decision-making behavior, identify potential sources of bias, and evaluate how explanations influence human perceptions of AI-generated hiring recommendations.

The project combines machine learning, algorithmic fairness, explainable AI, and human-subject evaluation to examine the role of explainability in responsible AI deployment for recruitment.

---

## Research Questions

This study addresses the following questions:

1. Which candidate attributes most strongly influence AI hiring recommendations?
2. Can SHAP explanations effectively identify sources of algorithmic bias?
3. Does university prestige contribute to disparate impact in hiring predictions?
4. Do SHAP explanations improve perceived fairness, transparency, trust, and adoption intention among human evaluators?

---

## Methodology

### Dataset

A feature-engineered resume dataset was constructed containing information related to:

* Academic performance (CGPA)
* Work experience
* Technical skills
* Soft skills
* Programming languages
* Certifications
* Projects
* Internships
* Research publications
* University tier

A research-grounded hiring score was used to generate hiring labels, creating a controlled environment for explainability and fairness analysis.

### Machine Learning Models

Two ensemble learning algorithms were evaluated:

* Random Forest Classifier
* XGBoost Classifier

Models were trained using an 80/20 stratified train-test split.

### Explainability

Model decisions were interpreted using:

* SHAP Global Explanations
* SHAP Local Explanations
* Feature Attribution Analysis

### Fairness Evaluation

The study evaluates:

* Demographic Parity
* Equal Opportunity
* Disparate Impact

University tier is used as a proxy variable for socioeconomic background.

### Human Subject Experiment

A controlled between-subjects experiment compared:

**Control Group**

* Hiring prediction only

**Treatment Group**

* Hiring prediction
* SHAP explanation

Participants evaluated:

* Trust
* Fairness
* Transparency
* Adoption Intention

---

## Results

### Model Performance

| Metric    | Random Forest | XGBoost |
| --------- | ------------- | ------- |
| Accuracy  | 0.9121        | 0.9247  |
| Precision | 0.8934        | 0.9102  |
| Recall    | 0.8711        | 0.8893  |
| F1 Score  | 0.8821        | 0.8996  |
| ROC AUC   | 0.9603        | 0.9714  |

### Key Findings

* Skills score was the strongest predictor of hiring recommendations.
* Experience and technical strength were major contributors to positive outcomes.
* SHAP identified university tier as a significant contributor to disparate impact.
* Tier 3 candidates experienced substantially lower selection rates than Tier 1 candidates.
* SHAP explanations significantly improved:

  * Perceived fairness
  * Transparency
  * Adoption intention
* Trust increased but did not reach statistical significance.

---

## Repository Structure

```text
xai-hiring-fairness/
│
├── README.md
├── LICENSE
│
├── XAIResearchPaper.pdf
│
├── code/
│   ├── ResearchCleanData.ipynb
│   ├── ResearchTrainModel.ipynb
│   └── ResearchDataAnalytic.ipynb
│
├── data/
│   ├── resume_dataset_200k_enhanced.csv
│   ├── resume_dataset_research_ready.csv
│   ├── Control.csv
│   └── Treatment.csv
│
├── figures/
│   ├── candidateA.png
│   ├── candidateB.png
│   ├── candidateC.png
│   ├── candidateD.png
│   ├── profile_A.png
│   ├── profile_B.png
│   ├── profile_C.png
│   └── profile_D.png
```

## Contents

### Paper

* **XAIResearchPaper.pdf**

  * Full research paper describing the methodology, experiments, results, and conclusions.

### Code

* **ResearchCleanData.ipynb**

  * Data cleaning, validation, feature engineering, and dataset preparation.

* **ResearchTrainModel.ipynb**

  * Random Forest and XGBoost model training and evaluation.

* **ResearchDataAnalytic.ipynb**

  * SHAP explainability analysis, fairness auditing, statistical testing, and visualization.

### Data

* **resume_dataset_200k_enhanced.csv**

  * Original enhanced synthetic resume dataset.

* **resume_dataset_research_ready.csv**

  * Cleaned and feature-engineered dataset used for model development.

* **Control.csv**

  * Survey responses from participants who received AI predictions without explanations.

* **Treatment.csv**

  * Survey responses from participants who received AI predictions with SHAP explanations.

### Figures

* **candidateA–D.png**

  * SHAP explanation visualizations presented during the human-subject experiment.

* **profile_A–D.png**

  * Candidate profiles used in the survey study.

---

## Reproducing the Study

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Train Models

```bash
python train_model.py
```

### Generate SHAP Explanations

```bash
python shap_analysis.py
```

### Run Fairness Evaluation

```bash
python fairness_analysis.py
```

---

## Citation

If you use this work, please cite:

```text
Dao, V. (2026).
The Impact of Explainable AI on Fairness Auditing and User Trust
in Software Engineering Resume Screening Systems.
```

---

## Limitations

* Synthetic hiring dataset
* Limited sample size (N = 60)
* Recruitment scenarios rather than real hiring decisions
* Evaluation focused exclusively on SHAP explanations

Future work will explore real-world hiring datasets, alternative explanation techniques, and larger participant populations.

---

## Author

Viet Dao

Computer Science Student
Denison University

---

## License

This project is released under the MIT License.
