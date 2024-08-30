# Telecom Churn Prediction

**Machine learning project to predict customer churn in the telecom industry using Python and AWS. Includes data loading, EDA, model building, and monitoring for data and model drift.**

## Table of Contents
- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Project Overview
Churn analysis is a critical process for telecom companies as it helps them identify customers who are likely to leave the service provider and take their business elsewhere. This project aims to build a predictive model that can accurately forecast customer churn, helping the company to take preventive actions.

The project also includes a feedback loop for continuous monitoring and retraining of the model to maintain its performance over time.

## Getting Started
To get a local copy up and running, follow these simple steps.

### Prerequisites
- Python 3.8 or higher
- AWS Account
- SQL Database (AWS RDS recommended)

### Installation
1. Clone the repo:
    ```sh
    git clone https://github.com/Carlosrod723/Telecom-Churn-Prediction.git
    ```
2. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```
3. Set up the database connection in `config.py` (instructions will be added here).

## Tech Stack
- **Language**: Python, SQL
- **Cloud**: AWS
- **Libraries**:
  - `pandas`: For data analysis and manipulation
  - `pyodbc`: For connecting with AWS cloud to fetch the data
  - `numpy`: For performing mathematical operations over data
  - `matplotlib`, `seaborn`: For data visualization
  - `scikit-learn`, `xgboost`: For model building
  - `deepchecks`: For continuous model monitoring

## Project Structure
Telecom-Churn-Prediction/ │ ├── README.md ├── LICENSE ├── requirements.txt ├── churn_modeling.ipynb ├── data/ │ ├── Telecom_data.csv │ ├── processed_telecom_churn_data.csv ├── images/ (optional) └── src/ (optional) ├── utils.py (for helper functions)


## Usage
1. Load and preprocess the data using the `churn_modeling.ipynb` notebook.
2. Train and evaluate the model.
3. Monitor the model for data and model drift.

## Results
The project developed three machine learning models to predict customer churn: Logistic Regression, Random Forest, and XGBoost. The performance of these models was evaluated based on F1 score and recall, which are critical for identifying customers at risk of churning.

| Model              | Train F1 Score | Train Recall | Test F1 Score | Test Recall |
|--------------------|----------------|--------------|---------------|-------------|
| Logistic Regression| 0.6097         | 0.4874       | 0.3333        | 0.2457      |
| Random Forest      | 0.9943         | 0.9903       | 0.4434        | 0.3946      |
| XGBoost            | 0.8252         | 0.7850       | 0.4929        | 0.4331      |

### Business Implications

- **Logistic Regression**: The model struggles to accurately identify customers who are likely to churn, leading to potential revenue loss due to missed opportunities for customer retention.
- **Random Forest**: Despite high performance on training data, this model overfits and fails to generalize well to unseen data, making it unreliable for predicting churn.
- **XGBoost**: This model provides the best balance between precision and recall, making it the most effective for identifying customers at risk of churning. The model's predictions can help the telecom company implement targeted retention strategies, reducing churn and increasing customer loyalty.

### Conclusion

XGBoost is recommended as the most reliable model for predicting customer churn, based on its performance metrics. The model's ability to generalize well to new data makes it a valuable tool for maintaining customer retention and reducing churn in the telecom industry.

## Contributing
Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
Distributed under the MIT License. See `LICENSE` for more information.

## Contact
Carlos Rodriguez - [LinkedIn](https://www.linkedin.com/in/carlos-rodriguez-b2534a62/)

Project Link: [https://github.com/Carlosrod723/Telecom-Churn-Prediction](https://github.com/Carlosrod723/Telecom-Churn-Prediction)
