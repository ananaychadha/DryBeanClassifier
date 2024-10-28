# DryBeanClassifier

## Objective
This project aims to evaluate the effectiveness of various classification models on the [UCI Dry Bean Dataset](https://archive.ics.uci.edu/ml/datasets/Dry+Bean+Dataset) to differentiate between types of beans. An additional objective is to address a scenario where one bean type, **‘Sira’**, is moderately poisonous, focusing on improving classification accuracy for this type of bean, where misclassification carries greater risk.

## Dataset
The dataset is available on the UCI Machine Learning Repository and on Brightspace in the file `Dry_Bean_Dataset.csv`. The dataset includes multiple features for different types of beans, facilitating the evaluation of classification model performance on a multi-class dataset.

## Tasks
1. **Data Loading and Preprocessing**: 
   - Load the data into a Python Jupyter Notebook.
   - Conduct exploratory data analysis (EDA) for insights into the features.

2. **Model Training and Evaluation**:
   - Test the following classifiers:
     - k-Nearest Neighbour
     - Decision Tree
     - Logistic Regression
     - Random Forest
   - Evaluation criteria:
     - **Accuracy, Precision, Recall**
     - **Confusion Matrices** for all models to visualize performance on each class.

3. **Addressing the Poisonous ‘Sira’ Class**:
   - Adjust model performance to prioritize the detection of the ‘Sira’ bean type, given its hypothetical poisonous nature.
   - Use **cost-sensitive learning techniques** to improve sensitivity on the ‘Sira’ class, specifically testing the `class_weight` parameter in `RandomForestClassifier` and exploring the **imbalanced-learn** library.
   - Evaluation metrics and approach:
     - Prioritise **Recall** for the ‘Sira’ class to minimise false negatives.
     - Implement techniques for improving classification without significantly affecting other classes.

4. **Results Discussion**:
   - Analyse and compare model performance across metrics.
   - Discuss adjustments made to enhance ‘Sira’ classification.

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/UCI-Dry-Bean-Classifier.git
   ```
2. Install necessary libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook to follow the project steps and observe the results.

## Libraries Used
- **pandas**: For data loading and preprocessing
- **scikit-learn**: Model implementation and metrics
- **imbalanced-learn**: Techniques for handling imbalanced datasets, specifically `class_weight` adjustments
- **matplotlib**: For visualising results, such as confusion matrices

## Results
Summarise key findings:
- Performance metrics for each model (accuracy, precision, recall).
- Confusion matrices to visualise classification results per bean type.
- Analysis of the adjustments made to enhance the recall for the ‘Sira’ bean.

## Contributing
Feel free to fork this project and make pull requests. Contributions that improve model performance, provide new visualisations, or enhance analysis are welcome!

---

### Additional Files
- **requirements.txt**: Include all dependencies (`pandas`, `scikit-learn`, `imbalanced-learn`, `matplotlib`).
- **LICENSE**: Add a licence file if required (e.g., MIT License).
- **notebook.ipynb**: Your main Jupyter Notebook with code, markdown explanations, and visualisations.
