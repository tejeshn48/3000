# PANDAS
It is a high-performance data analysis Tool
Pandas is a software library written for the python programming language for data manipulation and analysis.
The panda’s module mainly works the tabular data.
Pandas is capable of offering an in-memory 2d table object called DataFram.
The most widely use pandas data structures are the series and the DataFram.
Simply, a series is a similar column of data while a DataFram is similar to a sheet with rows and columns.
Working with a large amount of dataset.
Pandas is a very important library and data science
They represent in tabular data way (rows and columns).
Working on missing data.
Indexing – slicing -sub-setting a large amount of data.
You can merge and join two different data sets easily.
Reshape the datasets.
Pandas are used in the panda's data structure.

###    PANDAS USE 3 DATA STRUCTURES
- Series
- Data Frame
- Panel

###    INSTALLATION OF PANDAS
Go to the command prompt and change the location to where the python has been installed on your desktop/laptop and use the following command to install the PANDAS library 
```
pip install pandas
```
### IMPORTING PANDAS
To whether the panda's module is properly installed, try the given commend. 
```
Import pandas
```
To check the version of pandas, use the given command
   print(pandas.__version__)
 
 ###   Creating DataFrame
 
- Load the data from the EXCEL file
- Read_excel(“file_location”)
- Load the data from the CSV file
- Read_csv(“file_location”)
- Create DataFrame using DICTIONARY
- Create  DataFrame using LIST OF TUPLE 
###    INDEXING SLICING
- data_frame .head( number_of_rows)
- data_frame. tail(number_of_rows)
- data_frame.describe()
- data_frame. shape
- data_frame [ start: stop: step]
- data_frame[ 'column_name']
- data_frame[ [column_1, column_2]]
- data_frame[ [column_1, column_2] ][ start: stop: step]
- data_frame.lterrows()
- loc & iloc
 
###  UNDERSTANDING 
- LOC & ILOC
 
### UNDERSTANDING LOC[ ] (stop index included) 
- data_frame.loc[ row_number]
- data_frame.loc[ row_number, [column_name,...]]
- data_frame.loc[ start: stop ]
- data_frame.loc[ start: stop, "column_name"]
- data_frame.loc[ start: stop, ["column_1, column_2,... "]]
- data_frame.loc[ start: stop, "column_1": "column_n"]
### UNDERSTANDING ILOC[ ] (stop index excluded)
- data_frame.iloc[ row_number,column_number]
- data_frame.iloc[ row_start: row_stop, col_start: col_stop]
- data_frame.iloc[ start: stop, "column_number"]
- data_frame.iloc[ [row_1, row_2,...]]
- data_frame.iloc[[col_1, col_2, . . . ]]
- data_frame.iloc[ start: stop, [col_1, col_2,...] ]
###   SORTING DATA FRAME
- Data_frame.sort_values("column_name")
- Data_frame.sort_values("column_name", ascending=False)
- Data_frame.sort_values(["column_1","column_2"])
- Data_frame.sort_values(["column_1","column_2"],ascending=[0,1])
###   MANIPULATING DATA FRAME
#### ADDING COLUMN
- Data_frame['new_col_name']=default_value
- Data_frame['new_col_name']=Expression / Condition
#### REMOVING COLUMN
- Data_frame.drop(columns="column_name")
- Data_frame.drop(columns="column_name", inplace=True)
 ###  REMOVING DUPLICATES
- Knowing Duplicates
- Data_frame.duplicated() - Boolean Result
- Removing Duplicates
- Data_frame.drop_duplicates()
- Data_frame.drop_duplicates (inplace=True)
###   HANDLING MISSING DATA
- REMOVING MISSING DATA
- Data_frame.dropna( )
- Data_frame.dropna (inplace=True)
- FILL WITH DEFAULT VALUES
- Data_frame.fillna(default_value)
###   DATA FILTERING & CONDITIONAL CHANGES
- Data_frame.loc[simple_condition]
- Data_frame.loc[compund_condition]
- Data_frame.loc[simple_condition.str.contains(str)]
- Data_frame.loc[simple_condition.str.starts with(str)]
- Data_frame.loc[simple_condition.str.endswith(str)]
- Simple Condition
- Data_frame["Col_name"]>/</ == value
###   EXPORT DATAFRAME to EXCEL, CVS & TEXT FILE
- Data_frame.to_excel(PATH)
- Data_frame.to_excel (PATH,index=False)
- Data_frame.to_csv(PATH)
- Data_frame.to_csv(PATH, index=False) 
# BeautifulSoup
###  WEB SCRAPING
Web scraping refers to the extraction of data from a website. This information is collected and then exported into a format that is more useful for the user.
Web scraping is an automatic method to obtain large amounts of data from websites.
Web scraping is a method of extracting data from websites.
It uses software to extract all the information.
Most of the data is unstructured in HTML document format.
A large number of data analyses the web scraping from a simple format to use URL.
Although web scraping can be done manually, in most cases, automated tools are preferred when scraping web data as they can be less costly and work at a faster rate.
                  
