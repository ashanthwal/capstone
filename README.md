# Final Project for CS50 WEB

-This is the final project for CS50 Web Development built by Ashutosh Anthwal.

# Distinctiveness and Complexity:

- This project intends to be a showcase for CS50 Web Development students, a place to display and keep a track of their capstone projects, weekly projects and labs. They can add project descriptions, the tech stack used, links to their youtube live demos or the source code on github. It can act as a central place to manage and display all the CS50 labs and projects.

- The web app allows students of CS50's Web Development course to create a personal profile and add their projecsts, for other students, users and staff to have a look. It can act as a one stop to look at what projects other students have built and be inspired.

- Users can search projects by project name, tech stack/tags(eg Python) or by their names. They can also upvote/downvote a project so the most popular projects show on top.

- Additinally they can view a student profile if they like a projects, here they can look at all the projects they have built for the course and more. There is NO option to add/follow other users, however you can send a message to them if you wish to collaborate.

* Application Structure

- The project is broadly divided into two Django apps; users and projects.
- Projects app has three models for 1) projects 2) tags 3) review
- Users app has three models as well, for 1) personal profiles 2) skills 3) message
- the templates folder contains the common templaes used throughout the apps.
- the static folder contains all the static files like images, css and js

# How to run the application.

Follow the steps after downloading/cloning the files from the github repository:

- pip install and create virtualenv : scripts\activate
- cd into the folder
- pip install -r requirements.txt
- python manage.py runserver
- the project does not include the keys for the EMAIL_HOST_USER and EMAIL_HOST_PASSWORD.
