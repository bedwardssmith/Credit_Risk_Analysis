<h1>FastLending</h1>
<h2>Overview</h2>
<p>FastLending, a peer to peer lender, is looking to implement machine learning to credit card risk.  This analysis includes various models using the credit card credit dataset from LendingClub another peer-to-peer lending services company.</p>
<h2>Results</h2>
<p>Various models were used for which the performance of each was evaluated.</p>
<h3>Resampling Techniques</h3>
<h4>Naive Random Oversampling</h4>
<p>Naive Random Oversampling was the first technique used.  Oversampling is used where one class has too few instances in the training set, therefore, we choose more instances from that class for training.  In random oversampling, instances of the minority class are randomly selected and added to the training set.  This is done until the majority and minority classes are balanced.<p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .6631 WHICH MEANS</li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Random_Oversampling_Balanced_Accuracy_score.png">
<ul>
<li>Confusion Matrix - The confusion matrix TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Random_Oversampling_Conusion_Matrix.png">
<ul>
  <li>Imbalanced Classification Report - The imbalanced classification report TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Random_Oversampling_Classification_Report.png">
<br>
<h4>Smote</h4>
<p>SMOTE Oversampling was the second technique used.  SMOTE, which refers to synthetic minority oversampling technique, once again increases the size of the minority class.  However, new instancesa re interpolated rather than randomly selected as in the previous technique.  In SMOTE for an instance from the minority class a number of its closest neighbors is chosen.  Based on these values new values are created.</p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .6453 WHICH MEANS</li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/SMOTE_Oversampling_Balanced_accuracy_score.png">
<ul>
<li>Confusion Matrix - The confusion matrix TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/SMOTE_Oversampling_Confusion_Matrix.png">
<ul>
<li>Imbalanced Classification Report - The imbalanced classification report TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/SMOTE_Oversampling_Confusion_Matrix.png">
<br>
<hr>Cluser Centroid Undersampling</h4>
<p>The next technique used was cluster centroid undersampling.  In this method the algorithm identifies clusters of the majority class.  Synthetic data points are then generated that are representative of the clusers.  Unlike oversampling the majority class is undersampled down to the size of the minority class</p>
<ul>
<li>Balanced Accuracy Score - The balanced accruacy score is .6453 WHICH MEANS</li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Under_Sampling_Balanced_Accuracy_Score.png">
<ul>
<li>Confusion Matrix - The confusion matrix TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Under_Sampling_Confusion_Matrix.png">
<ul>
<li>Imbalanced Classification Report - The imbalanced classification report TELLS US </li>
</ul>
<img src="https://github.com/bedwardssmith/Credit_Risk_Analysis/blob/main/Images/Under_Sampling_Classification_Report.png">
<br> 
