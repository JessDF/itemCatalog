# Item Catalog

Udacity Fullstack Web Development Nanodegree Program - Project 6: Item Catalog

## You may need to run these commands:

	pip install flask
	pip install sqlalchemy
	pip install oath2client
	pip install requests

## PROMPT
You will develop an application that provides a list of items within a variety of categories as well as provide a user registration and authentication system. Registered users will have the ability to post, edit and delete their own items.

## SETTING UP THE ENVIRONMENT
To help with the setup of this project, you are provided with a vagrantfile
and two SQL scripts to set up the environment as intended for this project.  

Before you start:
Go to the [Google API Console](https://console.developers.google.com) and click "Credentials", then "Create Credentials", then "OAuth Client ID". This will bring you to a new screen fill in with:

1. Choose "Web application"
2. Project name can be whatever you want
3. Authorization Javascript origins: http://localhost:8080
4. Aurthorize Redirect URIs: 

	http://localhost:8080/category/ <br>
	http://localhost:8080/category/*
	
5. Then download the JSON file after saving and move it into the catalog folder and name it "client_secret.json"
6. You will also want to change the client ID within the templates/main.html file and the templates/login.html.

Follow these steps to get started:

1. Download [Vagrant](https://www.vagrantup.com/) and [Virtual Box](https://www.virtualbox.org/) and install.
2. Clone this repository to a directory of your choice.

   Now that you have everything in place, it's time to set up your virtual environment.
   
3. `cd` into `<FolderName>`:
   ```sh
   $ cd <FolderName>
   ```

4. Setting up Vagrant:
   ```sh
   $ vagrant up
   ```
   Once `vagrant up` has finished, you will see your shell prompt.

5. Log in to the virtual machine:
   ```sh
   $ vagrant ssh
   ```
   
6. Once logged in, navigate to the shared directory:
   ```sh
   cd /vagrant
   cd catalog
   ```
7. Run the python file:
   ```sh
   $ python item_catalog.py
   ```
8. In your browser go to: http://localhost:8080/
9. To exit the local server and close down vagrant:
   ```sh
   ^C
   $ exit
   $ vagrant halt
   ```
