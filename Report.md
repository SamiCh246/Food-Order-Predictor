# Xtern AI Work Sample Assessment Report

## Distributions and Biases

### Exploratory Data Analysis (EDA)

- **Skewed Distributions:** Several variables in the dataset exhibited significant skewness. For example, the 'Year' feature was highly skewed, dominated by years 2 and 3, while the 'Order' (target variable) displayed a relatively uniform distribution. This skewness could impact model performance and requires careful consideration.
- **Categorical Abundance:** The dataset contains a plethora of categorical features, indicating a need for specific preprocessing approaches. This bias towards categorical variables suggests that without data transformation, certain machine learning models may not perform optimally.
- **Visualizations and Findings:** EDA visualizations were generated to gain an in-depth understanding of the feature distributions and their interactions. The visuals offer insights into the relationships between variables, contributing to better model selection and data interpretation.

## Other Potential Use Cases

- **Predicting Spending Habits:** The data could be leveraged to predict the amount of money students are willing to spend on their orders, offering insights into pricing strategies.
- **Food Quantity Estimation:** A predictive model could be developed to estimate the quantity of food (in calories or servings) that students are likely to order, aiding inventory management.
- **Lunchtime Predictions:** The dataset could be harnessed to predict the average time students allocate for lunch based on a multitude of factors, helping in optimizing food truck schedules.

Furthermore, this dataset has the potential to support the creation of a generalized model that predicts a student's desired meal from an extended menu, broadening FoodX's offerings based on predicting factors like desired calories or price.

## Implications of Data Collection, Storage, and Data Biases

### Data Collection and Storage Implications

- **Ethical Considerations:** The data collection process must adhere to ethical guidelines, respecting user privacy, and obtaining necessary consents.
- **Business Requirements:** Efficient data storage and retrieval mechanisms are crucial to handle the growing volume of order data efficiently.
- **Technical Considerations:** The selection of appropriate data storage solutions and stringent data security measures are paramount to protect user data and maintain compliance with data protection regulations.

### Business Outcome Implications

- **Workload Reduction:** Accurate order predictions have the potential to significantly reduce staff workload, enhancing overall operational efficiency.
- **Cost Savings:** By minimizing incorrect order preparations, FoodX can reduce operational costs while offering customers a superior experience.

However, offering a discount to customers when predictions are incorrect could potentially attract more customers. Therefore, it's crucial to evaluate whether the cost of discounts is outweighed by the additional business.

### Technical Implications

- **Data Preprocessing:** Uneven distribution of values in certain variables can lead to overfitting, impacting model generalization. Grouping similar categories or majors is a potential solution to mitigate this issue.
- **Model Scaling:** Depending on data volume and update frequency, the model's storage and complexity could increase over time. Technical solutions should be implemented to accommodate these requirements.

## Model Development

### Model Selection

- **Categorical Features:** Given the abundance of categorical features in the dataset, a variant of random tree/forest classification was considered due to its compatibility with such data.
- **Ensemble Learning:** Random forest models were investigated for their ensemble nature, which often provides robust performance when considering combinations of categorical features.
- **Comparison with Alternative Models:** While various models were assessed, the strong dependence on categorical features led to the underperformance of models like K-nearest neighbors and support vector machines.
- **Decision Tree Classifier:** The decision tree classifier was selected as the final model due to its competitive performance and high interpretability.

### Training and Evaluation

The training process involved extensive data preprocessing to convert categorical features into numerical equivalents. The model's performance was evaluated using standard machine learning metrics, including accuracy, precision, recall, and the F1 score.

## Model Interpretability

Model interpretability is a crucial aspect that ensures transparency in the model's decisions. In the context of FoodX, the interpretability of the model plays a pivotal role in building user and stakeholder trust.

## Considerations for Implementation

- **Cost-Benefit Analysis:** A comprehensive analysis should be conducted to calculate cost savings resulting from the implementation of the model. It is essential to compare the impact of offering a 10% discount to customers for incorrect predictions against not providing the discount. This analysis will help gauge the effectiveness and cost-effectiveness of the model.
- **Benchmarking:** To determine the actual effectiveness of the model, benchmarking against simple strategies, such as guessing the most popular or expensive dish, is recommended. Benchmarking against random guessing reveals that the model's accuracy exceeds a random 1 in 10 chance, indicating the potential benefits of model implementation.
