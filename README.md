# BANKRUPTCY PREDICTION

This was a project that I made for my DATA PROGRAMMING class.

The data were collected from the Taiwan Economic Journal for the years 1999 to 2009. Company bankruptcy was defined based on the business regulations of the Taiwan Stock Exchange. 

The target variable has binary values making this a classification problem

We obtained the data from Kaggle, the URL for the same is mentioned below.

https://www.kaggle.com/datasets/fedesoriano/company-bankruptcy-prediction

# EXPLORATORY DATA ANALYSIS
<ul>
  <li>Our Dataset is a highly unbalanced dataset, one of the classes is in a significantly large portion than the other.</li>
  <li>It has around 7000 rows with 96 predictors./li>
</ul>
The screenshot below represents the initial 10 rows and 7 columns of our data set.

![image](https://user-images.githubusercontent.com/31709147/194932453-e7183e58-6891-437c-b3d4-6e883de96487.png)


# DATA CLEANING

There are no missing values in the entire dataset.

 ![image](https://user-images.githubusercontent.com/31709147/194932617-250b13f0-0e16-4b9b-a875-7e781a3fab5f.png)

All the columns are numerical and scaled.
 
 ![image](https://user-images.githubusercontent.com/31709147/194933281-2292eefa-8da4-420e-86ec-e192f7003eb6.png)

# VISUALIZATION

As we mentioned that the dataset is highly imbalanced, the graph below represents the number of 0s and 1s in our dataset for the variable Bankrupt.

![image](https://user-images.githubusercontent.com/31709147/194933046-d4812bff-dc2e-4675-ab7e-f53b553032b9.png)

To check the correlation we used the Pearson correlation and plotted the below heat map. The heat map is just one part of the whole diagram as we have around 96 columns. We analyzed the heatmap and thought PCA would be a better option to go ahead to reduce the columns as manually selecting columns would have been a lot more time-consuming.

![image](https://user-images.githubusercontent.com/31709147/194933375-e9c20591-6406-4425-aa71-df17f90f892f.png)



 

