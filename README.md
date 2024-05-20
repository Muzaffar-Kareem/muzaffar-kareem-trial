# muzaffar-kareem-trial
Repo for a Day Trial of Gaditek for Sr. Software Position.

**/////TASK # 01/////**
**Setup**
create an virtualenv
pip install -r requirements.txt which is present on main folder
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser

**Create an OAuth2 application by navigating to http://127.0.0.1:8000/admin/ and logging in with the superuser credentials. Add a new application under the "Applications" section with the necessary details:**
Client type: Confidential
Authorization grant type: Resource owner password-based
Redirect uris: http://localhost:8000/
Name: AuthApp

**Note: Copy ClientID and Client Secrete before Saving it else it will encrypted**


For Generating Token:
url: http://127.0.0.1:8000/auth/token/
Request : POST

Form Data:
grant_type:password
username:admin
password:adm1n123
client_id:<client id>
client_secret:<client secret>

**API REQUEST**

**GET ALL:**
url: http://127.0.0.1:8000/api/items/
Authorization: Bearer <token>
Request : GET

**GET by ID:**
url: http://127.0.0.1:8000/api/items/<id>/
Authorization: Bearer <token>
Request : GET

**POST:**
url: http://127.0.0.1:8000/api/items/
Authorization: Bearer <token>
Request : POST
Form Data:
name:Item1
price:100.55
description:Test Product


**PUT/PATCH:**
url: http://127.0.0.1:8000/api/items/<ID>
Authorization: Bearer <token>
Request : PUT
Form Data:
name:Item1
price:210.56
description:Test Product

**DELETE**
url: http://127.0.0.1:8000/api/items/<ID>
Authorization: Bearer <token>
Request : DELETE



**/////TASK # 02/////**
Script is under main folder named "script_task2"
