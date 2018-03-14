## Implementation of Flask Web

This repo contains the source code to a complete social blogging applications with Flask, a python microframework from ground up.

### What's included
* User Authentication
* User Roles
* User Profiles
* Blog Posts
* Followers
* User Comments
* API
* Email
* Unit Testing

##### Initialize a virtualenv
```
$ pip install virtualenv
$ virtualenv -p python3 env
$ source env/bin/activate
```

##### Install the dependencies

```
$ pip install -r requirements.txt
```

##### Add Environment Variables

```
MAIL_USERNAME=GmailUsername
MAIL_PASSWORD=GmailPassword
SECRET_KEY=SuperRandomStringToBeUsedForEncryption
```

Other Key value pairs:

* `FLASKY_ADMIN`: set to the default email for your first admin account (default is `flasky@demo.com`)
* `DEV_DATABASE_URL`: set to a dev postgresql database url (default is `data-dev.sqlite`)
* `TEST_DATABASE_URL`: set to a test postgresql database url (default is `data-test.sqlite`)
* `DATABASE_URL`: set to a production postgresql database url (default is `data.sqlite`)

##### Create the database

```
$ python manage.py recreate_db
```

##### Run Server

```
python manage.py runserver
```
