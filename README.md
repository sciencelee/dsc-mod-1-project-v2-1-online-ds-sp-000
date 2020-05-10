# What Movies Should a New Studio Produce?

![](images/banner-1155437_1280.png)


## The Project

This data project will look at a large dataset of movies with wide theatrical release, and will try to answer questions that might help guide a new studio looking to enter the industry.  The enirety of the project can be found in the [student.ipynb](https://github.com/sciencelee/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/student.ipynb) file.


## The Dataset

For this project, I chose to use the API for [The Movie Database](https://www.themoviedb.org/) (TMDB).
I chose 5000 movies from the last 10 years (2010-2019); that's nearly 10 releases per week of data, which represents essentially all of the major movie releases. The data for each movie is shown below.

```python
Index(['belongs_to_collection', 'budget', 'genres', 'id', 'imdb_id',
       'original_language', 'original_title', 'popularity',
       'production_companies', 'production_countries', 'release_date',
       'revenue', 'runtime', 'spoken_languages', 'title', 'vote_average',
       'vote_count', 'release_year', 'release_month',
       'revenue_to_budget_ratio', 'franchise'],
      dtype='object')
```

## Questions
The essential questions to be addressed by this project are:
* #### What factors affect the potential revenue for a new movie?
* #### What range of budgets produce the highest profit margins?
* #### What genres might be the most profitable?
* #### When should you release a movie to maximize profits?

# Analysis

## What factors affect revenue?

* ##### Budget 
A movie's Budget has the greatest correlation with the revenue of a movie of any factor I looked at. Big budget movies tend to produce big box office results with a Pearson coefficient of 0.76.
* ##### Sequels
If a movie is part of a franchise, the Pearson coefficient of budget/revenue is 0.77.  Standalone films are have a coefficient of 0.65.  29.63% of movies in past five years are part of a franchise.  Franchise movies make up 58.6% of all film revenues.
* ##### Weakly correlated factors
Audience score and runtime were only weakly correlated.  Audience score was also not closely correlated with profitablility of a movie as measured by revenue/budget.


## What range of budgets produce the highest profit margins?
For this study, profit margins were considered to be revenue/profits.  This assumption does not take into account the considerable amount spent promoting a movie (studios typically do not disclose this info).

The highest budget movies certainly produce the greatest revenue, but they do not have as high a revenue to budget ratio as the lower budget movies.  Movies in the first quartile significantly outperformed bigger budgets in terms of profitability.  Movies under 6 million USD were the most profitable by this measure.  Movies in the IQR for budget were the least profitable quartiles.  

## What genres are profitable?
The movies with the biggest revenues were Action, Adventure, Family, Animation, Science Fiction and Fantasy.  These also tend to be the most expensive to produce, which matches the budget to revenue relationship we observed.  

However, lower budget genres tend to outperform the big budget genres.  The most successful movies in terms of profit margin (revenue/budget) come from the genres Horror, Mystery and Thrillers.  Horror movies in particular have a revenue/budget which nearly doubles that of every other genre.  Horror movies are the least expensive to produce (above only Documentary films).

## When should we release our movies?
I chose to look at month of release only, to get general trends for what season or month of the year would be most profitable.  A long time practice in the film industry is to release the biggest films in May/June/July for the summer box office, or Nov/Dec for the holidays.  The dog days of summer Aug/Sep are generally "dump months" where Hollywood releases movies with low expectations or budgets.  Jan/Feb are generally when the awards movies are released.  

When looking at a barplot of movie releases by month, we can see the dump months have many movies and the big release months have less competition.  

When we look closer and examine revenue and profitability by month, we see that big budget movies are released in the expected summer and holiday months, but also see some indications fo strong April and October releases. A recent industry trend is to release big blockbuster films in April or October to deconflict with the release schedule of other big movies.  Some of the biggest releases in the past 5 years have been in April.

# Recommendations
* ##### Make many small budget films
While we don't make huge revenues, we also don't risk much, and on average the films will outperform the big budget action/adventure films in terms of profitability.

* ##### Make a select few big budget films
Big budget films will generate large profits.  This should be a part of any studio's offerings.  They are the more risky strategy, and careful consideration and planning should be used in the selection of directors, cast, crew, production compnanies, and release schedule.

* ##### Make Horror, Mysteries, Thrillers, Dramas and Comedies 
They are less expensive to make, and are very profitable.  While a single project won't net a huge sum, a diverse portfolio of genre films is a a recipe for success.  

* ##### Find or develop a franchise
Go out and acquire some potential franchises.  Popular novels, existing films, comic books, TV shows etc might reap huge profits.  If measured as a genre, sequels would only be outperformed by Horror films.  Of the top 20 grossing films of all time, 14 are sequels.

# Areas for further investigation
After choosing a general strategy, your company needs to do further investigation.  Among the topics of interest:

* ##### What production company, director, actors should we chose?
* ##### What marketing strategies work best for different film budgets?
* ##### What genres are best for each release month or week?
* ##### What factors will help you win movie awards?
* ##### What are the trends for each genre market you plan to enter?

![](images/popcorn-898154_640.png)
