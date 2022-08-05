## Django Login
## Set Up for Ubuntu.
First, install modules via venv and then activate your environment.  
Write a command to install requirements. Below are the commands to follow:
```
$ virtualenv env
$ source env/bin/activate
$ pip3 install -r requirements.txt 
```
 
## Setting  Up Database
Migrations are one of the features that come with Django. It automates the process of changing the database after modifications in the models. Below are the commands used to make migrations.
```
$ python3  manage.py makemigrations
$ python3  manage.py migrate
```
 
## Start the app
For output to be seen we mainly run the server at the terminal using this command:
```
$ python3  manage.py runserver
```
At this point, the app runs at [http://127.0.0.1:8000/]
 
## Create Users
By default, the app redirects guest users to authenticate. In order to access the private pages, follow this set up:
Access the sign-in page and authenticate
[http://127.0.0.1:8000/login/]
 
## Code-base structure
The project is coded using a simple and intuitive structure presented below:
```
< PROJECT ROOT >
   |stude
   |-- core/                               # Implements app configuration
   |    |-- settings.py                    # Defines Global Settings
   |    |-- wsgi.py                        # Start the app in production
   |    |-- urls.py                        # Define URLs served by all apps/nodes
   |
   |-- apps/
   |    |
   |    |-- home/                          # A simple app that serve HTML files
   |    |    |-- views.py                  # Serve HTML pages for authenticated users
   |    |    |-- urls.py                   # Define some super simple routes  
   |    |
   |    |-- authentication/                # Handles auth routes (login and register)
   |    |    |-- urls.py                   # Define authentication routes  
   |    |    |-- views.py                  # Handles login and registration  
   |    |    |-- forms.py                  # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/                     # Templates used to render page
   |         |-- accounts/                  # Authentication pages
   |         |    |-- login.html            # Login page
   |         |    |-- register.html         # Register page
   |         |
   |         |-- home/                      #successful Pages
   |              |-- index.html            # Index page
             |--layouts/
               |--base.html    
                       
                           
   |          
   |
   |-- requirements.txt                     # Development modules - SQLite storage
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- manage.py                            # Start the app - Django default start script
   ```
<img align="left" alt="GIF" src="media/Screenshot from 2022-08-04 22-37-08.png" width="470" height="350" />

<img align="right" alt="GIF" src="media/Screenshot from 2022-08-04 22-39-02.png" width="470" height="350" />

<img align="left" alt="GIF" src="media/Screenshot from 2022-08-04 22-39-07.png" width="470" height="350" />

<img align="right" alt="GIF" src="media/Screenshot from 2022-08-04 22-39-10.png" width="470" height="350" />
