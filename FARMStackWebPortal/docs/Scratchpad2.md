
### Build Structure
This project was build using the self contained waterfall structure.
We reference is at the Project [BuildStructure.md](./docs/buildstructure.md)

### Flow of Execution

#### Backend vs FrontEnd.
The fundamental way the frontend frameworks interact with the backend is by making HTTP calls via AJAX.
The typical interface to the backend is a REST API

### Database 
PostgreSQL and SQLite are two relation databases, SQLAlchemy is an [ORM](##addlinkhere) which gives you a set of tools for accessing the data in the database.

While [SQLAlchemy](#addlinkhere) is the Python SQL toolkit and Object Relational Mapper that gives us the full power and flexibility of SQL, we will use [Beanie](#addlinkhere) as it works with [MONGODB](#addlinkhere),as it is the database we will use and is an  Object Document Mapper that gives application developers the full power and flexibility of a NoSQL Database.

## Testing and Building
### Testing

FastAPI is an API;that we use or create a tool that would simplify the API testing process. We will utilise [Postman](https://en.wikipedia.org/wiki/Postman_(software)) for testing the app, and all its functionality because Postman is an API platform for building and using APIs that simplifies each step of the API lifecycle.


all the run tests uploaded to the testing directory.

[/coverage]

## Production

[/build]

### [Deployments](https://fastapi.tiangolo.com/deployment/)
To deploy an application means to perform the necessary steps to make it available to the users.
For a web API, it normally involves putting it in a remote machine, with a server program that provides good performance, stability, etc, so that your users can access the application efficiently and without interruptions or problems.
This is in contrast to the development stages, where we are constantly changing the code, breaking it and fixing it, stopping and restarting the development server, etc.

Deploying a FastAPI application is relatively easy.

#### Deployment Strategies
Depending on our specific use case and the tools that we use.when deploying a FastAPI application (although most of it applies to any other type of web application).

- We could deploy a server ourselves(Local Deployment) using a combination of tools, or
- We could use a [cloud service](#addlinkshere) and make a cloud deployment that does part of the work for us, or other possible options.

####  Cloud Deployment
Cloud Deployment with [linode-deploy-gunicorn-uvicorn-nginx](https://christophergs.com/tutorials/ultimate-fastapi-tutorial-pt-6b-linode-deploy-gunicorn-uvicorn-nginx/)

#### Local Deployment
-- Requirements for Local Deployment
+ [nginx-unit](https://unit.nginx.org/howto/fastapi/) : 
Nginx-unit is a Fast API 
+ [VirtualBox](#) : 
Virtual Box is a tool that is used to setup a virtual workspace using images
+ [Vagrant](#addvagrantlinkshere)
Vagrant is a tool for building and distributing development environments-

### References

[Generate Gitignore Files](#addlinkhere)

[Build a FARM Stack](#addlinkhere).

[FASTAPI](#addlinkhere)

[API documentation](https://github.com/swagger-api/swagger-ui)

[Pydantic Utilised Models](https://docs.pydantic.dev/latest/concepts/models/)

[Swagger-UI](https://github.com/swagger-api/swagger-ui)
* Swagger UI is a collection of HTML, JavaScript, and CSS assets;
* That dynamically generate beautiful documentation from a Swagger-compliant API.

[Auth Login Page](https://dev.to/athulcajay/fastapi-auth-login-page-48po
)
[Micro Frontends](https://www.telerik.com/blogs/building-micro-frontends)

[FastApiUsers](https://fastapi-users.github.io/fastapi-users)

## References

#### Back End


#### Front End
*   [Dash Framework for Python](http://www.dash.plotly.com)
*   [Getting-started](https://create-react-app.dev/docs/getting-started/)
*   [Create-React-App](https://github.com/facebook/create-react-app)

*  [Create React Front End](https://christophergs.com/tutorials/ultimate-fastapi-tutorial-pt-12-react-js-frontend/#theory)

### [Provisioning](#)

- [Automated](#)

- [Manual](#)

### [Deployments](https://fastapi.tiangolo.com/deployment/)
Deploying our FastAPI application is relatively easy.

#### Deployment Strategies
####  Cloud Deploy - Here we use a cloud service that does part of the deployment for us, or other possible options.

+ [Cloud Deploy using Linode](https://christophergs.com/tutorials/ultimate-fastapi-tutorial-pt-6b-linode-deploy-gunicorn-uvicorn-nginx/)

#### Local Deploy.
We deploy a server ourselves using a combination of tools)

Requirements
+ [vagrant](https://github.com/hashicorp/vagrant)
+
+ [install vagrant](https://developer.hashicorp.com/vagrant/install)
+
+ [nginx-unit](https://unit.nginx.org/howto/fastapi/)
+
+ [VirtualBox](#)

#### Integrations
+ [Unit](https://unit.nginx.org/howto/integration/)

[Data Visualisation with dash](https://dash.plotly.com/)
####  Documentation
#### [Redoc API Documentation](https://github.com/Redocly/redoc)

#### [Pycharm Documentation](https://www.jetbrains.com/help/pycharm/set-up-a-git-repository.html)

#### [sqlalchemy](https://www.sqlalchemy.org/)

###### ScratchPad

````
##
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
return {"message": "Hello World"}
@app.get("/api/v1/users")
async def get_users():
return db


@app.get("/hello/{name}")
async def say_hello(name: str):
return {"message": f"Hello {name}"}


## # main.py
@app.get("/api/v1/users")
async def get_users():
return db

##

# main.py

###

from uuid import UUID
from fastapi HTTPException
@app.delete("/api/v1/users/{id}")

async def delete_user(id: UUID):
for user in db:
if user.id == id:
db.remove(user)
return
raise HTTPException(
status_code=404, detail=f"Delete user failed, id {id} not found."
)



# main.py
from uuid import UUID
from fastapi import FastAPI, HTTPException
@app.delete("/api/v1/users/{id}")
async def delete_user(id: UUID):
for user in db:
if user.id == id:
db.remove(user)
return
raise HTTPException(
status_code=404, detail=f"Delete user failed, id {id} not found."
)

## 
db: List[User] = [
User(
id=uuid4(),
first_name="John",
last_name="Doe",
gender=Gender.male,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="Jane",
last_name="Doe",
gender=Gender.female,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="James",
last_name="Gabriel",
gender=Gender.male,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="Eunit",
last_name="Eunit",
gender=Gender.male,
roles=[Role.admin, Role.user],
),
]
@app.get("/")
async def root():
return {"message": "Hello World"}
@app.get("/api/v1/users")
async def get_users():
return db
@app.post("/api/v1/users")
async def create_user(user: User):
db.append(user)
return {"id": user.id}

=======
# main.py
from typing import List
from uuid import uuid4

import fastapi
from fastapi import FastAPI
from models import Gender, Role, User
from uuid import UUID
from fastapi import fastAPI, HTTPException
from fastapi import FastAPI
app = FastAPI()
from uuid import UUID
from fastapi import FastAPI, HTTPException

db: List[User] = [
User(
id=uuid4(),
first_name="John",
last_name="Doe",
gender=Gender.male,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="Jane",
last_name="Doe",
gender=Gender.female,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="James",
last_name="Gabriel",
gender=Gender.male,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="Eunit",
last_name="Eunit",
gender=Gender.male,
roles=[Role.admin, Role.user],
),
]
@app.get("/")
async def root():
return {"message": "Hello World"}
@app.get("/api/v1/users")
async def get_users():
return db
@app.post("/api/v1/users")
async def create_user(user: User):
db.append(user)
return {"id": user.id}
@app.delete("/api/v1/users/{id}")
async def delete_user(id: UUID):
for user in db:
if user.id == id:
db.remove(user)
return
raise HTTPException(status_code= 404, detail=f"Delete user failed, id {id} not found."
)

````
###
```` 


````

### Scratchpad
This scratchpad exists as evidence for purposes of documenting the steps and processes of this work.
Alot of ideas and information exists here.I choose to add it here for purposes of deisgn, ideation and build of this project.

### Build Structure
This project was build using the self contained waterfall structure.
We reference  is at the Project [BuildStructure.md](./docs/buildstructure.md)

### Flow of Execution

#### Backend vs FrontEnd.
The fundamental way the frontend frameworks interact with the backend is by making HTTP calls via AJAX.
The typical interface to the backend is a REST API

### Database 
PostgreSQL and SQLite are two relation databases, SQLAlchemy is an [ORM](##addlinkhere) which gives you a set of tools for accessing the data in the database.

While [SQLAlchemy](#addlinkhere) is the Python SQL toolkit and Object Relational Mapper that gives application developers the full power and flexibility of SQL, it provides a full suite of well known enterprise-level persistence patterns, designed for efficient and high-performing database access, adapted into a simple and Pythonic domain language. 
So basically SQLAlchemy gives you the tools to access SQL databases such as PostgreSQL and SQLite Mysql etc, and query them in a pythonic way.

## Testing and Building

## Building


### Testing
Apart from the initial API tests in the [tests](test_main_http.py) 

FastAPI is an API;this means that we use or create a tool that would simplify the API testing process
We will utilise [Postman](https://en.wikipedia.org/wiki/Postman_(software)) for testing the app, and all its functionality because Postman is an API platform for building and using APIs that simplifies each step of the API lifecycle and


and all the run tests uploaded to the testing directory.
#### Testing
Testing of our project is done in the [/coverage](##) directory.

### Production
Production builds are in the [/build](##) directory

### [Deployments](https://fastapi.tiangolo.com/deployment/)
To deploy an application means to perform the necessary steps to make it available to the users.
For a web API, it normally involves putting it in a remote machine, with a server program that provides good performance, stability, etc, so that your users can access the application efficiently and without interruptions or problems.
This is in contrast to the development stages, where we are constantly changing the code, breaking it and fixing it, stopping and restarting the development server, etc.

Deploying a FastAPI application is relatively easy.

#### Deployment Strategies
Depending on our specific use case and the tools that we use.when deploying a FastAPI application (although most of it applies to any other type of web application).

- We could deploy a server ourselves(Local Deployment) using a combination of tools, or
- We could use a [cloud service](#addlinkshere) and make a cloud deployment that does part of the work for us, or other possible options.

####  Cloud Deployment
Cloud Deployment with [linode-deploy-gunicorn-uvicorn-nginx](https://christophergs.com/tutorials/ultimate-fastapi-tutorial-pt-6b-linode-deploy-gunicorn-uvicorn-nginx/)

#### Local Deployment
-- Requirements for Local Deployment
+ [nginx-unit](https://unit.nginx.org/howto/fastapi/) : 
Nginx-unit is a Fast API 
+ [VirtualBox](#) : 
Virtual Box is a tool that is used to setup a virtual workspace using images
+ [Vagrant](#addvagrantlinkshere)
Vagrant is a tool for building and distributing development environments-

### References

[Generate Gitignore Files](#addlinkhere)

[Build a FARM Stack](#addlinkhere).

[FASTAPI](#addlinkhere)

[API documentation](https://github.com/swagger-api/swagger-ui)

[Pydantic Utilised Models](https://docs.pydantic.dev/latest/concepts/models/)

[Swagger-UI](https://github.com/swagger-api/swagger-ui)
* Swagger UI is a collection of HTML, JavaScript, and CSS assets;
* That dynamically generate beautiful documentation from a Swagger-compliant API.

[Auth Login Page](https://dev.to/athulcajay/fastapi-auth-login-page-48po
)
[Micro Frontends](https://www.telerik.com/blogs/building-micro-frontends)

[FastApiUsers](https://fastapi-users.github.io/fastapi-users)

References
=======
### Back End


### Front End
*   [Dash Framework for Python](http://www.dash.plotly.com)
*   [Getting-started](https://create-react-app.dev/docs/getting-started/)
*   [Create-React-App](https://github.com/facebook/create-react-app)

*  [Create React Front End](https://christophergs.com/tutorials/ultimate-fastapi-tutorial-pt-12-react-js-frontend/#theory)

### [Provisioning](#)

- [Automated](#)

- [Manual](#)

### [Deployments](https://fastapi.tiangolo.com/deployment/)
Deploying our FastAPI application is relatively easy.

#### Deployment Strategies
####  Cloud Deploy - Here we use a cloud service that does part of the deployment for us, or other possible options.

+ [Cloud Deploy using Linode](https://christophergs.com/tutorials/ultimate-fastapi-tutorial-pt-6b-linode-deploy-gunicorn-uvicorn-nginx/)

#### Local Deploy.
We deploy a server ourselves using a combination of tools)

Requirements
+ [vagrant](https://github.com/hashicorp/vagrant)
+
+ [install vagrant](https://developer.hashicorp.com/vagrant/install)
+
+ [nginx-unit](https://unit.nginx.org/howto/fastapi/)
+
+ [VirtualBox](#)

#### Integrations
+ [Unit](https://unit.nginx.org/howto/integration/)

[Data Visualisation with dash](https://dash.plotly.com/)
####  Documentation
#### [Redoc API Documentation](https://github.com/Redocly/redoc)

#### [Pycharm Documentation](https://www.jetbrains.com/help/pycharm/set-up-a-git-repository.html)

#### [sqlalchemy](https://www.sqlalchemy.org/)

###### ScratchPad

````
##
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
return {"message": "Hello World"}
@app.get("/api/v1/users")
async def get_users():
return db


@app.get("/hello/{name}")
async def say_hello(name: str):
return {"message": f"Hello {name}"}


## # main.py
@app.get("/api/v1/users")
async def get_users():
return db

##

# main.py

###

from uuid import UUID
from fastapi HTTPException
@app.delete("/api/v1/users/{id}")

async def delete_user(id: UUID):
for user in db:
if user.id == id:
db.remove(user)
return
raise HTTPException(
status_code=404, detail=f"Delete user failed, id {id} not found."
)



# main.py
from uuid import UUID
from fastapi import FastAPI, HTTPException
@app.delete("/api/v1/users/{id}")
async def delete_user(id: UUID):
for user in db:
if user.id == id:
db.remove(user)
return
raise HTTPException(
status_code=404, detail=f"Delete user failed, id {id} not found."
)

## 
db: List[User] = [
User(
id=uuid4(),
first_name="John",
last_name="Doe",
gender=Gender.male,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="Jane",
last_name="Doe",
gender=Gender.female,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="James",
last_name="Gabriel",
gender=Gender.male,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="Eunit",
last_name="Eunit",
gender=Gender.male,
roles=[Role.admin, Role.user],
),
]
@app.get("/")
async def root():
return {"message": "Hello World"}
@app.get("/api/v1/users")
async def get_users():
return db
@app.post("/api/v1/users")
async def create_user(user: User):
db.append(user)
return {"id": user.id}

=======
# main.py
from typing import List
from uuid import uuid4

import fastapi
from fastapi import FastAPI
from models import Gender, Role, User
from uuid import UUID
from fastapi import fastAPI, HTTPException
from fastapi import FastAPI
app = FastAPI()
from uuid import UUID
from fastapi import FastAPI, HTTPException

db: List[User] = [
User(
id=uuid4(),
first_name="John",
last_name="Doe",
gender=Gender.male,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="Jane",
last_name="Doe",
gender=Gender.female,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="James",
last_name="Gabriel",
gender=Gender.male,
roles=[Role.user],
),
User(
id=uuid4(),
first_name="Eunit",
last_name="Eunit",
gender=Gender.male,
roles=[Role.admin, Role.user],
),
]
@app.get("/")
async def root():
return {"message": "Hello World"}
@app.get("/api/v1/users")
async def get_users():
return db
@app.post("/api/v1/users")
async def create_user(user: User):
db.append(user)
return {"id": user.id}
@app.delete("/api/v1/users/{id}")
async def delete_user(id: UUID):
for user in db:
if user.id == id:
db.remove(user)
return
raise HTTPException(status_code= 404, detail=f"Delete user failed, id {id} not found."
)

````
###
```` 
#### MUST DO LIST
-Create main.py ,and must be in the the install directory(Root top level, and following the whole path of the a
-First do a packages update using the pip install upgrade command(in yellow-see-screenshot)
-Activation of the pip script must be done in the install directory(Root top level, and following the whole path of the activate script, see screensnapshot)
-To instantiate fastapi and python within the same venv, you must run it
-To run uvicorn, you must be in Command Prompt(see snapshot)

#### DONT DO LIST


#### THINGS TO REMEMBER
-- All snapshots and guides are in the snapshots folder.
--For typesafety, i have added the folder to gitignore file.

#### TO DO LIST
======

````

## Tools

## Software

### References

#### The following literature was utilised in this work.

#### Incase there is an errors to the authors and publishers,Please add yourself to the [Authors file](##)
-- OR Make a [pull request](##)

* [Foundations of making an app](##)

* [APIs](##)

* [Node.js](##) 

* [React](##)

* [Express](##)

* [Mongodb](##)

These were made with [Sphinx docs](##)

##Must Know Items
[Local Setup](https://github.com/ChristopherGS/ultimate-fastapi-tutorial/tree/main/part-01-hello-world)

[Poetry](https://earthly.dev/blog/python-poetry/)

[Web Framework]

[Login & Authentication]

[Documentation]

[fastapi](https://unit.nginx.org/howto/fastapi/)

[fastapi-people](https://fastapi.tiangolo.com/fastapi-people/)

[deploying-a-fastapi-app-with-nginx]()ttps://levelup.gitconnected.com/deploying-a-fastapi-app-with-nginx-supervisor-and-gunicorn-1e97e7421b46

[create-react-app](https://create-react-app.dev/docs/getting-started/)

https://binary-factory.kde.org/view/Windows%2064-bit/job/KDevelop_Release_win64/2141/badge/

[fastapi deployment](https://fastapi.tiangolo.com/deployment/)

[oauth configuration](https://fastapi-users.github.io/fastapi-users/12.1/configuration/oauth/)



#### MUST DO LIST
-Create main.py ,and must be in the the install directory(Root top level, and following the whole path of the a
-First do a packages update using the pip install upgrade command(in yellow-see-screenshot)
-Activation of the pip script must be done in the install directory(Root top level, and following the whole path of the activate script, see screensnapshot)
-To instantiate fastapi and python within the same venv, you must run it
-To run uvicorn, you must be in Command Prompt(see snapshot)

#### DONT DO LIST


#### THINGS TO REMEMBER
-- All snapshots and guides are in the snapshots folder.
--For typesafety, i have added the folder to gitignore file.

#### TO DO LIST
* Add SignUp Form to React App USING firebase
* And Login Form to React App using Firebase
* Add File Upload Form to React App
* Connect Database
* 
======

####
Would you like to define your main dependencies interactively? (yes/no) [yes] yes
You can specify a package in the following forms:
- A single name (requests): this will search for matches on PyPI
- A name and a constraint (requests@^2.23.0)
- A git url (git+https://github.com/python-poetry/poetry.git)
- A git url with a revision (git+https://github.com/python-poetry/poetry.git#develop)
- A file path (../my-package/my-package.whl)
- A directory (../my-package/)
- A url (https://example.com/packages/my-package-0.1.0.tar.gz)
###

This command will guide you through creating your pyproject.toml config.

Package name [webservportalproject]:  webservportalproject
Version [0.1.0]:  0.1.0
Description []:  This is a Web Services Portal Project      
Author [<biyita19@gmail.com>, n to skip]:  biyita19@gmail.com
License []:  MIT;GPL
Compatible Python versions [^3.9]:  ^3.9

Would you like to define your main dependencies interactively? (yes/no) [yes] yes
You can specify a package in the following forms:
- A single name (requests): this will search for matches on PyPI
- A name and a constraint (requests@^2.23.0)
- A git url (git+https://github.com/python-poetry/poetry.git)
- A git url with a revision (git+https://github.com/python-poetry/poetry.git#develop)
- A file path (../my-package/my-package.whl)
- A directory (../my-package/)
  license = "MIT;GPL"
  readme = "README.md"

[tool.poetry.dependencies]
python = "^3.9"


[build-system]
requires = ["poetry-core"]
build-backend = "poetry.core.masonry.api"


''

'

#### MUST DO LIST

-- All snapshots and guides are in the snapshots folder.
--For typesafety, i have added the folder to gitignore file.
-- [Flow of Execution](...docs/references.md)
-- [Add clean code workflow](...docs/workflows.md)
-- Create main.py ,and must be in the the install directory(Root top level, and following the whole path of the a
-- First do a packages update using the pip install upgrade command(in yellow-see-screenshot)
-- Activation of the pip script must be done in the install directory(Root top level, and following the whole path of the activate script, see screensnapshot)
-- To instantiate fastapi and python within the same venv, you must run it
-- To run uvicorn, you must be in Command Prompt(see snapshots folder)

**
/
