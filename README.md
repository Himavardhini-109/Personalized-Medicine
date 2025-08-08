# Personalized-Medicine
A machine learning model that predicts treatment effectiveness for personalized medicine based on patient characteristics and genetic markers.
 ##👨‍💻 Developer Information
 - **Name**:O.Himavardhini
 - **Roll No**:222T1A3140
 - **Institution**:Ashoka Womens Engineering College
## 📋 Overview

This project implements a Random Forest classifier to predict whether a medical treatment will be effective for individual patients based on their demographic information, genetic profile, and mutation scores. The model helps healthcare providers make data-driven decisions for personalized treatment plans.

## 🎯 Features

- **Patient Data Processing**: Automated data cleaning and preprocessing
- **Genetic Analysis**: Incorporates genetic markers (Gene A, B, C) for treatment prediction
- **Treatment Prediction**: Binary classification (Effective/Not Effective)
- **Model Performance**: Comprehensive accuracy metrics and classification reports
- **New Patient Prediction**: Ready-to-use prediction system for new patients

## 📊 Dataset

The model expects a CSV file (`personalized_medicine.csv`) with the following columns:

| Column | Description | Type |
|--------|-------------|------|
| `age` | Patient age | Numeric |
| `gender` | Patient gender (M/F) | Categorical |
| `gene_a` | Gene A expression (0/1) | Binary |
| `gene_b` | Gene B expression (0/1) | Binary |
| `gene_c` | Gene C expression (0/1) | Binary |
| `mutation_score` | Genetic mutation severity score | Numeric |
| `response` | Treatment effectiveness (0/1) | Binary (Target) |

## 🔧 How It Works

1. **Data Loading**: Reads the CSV dataset with patient information
2. **Data Preprocessing**: 
   - Cleans column names (removes spaces, converts to lowercase)
   - Encodes gender categorical variable (M→0, F→1)
3. **Feature Engineering**: Separates features (X) from target variable (y)
4. **Model Training**: Uses Random Forest algorithm with 80/20 train-test split
5. **Evaluation**: Provides accuracy score and detailed classification report
6. **Prediction**: Demonstrates prediction for new patient data

## 📈 Model Performance

The model outputs:
- **Accuracy Score**: Overall prediction accuracy
- **Classification Report**: Precision, recall, and F1-score for both classes
- **Individual Predictions**: Treatment effectiveness for new patients

## 💡 Usage Example

```python
# Example prediction for a new patient
new_patient = pd.DataFrame({
    'age': [55],
    'gender': [1],         # 1 = Female, 0 = Male
    'gene_a': [1],         # Gene A expressed
    'gene_b': [0],         # Gene B not expressed
    'gene_c': [1],         # Gene C expressed
    'mutation_score': [3.4] # Mutation severity
})

prediction = model.predict(new_patient)
# Output: "✅ Effective" or "❌ Not Effective"
```

## 🔍 Key Components

- **Random Forest Classifier**: Ensemble learning method for robust predictions
- **Binary Classification**: Predicts treatment response (0 = Not Effective, 1 = Effective)
- **Feature Importance**: Genetic markers and patient demographics
- **Cross-validation**: Train-test split for unbiased performance evaluation

## 📝 Applications

- **Clinical Decision Support**: Assist doctors in treatment selection
- **Drug Development**: Identify patient populations likely to respond
- **Healthcare Optimization**: Reduce trial-and-error in treatment approaches
- **Research**: Analyze genetic factors affecting treatment outcomes


## 🙏 Acknowledgments

- Built using scikit-learn machine learning library
- Designed for healthcare and personalized medicine applications
- Supports evidence-based treatment decisions

