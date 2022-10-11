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

![image](https://user-images.githubusercontent.com/31709147/194998863-afd6ba40-1934-4a35-a30e-913cbe469eca.png)


# DATA CLEANING

There are no missing values in the entire dataset.

 ![image](https://user-images.githubusercontent.com/31709147/194998706-d4a2fde2-9494-460d-b816-c68ce3562e38.png)

All the columns are numerical and scaled.
 
 ![image](https://user-images.githubusercontent.com/31709147/194999070-b9db09fe-137e-48a5-94f7-aecc825e47ab.png)

# VISUALIZATION

As we mentioned that the dataset is highly imbalanced, the graph below represents the number of 0s and 1s in our dataset for the variable Bankrupt.

![image](https://user-images.githubusercontent.com/31709147/194998150-1fe556f8-f1eb-4b18-a79f-bd13ae08e419.png)

To check the correlation we used the Pearson correlation and plotted the below heat map. The heat map is just one part of the whole diagram as we have around 96 columns. We analyzed the heatmap and thought PCA would be a better option to go ahead to reduce the columns as manually selecting columns would have been a lot more time-consuming.

![image](https://user-images.githubusercontent.com/31709147/194998385-7ae4592a-914a-422a-9092-fd97063ce682.png)


# PARTITION

We split our data into 80/20 ratios for further processing.

# DATA SAMPLING TECHNIQUES

To deal with imbalanced data we used multiple data balancing techniques. 
1.	OverSampling
2.	Undersampling
3.	SMOTE sampling

For the purpose of visualization, we have reduced the data dimension from 96 to 2, below are the snippets of original and sampled data.

![image](https://user-images.githubusercontent.com/31709147/194995908-c1630989-b121-43f6-83eb-c415dafbcace.png)

# DIMENSIONALITY REDUCTION

 To deal with high dimensionality we have used PCA which reduced column count 96 to 11-14 while capturing 0.99 information. We have defined a method called DimReduction() which takes data from the training data dictionary and performs PCA and stores the result in the training data dictionary.
 
 ![image](https://user-images.githubusercontent.com/31709147/194996237-c04dec4c-3cf4-449a-a8cd-fa5aedf31191.png)

Below is a snippet of the output of this method.

![image](https://user-images.githubusercontent.com/31709147/194996285-c1d4779e-a90a-4a84-8c8f-ab08f6e4780e.png)

# MODELING

We trained the below models on Original, Oversampled, Undersampled, and SMOTE sampled data.

1.	Logistic Regression
2.	Naive Bayes
3.	Random Forest
4.	Neural Network

# FUNCTION TO CONSOLIDATE OUTPUT

In total, we have 8 datasets and 4 models to train, to facilitate the training we created a dictionary with a key as the model name and value as a method as shown in the below snippet.

![image](https://user-images.githubusercontent.com/31709147/194996552-d8129713-7376-40e6-a357-b15d3b358092.png)

At last, all the above-mentioned models are trained using modelTraining() method as shown below in the snippet.

![image](https://user-images.githubusercontent.com/31709147/194996595-5d7f6840-c1e1-4827-bef3-f76ad9506e7e.png)

Each model is trained on eight datasets and results are stored in the “predicted” dictionary.


# EVALUATION

It’s a binary classification problem so we have used the ROC curve, Classification report, and Confusion matrix to evaluate the performance of trained models.

![image](https://user-images.githubusercontent.com/31709147/194997983-0e297fdc-9b93-4218-b027-282ad708f34a.png)

Random forest turned out to be the best-performing model on Undersampled Data.
