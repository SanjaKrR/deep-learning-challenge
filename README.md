# deep-learning-challenge
module 21 challenge
Neural Network Model Report: Alphabet Soup Charity Analysis

## Overview of the Analysis

The purpose of this analysis was to develop a deep learning model capable of predicting whether applicants for funding from Alphabet Soup, a philanthropic foundation, would be successful. Using a dataset of historical application records, we implemented a binary classification neural network to optimize the charity’s resource allocation and identify promising applicants.

---

## Results

### Data Preprocessing

- **What variable(s) are the target(s) for your model?**
  - The target variable is: `IS_SUCCESSFUL` (binary: 1 if funded, 0 if not)

- **What variable(s) are the features for your model?**
  - The features included:
    - Application Type
    - Affiliation
    - Classification
    - Use Case
    - Organization Income
    - Ask Amount
    - Special Status (e.g., if the organization has a prior grant)

- **What variable(s) should be removed from the input data because they are neither targets nor features?**
  - The following columns were removed:
    - `EIN` (Employer Identification Number, an ID field)
    - `NAME` (organization name, not relevant for prediction)

---

### ⚙️ Compiling, Training, and Evaluating the Model

- **How many neurons, layers, and activation functions did you select for your neural network model, and why?**
  - The final model architecture included:
    - **Input Layer**: matches the number of features (43)
    - **Hidden Layer 1**: 80 neurons, ReLU activation
    - **Hidden Layer 2**: 30 neurons, ReLU activation
    - **Output Layer**: 1 neuron, Sigmoid activation
  - ReLU was chosen for hidden layers due to its efficiency in training, and sigmoid for binary output.

- **Were you able to achieve the target model performance?**
  - ❌ **No** — The target accuracy was **75%**, but the final model only achieved **~72.5%** accuracy on validation data.

- **What steps did you take in your attempts to increase model performance?**
  - Increased neurons in hidden layers
  - Added a second hidden layer
  - Tuned `epochs` and `batch_size`
  - Normalized numerical input features
  - Removed noisy or uninformative features
  - Tried multiple one-hot encoding strategies for categorical data

---

### 📈 Model Training Graphs

#### 🟦 Accuracy Over Epochs

![Training and Validation Accuracy](accuracy_plot.png)

#### 🟥 Loss Over Epochs

![Training and Validation Loss](loss_plot.png)

---

## 📌 Summary

The deep learning model performed reasonably well, achieving ~72.5% accuracy, but fell short of the 75% target. The model was trained using a sequential neural network with two hidden layers and optimized using binary cross-entropy loss and the Adam optimizer.

Despite optimization efforts, overfitting and data limitations may have capped model performance. The model's accuracy plateaued, indicating the need for a more complex or different modeling approach.

---


