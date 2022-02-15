# Credit Risk Analysis
## Overview
In this analysis, the efficacy of machine learning methods were explored via Jupyter Notebook. The data set used was a credit card credit dataset from LendingClub, a peer-to-peer lending services company. The machine learning programs used 95 factors to predict the status of a loan. For the grading metric we looked specifically at the balanced accuracy, precision, and recall scores.

## Results
### Naive Random Oversampling
- Balanced Accuracy Score: 0.6573
- Precision Scores
    - High Risk: 0.01
    - Low Risk: 1.00
- Recall Scores
    - High Risk: 0.71
    - Low Risk: 0.60

![NaiveRandomOversamplingReport.PNG](/Screenshots/NaiveRandomOversamplingReport.PNG)

Figure 1. Naive Random Oversampling Report

### SMOTE Oversampling
- Balanced Accuracy Score: 0.6622
- Precision Scores
    - High Risk: 0.01
    - Low Risk: 1.00
- Recall Scores
    - High Risk: 0.63
    - Low Risk: 0.69

![SMOTEOversamplingReport.PNG](/Screenshots/SMOTEOversamplingReport.PNG)

Figure 2. SMOTE Oversampling Report

### Undersampling
- Balanced Accuracy Score: 0.5443
- Precision Scores
    - High Risk: 0.01
    - Low Risk: 1.00
- Recall Scores
    - High Risk: 0.69
    - Low Risk: 0.40

![UndersamplingReport.PNG](/Screenshots/UndersamplingReport.PNG)

Figure 3. Undersampling Report

### SMOTEENN Combined Oversampling and Undersampling
- Balanced Accuracy Score: 0.6876
- Precision Scores
    - High Risk: 0.01
    - Low Risk: 1.00
- Recall Scores
    - High Risk: 0.80
    - Low Risk: 0.57

![SMOTEENNCombinedReport.PNG](/Screenshots/SMOTEENNCombinedReport.PNG)

Figure 4. SMOTEENN Combined Oversampling and Undersampling Report

### Balanced Random Forest Classifier
- Balanced Accuracy Score: 0.6830
- Precision Scores
    - High Risk: 0.88
    - Low Risk: 1.00
- Recall Scores
    - High Risk: 0.37
    - Low Risk: 1.00

![BalancedRandomForestClassifierReport.PNG](/Screenshots/BalancedRandomForestClassifierReport.PNG)

Figure 5. Balanced Random Forest Classifier Report

### Easy Ensemble AdaBoost Classifier
- Balanced Accuracy Score: 0.9317
- Precision Scores
    - High Risk: 0.09
    - Low Risk: 1.00
- Recall Scores
    - High Risk: 0.92
    - Low Risk: 0.94

![EasyEnsembleAdaBoostClassifierReport.PNG](/Screenshots/EasyEnsembleAdaBoostClassifierReport.PNG)

Figure 6. Easy Ensemble AdaBoost Classifier Report

## Summary
### Naive Random Oversampling
This machine learning method had middling results in most categories compared to the other methods. The High Risk Recall Score is better than most but the Low Risk Recall Score is not great. 

### SMOTE Oversampling
This machine learning method had middling results in most categories compared to the other methods. The Low Risk Recall Score is better than most but the High Risk Recall Score is not great.  

### Undersampling
This machine learning method had middling results in most categories compared to the other methods. The Low Risk Recall Score and Balanced Accuracy Score the worst of all methods.

### SMOTEENN Combined Oversampling and Undersampling
This machine learning method had middling results in precision, the second worst Low Risk Recall Scores, but the second best High Risk Recall Score and Balanced Accuracy Score.

### Balanced Random Forest Classifier
This machine learning method had middling Balanced Accuracy Score, the best High Risk Precision Score by a wide margin, the best Low Risk Recall Score, and the worst High Risk Recall Score.

### Easy Ensemble AdaBoost Classifier
This machine learning method had the best Balanced Accuracy Score, the second best High Risk Precision Score, the best High Risk Recall Score, and the second best Low Risk Recall Score.

### Conclusions
The single most important score is the High Risk Recall Score. This is because if a loan is bad but the loaner thinks it is good, then the loaner doesn't make their money back. If the loaner thinks a loan is bad but it is actually good, the loaner does not make any money, but they do not lose any either. I would recommend using the Easy Ensemble AdaBoost Classifier because it performed in the top two of every category (except Low Risk Precision Score because all methods achieved 1.00).
