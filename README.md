<h1>FastLending</h1>
<h2>Overview</h2>
<p>FastLending, a peer-to-peer lender, is looking to implement machine learning to assess credit risk.  In order to determine an appropriate model credit card data from the LendingClub, another peer-to-peer lending services company, was used to evaluate the performance of various machine learning models.  Following the detailed analysis is a recommendation on whether these models should be used to predict credit risk.</p>
<h2>Results</h2>
<h3>Understanding of Information Presented</h3>
<h4>Balanced Accuracy Score</h4>
<p>The balance accuracy score is the average of specificity and sensitivity with a score of 1.0 being the highest and 0 being the lowest.  Note the specificity refers to the negatives which were predicted as negative; true negatives, whereas, sensitivity refers to the actual positives which were predicted as positives; true positives.</p>
<h4>Confusion Matrix</h4>
<p>The confusion matrix provides the count of true positives, false negatives, false positives, and true negatives which can then be used to calculate precision and sensitivity.  Precision, also known as positive predicted values, is equal to the true positives divided by the sum of the true positives and false positives (Precision = TP/(TP + FP)) and is a measure of how reliable a positive classification is.  Sensitivity, also known as recall, is the ability of the classifier to find all the positive samples and is equal to the true positives divided by the sum of true positives and false negatives (Sensitivity = TP/(TP + FN)).  The importance placed on either prevision or sensitivity is dependent on the situation for which the methodology is being applied.  For example, in looking at a medical diagnosis a high sensitivity is likely more important than prevision as it is best in this instance to detect everyone with the medical condition rather than miss those that may have the condition.  Ideally there is a balance between prevision and sensitivity in the methodology used.</p>
<h4>Classification Report</h4>
<p>The classification report provides the precision and sensitivity scores as well as the F1 score which is a summary statistic of precision and sensitivity (2(Prevision x Sensitivity)/(Precision + Sensitivity)).  Where a precision score is low it is indicative of a large number of false positives, whereas a low recall is indicative of a large number of false negatives.   The F1 is a weighted average of the two with 1 being the highest and 0 being the lowest.  Note that to the extent that there is a pronounced imbalance between sensitivity and prevision the calculation will yield a low F1 score. </p>
<h3>Resampling Techniques</h3>
<p>There are a number of resampling techniques available all of which attempt to address class imbalance.  Class imbalance refers to a dataset in which the classes are not equally presented.  As an example, the dataset may contain a greater number of instances with low credit risk than high credit risk.</p>
<h4>Naïve Random Oversampling</h4>
<p>In naïve random oversampling instances of the minority class are randomly selected and added to the training set until both classes, majority, and minority, are balanced.  The results using this model are reflected below.</p>
<ul>
<li>Balanced Accuracy Score = 66.03%.</li>
<li>High Risk Precision = 0.1</li>
<li>Low Risk Precision = 1</li>
<li>High Risk Recall = .74</li>
<li>Low Risk Recall = .58</li>
<li>Average F1 = .73</li>
</ul>
<img scr="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Oversampling_summary.png">
<h4>SMOTE</h4>
<p>SMOTE refers to synthetic minority oversampling and is another oversamping technique to address imbalanced datasets.  Similar to random oversampling the size of the minority class if increased to reach balance.  However, unlike random sampling, new instances of the minority set are interpolated.  What this means is that for an instance from the minority class a number of its closest neighbors is chosen.  Based on these neighboring values, new values are created.  Given that these synthetic values are based on neighbors of an instance from the minority class the model is vulnerable to outliers as the synthetic values will reflect this.</p>
<ul>
<li>Balance Accuracy Score = 65.37%</li>
<li>High Risk Precision = .01</li>
<li>Low Risk Precision = 1</li>
<li>High Risk Recall = .62</li>
<li>Low Risk Recall = .68</li>
<li>Average F1 = .81</li>
</ul>
<img scr=”https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/SMOTE_Summary.png">
<h4>Cluster Centroid Undersampling</h4>
<p>Cluster centroid undersampling, unlike the previous two techniques, uses undersampling rather than oversampling to address class imbalance.  In this case the majority class is decreased rather than the minority class increase to obtain balance.</p>
<ul>
<li>Balanced Accuracy Score = 54.38%</li>
<li>High Risk Precision = .01</li>
<li>Low Risk Precision = 1</li>
<li>High Risk Recall = .69</li>
<li>Low Risk Recall = .39</li>
<li>Average F1 = .56</li>
</ul>
<img scr="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Undersmapling_Summary.png">
<h4>SMOTEEN</h4>
<p>SMOTEEN is a combination of oversampling using SMOTE and undersampling using Edited Nearest Neighbors (ENN).  First the minority class is oversampled with SMOTE.  The resulting data is then cleaned with the edited nearest neighbor where if two nearest neighbors of a data point belong to two different classes that data point is dropped.</p>
<ul>
<li>Balanced Accuracy Score = 68.08%</li>
<li>High Risk Precision = .01</li>
<li>Low Risk Precision = 1</li>
<li>High Risk Recall = .77</li>
<li>Low Risk Recall = .59</li>
<li>Average F1 = .55</li>
</ul>
<img scr="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Combination_Summary.png">

