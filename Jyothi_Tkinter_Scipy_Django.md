# Tkinter      
Tkinter is the standard GUI library for python. Python when combined with Tkinter provides a fast and easy way to create GUI applications. Tkinter provides a powerful object-oriented interface to the Tk GUI toolkit.
In GUI modules:
                             There are three types of GUI modules
Tkinter
PyQt
WxPythons
By using Tkinter now I am going to write a GUI application

 import tkinter
 from tkinter import *
 root = Tkinter.Tk()
 root.title("tk")
 root.mainloop()
Output:
                    
 

Firstly we need  to import tkinter then we need to we need import*from tkinter
import* means the whole information in kinter will come to use
tkinter.Tk() to assign  root variable.


 If I run the above code it opens an application with a title called demo and the application will show in small size.

To change the small size of the application I need to run one more code which is below.

import tkinter
from tkinter import *
root = tkinter.Tk()
root.title("demo")
root.geometry(“600x600”)
root.mainloop()

If I run the above code it will increase the size of the application                                                                    
After writing code for the application and title and increasing the size of the application now I am writing code to create a label.

## Label creation:

Import tkinter
from tkinter import *
root = tkinter.Tk ()
root.title ("demo")
root.geometry(“600x600”)
label=tkinter.Label(root,text=”hii”).pack()
root.mainloop()

If I run the above code it will create a label for the application.

After creating a label now create a button.
## Button creation:

Import tkinter
from tkinter import *
root = tkinter.Tk ()
root.title ("demo")
root.geometry(“600x600”)
label=tkinter.Label(root,text=”hii”).pack()
b =Button(root,text=”subscribe”,bg=”orange”, fg=”red”)
b.grid(column=1,row=0)
root.mainloop()

after b= must use start with capital “B”

bg = background colure 
fg = front ground colure 

I used a word called GRID in code to place various buttons in various places in the application where they are required 

If I run the above code it will create a button for the application.

After creating a button now let's go to create the radio button
## radio button
Import tkinter
from tkinter import *
root = tkinter.Tk ()
root.title ("demo")
root.geometry(“600x600”)
label=tkinter.Label(root,text=”hii”).pack()
b =Button(root,text=”subscribe”,bg=”orange”, fg=”red”)
b.grid(column=1,row=0)
r =Radiobutton(root,text=”python”,value=1)
r.grid(column=2,row=1
root.mainloop()

If I run the above code it will create a radio button for the application 

Previously I created a single radio button now I gave other code to create multi-radio buttons
Button – the button is used to add various kinds of a button to the python applications

Import tkinter
from tkinter import *
root = tkinter.Tk ()
root.title ("demo")
root.geometry(“600x600”)
label=tkinter.Label(root,text=”hii”).pack()
b =Button(root,text=”subscribe”,bg=”orange”, fg=”red”)
b.grid(column=1,row=0)
r =Radiobutton(root,text=”python”,value=1)
r.grid(column=2,row=1)
r1 =Radiobutton(root,text=”python”,value=1)
r1.grid(column=2,row=2)
r2 =Radiobutton(root,text=”python”,value=1)
r2.grid(column=2,row=3)
root.mainloop()
  

If I run the above code it will create multi-radio buttons for the application
 I used a word called GRID in code because to place various buttons in various places in the application where they are required 

Previously I created a multi-radio button now I gave a code to create an entry
#  entry button creation
 t =Entry(root,width=10)
 t.grid(column=3,row=0)
If I run the above code it will create an entry application


# create a message box 
I used toPreviously I created an entry button on this application now I gave code to create a message box. these function

 Import tkinter
 from tkinter import *
 from tkinter import messagebox
 def button1():
   
messagebox.showinfo(“status”,” plz subscribe”)
b=button(root,text=”python life”,command=Buttons)
b.pack()
I used a function called pack(). which will pack the information and keep it. 
after creating a bottom box on this application like the below picture

  

Previously I created a message box now I gave code to create a combo box

## Combo box creation:


import tkinter as tk
from tkinter import ttk
root = tk.Tk()
root.title("combobox")
root.geometry("600x600")
ttk.Label(root,text="python life",background="blue" ,foreground="white",)
         
font=("Times new roman",15)).grid(row=0, =1)
 combo box
 n = tk.StringVar()column
 course=ttk.Combobox(root,width=27,textvariable=n)
