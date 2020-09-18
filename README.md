# Estimating IMDB film rating



Main question : What are some methods of determining the quality or success of a film prior to its cinematic debut?

## First Part - Parsing data

The first part aims to  extract information such as cast, directors, production companies, awards, genres, budget, gross, description, and IMDB rating from IMDB and other websites, and to compile this data into a file called movie_contents.json. 
``python3 parser.py nb_elements``  

## Second Part - Data Analysis

The second part is to examine the collected data and investigate any possible connections between the various variables. For instance, is there a relationship between the number of awards a movie has received and its global box office performance? Are the popularity of a film and the popularity of its cast members related? 
See the jupyter notebook file.  

![Correlation Matrix](https://github.com/alexattia/Data-Science-Projects/blob/master/pics/corr_matrix.png)

As illustrated in the figures above, there appears to be a correlation between IMDB rating, the number of awards a movie has received, and its gross revenue. However, there is not a significant correlation between the production budget and IMDB rating or the number of Facebook likes of the cast. Additionally, it is evident that domestic and worldwide gross are closely related. However, a higher production budget tends to result in higher gross revenue. The data also suggests that there is no significant correlation between production budget and the number of awards a movie receives. Interestingly, the popularity of the third most famous cast member has a stronger correlation with the IMDB score than the popularity of the most famous cast member (with a correlation coefficient of 0.2 versus 0.08).  
(Many other charts in the Jupyter notebook)

## Third Part - Predict the IMDB score

Machine Learning to predict the IMDB score with the meaningful variables.  
Using a Random Forest algorithm (500 estimators). 
![Most important features](https://github.com/alexattia/Data-Science-Projects/blob/master/pics/features.png)

