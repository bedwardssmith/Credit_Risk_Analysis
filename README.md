<h1>FastLending</h1>
<h2>Overview</h2>
<p>FastLending, a peer to peer lender, is looking to implement machine learning to assess credit card risk.  This following analysis includes various models using the credit card credit dataset from LendingClub; another peer-to-peer lending services company.</p>
<h2>Results</h2>
<p>Various models were used for which the performance of each is evaluated below.  In order to understand the results I have provided an explanation of each of the metrics reviewed.</p>
<h4>Balanced Accuracy Score</h4>
<p>The balanced accuracy score is the average of specificity and sensitivity with a score of 1.0 being the highest and 0 being the lowest.  Note that specificity refers to the negatives which were predicted as negative; true negatives.  wherease sensitivity, also referred to as recall, refers to the actual positivies which were predicted as positives; true positivies.   </p>
<h4>Confusion Matrix</h4>
<p>The confusion matrix shows the number of correct and incorrect predictions made by a classifier.  In other words it tells us the number of true positives and false positives.</p>  
<h4>Classification Schedule</h4>
<p>The classification schedule includes the F1 score amongst other information.  F1 is the harmonic average of precision and recall and is calculated as 2(Precision x Sensitivity)/(Precision + Sensitivity).  Sensitivity is the number of true positivies divided by the sum of true positives plus false negatives, wherease, precision is calculated by dividing true positivies by the sum of true positivies and false positives.  The importance of sensitivity versus precision is dependent on the situation.  For example when screening for critical illness a high sensitivity is more important than precision, whereas, in our case it is greater importance would be placed on precision.</p>

<h3>Resampling Techniques</h3>
<p>The intent of resampling is to improve a models performance.  Although there are a number of techniques available the ones covered in this analysis include Naive Random Oversampling, SMOTE, Cluster Centroid Undersampling and SMOTEENN.  Each are described below.
    
<h4>Naive Random Oversampling</h4>
<p>Oversampling is used where one class has too few instances in the training set, therefore, we choose more instances from that class for training.  In random oversampling, instances of the minority class are randomly selected and added to the training set.  This is done until the majority and minority classes are balanced.<p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .6601 using naive random oversampling.</li>
<li>Confusion Matrix - The confusion matrix shows us that there were 70 true positives and 31 false negatives, whereas, there were 10,352 false positives and 6,752 true negatives.</li>
<li>Imbalanced Classification Report - The imbalanced classification report tells us that the precision, reliability of a positive classification, is %1 for high risk and %100 for low risk.  The recall values, tells us that the model predicted high risk 74% of the time while only predicting low risk 58% of the time.  The F1 score of 2% for high risk and 73% for low risk attempts to combine precision and recall.</li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Oversampling_summary.png">

<h4>Smote</h4>
<p>SMOTE, which refers to synthetic minority oversampling technique, once again increases the size of the minority class.  However, new instancesa are interpolated rather than randomly selected as in the previous technique.  SMOTE relies on the concept of nearest neighbors to create synthetic samples from the minority class.</p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .654</li>
<li>Confusion Matrix - The confusion matrix shows us that there were 63 true positivies and 38 false negatives, whereas, there were 5,410 false postivies and 11,694 true negatives. </li>
<li>Imbalanced Classification Report - The imbalanced classification report tells us that the prevision, reliability of a positivie classification, is 1% of the time for high risk and %100 for low risk.  The recall values tells us that the model predicted high risk correctly 62% of the time while predicting low risk correctly 68% of the time.  The F1 score of 2% for high risk and 81% for low risk attempts to combine precision and recall.</li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/SMOTE_Summary.png">



<h4>Cluster Centroid Undersampling</h4>
<p>The next technique used was cluster centroid undersampling.  In this method the algorithm identifies clusters of the majority class.  Synthetic data points are then generated that are representative of the clusers.  Unlike oversampling the majority class is undersampled down to the size of the minority class</p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .6453 WHICH MEANS</li>
<li>Confusion Matrix - The confusion matrix TELLS US </li>
<li>Imbalanced Classification Report - The imbalanced classification report TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Undersmapling_Summary.png">

<h4>SMOTEENN</h4>
<p>SMOTEENN was used as the next technizue.  SMOTEENN combines SMOTE and Edited Nearest Neighbors algorithms.  First it oversamples the minority class using SMOTE and then cleans the resulting data with an undersampling strategy.</p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .6453 WHICH MEANS</li>
<li>Confusion Matrix - The confusion matrix TELLS US </li>
<li>Imbalanced Classification Report - The imbalanced classification report TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Combination_Summary.png">

<h3>Ensemble Learners Techniques</h3>

<h4>Balanced Random Forest Classifier</h4>
<p>A balanced random forest algorithim samples the data and builds several small, simpler decision trees in comparison to the more complex trees created by the decision tree method.  The trees are simpler as they are built from a random set of features.  Each if these simple trees are weak learners as NNNNNNN</p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .6453 WHICH MEANS</li>
<li>Confusion Matrix - The confusion matrix TELLS US </li>
<li>Imbalanced Classification Report - The imbalanced classification report TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Random_Forest_Summary.png">
                                                                                                                             
<h4>AdaBoost Classifier</h4>
<p>AdaBoostClassifier was the next technique.  NEED TO ADD IN FURTHER DETAIL</p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .6453 WHICH MEANS</li>
<li>Confusion Matrix - The confusion matrix TELLS US </li>
<li>Imbalanced Classification Report - The imbalanced classification report TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/AdaBoost_Summary.png">                                                                                                                           
