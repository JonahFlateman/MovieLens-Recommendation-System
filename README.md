# MovieLens Recommendation System

In this project we wil be making recommendations based on the MovieLens dataset, a collection of user ratings for movies from the GroupLens research lab at the University of Minnesota. We will build a model to provide the top movie recommendations to a user, based off of their ratings of other movies.

## Goals

* Interpret our data and prepare best possible modeling framework
* Understand business problems at hand, using recommendations for customer insights
* Iterate through several models and use Root Mean Square Error (RMSE) as key metric

## Methodologies

* Use collaborative filtering methods to create baseline methods using tools via Surprise algorithms
* Find best parameters using GridSearchCV, apply to SVD modeling and compare with KNN models
* Use matrix factorization with Alternating Least Squares via PySpark, cross validate and determine best parameters
* Build user input function to rate movies, and test using best applicable model

### What trends do we notice in our dataset?

![User ratings](images/userratings.png)
![Genre ratings](images/genreratings.png)

Most ratings fall in the 3 - 5 range, genres stay relatively consistant with some slight outliers.

### How accurate is our final ALS model?

![Test predictions](images/testpredictions.png)

Our RMSE on an untuned model started at 0.9958; after adjustments this was brought down to 0.8649.  Earlier modeling with Surprise produced a best RMSE of 0.8691 using SVD.

### What does the user input process look like?

![User interface](images/userinterface.png)

Our function takes in User ID, movie and title DataFrames, and number of desired inputs and recommendations (in this case, five and 10 respectively).