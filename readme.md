## Implementation of Flask Web

This repo contains the source code to a complete social blogging applications with Flask, a python microframework from ground up.

This app is implemented based on miguelgrinberg O'Reilly book [Flask Web Development](http://www.flaskbook.com)

Demo app: https://cslapp.herokuapp.com/

Demo admin account: flask@demo.com; pwd: 123123123
Demo guest account: guest@demo.com; pwd: 123123123
Demo guest account: guest2@demo.com; pwd: 123123123

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
$ python manage.py deploy
```

##### Run Server

```
python manage.py runserver
```

##### Deployment to heroku

```sh
$ heroku login
Enter your Heroku credentials.
Email: adam@example.com
Password (typing will be hidden):
Authentication successful.
```

```sh
$ heroku create flask-base-demo
Creating ⬢ flask-base-demo... done
https://flask-base-demo.herokuapp.com/ | https://git.heroku.com/flask-base-demo.git

```

Next we can run `git push heroku master`. This will push all your existing code to the heroku repository. Additionally, heroku will run commands found in your `Procfile` which has the following contents:

```txt
web: gunicorn manage:app
worker: python -u manage.py run_worker
```

recreate the database
```
heroku run python manage.py deploy
```
