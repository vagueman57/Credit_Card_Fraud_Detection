# Credit Card Fraud Detection

## Overview
This project is a **Credit Card Fraud Detection** system designed to identify fraudulent transactions from a large dataset of credit card records. The primary goal is to build a machine learning model capable of distinguishing between legitimate and fraudulent activities to prevent unauthorized charges.

## Dataset
The project utilizes a dataset containing transactions made by European cardholders in September 2013.
* **Scale**: The dataset consists of approximately 281,167 transactions.
* **Features**: It includes 30 numerical features (V1-V28, Time, and Amount).
* **Class Imbalance**: The dataset is highly imbalanced; fraud cases (491) represent only about 0.17% of total transactions.

## Project Structure
* `Credit_Card_Fraud_Detection.ipynb`: The main Jupyter Notebook containing data analysis, preprocessing, and model training.
* `requirements.txt`: A list of the Python libraries required to run the project.

## Technical Implementation
* **Algorithm**: The project employs a **Random Forest Classifier**, an ensemble learning method, to achieve high detection accuracy.
* **Data Cleaning (Handling NaN Values)**: 
  During the initial training phase, a `NaN` (Not a Number) error was encountered. To resolve this, the dataset was audited for missing values. It was discovered that the dataset contained an incomplete row. 
  
  **The Fix:** I implemented a cleaning step using `df.dropna()` to remove the null values before proceeding to the data splitting and training stages. This ensured that the feature matrix ($X$) and target vector ($Y$) were perfectly aligned and free of errors.

* **Preprocessing**: After cleaning, the data was split into training (80%) and testing (20%) sets using a `random_state` for reproducibility.



## Performance Results
After resolving the data issues, the model demonstrated exceptional performance across several industry-standard metrics:
* **Accuracy**: 99.95%
* **Precision**: 95.95% (High reliability in predicted fraud)
* **Recall**: 75.53% (Ability to catch the majority of actual fraud)
* **F1-Score**: 0.8452
* **Matthews Correlation Coefficient (MCC)**: 0.8511 (Indicating strong prediction even with imbalanced classes)



## How to Run
1. **Clone the repo**:  
   `git clone https://github.com/vagueman57/Credit_Card_Fraud_Detection.git`
2. **Install dependencies**:  
   `pip install -r requirements.txt`
3. **Run the Notebook**:  
   Open `Credit_Card_Fraud_Detection.ipynb` in Jupyter or Google Colab.

> **Note**: The raw dataset (`creditcard.csv`) exceeds GitHub's 100MB file size limit. Users should download the dataset locally or ensure it is ignored by Git to avoid push errors.