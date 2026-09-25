<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heart Disease Prediction - Machine Learning Project</title>
</head>

<body>

<h1>❤️ Heart Disease Prediction — Machine Learning Project</h1>

<h2>📌 Project Overview</h2>

<p>
This project predicts the presence of heart disease using patient medical data
and Machine Learning classification algorithms.
</p>

<p>The project includes:</p>

<ul>
    <li>Data preprocessing</li>
    <li>Train-test splitting</li>
    <li>Variable transformation using Yeo-Johnson</li>
    <li>Outlier handling using IQR</li>
    <li>Feature selection using Variance Threshold</li>
    <li>Feature scaling using StandardScaler</li>
    <li>Multiple Machine Learning classification models</li>
    <li>Model evaluation</li>
    <li>Model serialization using Pickle</li>
    <li>Flask web application for prediction</li>
    <li>Logging for tracking project execution</li>
</ul>

<hr>

<h2>🎯 Project Objectives</h2>

<ul>
    <li>To preprocess heart disease patient data.</li>
    <li>To identify and handle outliers.</li>
    <li>To transform numerical variables using Yeo-Johnson transformation.</li>
    <li>To remove constant and quasi-constant features.</li>
    <li>To scale numerical features.</li>
    <li>To train multiple classification algorithms.</li>
    <li>To evaluate model performance.</li>
    <li>To save the trained model and scaler.</li>
    <li>To create a Flask web application for prediction.</li>
</ul>

<hr>

<h2>📊 Dataset</h2>

<p>
The project uses a Heart Disease dataset containing patient medical information.
</p>

<h3>Target Variable</h3>

<p><code>target</code></p>

<ul>
    <li><strong>0</strong> → No Heart Disease</li>
    <li><strong>1</strong> → Heart Disease</li>
</ul>

<h3>Dataset Features</h3>

<table border="1" cellpadding="8" cellspacing="0">
    <thead>
        <tr>
            <th>Feature</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr><td><code>age</code></td><td>Age of the patient</td></tr>
        <tr><td><code>sex</code></td><td>Sex of the patient</td></tr>
        <tr><td><code>cp</code></td><td>Chest pain type</td></tr>
        <tr><td><code>trestbps</code></td><td>Resting blood pressure</td></tr>
        <tr><td><code>chol</code></td><td>Cholesterol level</td></tr>
        <tr><td><code>fbs</code></td><td>Fasting blood sugar</td></tr>
        <tr><td><code>restecg</code></td><td>Resting electrocardiographic results</td></tr>
        <tr><td><code>thalach</code></td><td>Maximum heart rate achieved</td></tr>
        <tr><td><code>exang</code></td><td>Exercise-induced angina</td></tr>
        <tr><td><code>oldpeak</code></td><td>ST depression induced by exercise</td></tr>
        <tr><td><code>slope</code></td><td>Slope of the peak exercise ST segment</td></tr>
        <tr><td><code>ca</code></td><td>Number of major vessels</td></tr>
        <tr><td><code>thal</code></td><td>Thalassemia</td></tr>
        <tr><td><code>target</code></td><td>Heart disease prediction</td></tr>
    </tbody>
</table>

<hr>

<h2>🔄 Machine Learning Pipeline</h2>

<pre>
Heart Disease Dataset
        ↓
Load CSV Dataset
        ↓
Check Dataset Shape
        ↓
Check Missing Values
        ↓
Train-Test Split
        ↓
Numerical Data Selection
        ↓
Yeo-Johnson Transformation
        ↓
IQR Outlier Handling
        ↓
Variance Threshold Selection
        ↓
Standard Scaling
        ↓
Multiple Classification Models
        ↓
Model Evaluation
        ↓
Save Model + Scaler
        ↓
Flask Web Application
        ↓
Heart Disease Result
</pre>

<hr>

<h2>🧹 Data Preprocessing</h2>

<h3>1. Train-Test Split</h3>

<p>
The dataset is divided into training and testing datasets.
</p>

<ul>
    <li>80% → Training Data</li>
    <li>20% → Testing Data</li>
</ul>

<pre>
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
</pre>

<h3>2. Variable Transformation</h3>

<p>
Yeo-Johnson transformation is used for numerical variables.
It helps transform the distribution of numerical data and reduce the effect
of skewness.
</p>

<pre>
yeojohnson()
</pre>

<h3>3. Outlier Handling</h3>

<p>
Outliers are handled using the <strong>IQR (Interquartile Range)</strong> method.
</p>

<pre>
IQR = Q3 - Q1

Upper Limit = Q3 + 1.5 × IQR

Lower Limit = Q1 - 1.5 × IQR
</pre>

<p>
Values outside these limits are capped using the calculated upper and lower limits.
</p>

<h3>4. Feature Selection</h3>

<p>
Feature selection is performed using <code>VarianceThreshold</code>.
</p>

<pre>
VarianceThreshold(threshold=0.0)
</pre>

<p>
This removes constant features.
</p>