Web scraping is legal or illegal
Web Scraping is actually not illegal on its own web scraping.
Beautiful Soup and Scrapy are such libraries of Python that supports web scraping.
 Web scraping can use some of the libraries in python.
#### They are 
 Requests, Beautiful Soup, scrapy, and selenium
 
Then used in BeautifulSoup in Web scraping then we discuss the BeautifulSoup in the topic of python

###  BeautifulSoup:
 
BeautifulSoup is a python library that makes it easy to scrape information for web pages.
That makes some documents HTML and XML files.
Beautiful Soup converts the files into HTML and XML documents.
The Beautiful Soup library helps with isolating titles and links from web pages.
Extract all the text from the HTML file.
We have a present updated version of BeautifulSoup BeautifulSoupbs4.
 
###  Install BeautifulSoup
```
 pip install BeatifulSoupbs4
```
 ###  Importing BeautifulSoup
```
 Import BeautifulSoupbs4
```
          
### Uses of BeautifulSoup
The Beautiful Soup library helps with isolating titles and links from web pages.
- Extracting data
- Filtering values
- Navigating data                                
# NUMPY

To understand NumPy you should know about arrays

## ARRAYS:

- The array is a collection of homogeneous elements.
- The array is used to store values in a single variable.
- The array is only stored in single-line variables (int, float, and str). Arrays are not stored in multiple values in a variable.

#### Ex :

 (‘i’, [2, 4, 5, 6, 3, 9])

#### Ex:

 (‘I’, [2, 4, 5.4 , 6, 3.5 ,9]) 

### IMPORTING ARRAY:
 ```
 Import array
 ```
We can use the arrays different types of arrays in single  “*”
“ * “  is used for all types of arrays
```
 From array import *
 ```
#### Ex  program:

From array import *

Arr1 = array (‘i’, [3, 5, 6, 7, 9])

Print (Arr1)

####  Note:
- i  -  signed
- I  -  unsigned  

## NumPy: 
NumPy full from is NUMARICALPYTHON
NumPy is used to create multi-dimensional arrays.
Proved a lot of functions to work in the domain of linear Algebra and metrics
Provide function related to arrays
Create an array called nd array (nd = n-dimensional arrays)
Working of nd arrays faster than lists 
### Check NumPy version

Get the version
 ```
 Print (numpy.__version__)
 ```
Most of the parts of NumPy are created a  c & c ++

Array create the nd array
###  Installation NumPy:
```
 Pip install numpy
```
 ### Importing numpy:
```
 import numpy as np
```
###  DTMENSIONAL ARRAYS:
 When the dimensional array is called in the single dimensional(D) array in
- 0 – D array is shown in the NumPy . array ( )
- 1 – D array is shown in the NumPy . array ([1, 2, 3])

Then the array is  0 - dimensional elements
- 2 – D array is shown in the NumPy . array ([[1, 2, 3], [4, 5, 6]])

Then the array is  1 - dimensional elements
- 3 – D array is shown in the NumPy . array ([[1, 2, 3], [4, 5, 6]], [[7, 8, 9], [10, 11, 12]])

Then the array is  2 - dimensional elements

NumPy gets an output matrix like rows and columns.

 ###   To use the “ SHAPE ” method
 To get the shape of the given input we will use the shape method rows and columns

#### Ex:

Import numpy as np

Arr = np . array ([[1, 2, 3], [4, 5, 6]])

Print(Arr . shape)

#### Output:
 [2 3]

### Import numpy as np
Arr = np . array ([[1, 2, 3], [4, 5, 6]])

Arr . shape = (3, 2)

Print(Arr)

#### Output :

[[1 2]

 [3 4]
 
 [5 6]]

 ###   To use the RESHAPE method
 When the reshape use an array of NumPy is created in the reshape numpy of the array to use in reshape method

#### Ex:

   Import numpy as np

   Arr = array ([[1, 2, 3], [4, 5, 6]])

   Arr2 = Arr . reshape (6, 1)

   Print (Arr2)

#### Output:

[[ 1 ]

 [ 2 ]
 
 [ 3 ]
 
 [ 4 ]
 
 [ 5 ]
 
 [ 6 ]]
 
  ###  To use the “ ARRANGE “method
 when the arrange is used to the numpy method can number of values. We have the curtain number to use the arrange method in the array. To use the array in the form of some values you particular value to use the arrange method.

