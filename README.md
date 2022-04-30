# Credit_Risk_Analysis
## Overview of the analysis
In this project, we use Python to build and evaluate several machine learning models to predict credit risk. And We will evaluate 
the performance of these models and make a recommendation on whether they should be used to predict credit risk.

We adopted the following procedure:
- Oversample the data using the RandomOverSampler and SMOTE algorithms.
- Undersample the data using the ClusterCentroids algorithm.
- Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
- Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.

## Results
### 1. RandomOverSampler model

The balanced accuracy score is 65%.
The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.

![Screen Shot 2022-04-30 at 4 46 48 PM](https://user-images.githubusercontent.com/95242493/166125059-9874f2cc-2599-4250-86ce-11af9d833618.png)

![Screen Shot 2022-04-30 at 4 47 00 PM](https://user-images.githubusercontent.com/95242493/166125065-7fb3dacd-c63d-42bd-a088-0fa841253f57.png)
![Screen Shot 2022-04-30 at 4 47 19 PM](https://user-images.githubusercontent.com/95242493/166125068-16ee0d56-5376-49bd-9a98-fde1a7384477.png)

### 2. SMOTE model

The results are pretty similar to the previous model.
The balanced accuracy score is 64%.
The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 66%.

![Screen Shot 2022-04-30 at 4 49 43 PM](https://user-images.githubusercontent.com/95242493/166125112-0af18521-6dda-496b-bb39-05cac07deb97.png)

![Screen Shot 2022-04-30 at 4 49 56 PM](https://user-images.githubusercontent.com/95242493/166125122-f156e4f7-9694-4208-9d04-6e6a38cb4f85.png)
![Screen Shot 2022-04-30 at 4 50 07 PM](https://user-images.githubusercontent.com/95242493/166125126-bf3dc7fb-9582-4dde-927e-5ee3abd18869.png)

### 3. ClusterCentroids model
Here the balanced accuracy score is down to about 53%.
The high_risk precision is still 1% only with 61% sensitivity which makes a F1 of 1%.
Due to the high number of false positives, the low_risk sensitivity is only 45%.

![Screen Shot 2022-04-30 at 4 52 02 PM](https://user-images.githubusercontent.com/95242493/166125165-2eff93b3-7845-48e7-9444-5b442ebf4191.png)
![Screen Shot 2022-04-30 at 4 52 15 PM](https://user-images.githubusercontent.com/95242493/166125172-dce4541e-9625-4c1c-acc6-5adc9a8dd264.png)

![Screen Shot 2022-04-30 at 4 52 27 PM](https://user-images.githubusercontent.com/95242493/166125180-aeee2fb4-01a4-4bed-89c8-64ca4a3432be.png)

### 4. SMOTEENN model

The balanced accuracy score is about 62%.
The high_risk precision is still 1% only with 68% sensitivity which makes a F1 of only 2%.
Due to the high number of false positives, the low_risk sensitivity is 57%.
![Screen Shot 2022-04-30 at 4 56 06 PM](https://user-images.githubusercontent.com/95242493/166125243-b69dbbc9-4ddb-4a61-99d5-bcbdfe65d091.png)
![Screen Shot 2022-04-30 at 4 56 17 PM](https://user-images.githubusercontent.com/95242493/166125249-4d67ec82-5667-4874-ad60-de4dfe773b45.png)
![Screen Shot 2022-04-30 at 4 56 28 PM](https://user-images.githubusercontent.com/95242493/166125253-aa39c93f-e91e-40a0-8e8e-d215f06e4e2b.png)

### 5. BalancedRandomForestClassifier model

The balanced accuracy score improved to about 79%.
The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.
![Screen Shot 2022-04-30 at 4 58 15 PM](https://user-images.githubusercontent.com/95242493/166125314-60acfb5e-8b9e-4b00-b413-00efbfa29fa7.png)
![Screen Shot 2022-04-30 at 4 58 27 PM](https://user-images.githubusercontent.com/95242493/166125316-b793f77f-5bd2-4678-a1d5-d8fd9655b7e7.png)
![Screen Shot 2022-04-30 at 4 58 40 PM](https://user-images.githubusercontent.com/95242493/166125322-b90cd55e-0a93-4feb-a8b7-a47755a1825a.png)

### 6. EasyEnsembleClassifier model

Now, the balanced accuracy score is high to about 93%.
The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.
Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.

![Screen Shot 2022-04-30 at 4 59 56 PM](https://user-images.githubusercontent.com/95242493/166125353-1ff5c71f-b67b-41ca-87ba-16322885fd7f.png)
![Screen Shot 2022-04-30 at 5 13 27 PM](https://user-images.githubusercontent.com/95242493/166125591-160fd38d-914b-4995-9714-b8ae3ddc3008.png)
![Screen Shot 2022-04-30 at 5 04 19 PM](https://user-images.githubusercontent.com/95242493/166125428-76dccc41-8b96-4bd6-9b06-8f1a02f68f7e.png)

## Summary
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.
For those reasons I would not recommend the bank to use any of these models to predict credit risk.



