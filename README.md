Student Performance Prediction - Machine Learning Project
 Project Overview

This project is an end-to-end Machine Learning pipeline built to predict student academic performance using demographic and educational features.  
The project focuses on data preprocessing, model training, evaluation, and artifact management, following industry-level ML practices.
Deployment is planned as the next phase and is not included in this version.
Problem Statement
Given student-related attributes such as:
Gender
Parental level of education
Lunch type
Test preparation course
Reading and writing scores
The goal is to predict student performance(score).
This is a regression problem.
Project Structure

MLproject/
│
├── artifacts/
│ ├── data.csv
│ ├── train.csv
│ ├── test.csv
│ ├── model.pkl
│ └── preprocessor.pkl
│
├── notebook/
│ ├── data/
│ │ └── stud.csv
│ └── catboost_training_config.json
│
├── src/
│ ├── components/
│ │ ├── data_ingestion.py
│ │ ├── data_transformation.py
│ │ └── model_trainer.py
│ └── pipeline/
      ├── logger.py
      ├── exception.py
│ └── predict_pipeline.py
│
├── logs/
├── requirements.txt
└── README.md
Tech Stack
python
Pandas , NumPy
Scikit-Learn
CatBoost
Logging and Custom Exception Handling
Git and GitHub
Machine learning Pipeline

Data Ingestion
- Dataset loaded from CSV
- Supports both automated ingestion and pre-split datasets
- Train and test datasets stored in artifacts

2.Data Transformation
- Numerical features scaled
- Categorical features encoded
- Preprocessing pipeline saved as preprocessor.pkl

3.Model Training
- Model used: CatBoost Regressor
- Hyperparameters loaded from a JSON configuration file
- Trained model saved as model.pkl

4.Model Evaluation
- Evaluation metrics: **R² Score / RMSE**
- Model evaluated on the test dataset

How to Run the Project

Step 1:Clone the repository

```bash
git clone <repository-url>
cd MLproject

Step 2:Install dependencies

pip install -r requirements.txt

Step 3:Run training pipeline

python -m src.components.data_ingestion.data_ingestion
Generated Artifacts
train.csv
test.csv
preprocessor.pkl
model.pkl
These artifacts are ready to be used for inference and deployment.

Key Highlights

Modular and scalable ML pipeline

Configuration-driven model training

Clean project structure

Reusable preprocessing and model artifacts

Production-oriented design (pre-deployment stage)

Deployment Status

Not deployed yet.

Planned deployment options:

Flask / FastAPI REST API
Model inference service
Cloud deployment

Conclusion

This project demonstrates a production-ready machine learning workflow up to the model training and evaluation stage.
The trained model and preprocessing artifacts are prepared for seamless deployment in the next phase.

Author 

Madhavi Chipade









 


