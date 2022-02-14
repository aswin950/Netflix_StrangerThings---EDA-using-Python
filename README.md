# Netflix_StrangerThings - EDA using Python
Netflix Stranger Things - Exploratory Data Analysis: using Python Jupiter Notebook
Dataset - https://github.com/aswin950/Netflix_StrangerThings---EDA-using-Python/blob/main/Netflix_StrangerThings.csv
Python Jupyter Notebook - https://github.com/aswin950/Netflix_StrangerThings---EDA-using-Python/blob/main/Netflix%20Stranger%20things%20Exploratory%20Data%20Analysis.ipynb

# I. INTRODUCTION:
The data set file name is “Netflix_StrangerThings.csv”. The data set contains 3,033 rows and 10 columns. The data set contains the User ID, Day of the Week, watched day which doesn’t have a name and will be named in this paper. It also contains the details about the Season number, Episode number, Gender of the Netflix account, whether the episode is watched or not which is mentioned with 0 and 1. 1 Means the episode is watched and 0 refers to episode is not watched. Time of Day also has 0 and 1 where 0 refers to night time and 1 refers to day time.

# II. EXPLORATORY DATA ANALYSIS:

Exploratory data analysis is carried out in this section in the context of data exploration. The four libraries used in this assignment are Pandas for data analysis, KNNImputer is used for imputing the missing values, Matplotlib for seaborn library data visualization.
       Head of Data Frame is used to display the first five rows from the data set.
       
 <img width="468" alt="image" src="https://user-images.githubusercontent.com/61600236/153931605-4ba1bcf8-341d-4c11-980c-fd8f0d0ecf71.png">

Figure 2.1 Head of Data Frame

Next, the data information is displayed to show the data type. The data set consists of 13 columns and 3033 rows. Numerical variables are Episode, Time Watched, Season and categorical variables are Show, Gender, Completed, Time of Day, Day of week.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/61600236/153931807-499fd7e9-adeb-4853-9da2-70585ae007d1.png">

Figure 2.2 Information of data

Data cleanup and preprocessing has to be done to remove the unwanted columns and the head of data is displayed.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/61600236/153931861-fbc48544-1204-4f1b-a3ba-5ddb39677b63.png">

Figure 2.3 Removed Unwanted Columns

We can observe that some columns are not given names and given wrong names. We will name these columns. The third column is empty and we will name it as Day of Week, and rename the Day of Week column to Date.

<img width="400" alt="image" src="https://user-images.githubusercontent.com/61600236/153931911-bc885b8d-3b72-4599-af45-89bd403d1e9f.png">

Figure 2.4 Renaming the Column

Now, we can convert date from object to data type

<img width="209" alt="image" src="https://user-images.githubusercontent.com/61600236/153931952-b13151e3-d962-4203-8412-29c5edd90489.png">

Figure 2.5 Convert date to object to data type

Missing values needs to be checked that are present in the data set. Missing values are present in the Gender and Completed Column.

<img width="206" alt="image" src="https://user-images.githubusercontent.com/61600236/153931995-bac59f31-8c29-4a7d-acaa-4986bbbc24d1.png">

Figure 2.6 Missing Values

The percentage of missing values in Gender and completed are 3.26% and 1.25% respectively. Percentage of missing values is very less, either we can ignore or we can impute these values by using mean, median and KNN imputation methods. Both variables Gender and completed are categorical variables. So, we are going to use KNN imputation method.

<img width="219" alt="image" src="https://user-images.githubusercontent.com/61600236/153932051-9cc07aa5-a3f7-4d06-b1e1-c194ca72b9a6.png">

Figure 2.7 Percentage of Missing Values

The Gender values are mapped as 0 and 1. And KNN Imputation for categorical variables is completed. Now, the original values are replaced with the imputed variable values and missing data is checked once again.

<img width="358" alt="image" src="https://user-images.githubusercontent.com/61600236/153932082-d3396405-ac12-41e8-8858-3a077a2e33a8.png">

Figure 2.8 Imputed Valued & Missing Values

When the data set was checked for duplicate values there were no duplicates found in the dataset.
Outlies / Anomalies are checked for Episode, Time Watched. No outliers are present in the Episode variable. Outliers are present in the Time watched variable. But, for this kind of dataset we can ignore outlier analysis because it is not so important.

<img width="455" alt="image" src="https://user-images.githubusercontent.com/61600236/153932126-0fd5909c-44e7-4a2d-8075-bcb5e7de86ff.png">

Figure 2.9 Boxplot of Episode

<img width="446" alt="image" src="https://user-images.githubusercontent.com/61600236/153932164-6b969cad-649e-4cec-9f4f-9a668a6750dc.png">

Figure 2.10 Boxplot of Time Watched

Since the data is cleaned and processed now, we can start the Exploratory Data Analysis. We can see summary statistics like mean, median, mode, count etc.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/61600236/153932223-b4c8aa46-5368-4878-9b21-8f28c79add7b.png">

