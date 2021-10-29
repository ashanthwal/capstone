# Final Project for CS50 WEB

-This is the final project for CS50 Web Development built by Ashutosh Anthwal.

YouTube Link: https://youtu.be/RYn2J6djwqw

# A comprehensive documentation of all the files and folders.

### Capstone Folder

The capstone folder on the root directory is also the main Django project and contains the urls.py and settings.py for the capstone project. Following is description of the files and its contents:

1. settings.py

   - The settings.py file has the basic setup for the application. I have added the two apps used in the project under the INSTALLED_APPS and it connects them all together.
   - The file cotains the settings for email backend required to send emails. I have created an account and the file contains valid credentials (will delete them eventually).
   - It also has the paths set up for the static files and images used throughout the project.

2. urls.py
   This file contains the routes to all the paths on the web application, this includes user and projects paths to different sections/apps of the web-application.

### Templates Folder on the root directory

Additionally, the root path also contains a folder called templates. The templates folder as the name suggests contains html templates that are used in all the apps for the capstone project. This includes templates for some common designs and features like the nav bar, pagination and the main.html and reset and delete templates.

# Apps for the web application

Moving on the project is broadly divided into two Django apps;

1. Users
2. Projects

### users folder

The users app on the root directory, also named as the ‘user’ directory, deals with all the functionality and routes associated with users (app) or students who create an account on the application. It takes care of registration, login/logout, user profiles.

#### users/templates

The sub-folder within the app, called templates contains the html templates specific to the app. These templates extend the main.html template which can be found on the templates folder on the root directory of the capstone project. The main templates take care of pages for the user account creation, profile page, login and registration

#### users/models.py:

The models.py file has two data models for

1. personal profiles (Profile)

2. Skills

#### users/forms.py:

The file uses Django forms to quickly create some common form classes for the user app. The forms created in the file takes care of skills forms and user profile forms used in the application.

#### users/utils.py

The file contains two functions for pagination and search users by name or skills.

#### users/admin.py:

The user models created in models.py are registered under this file.

#### users/signals.py

The file contains code that sends welcome messages to users once they register with a valid email. The code listens to certain events/actions (example create or delete account) and performs the action when a new user registration is saved.

- EMAIL_HOST_USER & EMAIL_HOST_PASSWORD need to be configured and setup in the settings.py in order to send the emails using the account

I have created a test account and will delete it after the course, the credentials are already updated under the capstone/settings.py for the email client for now.

Follow the link for more information on Django SMTP library:
https://docs.djangoproject.com/en/3.2/topics/email/

### projects folder

The second app for this Django project is called projects and it sits on the root directory of the Capstone project. The projects app takes care of all the projects that were submitted by the users.

#### projects/templates

The templates folder in the projects folder contains three templates for the projects page, project form (to add a new project) and an individual project template.

#### projects/models.py

The models.py file in the projects folder contains the models related to the projects app. It has a model defined for a project, tags and for reviews for projects submitted by other users. Furthermore the models also contain methods to rate projects by highest rated, count votes and avoid duplicate votes to name a few features.

#### projects/forms.py:

The file uses Django forms to quickly create some common form classes for the projects app. The forms defined in this file are for the reviews by other users and a form to add new projects.

#### projects/utils.py

The file contains two functions for pagination and search by projects by technology used for projects(tags).

#### projects/admin.py:

The user models created in models.py are registered under this file.

### Static folder

The static folder on the root directory contains all the static files like images, css and javascript files used in the web application. The images file contains all the images used in the project. The styles folder has a file called app.css, this is the main css file for the entire project and contains all the styling. Lastly, I have used a third party opensource CSS library for quick styling and it sits in the uikit folder.

- the staticfiles folder is used by the app in production and is built from the static folder when we run the "python manage.py collectstaic" command.

### env Folder

The project is built using the Django Framework. I have also used a virtual environment for the project to better manage dependencies properly and avoid any conflicts. A detailed list of all the packages is also available under the requirements.txt file in the root folder.

The virtual environment package used is called virtualenv. Follow the link for more details on the package.
env: https://virtualenv.pypa.io/en/latest/installation.html

#### Installation:

- Pip install virualenv

I have decided to name the virtual environment as “env” as seen on the root directory. To activate or run the virtual environment cd (browse) in the env folder and enter the following command:

- Scripts/activate

# Distinctiveness and Complexity:

- This project intends to be a showcase for CS50 Web Development students, a place to display and keep track of their capstone projects, weekly projects and labs for CS50 and CS50 Web Programming. They can add project descriptions, their preffered tech stack, links to their youtube live demos, the source code and more. Thus, act as a central place to manage and display all the CS50 labs and projects.

- The web app allows students of CS50's Web Development course to create a personal profile and add their projects, for other students, users and staff to have a look. It can act as a one stop to look at what projects other students have built and be inspired.

- The project has an advanced search feature where users can search by project name, tech stack(eg Python), skills (tags) or by their names. They can also upvote/downvote a project so the most popular projects show on top.

- The project uses django's SMTP library to send emails on registration, account updates or cancellation. The module used is called smtplib
- The styling is mobile responsive for all screen sizes.

- Additionally they can view a student profile if they like a projects, here they can look at all the other projects they have built and shared; for this course and more.
- Additionaly, the web app allows students of CS50 to create a personal profile and add their projecsts, for other students, users and staff to have a look.

- The project has an advanced search feature where users can search by project name, tech stack(eg Python), skills (tags) or by their names. They can also upvote/downvote a project so the most popular projects show on top.

- The project has advanced authentication, authorization, validation and password reset functionality implemented.

- The styling is mobile responsive for all screen sizes.

- Additinally users can view a students profile if they like their project, here they can view all other projects built and shared by the student.

# Application Structure

- The project is broadly divided into two Django apps; users and projects.
- Projects app has three models for 1) projects 2) tags 3) review
- Users app has two models, for 1) personal profiles 2) skills
- the templates folder contains the common templaes used throughout the apps.
- the static folder contains all the static files like images, css and js

# How to run the application.

Follow the steps after downloading/cloning the files from the github repository:

- pip install and create virtualenv : scripts\activate
- cd into the folder
- pip install -r requirements.txt
- python manage.py runserver
