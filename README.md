# Python Tutorial For Flask
> This is a tutorial I went through while going through the Bottega course.

## Start the server
- Run the following commands in your terminal while in the `python_flask` folder.
```
$ pipenv shell
(hello_flask) python app.py
```
- If you get an error saying it doesn't know about a package, you might need to install the packages, or you might not be in your `pipenv shell`
```
$ pipenv shell
(hello_flask) pipenv install
(hello_flask) python app.py
```

## Database Setup
- If you need to setup your database you will need to do the following inside a python repl while in your pipenv shell.
  - If you get a warning about `SQLALCHEMY_TRACK_MODIFICATIONS` it is ok.
```
>>> from fileName import db
>>> db.create_all()
```

## Routes
### GET ALL GUIDES
- url: localhost:5000/guides
### GET SINGLE GUIDE
- url: localhost:5000/guides/ID
### POST
- url: localhost:5000/guide
```json
body: {
	"title": "New York Pizza",
	"content": "$12"
}
```
### PUT
- url: localhost:5000/guide/ID
```json
body: {
	"title": "New York Pizza",
	"content": "$12"
}
```
### DELETE
- url: localhost:5000/guide/ID