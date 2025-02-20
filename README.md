# Decision Tree Classifier on Iris Dataset

This repository contains the implementation of a **Decision Tree Classifier** applied to the **Iris dataset** using different techniques such as **entropy** as the splitting criterion, **cross-validation**, and **visualizing decision boundaries**.

## Operations Performed:

### 1. **Loading the Dataset**
- The **Iris dataset** is loaded using the `sklearn.datasets.load_iris()` function.
- Only the first two features of the Iris dataset (sepal length and sepal width) are used for **decision boundary visualization**.

### 2. **Data Splitting**
- The dataset is split into **training** and **testing** sets using the `train_test_split` function.
- The split is performed in a **70-30 ratio** (70% for training and 30% for testing).

### 3. **Building the Decision Tree Classifier**
- A **Decision Tree Classifier** is trained using the **entropy criterion** (information gain).
- The classifier is built with a specific **maximum depth** for the tree (3, 4, and 5).
  
### 4. **Cross-Validation**
- **K-fold cross-validation** is applied to evaluate the model's performance.
- The code performs cross-validation with **5-fold**, **7-fold**, and **10-fold** to check model performance across different folds.
  
### 5. **Visualizing Decision Boundaries**
- The decision boundaries are visualized for tree depths 3, 4, and 5 using a meshgrid.
- The decision boundaries are plotted for the classifier trained on **entropy** and overlaid with the dataset.

### 6. **Analysis of Depth vs. Performance**
- We analyze how the tree depth (3, 4, 5) affects the **complexity of the decision boundaries**.
- The impact of deeper trees on **overfitting** is observed by visualizing how the decision boundaries become more intricate with increasing depth.

### 7. **Analysis of Cross-Validation Folds**
- We analyze the impact of different fold sizes (5, 7, and 10) on **cross-validation performance**.
- Increasing the number of folds generally leads to **better performance estimation** at the cost of higher computational expense.

## Installation

### Requirements
- Python 3.x
- Required libraries:
  - `numpy`
  - `matplotlib`
  - `sklearn`
  - `graphviz`

You can install the required libraries using `pip`:

```bash
pip install numpy matplotlib scikit-learn graphviz
```

### Running the Code
To run the code, execute the following Python scripts:

1. **Decision Tree Classifier**:  
```bash
python Aarti_Dashore_decision_tree_classifier_iris_.py
```

## Output

### 1. **Decision Boundary Graphs**
- The decision boundaries for the **entropy model** are visualized for tree depths **3**, **4**, and **5**.
- The boundaries show how the classifier's decision regions evolve with increasing depth.

### 2. **Cross-Validation Results**
- Cross-validation results for **5-fold**, **7-fold**, and **10-fold** are printed.
- The **accuracy** and **variance** of the model are reported across different folds.

### 3. **Analysis of Model Behavior**
- **Depth 3**: The decision tree classifier produces large, simple regions, indicating an underfit model.
- **Depth 5**: The decision tree classifier produces intricate decision boundaries, showing overfitting behavior.
- **Cross-validation with 10 folds** provides more reliable performance estimation, but it requires higher computational resources.

## Key Insights:
- **Increasing the Depth** of the decision tree results in more **complex decision boundaries**. However, deeper trees are more prone to **overfitting**, especially when trained on small datasets like Iris.
- **Increasing the Number of Cross-Validation Folds** improves the **reliability** of model performance estimates but comes at the cost of **higher computation** time.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
