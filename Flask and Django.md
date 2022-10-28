Flask
Flask is a web framework written in python. Flask is a micro web application framework. Flask is a small and lightweight python web framework that provides valuable tools and features that make creating web applications in python easier. Flask was developed by Armin Ronacher, who leads a team of international python groups on python enthusiasts called POCCO projects. Flask does not support dynamic HTML pages. Flask is used on the WSGI toolkit and jinja2 template engine. Flask is a micro framework that does not include an ORM.
ORM- Object Relational Manager. Flask uses the jinja2 template engine. Flask is a back-end framework, which means that it provides the technologies, tools, and modules that can be used to build the actual functionalities of the web app rather than its design or look of it.
Web framework:
A web application framework and or simply a web framework represents a collection of libraries and modules that allow developers to write web applications.
Modules:
a python module is a file containing python definitions and statements. A module can define function classes and variables.
Libraries:
a python library is simply a collection of codes or modules of codes that we can use in a program for specific operations.
template engine:
A template engine enables you to use static template files in your application. At runtime, the template engine replaces variables in a template file with actual values and transforms the template into an HTML file sent to the client. This approach makes it easier to design an HTML page.
What is WSGI?
WSGI – WEB SERVER GATEWAY INTERFACE
WSGI is an interface between the web server and web apps for python. Mod _ WSGI is an Apache HTTP server module that enables Apache to server Flask applications.
What is jinja2?
Jinja2 is a web template engine that combines a template with a certain data source to render dynamic web pages.
COMPANIES USING FLASK :
Netflix.
MIT.
Airbnb. Reddit.
Lyft.
Zillow.
Mozilla.
MailGui, etc.
FEATURES OF FLASK:
• Development server and debugger.
• Integrated support for unit testing.
• RESTful request dispatching.
• Uses Jinja templating.
• Support for secure cookies (client-side sessions).
• 100% WSGI 1.0 compliant.
• Unicode-based.
• Complete documentation.
• Google App Engine compatibility.
• Extensions available to extend functionality.
ADVANTAGES OF FLASK:
• Scalable. Size is everything, and Flask's status as a microframework means that you.
• can use it to grow a tech project such as a web app incredibly quickly. ...
• Flexible.
• Easy.
• Lightweight.
• Documentation.
• Not a lot of tools.
• Difficult to get familiar with a larger Flask app.
• Maintenance costs.
Flask installation process:
first, we should install python. Python 2.6 or higher is usually required for the installation of the flask. Recommended that flask should be installed on python 2.7. we use the command prompt for flask installation.
install virtualenv for the development environment:
virtualenv is a virtual python environment builder. it is used to create multiple python environments side by side. The following command is used to create a virtual environment. Pip installs virtualenv once install virtual environment. Then create a folder for virtualenv mkdir new folder then push created new folder move to drive cd new folder virtual environment push to folder virtualenv venv now activate scripts for folder data move into virtual environment venv\ script\ activate now ready to install flask in this environment pip install flask now the installation successfully done check that version for command pip __version now we have to create the file in command prompt mkdir. flask (here flask is a file name) Now we check whether that file was saved or not for use this command in command prompt dir Now pip list command Cd flask dir (dir means checking that file is exited or not)
Sample program
 from flask import Flask
 app=Flask(name)
 @app.route('/')
 def HelloWorld():
 return 'python is a programming language
 if name=='main':
 app.run(debug=True)
this program when debugging mode is on, can be refreshed on Url code no need to run the program. After the run, this Here debug mode is off, this program will run again After running debug off mode Flask debug mode allows developers to locate any possible error and as well the location of the error, by logon a traceback of the error '/' URL is bound with the hello() function. When the home page of the web server is opened in the browser, the output of this function will be rendered accordingly. The Flask application is started by calling the run() function. The method should be restarted manually for any change in the code. To overcome this, debug support is enabled to track any error.
DJANGO
WHAT IS DJANGO?
Django is a free and open-source web application framework written in python. Django is a popular web framework. it is a high-level web framework Django is a backend server-side web framework. it is like most modern frameworks. Django is a python framework that makes it easier to create websites using python. Django is especially helpful for database-driven websites. Django follows the MVT design pattern (Model View Template). Django offers dynamic HTML pages.
MVT:
Django, a Python framework to create web applications, is based on Model–View–Template (MVT) architecture. Django is a software design pattern for developing a web application. It consists of the following three entities: 1. Model: 2. View : 3. Template:
1 . Model:
A is an object that defines the data structure in the Django application. It is responsible for maintaining the entire application's data for which it provides various mechanisms to add, update, read and delete the data in the database.
2 . view:
A view is a handler function that accepts HTTP requests, processes them, and returns the HTTP response . it retrieves the necessary data to fulfill the request using Models and renders them on the user interface using Templates. It can also create an HTML page using an HTML template dynamically, and populate it with data fetched from model
3. Template:
A Template is a text file that defines the structure or layout of the user interface. The text file can be any type of file; for example HTML, XML, etc. It can accept data from the view and render it using jinja syntax.
Companies using Django :
Instagram.
Coursera.
Mozilla.
Pinterest.
National Geographic.
Spotify.
Udemy.
Zapier, etc.
Advantages of Django Here are a few advantages of using Django can be listed out here − Object-Relational Mapping (ORM) __ Django provides a bridge between the data model and the database engine and supports a large set of database systems including MySQL, Oracle, Postgres, etc. Django also supports the NoSQL database through the Django-nonrenal fork. For now, the only NoSQL databases supported are MongoDB and google app engine. Multilingual __ Django supports multilingual websites through its built-in internationalization system. So you can develop your website, which would support multiple languages. Framework __ Django has built-in support for Ajax, RSS, Caching, and various other frameworks. Administration GUI − Django provides a nice ready-to-use user interface for administrative activities. Development Environment − Django comes with a lightweight webserver to facilitate end-to-end application development and testing. Django development environment consists of installing and setting up Python, Django, and a Database System. Since Django deals with web applications, it's worth mentioning that you would need a web server setup as well.
Disadvantages of Django-based systems :
lower flexibility.
lower compatibility with the latest technologies. monolithism.
the higher entry point for simple solutions.
the larger size of the code base.
Django installation:
Installing Django is very easy, but the steps required for its installation depend on your operating system. we create a virtual environment first, so then we go to the command prompt. In the command prompt first, go to drive and use this
command C: or D:
then folder create
command mkdir (folder name)
command dir
Use D drive or c drive. And then create the virtual environment. Virtualenv venv (venv-folder name) is the virtual environment folder name, Then created folder is moved to the drive. For use this
command . . . . . . virtualenv venv
command. . . . . . cd dir
then active scripts
command. . .. . . scripts\activate
dir use this command for folder creation or not. now create scripts, this is to activate the virtual environment. use this command to activate the script . . scripts\activate then back to the device for use this ##command . . . . . . cd.. And then install Django to use this
command . . . . . Pip install Django
Then create a project using this
command . . . . . Django-admin start project
any name now created a project then move to the drive. cd any name now create room for to send the project to client send easily with this room use
command . . . . . py .manage.py startapp
any name now goes to pycharm in go to file open, then opened created file Django created new project display like this . . . . .
New project:
      init.py

      asgi.py

      Settings.py

      urls.py

       wsgi.py

       Manage.py