Figure 2.11 Glimpse of Dataset

Correlation Matrix is displayed to find the correlation between the variables. It can be observed that there is less correlation between the variables.

<img width="411" alt="image" src="https://user-images.githubusercontent.com/61600236/153932272-3dbd78f1-092e-4d15-a654-f0bd1c44a72b.png">

Figure 2.12 Correlation Matrix

Univariate Analysis is used to know the count for the Day of Week and it is visualized.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/61600236/153932329-e45bf6a8-1fc5-4333-8353-58a6877c19b7.png">

Figure 2.13 Bar Graph to Count the Day of Week

From the above visualization it can be observed that many users watched Netflix shows on Tuesday followed by Saturday, Monday and Sunday.
  
  The most watched Netflix show is Stranger things, Orange is the New Black and American Horror Story.
  
<img width="377" alt="image" src="https://user-images.githubusercontent.com/61600236/153932619-19502287-3b1e-4b05-bf18-c7b7e8695d0a.png">

Figure 2.14 Most Watched Netflix Shows

Count graph for Male and Female users who watch Netflix shows. Male is represented with 0.0 and Female is represented with 1.0

<img width="382" alt="image" src="https://user-images.githubusercontent.com/61600236/153933156-cfb02c34-b7cb-4fc2-a806-36f7472155c5.png">

Figure 2.15 Male & Female Users Watching Netflix

We can observe that most users are not completed watching Netflix shows, followed by users who are completed watching Netflix shows and users who have watched 50% of Netflix shows.

<img width="385" alt="image" src="https://user-images.githubusercontent.com/61600236/153933197-1e7d3596-f2c0-4247-a79b-abcfbe998714.png">

Figure 2.16 Number of Users Completed Watch Status

The below visualization refers to the time of the day Netflix users watched the show. 0 represents night time and 1 represents day time. It can be observed that many users have watched Netflix shows in night than day time.

<img width="328" alt="image" src="https://user-images.githubusercontent.com/61600236/153933239-99ab3ddf-5cc0-4bd3-b6ef-fe7d4feba843.png">

Figure 2.17 Time of Day

Bivariate Analysis is used to compare different shows on Netflix.

<img width="375" alt="image" src="https://user-images.githubusercontent.com/61600236/153933277-ac02e475-7e55-4ea7-bf21-569712baa9ad.png">

Figure 2.18 Time Watched & Shows

The above visualization helps us to find which are the shows watched in day time and night time. 

The below visualization helps us to find which shows are in watched status and which shows are not watched.

<img width="400" alt="image" src="https://user-images.githubusercontent.com/61600236/153933521-014cb813-3b4d-48a7-9f65-22ea3ea9e367.png">

Figure 2.19 Completed Status of Various Netflix Shows

We can use bar graph to find during which day of the week most users watched Netflix shows and during which time of the day. From the graph we can say that during Sunday day time most people watch Netflix Shows. The below graph gives the said comparison.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/61600236/153933560-5e1e83bf-9c9a-4ec4-9c89-f174fc541ab8.png">

Figure 2.20 Comparing Days with Time of Day

Now, we can find which gender watches most on the given day of the week.

<img width="468" alt="image" src="https://user-images.githubusercontent.com/61600236/153933620-ad5948a8-2e9a-418c-9518-a4fe49f88af6.png">

Figure 2.21 Male Vs Female Watch Status

The above visualization is used to find pattern about which gender watched most on a given day of week.

# CONCLUSION AND NEXT STEPS:
The given Netflix data was cleaned and preprocessing steps were carried out before starting the Exploratory Data Analysis. Missing values and duplicates were checked during the process. Outliers and Anomalies were found on the required variable. During the EDA process summary statistics like mean, median, mode and count were found. Correlation matrix was plotted to find the correlation between the variables. Both Univariate and Bivariate analysis was carried out to find meaningful insights from the data.
    The next steps will be to recommend users to show a big continue watching tab in their home screen once the user logs in.
    
# REFERENCES

Htoon, K. S. (2020, July 3). A Guide to KNN Imputation. Medium. Retrieved from: https://medium.com/@kyawsawhtoon/a-guide-to-knn-imputation-95e2dc496e

Kaushik. (2020, July 20). KNNImputer: Way To Impute Missing Values. Analytics Vidhya. Retrieved from: https://www.analyticsvidhya.com/blog/2020/07/knnimputer-a-robust-way-to-impute-missing-values-using-scikit-learn/

Bronshtein, A. (2019, October 29). A Quick Introduction to the "Pandas" Python Library. Medium. Retrieved from: https://towardsdatascience.com/a-quick-introduction-to-the-pandas-python-library-f1b678f34673

10 minutes to pandas. 10 minutes to pandas - pandas 1.3.0 documentation. (n.d.). Retrieved from: https://pandas.pydata.org/docs/user_guide/10min.html#missing-data

Matplotlib Pyplot. (n.d.). Retrieved from: https://www.w3schools.com/python/matplotlib_pyplot.asp

 
