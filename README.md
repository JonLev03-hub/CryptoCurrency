# CryptoCurrency
I will be working with unsupervised learning algorithms to discover patterns in cryptocurrency

The purpose of this repository is to use Kmeans in python to group crypto currencies into different categories. Bitcoin seems like an interesting investment for a lot of people because of the way it was designed and the talk behind it, but because of its popularity its price has gotten so high that its just not realiztic for a lot of individual investors to effectly buy it. Because of this I will be using Kmeans to categorize different crypto currencies to see if there could be simmilar options.

## The cleaning and transformation

First I had gotten a csv that contained a list of cryptocurrencies, along with different data about them. First I had to filter the list and remove all the currencies that had broken algorithms, and or no coins mined. This is done in the assumption that a coin with a broken algorithm will likely not take off since you cant create them. After this was done I used pandas functions to drop all rows with null values. 

Following the first steps I seperated the data so that i had a dataframe that only had information that I would like to input into the machine learning model. I Selected the 	Algorithm, ProofType, TotalCoinsMined, and TotalCoinSupply columns. Following this to prep the data for PCA I had to seperate the Algorithm and ProofType columns to useable data with the get_dummies method in pandas. 

Following that to speed up the machine learning algorithm used PCA to compile the data into 3 Usable columns. 

## Clustering and visualization. 

Because this was a small dataset I had no issues creating an elbow curve for the machine learning model so see the best way to cluster the data.  (Displayed Below)
![image](https://user-images.githubusercontent.com/81537476/152652816-3d2d38c0-9c41-4cd9-b968-614228d1e1b8.png)

After this was done I decided that it would be best to use 4 clusters. I applied Kmeans to the data and then finally used plotly express to create a 3d visualization of the categorization.  The visualization is displayed below.
![image](https://user-images.githubusercontent.com/81537476/152652906-cbe3bf2d-2d5a-4cba-9e13-e5708d1612d5.png)


## Application

To apply the data from this project the best use would be to find currencies that are simmilar to one you would like. So if you would like to find something that is simmilar to bitcoin you would simply need to find the class that is given to bitcoin and look into other coins in its class. 

For extra analysis you could simply only display one class of coin in the chart and see what are most simmilar to the desired coin, and see how each coin compares on a smaller scale.
