# Properati Dataset
Predicting Houses Prices of Capital Federal,Argentina


This project was part of my final work done for Digital House bootcamp. The only rule for the project as to apply all the concepts we learned (when nessesary of course) in a dataset that is somewhat complex. Not a titanic dataset for example, but something that challenges you.

I've decided to use a dataset of Properati to predict the prices of houses in my city. At the moment of this project i was looking for a new place to live in Capital Federal, Argentina, so i find it quite intresting to do my project regarding this matter. I was curious as of what determines the prices of houses in this city, as well as see how much the price affects other variables, for example the length of the description or the most common words used in the titles, etc.

Model_rf.rar and properati.rar are the selected model and the original dataset.

The project is divided into five notebooks :
- The first notebook is about preparing the data for further analysis. The dataset has a lot of nulls and outliers, so i tried to fix this issues.
- The second notebook is the analysis of the data. I made some plots that i think represent the data well.
- In the third notebook i divided the observations into clusters and add this clusters as features, and then trained different models.
- In the fourth notebook i created a Flask API to implement my model. The api transforms the data and returns the price prediction.
- The last notebook is just the the test for the API, making requests with different features and getting the prediction.

<p>&nbsp;</p>



<img align="left"  width="300" height="400" src="https://user-images.githubusercontent.com/70241561/118366162-f4ee6f80-b575-11eb-91a1-d4c935805c53.png"> 




The percentage of nulls was great. I had to drop a lot of columns due to nulls or lacking useful any information.


I also filled lots of nulls based on other columns, as well as using regex to get information from the description: 

<p>&nbsp;</p> 
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>


-------------

 The most notorius charts are density of the price, the price per place name and a wordcloud of the descriptions. 
 
 
![image](https://user-images.githubusercontent.com/70241561/118368493-a7273680-b578-11eb-89ea-6feecc8b6432.png)  

We can see the distribution of my target variable here. There is a pretty notorious outlier. I'll use trees as a model so it doesn't affect the training that much.
Also the distribution is somewhat gaussean.

<p>&nbsp;</p> 

![image](https://user-images.githubusercontent.com/70241561/118369010-20268e00-b579-11eb-997c-e09806899480.png)

This is a simple chart to show the prices in each place_name (the neighbourhood if you wish).\
Puerto madero is the most expensive one, so thats a place im not gonna move in.

<p>&nbsp;</p> 

![image](https://user-images.githubusercontent.com/70241561/118369044-3b919900-b579-11eb-8483-12e676efa4e7.png)

This chart represents the most frecuent words in descriptions of properties. There are quite intresting things here. For example, Al frente("front") means the apartment faces the street. We can deduct most apartments face the street and not the other way. Lighting is something that appears quite often, maybe because it makes an impact in buyers.
Things like air conditioning, hot water or suitable professional are also somewhat frecuent. We can see how descriptions are written in this city and also what people want to see more when buying houses in Capital Federal.

<p>&nbsp;</p> 

-------------

Next i did some feature importance with a Random Forest and Extra Trees. I trained them without the place name. As i already knew the place name was a big factor on predicting the prices, i wanted to know how the other variables affect the prediction. We can see surface, rooms and suite are quite important. Also the len of the description aparently is also important, but i will not use it in the final model since thats not concrete data.

![image](https://user-images.githubusercontent.com/70241561/118369428-b5298700-b579-11eb-9d5c-eb08a93eaf94.png)

I also added quite a few features gathering information form the description, as well as adding clusters as a new variable. I used k-means with two clsuters to group the observations, and then used those clsuter to see if the prediction would improve. I selected 2 clusters after analysing the square distances,silhouette and calinski harabasz score, as well as doing some hierarchical clustering

-------------

After training some models, namely Lasso, Random Forest, ADABoost, XGBOOST and an ANN, I choose the random forest, both because of scores and because of simplicity.\
Then i analysed the selected model to see what influence a prediction the most using the lime library 

![image](https://user-images.githubusercontent.com/70241561/118369654-9081df00-b57a-11eb-8875-7bb167493628.png)


![image](https://user-images.githubusercontent.com/70241561/118369664-9aa3dd80-b57a-11eb-9a4a-4a34582f9d8e.png)


![image](https://user-images.githubusercontent.com/70241561/118369667-a1325500-b57a-11eb-8b15-f4869ad54ba0.png)


![image](https://user-images.githubusercontent.com/70241561/118369673-a8f1f980-b57a-11eb-8711-1e282566e706.png)

The randomized search best parameters


![image](https://user-images.githubusercontent.com/70241561/118369680-b0190780-b57a-11eb-92e8-eb06c535da39.png)

The place-name is what most affect prediction


-------------------


Finally i used flask for the deployment of my model.

![image](https://user-images.githubusercontent.com/70241561/118370009-194d4a80-b57c-11eb-8ede-ef87767c0d33.png)



![image](https://user-images.githubusercontent.com/70241561/118370019-223e1c00-b57c-11eb-8a4c-961571735b16.png)