#### Ex:

Import numpy as np

Arr = np . arrange ( 24 )

Print ( Arr )

#### Output:

[ 0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 ]

 It is just called the arrange the value of 24 in output is 0 to 23 to called in arrange.
 
 We can use the other way of arranging in to use the reshape 



#### Ex:

Import numpy as np

Arr = np . arrange ( 24 )

Arr2 = Arr . reshape ( 3, 8 )

Print( Arr2 )

#### Output:

[ 2  7 ]
  ###  To check the value of ‘SIZE’ in numpy use array
 When checking the SIZE of numpy to use the array in masseur the size of numpy in value.
 
#### Ex:

Import numpy as np

Arr = np . array ([1, 2, 3, 4, 5 ])

Print(Arr . itemsize)

###    Used only for int values
#### Ex:

Import numpy as np

Arr = np . ones

( 5 ) 

Print (Arr )

 have a matrix with ROWS and COLUMNS in numpy 
 
Import numpy as np

Arr = np . ones

(( 1, 2, 3, 4 , 5, 6, 7, 8, 9, 10) int )

 Print ( Arr . dtype )

# Django

 Django is a Python-based web framework that allows you to quickly create efficient web applications.
 When you’re building a website, you always need a similar set of components: a way to handle user authentication (signing up, signing in, signing out)
 Django gives you ready-made components to use and that too for rapid development.
 Django is based on MVT (Model-View-Template) architecture.
## MVT
MVT is a software design pattern for developing a web application.
Here a user requests for a resource to the Django, Django works as a controller and check to the available resource in URL.
### Install Django:
 ```
 Pip install django
 ```
 If we want to create a Django project, we have to use some commands.

### Start project:
```
 django-admin startproject projectName
```
go to the project to use this command
```
 cd projectName
```
 A New Folder with the name project name will be created. In that folder we have the manage.py file, if we want to run our server we have to call that file from that location.

### Strat run server:
```
 python manage.py runserver
```
Then it will display the URL to open that website, open that URL in the browser, and there you can see the welcome page. Apart from this, we have another webpage called admin, to open that webpage add /admin in the URL.
Django is famous for its unique and fully managed app structure.
For every functionality, an app can be created like a completely independent module.
To create an app we have one more command.
```
 python manage.py startup project app 
 ```
In this, Project Structure is very important. So let us have a look.

### Create a website page
To consider the app in your project you need to specify your project name in the INSTALLED_APPS list in settings.py
In our webpage is showing the default webpage. Now we are changing that to our custom page. In this Django project, one more important part is URLs, if we want to open different webpages in the browser we have to focus on the URL of that webpage. So first we have to update the urls.py file under the main project.
In the urls.py file we have to include our app's URL file. From there we can open our desired webpage and we can display that in the browser.
Now we have to create one file under the app, and save that file as urls.py. From this file, we can call different webpages based on URL.
In that file we have to import the views file, and we have to call a function from the views.py file based on the received URL.
Last and Final step are to create a function in the views.py file, with the same name as used in the urls.py page.
#### Settings.py
INSTALLED_APPS = [

'my_first_app',
  
'django.contrib.admin',
    
'django.contrib.auth',
    
'django.contrib.contenttypes',
    
'django.contrib.sessions',
    
'django.contrib.messages',
    
'django.contrib.staticfiles',
    
]

#### my_first_project/urls.py

from django.contrib import admin

from django.URLs import path

from django.URLs import include

urlpatterns = [
   
path('admin/', admin.site.URLs),
   
path('',include("my_first_app.URLs"))

]

#### my_first_app/urls.py

from django.URLs import path

from. import views

urlpatterns = [
   
path('',views.my_welcome_page)

]

#### my_first_app/views.py

from django.shortcuts import render

from django. shortcuts import HttpResponse

def my_welcome_page(request):
   
return HttpResponse("Welcome to our webpage")

After that we have to create tables for pre-installed apps. For that we have two more commands.
```
 python manage.py makemigrations
```
```
 python manage.py migrate
```
After that we have to create a superuser to login to the admin page. For that use the below command.
```
 python manage.py createsuperuser
 ```
After that command it will ask to enter a username, email, and password, enter those details by using those details you can log in to the admin panel.

Shell is an interpreter between PyCharm to django.

PyCharm programming assigned to the django.

From django.db import connection

A python shell that gives you access to the database API included with Django.
```
python manage.py shell
```
How to use shell?

Open terminal with the current directory as Django project. You can see the manage.py in your current directory.

The Django shell is an interactive command-line interface shell environment that combines the Django framework functionality with the regular python shell.
