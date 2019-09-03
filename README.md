# Item-Catalog-Project
An Udacity Full Stack Web Developer II Nanodegree project 

## Description

In this project, you will be developing a web application that provides a list of items within a variety of categories and integrate third party user registration and authentication. Authenticated users should have the ability to post, edit, and delete their own items.

You will be creating this project essentially from scratch, no templates have been provided for you. This means that you have free reign over the HTML, the CSS, and the files that include the application itself utilizing Flask.

## About
This application provides a list of items within a variety of categories , Here you can view all the items filtered by a particular category.
Click on a specific category to view, add, or delete items.
as well as provide an authentication system.
Registered users will have the ability to post, edit, and delete their own items.

### Features
- Proper authentication and authorisation check.
- Full CRUD support using SQLAlchemy and Flask.
- JSON endpoints.
- Implements oAuth using Google Sign-in API.

### Project Structure
```
.
├── static 
│   └── style.css : Cascading Style Sheets (CSS) describe how documents are presented on screens
├── templates : HTML webpage templates.
│   ├── delete_category.html
│   ├── delete.html
│   ├── edit_category.html
│   ├── index.html
│   ├── items.html
│   ├── layout.html
│   ├── login.html
│   ├── new-category.html
│   ├── new-item-2.html
│   ├── new-item.html
│   ├── update-item.html
│   └── view-item.html
├── app.py : Main Flask app Python file.
├── client_secrets.json : json file used for authantication with google.
├── database_setup.py : Python file used to configure the database.
├── database_data.py : Python file used to populate the database.
├── itemcatalog.db : SQLite database.
└── README.md : This file, a concise description of the project.

```


## Project Requirements
System setup and how to view this project:

This project makes use of Udacity's Linux-based virtual machine (VM) configuration which includes all of the necessary software to run the application.

1. Download [Vagrant](https://www.vagrantup.com/) and install.
2. Download [Virtual Box](https://www.virtualbox.org/) and install. 
3. Clone or download the Vagrant VM configuration file from [here](https://github.com/udacity/fullstack-nanodegree-vm).
4. Clone this repository to a directory of your choice inside `vagrant/` sub-directory.


#### Run these commands from the terminal in the folder where your vagrant is installed in: 
1. ```vagrant up``` to start up the VM.
2. ```vagrant ssh``` to log into the VM.
3. ```cd /vagrant``` to change to your vagrant directory.
4. ```cd "type the location of this repo "``` to change to your repo directory.
5. ```python logs_project.py``` to run the reporting tool.
6. Install or upgrade Flask:
    ```bash
    sudo python -m pip install --upgrade flask
    ```
7. Set up the database:
    ```bash
    python database_setup.py
    ```
8. Insert dummy values. **If you don't run this, the application might not run.**
    ```bash
    python database_data.py
    ```
9. Run this application:
    ```bash
    python app.py
    ```
10. Open `http://localhost:5000/` in your browser, and start exploring .

## JSON endpoints
this application has 3 JSON Endpoints 

1. `http://localhost:5000/catalog.json`
    - Return JSON of all the items in the catalog.

2. `http://localhost:5000//categories/<int:category_id>/item/<int:item_id>/json`
	- Return JSON of a particular item in the catalog.

3. `http://localhost:5000//categories/json`
 	- Returns JSON of all the categories in the catalog.


## Need Help 
In case you run into any trouble, create an issue on GitHub.
I will make sure to look into it as soon as possible.
