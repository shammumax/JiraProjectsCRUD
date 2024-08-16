
# Project Title

API Automation of Jira Rest API  v3(beta) Collections
through Postman , Newman and Jenkins






# Project Description
With the help of this Jira Rest API end points we able to add/modify/update/delete Jira Projects .Automated these operations and executed through postman in local , executed through Newman on AWS EC2 instance and created a job for this on Jenkins .
Jenkins will do execution of this collection by picking it from github.

## End points 
1)https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-projects/#api-rest-api-3-project-post - To Create Project

2)https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-projects/#api-rest-api-3-project-projectidorkey-put - To Update project

3)https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-projects/#api-rest-api-3-project-projectidorkey-delete - To Delete Project

4)https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-projects/#api-rest-api-3-project-get - To Get All projects




## Tools 
* Postman
* Newman
* AWS EC2 Instance
* Jenkins
* Github

## Project Structural diagram
![postmanAutomation  MConverter eu](https://github.com/user-attachments/assets/3549daa3-6270-4271-a7af-6a7a22491b87)

## Practical Demo
Initial projects as follows,

![Manual1](https://github.com/user-attachments/assets/f07f6f91-ebeb-4cbf-bb84-c079ef1e019e)

After adding project through post request as follows,

![Manual2](https://github.com/user-attachments/assets/bc1eb4a6-fb13-4dba-a187-3d2210294cad)

After modifying project name through put request as follows,

![Manual3](https://github.com/user-attachments/assets/a9b77690-8675-4d0c-aa3f-78d2a0fe5115)

After deleting project through delete request as follows,

![Manual4](https://github.com/user-attachments/assets/e816d650-92a4-45f8-9807-7a1998638bc1)


## Execution through Newman in AWS EC2 instance as follows,

![Screenshot (10)](https://github.com/user-attachments/assets/8a39f251-ce91-44e4-a988-4fcd5906edc1)


![Screenshot (11)](https://github.com/user-attachments/assets/2840b766-c236-477b-980d-b998d61b8662)


## Commands executed to run the collection through Newman in AWS EC2 instance as follows,

newman run "/var/lib/jenkins/workspace/JiraProjectsOperations/JiraRestProjects.postman_collection" -g, --globals "/var/lib/jenkins/workspace/JiraProjectsOperations/workspace.postman_globals.json" --global-var "token=ATATT3xFfGF0mBN3qdQwpAZlbJkqF93ZdwUJqBxfqPMiIcBhTtykYfvmzM9D1zUiA5ooZ-2lEsrIhA-P8njKJhYpiy0znrGOhyXXRVqWnbL8KjrfLedOBFM-a23vk4YKduHV79SnvenrJYjg_Zv2r2ga86OhnNA4LF4ickzIZvly2zKtzBouwt0=9A10D472"



## Execution through Newman in Jenkins as follows,

![jenkinsfront](https://github.com/user-attachments/assets/c08c9d0a-629c-4da8-9c8e-ebd3eef70b2a)


![Screenshot (19)](https://github.com/user-attachments/assets/90005b2c-c9fa-4828-836c-46176b2cf4c9)


![Screenshot (20)](https://github.com/user-attachments/assets/21f2c2f7-3710-4d76-a134-32f66f5bd84e)


![Screenshot (21)](https://github.com/user-attachments/assets/ec21f977-6d15-4ae1-8bf0-1c81299ccdce)


![Screenshot (22)](https://github.com/user-attachments/assets/2abc0843-b881-473a-8cf9-b3506311d0c4)


## Shell Script commands executed while build process in Jenkins as follows,
#!/bin/bash

whoami

date

newman -version

newman run "/var/lib/jenkins/workspace/JiraProjectsOperations/JiraRestProjects.postman_collection" -g, --globals "/var/lib/jenkins/workspace/JiraProjectsOperations/workspace.postman_globals.json" --global-var "token=ATATT3xFfGF0mBN3qdQwpAZlbJkqF93ZdwUJqBxfqPMiIcBhTtykYfvmzM9D1zUiA5ooZ-2lEsrIhA-P8njKJhYpiy0znrGOhyXXRVqWnbL8KjrfLedOBFM-a23vk4YKduHV79SnvenrJYjg_Zv2r2ga86OhnNA4LF4ickzIZvly2zKtzBouwt0=9A10D472" -r cli,json

## Html Reports

![reports1](https://github.com/user-attachments/assets/38d00712-fe3d-409c-bfe8-22d2ebef3482)


![reports2](https://github.com/user-attachments/assets/aecf171c-d7ed-43f0-8437-aea59b8fa9f2)


