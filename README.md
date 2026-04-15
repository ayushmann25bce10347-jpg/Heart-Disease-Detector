# Heart-Disease-Detector


This project is a machine learning–powered diagnostic tool that analyzes a patient’s clinical data to estimate their likelihood of having heart disease. Instead of giving a simple yes/no result, it provides a probability score, helping users better understand risk levels. The application runs through a clean, easy-to-use terminal interface and also includes visual comparisons with historical patient data.

### Features

**Probability-Based Results**
Rather than offering a basic classification, the tool calculates a precise percentage indicating the likelihood of heart disease.

**Interactive Terminal Interface**
The program guides users step by step, explaining medical terms along the way to make data entry straightforward and accessible.

**Population Comparison**
It generates a scatter plot that visually compares the current patient’s data with a broader dataset of clinical cases.

**Consistent Input Handling**
Using metadata tracking, the system ensures that all user inputs align perfectly with the format expected by the trained model.

### Installation

**1. Prerequisites**
Make sure Python 3.8 or later is installed on your system.

**2. Install Required Libraries**
Run the following command:

```
pip install pandas joblib matplotlib seaborn scikit-learn
```

**3. Required Files**
Place the following files in the same directory:

* `heart_predictor.py` – main application script
* `heart_model.pkl` – trained machine learning model
* `model_columns.pkl` – metadata for feature consistency
* `heart.csv` – dataset used for visualization

### How to Use

1. Open your terminal or command prompt.
2. Navigate to the project folder.
3. Run the program:

   ```
   python heart_predictor.py
   ```
4. Enter patient details when prompted.

   * Example: For sex, input `1` for male and `0` for female
   * Example: For cholesterol, enter the value in mg/dl (e.g., 240)
5. Review the predicted result and probability score.
6. A visualization window will appear, showing where the patient falls compared to historical data.

### Technical Overview

The system relies on a pre-trained classification model. By using `predict_proba`, it can detect borderline cases—situations where a patient may not currently have heart disease but shows a relatively high risk (for example, 48%). This allows for earlier awareness and potential intervention.

For visualization, the tool plots cholesterol levels against maximum heart rate, two key indicators of heart health. By highlighting the “current patient” on this chart, users can clearly see how their data compares to broader population trends, making the results easier to interpret.

