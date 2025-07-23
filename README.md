# predictive-model-to-improve-the-cost-effectiveness-of-marketing-campaign
a. Logistic Regression  b. Classification Tree  c.   Random Forest  d. Neural Network  e. Linear Discriminant Analysis 

1.	Provide me with a frequency table of donors VS no donors with the average donation for all donors. 
 
The output reveals that the dataset is evenly split between donors and non-donors, with each group comprising 1,560 individuals. This balanced distribution of the target variable (TARGET_B) is ideal for developing a classification model, as it minimizes the risk of bias toward either class. Additionally, the analysis indicates that the average donation amount among individuals who contributed is $13.00, which corresponds with the figure provided in the case study background. Considering that the cost of each fundraising mailing is $0.68, the potential return from accurately identifying donors is substantial.
2.	Drop non-useful columns ['Row Id', 'Row Id.', 'TARGET_D'] 
   
The output confirms that the unnecessary columns ('Row Id', 'Row Id.', and 'TARGET_D') were successfully removed from the dataset.
3.	Partition the dataset into 60% training and 40% validation with specifying “TARGET_B” is the outcome variable, while others are input variables in form of X and Y objects. 
 
4.	Run the following models with providing confusion matrix: 
a.	Logistic Regression 
 
 
The logistic regression model correctly identified 347 non-donors and 329 donors. However, it also misclassified 277 non-donors as donors and missed 295 actual donors with accuracy of 54.17%. While the model performs moderately well, the high number of false positives could lead to unnecessary mailing costs, and the false negatives represent lost donation opportunities.
b.	Classification Tree 
 
 
c.	Random Forest 
 
 
d.	 Neural Network 
 
 
e.	Linear Discriminant Analysis 
 
 
5.	What do you think is the best model?
Random Forest.
Among the classification models assessed, the Random Forest classifier demonstrated superior predictive performance, achieving the highest accuracy among all approaches by offering the highest accuracy and effectively minimizing both Type I and Type II errors, where false positives lead to unnecessary expenditures and false negatives result in lost donation opportunities.

Testing Model After Data Cleaning:
•	There are no missing values.
•	Outliers:
 
 
•	Apply log transfer:
 
 
Outlier analysis showed that 3% to 6% of values in donation-related variables were unusually high, a common pattern in fundraising data. These outliers can distort model performance, especially in scale-sensitive algorithms. To reduce their impact, we applied a log transformation, which compresses extreme values, reduces skewness, and improves model stability without losing data.
Modeling using the cleaned/log-transformed version:
 
 
 
 
6.	What do you think is the best model after log-transfer?
Linear Discriminant Analysis.
The updated results show that Linear Discriminant Analysis (LDA) achieved the highest accuracy at 56.01%, outperforming all other models after applying log transformation. This indicates a shift from earlier results where Random Forest was stronger. Log transformation likely helped LDA more than the tree-based models, as LDA assumes normally distributed features and benefits significantly from reducing skewness.
