# student-list project

Please find the specifications by clicking [here](https://github.com/diranetafen/student-list.git "here")

!["Crédit image : eazytraining.fr"](https://eazytraining.fr/wp-content/uploads/2020/04/pozos-logo.png) ![project](https://user-images.githubusercontent.com/18481009/84582395-ba230b00-adeb-11ea-9453-22ed1be7e268.jpg)

------------

Firstname : PIOBLI NINGA

Surname : JEAN-THIBAUT

For Eazytraining's DOCKER PROJECT

FRIDAY the 08th, JUNE 2023



## Application

I had to deploy an application named "*student_list*", which is very basic and enables POZOS to show the list of some students with their age.

student_list application has two modules:

- The first module is a REST API (with basic authentication needed) who send the desire list of the student based on JSON file
- The second module is a web app written in HTML + PHP who enable end-user to get a list of students


## The need

My work was to :
1) build one container for each module
2) make them interact with each other
3) provide a private registry


## My plan

First, let me introduce you the six ***files*** of this project and their role 

Then, I'll show you how I ***built*** and tested the architecture to justify my choices

Third and last part will be about to provide the ***deployment*** process I suggest for this application.


### The files' role

In my delivery you can find three main files : a ***Dockerfile***, a ***docker-compose.yml*** and a ***docker-compose.registry.yml***

- docker-compose.yml: to launch the application (API and web app)
- docker-compose.registry.yml: to launch the local registry and its frontend
- simple_api/student_age.py: contains the source code of the API in python
- simple_api/Dockerfile: to build the API image with the source code in it
- simple_api/student_age.json: contains student name with age on JSON format
- index.php: PHP  page where end-user will be connected to interact with the service to list students with their age# MINI-PROJET-DOCKER
