# MachineLearningProject_MDS640
### Note Book Problems and Descriptions


Problem 1 and Problem 2
Upon previewing the data set and looking at the types of values that are stored in each column. It is easy to see that the ‘Income’ column needed to be tweaked to be properly processed. I used the .srt and .replace functions to grab the unwanted characters in the column and remove them. I also removed the CustomerID field since it is not relevant to our computations. 

Problem 3
Using the .describe funciton, we can gather that there is a large discrepancy between SpendingScore and Income. This is because the spending score that a customer is given is based on the percentile of spender that they are at this specific establishment. This is useful to correlate the amount of income that a person makes to the amount of money that they spend. The lowest spenders were making around~$1500 where the highest spenders where making anywhere up to ~$137,000. To normalize the data, we used the z-score normalization. The formula for the method is as follows: 
z = (x - μ) / σ 
Where x is the data that you are normalizing,  μ is the mean of the dataset, and σ is the standard deviation. 

Problem 4
To cluster the data into different labeled groups, I used the elbow method to determine the k-means. After getting the array of k-means points, I used a library called KneeLocator to determine where the elbow, or in this case the knee, was located at. The KneeLocator determined that the largest change in value was located at the third ‘joint’, so this was determined to be the ‘knee’ and was used as our k value. After this, we used the data that we had gathered to create a scatter plot of the data clusters, so that we could view the distribution. Admittedly, the scatter plot looked  like there could be five distinct clusters, but I chose to go with the results of the elbow plot and the KneeLocator, as they both seemed to agree. 

Problem 5
Now that we had our clusters broken up into separated values, I calculated the average Age, Income, and SpendingScore for each cluster. I also gathered the amount of Males and Females per cluster. With this data, we can draw conclusions about the demographic inside of each clusters and give them more proper labels. 

In cluster zero, there tended to be more Females (45) than Males (29). This was the second largest cluster, with a total of 74 people. The average income of this group was ~$1,294, and a spending score was  ~0.001151. This group could be described as majority women, with lower income, and less spending. 

In cluster one, there were an almost even number of Males (40) to Females (49). This was the largest cluster, with a total of 89 people. The average income of this cluster was ~$2,596, with a spending score of ~0.007745.This group had a spending score increase of ~572% and a income increase of  ~100%. This group could be described as a gender neutral group with median income and spending habits. 

The last cluster, cluster two, also had an average number of Males (17) and Females (18). This was by far the smallest cluster, with only 35 people. This group had an average income of ~$3,866 and a spending score of ~0.016996. This group had a significantly higher spending score of ~119% with an income increase of ~49%. This group could be described as the higher income and higher spending group. 

All groups had a consistent average age of ~38. The difference in percentage of income and spending score between the clusters shows that even though the last cluster spends the most money, the largest increase in spending occurred between the transition from cluster zero to cluster one. 