course["values"]=("python" "Django", "machine learning")
course.grid(column=1,row=5)
course.current()
root.mainloop()

If I run above the code it will create a combo box.

Previously I created a combo box now I gave code to create a scrolling test

## scroll test creation:

import tkinter as tk
from tkinter import ttk
from tkinter import scrolledtext
root = tk.Tk()
root.title("scrolledtext")
root.geometry("600x600")
ttk.Label(root,text="python life",background="blue" ,foreground="white",
         
font=("Times new roman",15)).grid(row=0,column=1)
text1=scrolledtext.ScrolledText(root,wrap=tk.WORD,width=40,height=10)
text1.grid(column=0,pady=10,padx=10)
text1.focus()

root.mainloop()
By using Tkinter I prepared a small project which is as below.

# demoproject:

from tkinter import*
from tkinter import messagebox
def ok():
    uname=el.get()
    password =e2.get()
if(uname=”” and password=””):
  
messagebox.showinfo(“,”Blank not allowed”)
elif(uname==”admin”and password==”123”):
               messagebox.showinfo(“,”login success”)
               root.destroy()
else:
               messagebox.showinfo(“,” incorrect user name and password”)
root=Tk()
root.tittle(“login”)
root.geometry(“300x200”)
global e1
global e2
label(root,text=”username”).place(x=10,y=10)
label(roo,text=”password”).place(x=10,y=40)
e1=Entry(root)
e1.place(x=140,y=10)
e2=Entry(root)ss
e2.place(x=140,y=40)
e2.config(show=””)
button(root,text”login”,command=ok,height=3,width=13).place(x=10,y=100)
root.mainloop()
#     Scipy
### What is scipy
Scipy is a scientific computation library scipy uses under Numpy.
Scipy stands for scientific python
Like NumPy,scipy is open source so we can use it freely
Scipy was created by Numpy creator Travis oliphant

Which language is scipy written In
Scipy is primarily written in python. but few segments are written in C

### Installation of scipy
If you have python and pip already installed on a system, then installation of scipy is very easy.
If we can install this scipy using this command
C:\user\your name\pip install scipy
Import scipy
Once install scipy then use the import scipy module
You went to use in your application by adding “fromscipy import module”:
Syntax:  from scipy import Constance
If you have imported Constance from scipy, the application will be ready to use it.
For example:
* How many cubic meters are  in one  liter
From scipy import Constance
Print(constants.liter)
o\p: 1 liter=0.0001

Firstly import the module from scipy with constant then print the constants. liter. It will show the cubic meters in one liter

Constants: scipy offers a set of mathematical constants, one is “liter” which returns 1 liter as cubic meters

#### How to check the scipy version in python
The scipy version is a string to store under the _version_attribute.
Example: version of scipy
Import scipy
Print(scipy._version_)
       o\p: it will be shown the latest version of scipy
Firstly we can import scipy module and then print the scipy._version_ .it will show the latest version of scipy

#### Scipy constants:
Scipy is more focused on scientific implementation, it also built-in scientific
#### constants
These constants can be useful when you are working with data science
* Example: print the constant value of PI

