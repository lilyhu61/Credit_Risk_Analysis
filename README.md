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
**1. RandomOverSampler model**
The balanced accuracy score is 65%.
The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.

![Screen Shot 2022-04-30 at 4 46 48 PM](https://user-images.githubusercontent.com/95242493/166125059-9874f2cc-2599-4250-86ce-11af9d833618.png)

![Screen Shot 2022-04-30 at 4 47 00 PM](https://user-images.githubusercontent.com/95242493/166125065-7fb3dacd-c63d-42bd-a088-0fa841253f57.png)
![Screen Shot 2022-04-30 at 4 47 19 PM](https://user-images.githubusercontent.com/95242493/166125068-16ee0d56-5376-49bd-9a98-fde1a7384477.png)

**2. SMOTE model**
The results are pretty similar to the previous model.
The balanced accuracy score is 64%.
The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 66%.

![Screen Shot 2022-04-30 at 4 49 43 PM](https://user-images.githubusercontent.com/95242493/166125112-0af18521-6dda-496b-bb39-05cac07deb97.png)

![Screen Shot 2022-04-30 at 4 49 56 PM](https://user-images.githubusercontent.com/95242493/166125122-f156e4f7-9694-4208-9d04-6e6a38cb4f85.png)
![Screen Shot 2022-04-30 at 4 50 07 PM](https://user-images.githubusercontent.com/95242493/166125126-bf3dc7fb-9582-4dde-927e-5ee3abd18869.png)

**3. ClusterCentroids model**
![Screen Shot 2022-04-30 at 4 52 02 PM](https://user-images.githubusercontent.com/95242493/166125165-2eff93b3-7845-48e7-9444-5b442ebf4191.png)
![Screen Shot 2022-04-30 at 4 52 15 PM](https://user-images.githubusercontent.com/95242493/166125172-dce4541e-9625-4c1c-acc6-5adc9a8dd264.png)

![Screen Shot 2022-04-30 at 4 52 27 PM](https://user-images.githubusercontent.com/95242493/166125180-aeee2fb4-01a4-4bed-89c8-64ca4a3432be.png)
