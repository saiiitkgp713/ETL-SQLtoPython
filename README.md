# Pipeline-SQLtoPython
In the Process of ETL we transport data from one environement to the other for various purposes. The file provided "SQL to Python.ipynb" contains a python implementation of data transport from SQL server to the python environment. 

Prenote:
I have an SQL server 2019 version already set up and running in my PC. I have created some users and granted selective permission to access the data. Here we used one of the user credentials to connect to the server. 


In the first line of code we imported Pyodbc and Sqlalchemy modules that provide necessary support to coonect to SQL server. ODBC generally stands for OPEN Database Cnnectivity. it Mianly provides the driver that are necessary to maintain the connection between server and the python environment. Sqlalchemy actually makes the connection and imports the data.

In the second line of code, we checked for drivers necessary that are supported by pyodbc and used "ODBC Driver 17 for SQL Server" in this use case. Sql alchemy demands a URL to actually create a connection. Here we used URL.create() functionality provided by the sqlaclhemy module which parses a given string into an URL.

The connection string contains the details of the driver name, server name, user id, password and the database we are trying to connect. All these details are fed to string called connection string which is then transformed into an URL which connects the database using create_engine()

After creating the engine we can look for schema and the tables existing in the mentioned database. We read these tables into dataframe objects in our Python environment. We can also perfrom SQL queries on this database and using read_sql_query fucntionality to perform the necessary operation as stated by the query. Here we have used 2 queries naming query1 and query2 and we ran them to get the respective results.