<h3>Ensemble Learners Techniques</h3>
<p>Ensemble learner techniques combine multiple models to help improve the accuracy and robustness, as well as decrease variance of the model, all of which increase the overall performance of a model.  Where an ensemble learner technique is used the final prediction is based on the accumulated predictions from each algorithm.<p>
<h4>Balance Random Forest Classifier</h4>
<p>A random forest algorithm samples the data and builds several smaller, simpler decision trees. These simpler decision trees are built from a random subset of features and due to this fact are considered weak learners as these decision trees are based on only a small portion of the data.  However, these small decision trees can be combined to create a strong learner as all of the weak learners are trained on different pieces of the data.  An additional benefit of the balanced random forest classifier is the ability to rank the importance of features which allows us to see which features have the most impact on a decision.  This ranking can then be used to drop features which will improve the performance of the model.</p>
<ul>
<li>Balanced Accuracy Score = 78.85%</li>
<li>High Risk Precision = .03</li>
<li>Low Risk Precision = 1</li>
<li>High Risk Recall = .7</li>
<li>Low Risk Recall = .87</li>
<li>Average F1 = .93</li>
</ul>
<img scr="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Random_Forest_Summary.png">

<h4>Easy Ensemble AdaBoost Classifier</h4>
<p>When an AdaBoost Classifier is used a model is trained and then evaluated.  Once the errors of the first model are evaluated another model is trained, however, extra weight is given to the errors from the previous model.  This weighting is used to minimize similar errors in subsequent models.  This process continues until the error rate is minimized.</p>
<ul>
<li>Balanced Accuracy Score = 93.17%</li>
<li>High Risk Precision = .09</li>
<li>Low Risk Precision = 1</li>
<li>High Risk Recall = .92</li>
<li>Low Risk Recall = .94</li>
<li>Average F1 = .97</li>
</ul>
<img scr="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/AdaBoost_Summary.png">
<h2>Summary</h2>
<p>In reviewing the results the ensemble learner techniques outperformed the random sampling techniques with the Easy Ensemble AdaBoost Classifier achieving a balanced accuracy score of 93.17% whereas the highest score using a random sampling technique was 69.08% using the SMOOTEEN model.    The poorest performing model was Cluster Centroid Undersampling with a balanced accuracy score of 54.39%.</p>
<p>Although the Easy Ensemble AdaBoost Classifier model obtained the highest scores we must look at the scores themselves to determine if in fact this model should be recommended for use.  As noted previously precision tells us how reliable a positive classification is.  In this case it is .09 reliable for high-risk instances and 1.0 reliable for low-risk instances.  On the other hand, recall tells us the ability of the classifier to find all the positive samples which in this case is .92 for high-risk instances and .94 for low-risk instances; a difference of .02.  Lastly, we look at the F1 value which is .16 for high risk and .97 for low-risk instances.   Based on these scores I would recommend the model for prediction of credit risk; although there are a significant number of low risk instances which were predicted by the model as high risk the number of instances that were predicted as low risk which were in fact high risk were minimal.<p>
<p>Based on the models recall scores, balanced accuracy score and average F1 I would recommend the model for prediction of credit risk.</p>



