# Module 12 Report Template

## Overview of the Analysis

This model classifies loans into high and low risk, using a supervised training dataset.

The factors that go into the classfication are: 
* loan size
* interest rate
* borrower income
* debt to income ratio
* number of accounts
* derogatory marks - indications of previous times a loan was not repaid as scheduled. 
* total debt

The prediction was based on previous (presumably human) classification of high- or low-risk loan status in 77536 previous loans.

In this analysis we split the dataset into X and y testing and training sets. The training dataset was used to fit a logistric regression classification model. The testing X dataset was used to generate predictions from the fit model. These predictions were used ina  confusion matrix and classifcation report (precision, recall, f1-score) to assess the the model performance.

## Results

* Logistic Regression Model:
    * **Accuracy** - Accuracy is 99%, indicating a very good overall classification score.
	* **Precision** 
		- Precision in low-risk loan classifcation (0) was extremely good. The model classified very few high-risk loans (1) as low-risk. 
		- Precision in high-risk loans was lower than in low risk loans. This indicates the model classified some low-risk loans as high risk.
	* **Recall** - The recall in both cases was quite good. In low risk loans it was 99%, and in high-risk it was 94%. 
	* **Support Score** - The support score for high-risk loan classifcation is rather low compared to the size of the dataset, indicating that the precision and recall being moderately lower than the low-risk classifications is not unexpected.

## Summary

This model serves the purpose of classifying loans well. It prefers to classify high-risk loans, which is desireable from a business standpoint. Low risk loans do not see more attention given to them, and therefore a high-risk loan classified as low-risk could result in a missed opportunity to address the risk.

High-risk loans are given more attention to see if there is a risk-mitigation measure that can be implemented. A low-risk loan classified as high-risk, can be quicky reclassifed at no additional risk, and little addtional spending.