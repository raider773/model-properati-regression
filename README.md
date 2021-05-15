# Properati Dataset
Predicting Houses Prices of Capital Federal,Argentina


This project was part of my final work done for Digital House bootcamp. The only rule for the project as to apply all the concepts we learned (when nessesary of course) in a dataset that is somewhat complex. Not a titanic dataset for example, but something that challenges you.

I've decided to use a dataset of Properati to predict the prices of houses in my city. At the moment of this project i was looking for a new place to live in Capital Federal, Argentina, so i find it quite intresting to do my project regarding this matter. I was curious as of what determines the prices of houses in this city, as well as see how much the price affects other variables, for example the length of the description or the most commong words used in the titles, etc.

The project is divided into five notebooks :
- The first notebook, this one, is about preparing the data for further analysis. The dataset has a lot of nulls and outliers, so i tried yo fix thise issues.
- The second notebook is the analysis of the data. I made some charts that i think represent the data well.
- In the third notebook i divided the observations into clusters and add this clusters into features, and then trained different models.
- In the fourth notebook i created a Flask API to implement my model. The api transforms de data to fit my model and then returns the price prediction.
- The last notebook is just the the test for the API, making requests with different features and getting the prediction.


<img align="left" src="https://user-images.githubusercontent.com/70241561/118366162-f4ee6f80-b575-11eb-91a1-d4c935805c53.png"> 




The percentage of nulls was great. I had to drop a lot of columns due to nulls or not giving any information.


I also filled lots of nulls based on other columns, as well as using regex to get information from the description.




The most notorius charts are density of the price, the price per place name and a worcloud chart of the descriptions. <br />





![image](https://user-images.githubusercontent.com/70241561/118367003-f9675800-b576-11eb-9733-f71fc3dc3e5d.png)

This chart represents the most frecuent words in descriptions of properties. There are quite intresting things here.For example, Al frente("front") means the apartment faces the street. We can deduct most apartments face the street and not the otehr way. Iluminated is something that appears quite often, maybe because it makes an impact in buyers. Things liek air conditioning, hot water or suitable professional are also somewhat frecuent. We can see how descriptiosn are written in this city and also what people want to see more when buying houses in Capital Federal






