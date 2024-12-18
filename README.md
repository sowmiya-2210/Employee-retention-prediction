# Employee-retention-prediction
HR Analytics
  

## Overview  
This project leverages machine learning to predict employee retention and job change tendencies, enabling organizations to optimize talent retention strategies. By analyzing employee data, the model identifies key factors contributing to job changes and provides actionable insights for Human Resources teams.  

## Objectives  
- Predict whether an employee is likely to change jobs.  
- Identify key drivers of employee attrition using statistical and machine learning techniques.  
- Provide recommendations to HR for reducing turnover and improving employee engagement.  

## Dataset  
- **Size**: 19,158 records.  
- **Target Variable**: `Target`  
  - `0`: Employee is not looking for a job change.  
  - `1`: Employee is looking for a job change.  
- **Features**: Includes both numerical and categorical variables such as city development index, training hours, education level, experience, and company size.  

## Data Preprocessing  
1. **Missing Values**:  
   - Imputed numerical features using mean/median.  
   - Filled categorical features with the most frequent value or "Unknown".  
2. **Outliers**:  
   - Detected using statistical methods like Interquartile Range (IQR).  
   - Treated outliers using capping and log transformations.  
3. **Class Imbalance**:  
   - Handled using **SMOTE** (Synthetic Minority Over-sampling Technique).  
4. **Encoding**:  
   - **Label Encoding** for ordinal data (e.g., education levels).  
   - **One-Hot Encoding** for nominal data (e.g., city).  
5. **Standardization**:  
   - Applied standard scaling to ensure features have a mean of 0 and a standard deviation of 1.  

## Statistical Insights  
- Conducted ANOVA and Chi-Square tests to identify relationships between features and job change tendencies:  
  - **Significant Predictors**:  
    - `City Development Index`  
    - `Training Hours`  
    - `Education Level`  
    - `Experience`  
    - `Company Size`  
    - `Relevant Experience`  

## Model Building  
### Algorithms Evaluated:  
1. Random Forest Classifier (Best Performer)  
2. Logistic Regression  
3. K-Nearest Neighbors (KNN)  
4. Gaussian Naive Bayes  
5. XGBoost  

### Why Random Forest?  
- Robust against outliers and noise.  
- Effectively handled class imbalance using `class_weight='balanced'` and SMOTE.  
- Achieved the highest accuracy and ROC-AUC scores.  

### Evaluation Metrics:  
- **Accuracy**: 80%  
- **ROC-AUC**: 80%  
- **Precision**: 81%  
- **Recall**: 80%  
- **F1-Score**: 80%  

## Key Results  
- Random Forest outperformed other models with superior generalization on unseen test data.  
- Test dataset: 2,129 rows (preprocessed and transformed like training data).  
- Confusion Matrix:  
  - True Negatives: 2430  
  - False Positives: 450  
  - False Negatives: 332  
  - True Positives: 620  

## Business Impact  
- **Cost Savings**: Retaining employees saves 50%-200% of their annual salary.  
- **Improved Workforce Planning**: Predictive insights enable better hiring, training, and retention strategies.  
- **Increased Engagement**: Addressing attrition drivers fosters productivity and morale.  
- **Enhanced Competitive Edge**: Reducing turnover ensures continuity and reduces disruptions.  

## Recommendations  
### Employee Retention Strategies: Cultivating a Robust and Sustainable Team 🔍  

Discover effective tactics to retain top talent and nurture a culture of loyalty and engagement within your company.  

✅ **Continuous Professional Development** 📚 *Invest in Growth*  
Empower employees with continual learning opportunities and skill enhancement through tailored training, workshops, and mentorship programs.  
**Benefits**: Enhanced job satisfaction, heightened employee engagement, and improved retention rates.  

✅ **Recognition & Rewards** 🏆 *Celebrate Achievements*  
Acknowledge and reward employees for their dedication, accomplishments, and contributions using initiatives like "Employee of the Month" and peer-to-peer recognition platforms.  
**Benefits**: Elevated morale, increased motivation, and strengthened team cohesion.  

✅ **Positive Work Environment** 🌈 *Foster Collaboration and Well-being*  
Cultivate an inclusive and supportive workplace that prioritizes open communication, teamwork, and a healthy work-life balance.  
**Benefits**: Elevated employee satisfaction, heightened productivity, and reduced turnover.  

✅ **Retain Your Exceptional Talent** ✨ *Promote an Engaging Culture*  
Through robust professional development, meaningful recognition, and a nurturing work environment, organizations can retain top talent and drive sustained success.  


## How to Run  
1. Clone this repository.  
2. Install dependencies:  
   ```bash  
   pip install -r requirements.txt  
   ```  
3. Preprocess the data by running:  
   ```bash  
   python preprocess.py  
   ```  
4. Train and evaluate the model:  
   ```bash  
   python train_model.py  
   ```  
5. Visualize results and insights using:  
   ```bash  
   python visualize_results.py  
   ```  

## Future Work  
- Expand analysis to other roles and industries.  
- Integrate additional external factors like economic indicators.  
- Test other advanced machine learning algorithms like deep learning models.  
