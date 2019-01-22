#  Capstone Project: Create a Customer Segmentation Report for Arvato Financial Services

  For Udacity Data Scientist Capstone Project Arvato Financial Solutions: Identify Customers from a Mailout Campaign, this is a mail-order sales company in Germany is interested in identifying segments of the general population to target with their marketing in order to grow. Demographics information has been provided for both the general population at large as well as for prior customers of the mail-order company in order to build a model of the customer base of the company. The target dataset contains demographics information for targets of a mailout marketing campaign. The objective is to identify which individuals are most likely to respond to the campaign and become customers of the mail-order company. <br>
## project require library:
1. sklearn  <br>
2. seaborn  <br>
3. pandas   <br>
4. numpy    <br>

## at Arvato Project Workbook.ipynb document have <br>
### part I : Cluster data analysis
In this aprt, I analyzed AZDIAS data through clustering and compared it with CUSTOMERS data for comparative analysis. <br>
first I analysis missing data.<br>

find missing data I explore after to fill na data.<br>
 ![avatar](/Image/missing_data.png)<br>
fill data after,I use silhouette score evluate model.<br>
![avatar](/Image/silhouette_score.png)<br>
cluster 4 class compare customer data.<br>
![avatar](/Image/data_comparte.png)

### part II: Supervised learning
At this module I use RandomForestClassifier 、GradientBoostingClassifier、
LGBMClassifier、MLPClassifier、LogisticRegression、Xgboosting model for train Udacity_MAILOUT_052018_TRAIN data. this is validation socre <br>
![avatar](/Image/model_compare.png)
### part III: predicted data to kaggle
Since the project prediction is a binary classification, all the prediction results can be evaluated using a confusion matrix.
However, the confusion matrix has too many evaluation indicators to evaluate the classification results with one indicator, so the ROC curve AUC area is used to integrate the results of the confusion matrix to evaluate the classification effect.<br>
![avatar](/Image/roc_auc.jpeg)  ![avatar](/Image/formula.jpeg) <br>
The ROC curve AUC area can be represented by the  cograph left . The RCO curve is a comprehensive indicator of sensitivity and specificity. It calculates a series of sensitivities and specificities by setting successive variables to different thresholds. Then the sensitivity is plotted on the ordinate and the specificity is plotted on the abscissa. The larger the area under the curve, the higher the accuracy of the discrimination. On the ROC curve, the point closest to the upper left of the graph is a critical value with higher sensitivity and specificity. AUC is the area under the curve.The coordinate formula is cograph right.<br>
So using the roc_auc indicator can be a good way to evaluate the model classification results.<br>
At end I use model predict Udacity_MAILOUT_052018_TEST data to submit kaggle.<br>
![avatar](/Image/kaggle_score.png)<br>
### part IV: report
this is my reprot url: https://medium.com/@yangwang_57085/for-arvato-financial-services-find-value-customer-b7aa8445717b
