# Final_Group_Project

## Project Content

•	Selected topic – Popular music

•	Reason they selected the topic – This topic had a wide variety of data and we find music interesting

•	Description of the source of data – Excel-based spreadsheet data with music broken down by song

•	Questions they hope to answer with the data
  	What do the most popular songs have in common?
  	How do these popularity characteristics change over time?
  
## Synopsis of Results/Analysis

In order to complete this analysis, we looked at the following datasets available from Kaggle.

- top50.csv – top 50 songs from Spotify for the year 2019
- spotify_top50_2021.csv – top 50 songs from Spotify for the year 2021
- top10s.csv – top songs from 2010 – 2019

All the songs contained the same measured characteristics: BPM, energy, danceability, loudness, liveness, valence, acousticness, speechiness, and popularity. Before attempting to run any models we first removed the song and artist title from all datasets as we did not believe this would have a direct impact on the popularity of a song. 
To begin the analysis we ran a logistic regression to determine if there was any correlation between certain characteristics of a song and its popularity score.  As shown below, the results did not present any correlation that would help us predict a song’s popularity score. In an effort to improve or determine existence of a correlation, the model was adjusted multiple times to include different variables (loudness, bpm, etc.) in different combinations. Unfortunately, no correlation could be made. The r-squared value of 0.198 was one of the best values seen. Some of the p-values were below 0.06. We also scaled our logistic regression values but that only hinder the results further. We believed using the largest dataset, top10s.csv, would be the most likely to provide us with worthwhile results. After conducting the first test with the results below, we tried to use the smaller datasets, but results were far worse with some r-squared values of 0.010. 

![image](https://user-images.githubusercontent.com/96085210/173848545-6b72fc12-8ecf-4f10-8e96-23f511174bc8.png)

Our next plan of action was to run our data through a few other machine learning models.

### Random Oversampling

Results from top10s_2010_2019.csv shown below. Accuracy of 61%.

![image](https://user-images.githubusercontent.com/96085210/173848781-6b43e815-e8df-45e6-9ff5-970c1891e95a.png)

Results from top50.csv shown below. Accuracy of 79%.
 
![image](https://user-images.githubusercontent.com/96085210/173848844-c25b981d-893a-4b99-87a8-68cdf1a89371.png)

 
### Smote Oversampling

Results from top10s_2010_2019.csv shown below. Accuracy of 68%.
 
![image](https://user-images.githubusercontent.com/96085210/173849114-ac2bffcc-a64f-4381-8381-2e5fe9cdf23c.png)


Results from top50.csv shown below. Accuracy of 79%.

![image](https://user-images.githubusercontent.com/96085210/173849137-c4df560a-4ffc-4b41-9ca4-7a6e46019f4c.png)

 
### Undersampling

Results from top50.csv shown below. Accuracy of 70%.
 
![image](https://user-images.githubusercontent.com/96085210/173849198-a1173857-f7da-4703-a59b-196901acb172.png)


### Combination (Over and Under) Sampling

Results from top50.csv shown below. Accuracy of 70%.

![image](https://user-images.githubusercontent.com/96085210/173849255-6a402d6e-9a01-458b-b97f-987aa9f6826d.png)
 
### Balanced Random Forest Classifier

Results from top10s_2010_2019.csv shown below. Accuracy of 68%.

![image](https://user-images.githubusercontent.com/96085210/173849318-ff8d7d49-949c-4326-98e2-63c4d73a16db.png)
 
Results from top50.csv shown below. Accuracy of 75%.

![image](https://user-images.githubusercontent.com/96085210/173849356-95d23010-f445-4732-a9f4-c1832c2aefd5.png)
 
### Easy Ensemble AdaBoost Classifier

Results from top50.csv shown below. Accuracy of 70%.

![image](https://user-images.githubusercontent.com/96085210/173849457-2c068800-68f9-4fea-b385-999191c7c5e7.png)

 
As shown above the results do not lead us to have significant confidence in any models. Even when we scaled the data and/or increased/decreased the amount of data we were unable to determine any correlation between the data and a song’s popularity score. The analysis may show that the top songs are all consistent different characteristics. The variables that predict a popularity score are extremely different and fluctuate song to song. 

In the end, it appeared that some models would generically predict if a song would be popular but would fail in determining to what extent. A model would be able to predict if the popularity score would be over the mean but the deviation from the ‘true’ popularity score was immense. 


Link to Google Slide Presentation - https://docs.google.com/presentation/d/1eonvxaeexxP1OR3qs7QrAmMA7I7W4d7aHEfBT5ostdE/edit?usp=sharing
