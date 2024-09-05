# Diabetes_DS
This is a data science project aimed at understanding a diabetes dataset from Kaggle.
![image](https://github.com/user-attachments/assets/f4f65538-3151-482d-897e-726de65b40e0)
A short overview of the dataset shows us the 8 featuers and the target variable. 
I started visualizing the dataset to determine what consistencies and patterns were there. Some graphs and models used were pairplots, heatmaps, and histograms.
![image](https://github.com/user-attachments/assets/72abb6be-17df-4d53-9bb2-28ef68e09ef9)

From the graphs I then started looking into what variables were problematic, as in they had collinearity, using correlation matrices, SelectKBest, and RecursiveFeatureElimination.
![image](https://github.com/user-attachments/assets/4f2a5fb4-738b-4107-b50f-093c82de6a5b)

For feature engineering, I utilized F-tests, RFE, and forestClassifier to rank the importance and prevalence of the features.
![image](https://github.com/user-attachments/assets/e1bcfb53-fdcb-48bb-bffa-6631c0d8e1b4)

From the results of feature engineering, I removed SkinThickness from one of the variables used for the model. With the remaining data, I split my data into training and split (20%), and then I scaled the data.
The data was then evaluated using cross_validation and put into the forestClassifier model
![image](https://github.com/user-attachments/assets/095cd6f6-5441-4c2f-8b88-7522cf723224)

I also went ahead and tuned the hyper parameters for the forest model using GridSearchCV:
Final best parameters:  {'max_depth': None, 'min_samples_leaf': 4, 'min_samples_split': 5, 'n_estimators': 100}
I compared my main model RandomForestClassifier with two more models: GradientBoosting and Logistic Regression
For gradient boosting i used cross val score with the scaled data to obtain:
![image](https://github.com/user-attachments/assets/d4598463-4f23-48e4-8b70-51b840e2ed1b)
For logistic regression I use accuracy_score and even applied an L2 penality 
![image](https://github.com/user-attachments/assets/8182bbea-36da-474c-8884-7946172f88e7)

Key Takeaways:
The project showed us what healthcare providers need to pay extra attention to in patients that might contract diabetes. 
For instance, a patient's glucose levels, BMI, and age can be very indictive of their health and might make them prone to developing diabetes. Of course, these features need to be evaluated further with other factors and taken into consideration with outside factors such as family history, habits, diet, etc. Still, running a program like this and inputting patient's medical records into a model like this can help healthcare providers and patients pay more attention to their health. 
