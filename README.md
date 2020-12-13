# Applying SQL queries on sample IMDB movies datset 

This repository consists of a sample IMDB database along with a set of 10 SQL Problems (Difficulty level: intermediate to diffciult).
Solving these help as a quick SQL refresher since these questions cover all the commonly used scenarios.

One of the challenges in the given DB is that the data is not completely cleaned, please make sure to analyze before writing your queries.

I have tried to provide explanations and the thought process behind most of the solutions, hopefully that helps. Even better if you can come up with a more effecient way of solving.

Please create a pull request if you find a more optimized query or if there are any corrections that you notice.

## List of files :

* __Database Schema (jpg file)__ - Provides a schematic of all the tables in the database and their relationships.
* __Db-IMDB-Assignment.db__ - Sample IMDB database that we would be using.
* __sql_questions.pdf__ - List of 10 SQL problems.
* __sql_on_IMDB_dataset.ipynb__ - IPython Notebook with all the solutions.

We would be using python pandas library in a ipython notebook to coonect to the given database and run our sql queries. The installation process and how to run queries using pandas can be found below.

## Installation :

### Required Softwares :

* __Python 3__  - Please install the latest version of python 3 from [here](https://www.python.org/downloads/). At the end of the installation don't forget to click _add python_ to path.
* __Anaconda__ - Anaconda is an open source distribution of python, it consists of all the frequently used python packages that we need. Install it from [here](https://www.anaconda.com/distribution/). Please choose the python 3 version.

If you are new to Jupyter notebook interface, you can find a quick overview [here](https://www.youtube.com/watch?v=HW29067qVWk).

## Steps to connect to the database using pandas :

* Create a new Jupyter notebook, preferably in the same folder where you put the Db-IMDB-Assignment.db file.
* We need to import couple of libraries - _pandas_ and _sqlite3_.

     import pandas as pd
     import sqlite3 
        
* Make a coonection to the sample imdb database.

     conn = sqlite3.connect("Db-IMDB-Assignment.db")
    
* Once we have the connection we can use pandas to write sql queries and see the results.The below query gives list of all the tables in the database - 

    tables = pd.read_sql_query("SELECT NAME AS 'Table_Name' FROM sqlite_master WHERE type='table'", conn)
    print(tables)
    
## Acknowledgement :
The sample IMDB database and the SQL problems are provided by the [Applied AI](https://www.appliedaicourse.com/) as part of their AI & Machine Learning Course.
