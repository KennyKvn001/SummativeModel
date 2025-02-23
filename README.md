# Dropout Predictor Model

## Problem statement

Student dropout is a significant issue in Rwanda's higher education sector, influenced by financial, academic, and personal challenges. Existing research underscores the need for context-specific, predictive approaches to address dropout risks in Rwanda. For instance, a study on school dropout and students' academic performance in Rwanda highlights the impact of dropout rates on educational productivity. This Model aims to bridge the gap by incorporating Rwanda-specific data and providing a solution for educators and policymakers.

## Date source

Used data from [Kaggle](https://www.kaggle.com/datasets/tulasiram574/students-dropout-and-academic-success)

## Model Training Results

| Training Parameters | Instance 1                   | Instance 2                   | Instance 3                   | Instance 4                   |
| ------------------- | ---------------------------- | ---------------------------- | ---------------------------- | ---------------------------- |
| Optimizer           | Not used                     | Adam                         | Adam                         | RMSprop                      |
| Regularizer         | Not used                     | Not used                     | L2, 0.001                    | L2, 0.001                    |
| Epochs              | 100                          | 300                          | 300                          | 500                          |
| Early Stopping      | No                           | Yes                          | Yes                          | Yes                          |
| Number of Layers    | 3                            | 3                            | 3                            | 3                            |
| Learning Rate       | Not used                     | 0.0001                       | 0.0001                       | 0.0001                       |
| F1 score            | class 0(0.92), class 1(0.79) | class 0(0.92), class 1(0.80) | class 0(0.92), class 1(0.79) | class 0(0.91), class 1(0.78) |
| Accuracy            | 0.88073                      | 0.88440                      | 0.88073                      | 0.87155                      |
| Recall              | class 0(0.95), class 1(0.73) | class 0(0.95), class 1(0.73) | class 0(0.95), class 1(0.73) | class 0(0.95), class 1(0.71) |
| Precision           | class 0(0.88), class 1(0.87) | class 0(0.89), class 1(0.88) | class 0(0.89), class 1(0.87) | class 0(0.88), class 1(0.86) |

The combination that worked better was for the second instance where I used Adam and BatchNormalization and dropout compared to other models.

Between Neural Networks models and ML algorithms, the ML algorithm I used (XGBoost) performed better compared to the NN models.

The Hyperparameters used in XGBoost:
{'colsample_bytree': 0.8, 'learning_rate': 0.1, 'max_depth': 3, 'n_estimators': 100, 'subsample': 0.9}

And the Accuraccy, F1 score, Recall and Precision of XGBoost are:
{'accuracy': 0.8862385321100917, 'precision': 0.8811188811188811, 'recall': 0.7368421052631579, 'f1_score': 0.802547770700637}

### Demo Video

## How to Use This Repository

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Setup and Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/dropout-predictor.git
   cd dropout-predictor
   ```

### Using the Model

1. Prepare your data:

   - Ensure your data follows the same format as the training dataset
   - Save your data as a CSV file in the `data` directory

2. Train the model:

   ```bash
   python train.py --data_path data/your_data.csv
   ```

3. Make predictions:
   ```bash
   python predict.py --input_file data/test_data.csv --output_file predictions.csv
   ```