<pre>
VarianceThreshold(threshold=0.1)
</pre>

<p>
This removes quasi-constant features.
</p>

<h3>5. Feature Scaling</h3>

<p>
StandardScaler is used to scale the numerical features.
</p>

<pre>
Mean = 0
Standard Deviation = 1
</pre>

<hr>

<h2>🤖 Machine Learning Models</h2>

<ul>
    <li>K-Nearest Neighbors</li>
    <li>Gaussian Naive Bayes</li>
    <li>Logistic Regression</li>
    <li>Decision Tree</li>
    <li>Random Forest</li>
    <li>AdaBoost</li>
    <li>Gradient Boosting</li>
    <li>XGBoost</li>
    <li>Support Vector Machine</li>
</ul>

<hr>

<h2>📈 Model Evaluation</h2>

<p>The trained models are evaluated using:</p>

<ul>
    <li>Accuracy</li>
    <li>Confusion Matrix</li>
    <li>Classification Report</li>
    <li>ROC Curve</li>
</ul>

<h3>Accuracy</h3>

<p>
Accuracy measures the percentage of correctly predicted observations.
</p>

<pre>
Accuracy =
Correct Predictions / Total Predictions
</pre>

<h3>Confusion Matrix</h3>

<ul>
    <li>True Positive</li>
    <li>True Negative</li>
    <li>False Positive</li>
    <li>False Negative</li>
</ul>

<h3>Classification Report</h3>

<ul>
    <li>Precision</li>
    <li>Recall</li>
    <li>F1-score</li>
    <li>Support</li>
</ul>

<h3>ROC Curve</h3>

<p>
The ROC curve is used to evaluate classification performance at different
threshold values.
</p>

<hr>

<h2>💾 Model Saving</h2>

<p>
The trained model and scaling object are saved using Pickle.
</p>

<h3>Model</h3>

<p><code>Heart_Disease_Model.pkl</code></p>

<h3>Scaler</h3>

<p><code>scaled_model.pkl</code></p>

<hr>

<h2>🌐 Flask Web Application</h2>

<p>
A Flask web application is created for real-time heart disease prediction.
The application takes patient medical information as input and provides a prediction.
</p>

<pre>
User Input
    ↓
Convert Input to Numerical Values
    ↓
Scale Features
    ↓
Load Machine Learning Model
    ↓
Make Prediction
    ↓
Display Result
</pre>

<hr>

<h2>🖥️ Web Application Features</h2>

<p>The web interface contains input fields for:</p>

<ul>
    <li>Age</li>
    <li>Sex</li>
    <li>Chest Pain Type</li>
    <li>Resting Blood Pressure</li>
    <li>Cholesterol</li>
    <li>Fasting Blood Sugar</li>
    <li>Resting ECG</li>
    <li>Maximum Heart Rate</li>
    <li>Exercise Induced Angina</li>
    <li>Oldpeak</li>
    <li>Slope</li>
    <li>Number of Major Vessels</li>
    <li>Thalassemia</li>
</ul>

<p>
The application displays the prediction result to the user.
</p>

<hr>

<h2>📁 Project Structure</h2>

<pre>
ML_Heartdiseasa/
│
├── heart.csv
│
├── main.py
├── all_models.py
├── fs.py
├── yeo_timing.py
├── log_code.py
├── app.py
│
├── Heart_Disease_Model.pkl
├── scaled_model.pkl
│
├── templates/
│   └── index.html
│
└── logs/
    ├── main.log
    ├── fs.log
    └── yeo_timing.log
</pre>

<hr>

<h2>📄 File Description</h2>

<table border="1" cellpadding="8" cellspacing="0">
    <thead>
        <tr>
            <th>File</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr><td><code>heart.csv</code></td><td>Heart disease dataset</td></tr>
        <tr><td><code>main.py</code></td><td>Main Machine Learning pipeline</td></tr>
        <tr><td><code>all_models.py</code></td><td>Contains classification models</td></tr>
        <tr><td><code>yeo_timing.py</code></td><td>Yeo-Johnson transformation and outlier handling</td></tr>
        <tr><td><code>fs.py</code></td><td>Feature selection</td></tr>
        <tr><td><code>log_code.py</code></td><td>Logging configuration</td></tr>
        <tr><td><code>app.py</code></td><td>Flask application</td></tr>
        <tr><td><code>index.html</code></td><td>Web application interface</td></tr>
        <tr><td><code>Heart_Disease_Model.pkl</code></td><td>Saved Machine Learning model</td></tr>
        <tr><td><code>scaled_model.pkl</code></td><td>Saved StandardScaler</td></tr>
        <tr><td><code>logs/</code></td><td>Stores project execution logs</td></tr>
    </tbody>
</table>

<hr>

<h2>📝 Logging</h2>

<p>
Logging is implemented to track the execution of different stages of the project.
</p>

<p>Example log files:</p>

