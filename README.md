# Tmdb-movies-data-EDA


Overview:  This data set contains information about 10,000 movies collected from The Movie Database (TMDb), including user ratings and revenue.
XYZ is a company who wants to enter the media production field and gathered this data to learn about the top profitable movies to produce, which genres to pick, who are the top directors to hire, who are the top profitable main actor to attract .... etc.? generally the asks for an answer for the questions below to get an accurate information to build a decision upon.

Exploratory data analysis on Tmdb movies data to find information about 
the most profitable movies to produce as well as checking the distribution of each
numerical variables - outlier detection along with correlation analysis to assess the
relationship between the continuous variables. 
trend projection for the profit over the time 
exploring the most profitable genres 

skills and tools : 
EDA, Univariate analysis , Bivariate analysis


Questions:
1- what is the most frequent genres (number of occurrence)?
2- what are the characteristics of top 10 most popular movies (in terms of popularity)?
3- what is the most watched genre?
4- how does the revenues and profits change over years? 
5- What are the top profitable genres?
6- what are the top 10 most profitable movies?
7- what is the average vote received for most profitable genre?
8- is there a relationship between popularity and profit?

Data issues and limitations:
- There are multiple values recorded in the cast column for each movie as well as genres column.
- Categorical variables are stored as object data type
- Year of release stored as int datatype and also there is another release date column stored as object type.
- Budget, revenue and runtime columns include values recorded as 0 which indicate missing data.
- Currency is not provided for the budget and revenue column. 
- There are some missing values in genres, director and cast columns.
- Vote count variable significantly varies from a movie to another which mean the average vote received can be biased based on the number of votes received.
- There is one duplicated row only in our dataset

Data Assessing and Cleaning justifications:
-	we need to separate the first value from the cast column to extract the main actor of each movie(assumption)
-	do the same for genre column as the first value indicate to the main genre of the movie(assumption).
-	since the revenue and budget columns doesn't have currency symbol indicator, we will assume that the currency used is united states dollar(assumption).
-	drop the release date as there is a release year column so it's not necessary for our analysis.
-	values of zeros in budget, revenue and runtime columns will affect the accuracy of our statistical summary so we'll drop them after a general investigation on our dataset.
-	drop the columns that aren't needed for our analysis such as id, imdb_id, homepage, keywords, overview, production companies, budget adj and revenue adj.
- create a column with showing the profit (the difference between the budget and the revenue.
-	we'll drop the columns with missing values as well as the duplicated row.

Findings: 
The most frequent genre in the dataset is the drama genre, it represents 23.1% from all the observations in our dataset followed by comedy and action.
The top 10 most popular movies in terms of popularity scores between 10.74% up to 33%, 6 out of them are action genres, with average budget around 127 million.
The most watched genre (sum of runtimes) as per our dataset is drama 104557 times. followed by comedy 80386 times and action 76124 times. with a high gap with the fourth position (adventure) which have been watched 36048 times.
Sum of revenues increases over time showing smooth ascending trend since 1960 up to date. As well as profit increases over time the trend is very hesitant which means there are some years with high drops in profits sums while other years show significant increase.
The Most profitable genre over the time is Action followed by adventure, comedy and drama respectively.
The top 10 most profitable movies over the time are: Avatar, Star Wars: The Force Awakens, Titanic, Jurassic World, Furious 7, The Avengers, Harry Potter and the deathly hallows part 2, Avengers: Age of Ultron, Frozen, The Net. 5 out of them has main genre as Action genre.
The average vote received for the most profitable genre (Action Genre) is almost 6 over the time.
there may be a relationship between the profit and the popularity moderate as the correlation score between them is almost 60%.
The most profitable genre over years is the action genre as the trend show significant increase in the last 10 years. While drama and comedy genres remain steady over the last 10 years.
