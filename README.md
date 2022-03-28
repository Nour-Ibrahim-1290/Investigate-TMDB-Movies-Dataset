# Investigate-TMDB-Movies-Dataset

Explatory Data Analysis of [TMDB best movies list](https://www.kaggle.com/datasets/juzershakir/tmdb-movies-dataset) (part of 3rd stage of [Data Analysis Nanodegree](https://egfwd.com/specializtion/data-analysis-advanced/) powered by [Udacity](https://www.udacity.com/))

## Files:
* [Investigate_TMDB_Movies_Dataset.ipynb](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/Investigate_TMDB_Movies_Dataset.ipynb): a [Jupyter Notebook](https://jupyter.org/) of the EAD of the TMDB best movies dataset.
* [tmdb-movies.csv](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/tmdb-movies.csv): the dataset.

## ## Explanatory Data Analysis steps:
In order to answer  5 Posted Questions of the TMDB Dataset,
1. Data [Wrangling](https://en.wikipedia.org/wiki/Data_wrangling#:~:text=Data%20wrangling%2C%20sometimes%20referred%20to%20as%20data%20munging%2C,wrangling%20is%20to%20assure%20quality%20and%20useful%20data.) & [Cleaning](https://www.bing.com/search?q=data+cleaning+wiki&go=Search&qs=ds&form=QBRE).
2. Basic Statistical Analysis and Explatory Visualization.
3. Exploring 1st Question, most popular genre.

![PieChart](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/Investigate%20TMDB%20Dataset-PieChart.PNG)

4. Exploring 2nd Question:
   Visualizing the relation between revenue and budjet with both Hist and Scatter with Regression line.
![Visual2nd](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/Investigate%20TMDB%20Dataset-Hist01.PNG)
![Visual2nd](https://raw.githubusercontent.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/6e7f357526f8fa33c85636675a3bf52153d19d5d/Investigate%20TMDB%20Dataset-Scatter01.PNG)

   Exploring the relation between revenue and vote_count with both Hist and Scatter with Regression line.
![Visual2nd](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/Investigate%20TMDB%20Dataset-Hist02.PNG?raw=true)
![Visual2nd](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/Investigate%20TMDB%20Dataset-Scatter02.PNG?raw=true)

   Exploring the relation between revenue and release year with with both Hist and Scatter with Regression line.
![Visual2nd](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/Investigate%20TMDB%20Dataset-Scatter03.PNG?raw=true)

5. Exploring the production company with consistent success over the years
    use fun expload to get dataframe with unique production_company value on each record --> seeting threshold with describe fuction with profir at 75%
    --> filtering out the records with profit more than 75% --> grouping by the production_company and extracting unique count of production years
    --> extracting the name of the production company with the most #years of success (having profit >= 75%)
    
6. Exploring the flop major films (films cost over $100M)

![BarChart](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/Investigate%20TMDB%20Dataset-BarChart01.PNG?raw=true)

   removing the outlier (The Worrior's Way --> damn flopped!!)
 ![BarChart2](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/Investigate%20TMDB%20Dataset-BarChart02.PNG?raw=true)
 
 7. Exploring the Director with the highest rates and revenues In the 80th and 90th
 
 ![LineChart](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/Investigate%20TMDB%20Dataset-LineChart01.PNG?raw=true)
 
 ![Linechart2](https://github.com/Nour-Ibrahim-1290/Investigate-TMDB-Movies-Dataset/blob/main/Investigate%20TMDB%20Dataset-LineChart02.PNG?raw=true)
 
 ## Special [Function](https://www.w3schools.com/python/python_functions.asp) Definitions:
 1. **expload(dataframe: pandas.DataFrame, column name:str)**
    INPUT: a dataframe df and a column name str in the dataframe col
    PROCEDD: spreading the multiple information in col separated by '|' into multiple rows
            with the same info of the rest of the row.
    OUTPUT: a dataframe df with the spreaded multiple rows instead
 2. **identifybytick(df: pandas.DataFrame,tick: value,col: str column name)**
    INPUT: a dataframe df, a tick column cell value int, and a column name str.
    PROCESS: identify a cell value in the col by the tick value.
    OUTPUT: The identified cell value
 3. **printmovie(df,tick)**
    INPUT: a dataframe df, and a tick value of the tick column.
    PROCESS: print the column information of the tick value provided 
            as a display of the specific row info
    OUTPUT: no output, only the print statment
    

## Using these [Python](https://www.python.org/) Libraries:
* [Pandas](https://pandas.pydata.org/docs/)
* [Matplotlib.pyplot](https://matplotlib.org/stable/users/index.html)
* [seaborn]()
 