<ul>
    <li><code>main.log</code></li>
    <li><code>fs.log</code></li>
    <li><code>yeo_timing.log</code></li>
</ul>

<p>The logs contain information such as:</p>

<ul>
    <li>Dataset shape</li>
    <li>Training and testing data size</li>
    <li>Column information</li>
    <li>Feature selection information</li>
    <li>Errors during execution</li>
</ul>

<hr>

<h2>🛠️ Technologies Used</h2>

<h3>Programming Language</h3>
<ul>
    <li>Python</li>
</ul>

<h3>Machine Learning</h3>
<ul>
    <li>Scikit-learn</li>
    <li>XGBoost</li>
</ul>

<h3>Data Processing</h3>
<ul>
    <li>Pandas</li>
    <li>NumPy</li>
    <li>SciPy</li>
</ul>

<h3>Visualization</h3>
<ul>
    <li>Matplotlib</li>
    <li>Seaborn</li>
</ul>

<h3>Web Development</h3>
<ul>
    <li>Flask</li>
    <li>HTML</li>
    <li>CSS</li>
</ul>

<h3>Model Serialization</h3>
<ul>
    <li>Pickle</li>
</ul>

<h3>Development Environment</h3>
<ul>
    <li>VS Code</li>
    <li>Python Virtual Environment</li>
</ul>

<hr>

<h2>📦 Python Libraries</h2>

<pre>
numpy
pandas
scikit-learn
scipy
matplotlib
seaborn
xgboost
flask
</pre>

<hr>

<h2>🧠 Implementation Details</h2>

<p>
The project follows an object-oriented approach in the main Machine Learning pipeline.
</p>

<p>The main class is:</p>

<pre>
HEARTPREDECTION
</pre>

<p>The class handles different stages of the project:</p>

<pre>
Dataset Loading
      ↓
Train-Test Split
      ↓
Data Preprocessing
      ↓
Variable Transformation
      ↓
Feature Selection
      ↓
Model Training
</pre>

<p>
Exception handling is also implemented using <code>try-except</code> blocks.
</p>

<hr>

<h2>🔄 Complete Workflow</h2>

<pre>
1. Load Heart Disease Dataset
            ↓
2. Check Dataset Information
            ↓
3. Separate Independent and Dependent Variables
            ↓
4. Split Data into Training and Testing
            ↓
5. Select Numerical Variables
            ↓
6. Apply Yeo-Johnson Transformation
            ↓
7. Handle Outliers using IQR
            ↓
8. Remove Constant Features
            ↓
9. Remove Quasi-Constant Features
            ↓
10. Apply StandardScaler
            ↓
11. Train Classification Models
            ↓
12. Evaluate Models
            ↓
13. Save Model and Scaler
            ↓
14. Load Model in Flask
            ↓
15. Enter Patient Information
            ↓
16. Predict Heart Disease
</pre>

<hr>

<h2>🎓 Learning Outcomes</h2>

<ul>
    <li>Python programming</li>
    <li>Pandas and NumPy</li>
    <li>Data preprocessing</li>
    <li>Train-test splitting</li>
    <li>Variable transformation</li>
    <li>Yeo-Johnson transformation</li>
    <li>Outlier handling</li>
    <li>IQR method</li>
    <li>Feature selection</li>
    <li>Variance Threshold</li>
    <li>Feature scaling</li>
    <li>Classification algorithms</li>
    <li>Model evaluation</li>
    <li>Confusion matrix</li>
    <li>Classification report</li>
    <li>ROC curve</li>
    <li>Pickle model serialization</li>
    <li>Flask application development</li>
    <li>Logging</li>
    <li>Machine Learning deployment</li>
</ul>

<hr>

<h2>👩‍💻 Author</h2>

<p>
<strong>Anuharika</strong><br>
B.Tech — Computer Science and Engineering (AI & ML)
</p>

<hr>

<h2>⭐ Project Highlights</h2>

<ul>
    <li>End-to-end Machine Learning project</li>
    <li>Multiple classification algorithms</li>
    <li>Yeo-Johnson variable transformation</li>
    <li>IQR-based outlier handling</li>
    <li>Variance Threshold feature selection</li>
    <li>StandardScaler preprocessing</li>
    <li>Model evaluation</li>
    <li>Pickle model saving</li>
    <li>Flask web application</li>
    <li>Logging implementation</li>
    <li>Ready for GitHub and deployment</li>
</ul>

<hr>

<h2>🔗 Project Links</h2>

<table border="1" cellpadding="8" cellspacing="0">
    <thead>
        <tr>
            <th>Resource</th>
            <th>Link</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>GitHub Repository</td>
            <td>https://github.com/anuharika21/</td>
        </tr>
        <tr>
            <td>Live Demo</td>
            <td>https://heart-disease-predection-4.onrender.com</td>
        </tr>
        <tr>
            <td>LinkedIn</td>
            <td>https://www.linkedin.com/in/anuharika/</td>
        </tr>
    </tbody>
</table>

</body>
</html>