now go to settings add room name and then go to models This is done in a file called urls.py The models are usually located in a file called models.py
What is managed:
A Manage is an interface through which database query operations are provided to Django models.
What are settings:
In settings, we have to add the app name The register function is used to add models to the Django admin so that data for those models can be created, deleted, updated, and queried through the user interface. We have to open p y charm after creating a new project and new app then now click on files and open the file which you created and here we see the both app and project and in that we can see the files. Next, open the setting files and add the file name with respected strings and commas last now move to the models.py file, and first, we write the class function then go to the terminal to create a shell, we are connecting the database to the python. Before going to the shell we move to d drive.
command. Py .\manage.py shell
Then import connection for use this
command . . . . . From Django.DB import connection
The next
command is C=connection cursor()
Now the exit
command is Exit()
Now do make the migration, here python file is changing into SQL from the app
command. . . Py .\manage.py makemigrations
we should migrate using the
command py .\manage.py migrate
Now to store the data we have to create the superuser using this
command. . . . py .\manage.py createsuperuser
Now create any name or Email Address u want to give then skip Create password, give any words or names Re-enter the password, and give the same words or names Now you created a superuser successfully After finishing it we have to run the server, we use to this
commands . . py .\manage.py runserver
after we get to the code, click on that code open in the URL. we add admin in URL code after then we go to pycharm and open in admin.py we have to do from app. app name import class beside what we represent that we take here logic is: from app. app name import name, To see we have to register in that logic is admin. site.register(class defines the name) after running the server we get the URL code open that code in the URL and add admin now open the link we see the app name now add the objects and save here objects are created but I want to see the details so again move to models.py in pycharm. Now define function it is called the dunder method Logic is def str(self): Then return self. name (what the information given in class that should be taken ) we can not get all full details if we need full details move to admin.py and use the class function that is classempolyerAdmin(admin.ModelAdmin): List _display =[what we want to display that we can give] Now register here again Admin. site. register(employee, employee admin) Then run the server Then we get all the details in the rows and columns. this is Django.
DEFERENCE BETWEEN DJANGO AND FLASK:
DJANGO ## FLASK
1 . Django is a full–stack web framework 1 . Flask is a lightweight framework that enables ready-to-use solutions with gives abundant features without Its batteries – included approach external libraries and is minimalist. .features . 2 . Django is suitable for multiple pages 2. Flask is suitable for only single-page applications. applications. 3 . The working style of Django is 3. The working style of the flask is Monolithic. diversified style. 4 . Django does not support any virtual 4 . Flask has an inbuilt debugger that offers Debugging. virtual debugging. 5 . Django framework supports the 5. Flask web framework allows the Mapping of URLs to views through a URL to class-based view with werkzeug. request. 6 . Django framework structure is more 6. The Flask web framework structure is conventional. random. 7 . Django supports dynamic HTML pages. 7 . Flask framework does not support Dynamic HTML. 8 . Best features 8. Best features (i) Open–source. (i) Extensive documentation . (ii) Great community. (ii) lightweight. (iii) Fast development. (iii) minimal features. (iv) Easy to learn (iv) Full control over the development. process. (v) secure . (v) open–source. 9 . Django is suitable for high–end 9 . Flask is suitable for companies and projects Technology companies like that want experimentation with the Instagram, Udemy, Coursera, etc . module, and architecture of the Framework like Netflix, Reddit, Airbnb, Etc.
Conclusion Django vs flask:
Django vs Flask: one is an open-source framework for rapid development while the latter is a light-end framework for standard functionalities. Django and Flask are types of frameworks written in the Python programming language. These python-based frameworks are considered to be one of the popular frameworks for web development, according to the Developers Survey 2018. After reading and understanding the in-depth detail about both of the web frameworks, one must easily conclude that both have their functionalities. It means that there must be a reason why both are among the popular python-based frameworks in the domain of web development. Flask renders full control and is highly suitable for small projects that necessitate experimentation. Django is complicated and requires vast knowledge but it stands out as one of the best frameworks for building sophisticated applications.


















  
