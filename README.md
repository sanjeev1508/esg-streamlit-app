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

## Future Enhancements
- Integrate more advanced deep learning models.
- Improve risk analysis using probabilistic models.
- Extend to real-time ESG data streaming.

## License
This project is open-source and available under the MIT License.
