In the prediction, I use various prediction model ranging from Random Forest to Boosting , Linear regression to KNeighborsRegressor and finally found that linear regression is the best model to get the nearest result. 
In the code, I do the data processing first. Since there are many string fields which contain many different adjective to describe the games so I use one-hot coding to split the content into column. Also, I remove “tag” fields since tag is subjective opinion which may lead to overfitting.

In addition, I do some calculation on the purchase and release date. I take use the time difference between these two fields since I think the larger the time difference user will spend less time on that game. So I think time difference will be a factor to affect the time user spend on the game. Since there are some records without purchase or release date so I take the average time difference among all games and put it back to those games which do not have the date information.

Moreover, there are some records may have missing fields. I will assign zero for those fields to ensure all records have content for prediction.

After the data processing, I use different models to predict the final result and the linear regression model can get the nearest result with the TA’ prediction.
