# Car Price Prediction with Traditional Regression Models

This project explores different traditional regression models to predict the prices of new/used cars based on various features. It includes exploratory data analysis (EDA), data preprocessing, and model training using Scikit-Learn. The goal is to compare model performance and understand which approaches work best for this type of dataset.

## Dataset

The dataset used in this project contains listings of used cars, with 11,000+ entries and 15 features including brand, model, year, vehicle style, and more. The target variable is the car price.

- **Source**: *[Kaggle Dataset Link](https://www.kaggle.com/datasets/CooperUnion/cardataset)*
- **License**: *Unknown*  

The dataset is not included in this repository due to licensing restrictions. To use it, please download it directly from the Kaggle link above and place it in a `data/` folder.

## Project Structure

car-price-regression-models/  
├── data/  # Placeholder folder for dataset (not included)  
│ └── README.txt  # Instructions to manually download the dataset  
├── notebooks/  # Jupyter notebook with EDA, preprocessing, and modeling  
│ └── car-price-prediction-using-regression-models.ipynb  
├── outputs/  # Folder for generated outputs (optional)  
├── README.md  # Project documentation  
├── requirements.txt  # Python dependencies  
└── .gitignore  # Files/folders excluded from version control  

## How to Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/CobraJet-429/car-price-regression-models.git 
   cd car-price-regression-models
   ```
                                                                          
2. **Download the dataset manually** from [this Kaggle link](https://www.kaggle.com/datasets/CooperUnion/cardataset) and place the CSV file in the `data/` folder.

3. **(Optional)**: Create and activate a virtual environment

4. **Install required packages**: 
   ```bash 
   pip install -r requirements.txt
   ```
                                                                            
5. **Open the notebook**: 
   ```bash 
   jupyter notebook notebooks/car-price-prediction-using-regression-models.ipynb
   ```
                 
## Requirements

To run this project, you'll need the following Python packages:

- pandas
- numpy
- matplotlib
- seaborn
- plotly
- scikit-learn
- scipy
- jupyter

You can install them all at once using:

```bash
pip install -r requirements.txt
```

## Sample Results

Performance comparison across models based on MSE and R-squared scores:

| Model                    | Train MSE | Train R2  | Val MSE  | Val R2   | Test MSE | Test R2  |
|--------------------------|-----------|-----------|----------|----------|----------|----------|
| Linear Regression        | 0.0360    | 0.9640    | 0.0585   | 0.9392   | 0.0662   | 0.9357   |
| Linear Regression with L1 (Lasso) Regularization         | 0.0384    | 0.9616    | 0.0620   | 0.9356   | 0.0701   | 0.9319   |
| Linear Regression with L2 (Ridge) Regularization          | 0.0360    | 0.9640    | 0.0585   | 0.9392   | 0.0662   | 0.9358   |
| Polynomial Degree 2 (L2-Regularized)     | 0.0272    | 0.9728    | 0.0427   | 0.9556   | 0.0512   | 0.9503   |
| Polynomial Degree 3 (L2-Regularized)     | 0.0145    | 0.9855    | 0.0353   | 0.9633   | 0.0325   | 0.9684   |
| Decision Tree Regression | 0.0148    | 0.9852    | 0.0148   | 0.9846   | 0.0199   | 0.9807   |

Among all models, **Decision Tree Regression** achieved the best performance on both validation and test sets.
