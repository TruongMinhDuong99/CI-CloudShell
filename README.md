# Overview

<TODO: complete this with an overview of your project>

## Project Plan
<TODO: Project Plan

* A link to a Trello board for the project
* A link to a spreadsheet that includes the original and final project plan>

## Instructions

<TODO:  
* Architectural Diagram (Shows how key parts of the system work)>

<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

* Project running on Azure App Service

* Project cloned into Azure Cloud Shell

* Passing tests that are displayed after running the `make all` command from the `Makefile`

* Output of a test run

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

* Running Azure App Service from Azure Pipelines automatic deployment

* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

* Output of streamed log files from deployed application

> 

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>
ssh-keygen -t rsa
cat /home/odl_user/.ssh/id_rsa.pub

git clone ...
cd CI-CloudShell
nano Makefile
nano requirements.txt
nano hello.py
nano test_hello.py
python3 -m venv ~/.myrepo
source ~/.myrepo/bin/activate
make all
deactivate

cd..
git clone git@github.com:udacity/nd082-Azure-Cloud-DevOps-Starter-Code.git
cp -r nd082-Azure-Cloud-DevOps-Starter-Code/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/* CI-CloudShell

cp -r nd082-Azure-Cloud-DevOps-Starter-Code/C2-AgileDevelopmentwithAzure/project/starter_files/.gitignore CI-CloudShell

cd CI-CloudShell
python3 -m venv ~/.myrepo
source ~/.myrepo/bin/activate
make all
export FLASK_APP=app.py
flask run

create new session
Switch Bash
python3 -m venv ~/.myrepo
source ~/.myrepo/bin/activate
cd CI-CloudShell
nano make_prediction.sh => edit port = 5000
./make_prediction.sh
CTRL + C
deactivate

cd CI-CloudShell
az webapp up --name project2-flask-app --resource-group Azuredevops --runtime "PYTHON|3.9"
copy name property
nano make_predict_azure_app.sh 
Change url website to project2-flask-app
./make_predict_azure_app.sh
check log: https://project2-flask-app.scm.azurewebsites.net/api/logs/docker
or az webapp log tail


Push source to git:
git add .
git config --global user.email "minhduong.truong99@gmail.com"
git config --global user.name "duong"
git commit -m "Update content"
git push -u origin main

Config Action Git
Replace  name pythonapp.yml
check version: python --version
Change content using python 3.9.19