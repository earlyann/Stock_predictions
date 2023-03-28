## Stock Predictions: Enhancing Investment Strategies

### Project Overview
I sought to elevate my investments by developing a project that predicted annual stock returns using and comparing a Support Vector Machine (SVM) model, a Balanced Random Forest Model, and an Easy Ensemble model based on stock-picking concept weights. My aim was to refine traditional models and tailor weighting combinations to cater to diverse investor preferences.

### Models
Support Vector Machine (SVM) model: This supervised machine learning algorithm classifies stocks based on their potential for positive or negative annual returns. The algorithm identifies the optimal hyperplane that separates data points for these two categories.

Balanced Random Forest Model: A variant of the Random Forest model, this model balances class weights to handle imbalanced datasets more effectively.

Easy Ensemble model: This ensemble learning method combines multiple base classifiers to improve prediction performance. It focuses on resampling the dataset to balance class distribution.

### Technologies:
Python
Pandas: Data manipulation
Scikit-learn: SVM model training and evaluation
Imbalanced-learn: Balanced Random Forest and Easy Ensemble model training and evaluation
Matplotlib: Data visualization

### Methods:
- Data collection and preprocessing: I obtained and preprocessed a dataset from the UCI Machine Learning Repository.
- Feature engineering: I created SVM model inputs from the dataset, representing stock-picking concept weights.
- Model training: I trained the SVM, Balanced Random Forest, and Easy Ensemble models using scikit-learn and imbalanced-learn libraries.
- Model evaluation: I assessed performance using accuracy, precision, and recall metrics.

### Project Description

I utilized a dataset containing historical US stock market data and stock-picking concept weights from a weighted scoring stock selection model to predict stocks' annual returns.

Visualizing the data in pair plots allowed me to see the relationship between the concepts. The diagonal plots were histograms of each feature. The most notable observation was the scarcity of negative annual results. This prompted me to fine-tune each model to successfully predict instances of the minority class (negative annual results).

![Screen Shot 2023-03-28 at 1 24 41 PM](https://user-images.githubusercontent.com/119711479/228333578-81031976-d88e-47b0-a92e-c67ba026b3f5.png)

Each model input (X1-X6) represented weights of Large B/P, Large ROE, Large S/P, Large Return Rate in the last quarter, Large Market Value, and Small Systematic Risk concepts. The output was a binary label indicating positive or negative annual return based on a 0.0 threshold. Higher weights implied stronger emphasis on the corresponding concept. Each model learned the relationship between stock-picking concept weights (X1-X6) and the binary label to make predictions. Once trained, each model predicted annual returns based on concept weights.

![Screen Shot 2023-03-28 at 1 23 13 PM](https://user-images.githubusercontent.com/119711479/228333905-53230cc8-ff5c-41b8-87f3-01f1db1c86ec.png)
![Screen Shot 2023-03-28 at 1 24 00 PM](https://user-images.githubusercontent.com/119711479/228333930-1a3dd474-15d6-4acc-9045-af47ef8eca4b.png)

### Model Performance
I present the accuracy, precision, recall, and f1-score for each model:

#### Support Vector Machine (SVM):
Accuracy: 1.0
Precision: 1.00
Recall: 1.00
F1-score: 1.00

#### Balanced Random Forest (BRF):
Accuracy: 1.0
Precision: 1.00
Recall: 1.00
F1-score: 1.00

#### Easy Ensemble (EE):
Accuracy: 1.0
Precision: 1.00
Recall: 1.00
F1-score: 1.00

#### Prediction Function
I developed a function that takes one of my predefined models (SVM, BRF, or EE) and a set of X1-X6 data and predicts whether that set of data will yield a positive or negative annual result. The model parameter in the function accepts any model that has a predict method, which is true for most machine learning models in scikit-learn and imbalanced-learn. I was able to pass my previously defined models svm_best_model, brf_best_model, or ee_best_model as the first argument to the function, and it used the respective model for making predictions. This made it easy to test and implement different models within my framework and offered flexibility for users to explore other machine learning models that fit their specific needs.

### Conclusion
My project successfully demonstrated the application of three machine learning models - Support Vector Machine, Balanced Random Forest, and Easy Ensemble - for predicting positive or negative annual returns based on stock-picking concept weights. Each model showed excellent performance in terms of accuracy, precision, recall, and f1-score, emphasizing the potential for machine learning to enhance investment strategies.

By comparing the strengths of these models, I realized that investors can choose the most suitable approach to guide their investment decisions, optimizing their portfolio based on their preferences and risk tolerance.

I also provided a flexible prediction function, compatible with various machine learning models, making it easy for users to test and implement different models within my framework.

In the future, I could explore predicting other investment performance indicators (Y2-Y6) and using an epsilon-SVR model for continuous value predictions. Additionally, incorporating more diverse datasets and exploring feature importance could further enhance the model's performance and provide deeper insights into the stock-picking process.