From scipy import constants
Print(constants.PI)
o\p:3.141492….
Firstly import module scipy with constant. than print constant.PI otherwise it will return the constant value of PI
##### Constant unit : 
A list of all units under the constant module can be using the dir() function
Example: 
list of all constants
From scipy import constants
Print(dir(constants)
Firstly import module scipy with constants .than print dir, constants.   it returns the list of all constants
#### Scipy sparse data
##### What is sparse data:
 
* Sparse data is data that has mostly unused elements.
* Unused elements mean that elements don’t carry any information
* It can be an array like this one:
* Example: [1, 0, 2, 4, 0, 0, 0]
* Sparse data is data  in which  values are zero
* Dense array: a data in which values are not equal to zero. This is 
* It is totally the opposite sparse data.
##### How to use sparse:
Scipy has a module,scipy. sparse that provides functions to deal with sparse data
There are two types of sparse matrices:
1 CSC
2 CSR
CSC: CSC stands for the compressed sparse column. Csc efficiently arithmetic, fast column slices.
CSR: CSR stands for the compressed sparse row.


* Scipy is a python library used to solve scientific and mathematical problems
* Built on Numpy
* Allows manipulation and visualizing
#### What is scipy:
 scipy is very popular library in python
Scipy is a free and open source python library used for scientific computing and technical computing

It is a collection of mathematical algorithms and convenience functions built on the Numpy extension of python.
It adds significant power to the interactive python session by providing the user with high-level commands and classes for manipulating and visualizing data.
##### Installing scipy:
Install scipy using pip
We can install the scipy library by using the pip command
Pip is a recursive acronym that stands for “pip installs packages “.
It is a standard package manager which is installed in most the operating system
It is a standard package manager which can be installed in most operating systems.
To install, run the following command in the terminal:
Pip install scipy
Sub packages in scipy 
Scipy. cluster: cluster algorithms are used to vector quantization /k means 
* Scipy. constants: these represent physical and mathematical constants
* Scipy.integrate:integration routines
* Scipy. lincoln: it is used for linear algebra routine
* Scipy.io:it is used for data input and output
* Scipy.ndinge:it is used for the n-dimension image
* Scipy.ord: orthogonal distance regression
* Scipy. optimized: it is used for optimized
* Scipy. signal: it is used in signal processing
* Scipy. sparse: sparse matrices and associated routines
* Scipy. spatial: spatial data structures and algorithms
* Scipy.stars: statistics.
* Scipy. waves: it is a tool for writing

Here we will see how to implement the K-means clustering algorithm which is one of the popular clustering algorithms.
 The k-means algorithm adjusts the classification of the observations into clusters and updates the cluster centroids until the position of the centroids is stable over successive iterations.
* SymPy is a symbolic mathematics library while SciPy is a numeric mathematics library.
*  SciPy does not understand anything to do with SymPy's symbols and it will only work with numeric values such as floats.
*  Sympy is a Python library for symbolic mathematics. It aims to become a full-featured computer algebra system (CAS) while keeping the code as simple as use

# Django
* To understand Django before you know python
* Django is a web framework.
##### Framework:
frameworks are software that is developed. Frameworks are used by developers to build the application.
##### The best frameworks in python: 
* Django
* Bottle
* Cherry py
* Falcon
* Pylons
##### Web framework works:
web frameworks is a software framework. that is designed to support the development of web applications.
##### Two web frameworks available in python
* Django
* Flask
##### Django:
* Django is a free open-source web application framework written in python.
*  Django is invented by Adrian Holovaty and Simon Willison.
* Adrian holovaty and Simon Willison used to like famous guitarist Django hainhardt such that they named this web framework as Django 
* Created in 2003 open sourced in 2005.
##### Versions:
* present version of Django was 4.1
##### Features of Django:
* Stability
* Excellent documentation
* Resolve security issues
* Highly scalable
* Utilizes SEO(search engine organization)
* Huge library of packages
##### Below Top companies that are using Django:
* Instagram.
* National Geographic
* Mozilla
* Spotify
* Pinterest
* Disqus
* Bitbucket
* Eventbrite

These 9  global companies are using Django
##### How to install Django:
* To install Django, you must have python installed, and a package manager like PIP.
* Django Requires Python
* To check if your system has Python installed, run this command in the command prompt:
##### Python—version
If Python is installed, you will get a result with the version number, like this
Python 3.9.2
##### Pip: 
* To install Django, you must use pip, which is included in Python from version 3.4.
* To check if your system has PIP installed, run this command in the command prompt:
##### Pip—version
* If PIP is installed, you will get a result with the version number.
For me, on a windows machine, the result looks like this:
Pip 20.2.3
##### Let's create a virtual environment
* Firstly we created a virtual environment for every Django project.
* Run this command in the command prompt:
* Py –m venv myproject
* This will set up a virtual environment, and create a folder named "myproject" with subfolders and files, like this:
* My project
* Include
* Lib 
* Scrips
* Pyvenv.cfg
* 
Then you have to activate the environment, by typing this command:
* Myproject\scripts\activate.bat

prompt Once the environment is activated, you will see this result in the command:
* (myproject)c:\users\your name
* Install Django
* Finally, we can install Django.

Django is installed using pip,with this command:
* py –m pip install Django
* Check Django Version
* You can check if Django is installed by asking for its version number like this:
##### Django-admin –version
* Now you are ready to create a Django project in a virtual environment on your computer.
##### Project creation:
* Once you have come up with a suitable name for your Django project, like mine:
* New project\ navigate to where in the file system you want to store the code (in the virtual environment) and run this command in the command prompt:
* Django-admin startproject new project
* An app is a web application that has a specific meaning in your project, like a homepage
* Django works on MVT architecture.
