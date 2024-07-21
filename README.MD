### Project Creation

To set up a virtual environment (venv) for your project that you can activate with the command source venv/bin/activate, follow these steps:

1. `python3 -m venv venv`

2. To activate the virtual environment run the command:

`source venv/bin/activate`

3. In `Flask`, the `FLASK_APP` environment variable is used to specify how to load the application which can be set to a python file, a module, or a package. In this case, it's being set to the `app.py` file which is where my `Flask` application is defined. When you execute the command `flask run`, `Flask` uses the value of `FLASK_APP` to find my application and run it. If `FLASK_APP` is not set, `Flask` won't know where the application is and won't be able to run it. So before you run the application you must run the command:

`export FLASK_APP=app.py`

4. Now you can run the application with the debugger module activated using the command:

`flask run --debugger`

### running the application:

[Back to TOC](#notarious---table-of-contents)

1. There is a virtual environment already set up for this project so you need to activate it:

`source venv/bin/activate`

2. In Flask, the `FLASK_APP` environment variable is used to specify how to load your application. It can be set to a python file, a module, or a package. In this case, it's being set to the `app.py` file, which is presumably where your Flask application is defined.

When you run `flask run`, Flask uses the value of `FLASK_APP` to find your application and run it. If `FLASK_APP` is not set, Flask won't know where your application is and won't be able to run it. So before you run the application you must run the command:

`export FLASK_APP=app.py`

3. Now you can run the application:

`flask run --debugger`

### psql and the database:

1. Since this is a Unix-based system you must activate the PostgreSQL service with the command:
   NB--> be prepared to enter your `psql` password

`sudo service postgresql start`

2. To log in to your PSQL account you must use the `psql` command with the `-U` option followed by your username:

`psql -U your_username`

### How to use `flask_migrate`

To generate a migration script and update your data models using Flask-Migrate, follow these steps:

1. Generate Migration Script: This command auto-generates a migration script from the detected changes in the models.