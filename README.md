<h1>FastLending</h1>
<h2>Overview</h2>
<p>FastLending, a peer to peer lender, is looking to implement machine learning to credit card risk.  This analysis includes various models using the credit card credit dataset from LendingClub another peer-to-peer lending services company.</p>
<h2>Results</h2>
<p>Various models were used for which the performance of each is evaluated below.  In order to understand the results I have provided an explanation of each of the metrics reviewed.</p>
<h4>Balance Accuracy Score</h4>
<p>The balanced accuracy score is the average of specificity and sensitivity.  A score of 1.0 is the highest with 0 being the lowest.</p>
<h4>Confusion Matrix</h4>
<p>The confusion matrix shows the number of correct and incorrect predictions made by a classifier.  In other words it tells us the number of true positives and false positives.</p>  
<h4>Classification Schedule</h4>
<p>The classification schedule includes the F1 score amongst other information.  F1 is the harmonic average of precision and recall and is calculated as 2(Precision x Sensitivity)/(Precision + Sensitivity).  Sensitivity is the number of true positivies divided by the sum of true positives plus false negatives, wherease, precision is calculated by dividing true positivies by the sum of true positivies and false positives.  There is a tradeoff between precision and sensitivity with some situations where sensitivity is more important.</p>
<h3>Resampling Techniques</h3>
<h4>Naive Random Oversampling</h4>
<p>Oversampling is used where one class has too few instances in the training set, therefore, we choose more instances from that class for training.  In random oversampling, instances of the minority class are randomly selected and added to the training set.  This is done until the majority and minority classes are balanced.<p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .6601 WHICH MEANS</li>
<li>Confusion Matrix - The confusion matrix provides an F1 score of .6 </li>
<li>Imbalanced Classification Report - The imbalanced classification report provides an F1 score of .73. </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Oversampling_summary.png">

<h4>Smote</h4>
<p>SMOTE Oversampling was the second technique used.  SMOTE, which refers to synthetic minority oversampling technique, once again increases the size of the minority class.  However, new instancesa re interpolated rather than randomly selected as in the previous technique.  In SMOTE for an instance from the minority class a number of its closest neighbors is chosen.  Based on these values new values are created.</p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .6453 WHICH MEANS</li>
<li>Confusion Matrix - The confusion matrix TELLS US </li>
<li>Imbalanced Classification Report - The imbalanced classification report TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/SMOTE_Summary.png">

<h4>Cluser Centroid Undersampling</h4>
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
