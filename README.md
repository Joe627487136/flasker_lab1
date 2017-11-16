# Flasker Blog #
## Before running the server ##
a. Direct to your project directory in your terminal eg: cd /Users/zhouxuexuan/PycharmProjects/flasker_lab1

b. Then enter python enironment by key "python" in terminal

c. Create related database by python:

from flasker import db

db.create_all()

d. Under "Flasker" directory to setting.py

Please implement your own database access info:

eg:
SQLALCHEMY_DATABASE_URI = "mysql://root:somepassword@127.0.0.1:3306/Flasker_DB"




You can also refer to below screenshot if you have any problems during setup.
If you have encounter error of missing library package, please install before you create the database.

![Alt text](https://github.com/Joe627487136/flasker_lab1/blob/master/Setup_Screenshot/Screenshot%202017-09-26%2015.10.17.png?raw=true "Title")



## After the server is running ##

### Down below are several curl commands which can implement to create your user without using MySQL commands: ###

#### Create user(username="Teckwu3", password="teck123") ("POST"):
curl -H "Content-type: application/json" \ -X POST http://127.0.0.1:5000/User -d '{"username":"Teckwu3", "password":"teck123"}'

#### Update user with new password (username="Teckwu3", old password="teck123", new password="teck") ("PUT"):
curl -H "Content-type: application/json" \ -X PUT http://127.0.0.1:5000/User -d '{"username":"Teckwu3", "password":"teck123", "newpassword";"teck"}'

#### Delete user(username="Teckwu3", password="teck") ("DELETE"):
curl -H "Content-type: application/json" \ -X POST http://127.0.0.1:5000/User -d '{"username":"Teckwu3", "password":"teck"}'
