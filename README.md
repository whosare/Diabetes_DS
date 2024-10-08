# Diabetes_DS
This is a data science project aimed at understanding a diabetes dataset from Kaggle.
A short overview of the dataset shows us the 8 featuers and the target variable. 
I started visualizing the dataset to determine what consistencies and patterns were there. Some graphs and models used were pairplots, heatmaps, and histograms.

![image](https://github.com/user-attachments/assets/72abb6be-17df-4d53-9bb2-28ef68e09ef9)

From the graphs I then started looking into what variables were problematic, as in what features were too closely related that could cause issues for data processing. I used a heatmap to see this:
![image](https://github.com/user-attachments/assets/67727411-1dec-467b-b31c-07e579d6c05c)

For feature engineering, I utilized F-tests, RFE, and forestClassifier see how important each data variable was to the overal model.
From the results of feature engineering, I removed SkinThickness from one of the variables used for the model. With the remaining data, I split my data into training and split (20%), and then I scaled the data.
The data was then evaluated using and put back into the model for further analysis.

I also went ahead and tuned the hyper parameters for the forest model using GridSearchCV, to make the model perform better. 
For logistic regression I use accuracy_score and even applied an L2 penality 

Key Takeaways:
The project showed us what healthcare providers need to pay extra attention to in patients that might contract diabetes. 
For instance, a patient's glucose levels, BMI, and age can be very indictive of their health and might make them prone to developing diabetes. Of course, these features need to be evaluated further with other factors and taken into consideration with outside factors such as family history, habits, diet, etc. Still, running a program like this and inputting patient's medical records into a model like this can help healthcare providers and patients pay more attention to their health. 

Future Goals:
To improve this project in the future, I want to look at more datasets because with more data I can more accurately test different features. In a later stage, I want to pay special attention to the machine learning model and fine tune it to be able to predict a patient's proneness to contracting diabetes. That way, the model can be fed patient information from a hospital database and showcase which patients need extra care to help prevent diabetes. This project can even be applied to various other diseases if the right data is present. 
