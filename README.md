# Applying SQL queries on sample IMDB movies datset 

This repository consists of a sample IMDB database along with a set of 10 SQL Problems (Difficulty level: intermediate to diffciult).
Solving these help as a quick SQL refresher since these questions cover all the commonly used scenarios.

One of the challenges in the given DB is that the data is not completely cleaned, please make sure to analyze before writing your queries.

Please refer to the solutions if you are stuck anyhwere, I have tried to provide explanations and the thought process behind most of the solutions, hopefully that helps and even better if you can come up with a more effecient way of solving.

Please create a pull request if you find a amore effecient way or if there are any corrections needed in the solutions.

List of files :
Database Scema Diagram - Provides a schematic of all the tables in the database and their realtionships.
Db-IMDB.db - Sample IMDB database that we would be using.
Questions.pdf - Provides the list of questions to be solved.
Solutions-Jupyter notebook.ipynb -- Ipython notebbok with all the solutions.
Solutions-PDF.pdf - PDF version of the ipython notebook.
Solution.sql - List of all the solutions saved as a sql file.
We would be using python pandas library in a ipython notebook to coonect to the given database and run our sql queries. The installation process and how to run queries using pandas can be found below.

Install :
Required Softwares :
Python 3 : - Please install the latest version of python 3 from here . At the end of the installation don't forget to click add python to path.
Anaconda - Anaconda is an open source distribution of python, it consists of all the frequently used python packages that we need. Install it from here . Please choose the python 3 version.
That's it , you should have all the softwares you need to run.

If you have never used a jupyter notebook, don't worry it's pretty straight forward, you can find a quick overview here.

Steps to connect to the database using pandas :
Create a new hupyter notebook, preferably in the same folder where you put the Db-IMDB.db file.
We need to import couple of libraries pandas and sqllite3.
    import pandas as pd
    import sqlite3 as sql # included as part of python standard library
Make a coonection to the sample imdb database.
    conn = sql.connect("Db-IMDB.db")
Once we have the connection we can use pandas to write sql queries and see the results.The below query gives all the tables in the database
    result = pd.read_sql_query("SELECT * FROM sqlite_master where type = 'table';" )
    print(result)
Contributions :
The sample IMDB database and the questions are provided by the Applied AI Team as part of their machine learning course.


