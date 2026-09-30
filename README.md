Montessori-Management:                                                                                                                   
 1. Dataset and Problem

This project uses a simple Montessori student management dataset containing information about students such as age, gender, attendance, Mathematics score, Reading score, Practical Life score, Social Skill score, and Concentration score. The dataset is designed to analyze student performance and predict the overall performance category of a student.

The main problem is to use student academic and developmental information to predict whether a student's performance is **Poor, Average, Good, or Excellent.

2. Data Loading and Exploration

The dataset was created and loaded using the Python Pandas library. The structure of the dataset was examined using head(), info(), describe(), and shape checking. Missing values, duplicate records, and numerical values were also checked.

Exploratory Data Analysis was performed using graphs such as performance distribution, overall score distribution, and attendance versus overall score. These visualizations help understand student performance and identify patterns in the dataset.

 3. Data Cleaning

Data cleaning was performed to improve the quality of the dataset. Missing values were identified and replaced using the median for numerical columns. Negative values were treated as invalid and replaced with missing values before filling them. Duplicate records were removed.

Outliers and invalid values in Age, Attendance, and student scores were also checked and corrected. Scores were kept within the valid range of 0 to 100, while Attendance was restricted to a maximum of 100.

 4. Feature Engineering

A new feature called Development_Score was created using Practical Life, Social Skill, and Concentration scores. This feature represents the student's overall developmental performance.

An Attendance_Category was also created by grouping attendance into Low, Average, and High categories.

The main features used for machine learning were Attendance, Math Score, Reading Score, Practical Life, Social Skill, Concentration, and Development Score.

 5. Machine Learning

Since the target variable contains categories such as Poor, Average, Good, and Excellent, this project uses classification.

Two machine-learning models were trained:

. Logistic Regression
.Random Forest Classifier

The data was divided into training and testing sets. StandardScaler was used for scaling where required.

Text vectorization was not required because the selected machine-learning features were numerical.

 6. Validation and Comparison

The models were evaluated using accuracy and a classification report. A confusion matrix was also used to examine correct and incorrect predictions for each performance category.

Five-fold cross-validation was performed to check the consistency of the model.

The actual accuracy values are obtained when the notebook is executed. The two models can then be compared using the generated accuracy table and graph.

7. Model Saving and Prototype

The trained Random Forest model was saved using the Joblib library as:
montessori_management_model.pkl

The saved model was loaded again and used to create a prediction function. A simple Gradio GUI was also developed. The user can enter a student's attendance, academic scores, Practical Life, Social Skill, and Concentration scores, and the system predicts the student's performance category.

8. Key Findings

The project demonstrates how student academic and developmental information can be analyzed using machine learning. Attendance and student scores provide useful information for understanding overall performance, while the Development Score combines important Montessori-related developmental areas.

The system can help organize student information, analyze performance patterns, and provide a simple performance prediction. However, the prediction should be considered a supporting tool, while teachers' observations and professional judgment remain important in Montessori student management.
