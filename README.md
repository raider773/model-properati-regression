# Properati Dataset
Predicting Houses Prices of Capital Federal,Argentina


This project was part of my final work done for Digital House bootcamp. The only rule for the project as to apply all the concepts we learned (when nessesary of course) in a dataset that is somewhat complex. Not a titanic dataset for example, but something that challenges you.

I've decided to use a dataset of Properati to predict the prices of houses in my city. At the moment of this project i was looking for a new place to live in Capital Federal, Argentina, so i find it quite intresting to do my project regarding this matter. I was curious as of what determines the prices of houses in this city, as well as see how much the price affects other variables, for example the length of the description or the most commong words used in the titles, etc.

The proejct is divided into five notebooks :
- The first notebook, this one, is about preparing the data for further analysis. The dataset has a lot of nulls and outliers, so i tried yo fix thise issues.
- The second notebook is the analysis of the data. I made some charts that i think represent the data well.
- In the third notebook i divided the observations into clusters and add this clusters into features, and then trained different models.
- In the fourth notebook i created a Flask API to implement my model. The api transforms de data to fit my model and then returns the price prediction.
- The last notebook is just the the test for the API, making requests with different features and getting the prediction.
