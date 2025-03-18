# ESG Data Analysis and Optimization Platform

## Overview
This project is a data-driven platform for analyzing and optimizing ESG (Environmental, Social, and Governance) metrics using machine learning, statistical analysis, and linear programming. It integrates various data sources to evaluate ESG scores, predict future ESG trends, and optimize project investments.

## Features
- **Data Cleaning & Processing**: Handles missing data, normalizes values, and merges multiple datasets.
- **Machine Learning**:
  - Regression Model for ESG Score Prediction.
  - Random Forest Model for ESG Classification.
- **Optimization**:
  - Linear Programming for maximizing ESG impact under budget constraints.
- **Visualization**:
  - Interactive dashboards using Streamlit and Plotly.
- **SMOTE for Data Balancing**: Handles class imbalance in ESG classification.
- **Automated Ranking System**: Ranks projects based on predicted ESG impact.

## Technologies Used
- **Python Libraries**: `pandas`, `numpy`, `sklearn`, `pulp`, `imblearn`, `streamlit`, `plotly`
- **Machine Learning Models**: Linear Regression, Random Forest Classifier
- **Optimization Algorithm**: Linear Programming using `pulp`
- **Web Framework**: Streamlit

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name.git
   cd your-repo-name
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Dataset
The project uses multiple ESG-related datasets:
- `ESGCountry.csv`
- `ESGSeries.csv`
- `ESGSeries-Time.csv`
- `ESGData.csv`
- `ESGFootNote.csv`
- `ESGCountry-Series.csv`

## How to Run
1. Place the CSV files in the project directory.
2. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

## Model Training and Evaluation
- **Regression Model**: Trained using `LinearRegression()` on ESG time-series data.
- **Random Forest Classifier**: Tuned using `RandomizedSearchCV` for ESG classification.
- **Performance Metrics**:
  - Mean Squared Error (MSE)
  - Accuracy Score
  - F2 Score
  - Confusion Matrix

## Optimization Approach
- Uses **Linear Programming** to allocate budget to maximize ESG impact while minimizing risk.
- Constraints:
  - Budget Limit
  - Risk Factors
  - Predicted ESG Score

## Visualization
- Scatter Plot: Projected Impact vs Predicted ESG Score
- Bar Chart: Top 10 ESG Projects by Score

## Deploying on Hadoop (Ubuntu 22)
This section provides steps to deploy the ESG data analysis platform on **Hadoop** using **Ubuntu 22**.

### **Step 1: Mount the Shared Directory (if applicable)**
If using a shared folder to transfer CSV files, mount it before accessing:
```bash
sudo mount -t vboxsf <shared_folder_name> /media/<mount_point>
```
Verify the files:
```bash
ls -l /media/<mount_point>/
```

### **Step 2: Create a Directory in HDFS**
Create a directory in **HDFS** to store CSV files:
```bash
hdfs dfs -mkdir -p /esg_project/csv_files/
hdfs dfs -ls /esg_project/
```

### **Step 3: Upload CSV Files to HDFS**
Upload all ESG dataset files into the **HDFS directory**:
```bash
hdfs dfs -put /media/<mount_point>/*.csv /esg_project/csv_files/
hdfs dfs -ls /esg_project/csv_files/
```

Once the dataset is uploaded, you can process the data using **Hadoop MapReduce**, **Apache Spark**, or integrate it with **Streamlit** for visualization.

## Future Enhancements
- Integrate more advanced deep learning models.
- Improve risk analysis using probabilistic models.
- Extend to real-time ESG data streaming.

## License
This project is open-source and available under the MIT License.

