# 1.5 Describe the benefits of Python virtual environments

Isolate dependencies between projects to avoid conflicts

## venv

    python -m venv env

Activate the virtualenv in Linux:

    source env/bin/activate

Or in Windows:

    .\env\Scripts\activate.bat

Creates a virtual environment called `env` in the current working directory

## virtualenv

    pip install virtualenv
    virtualenv env

Activate the virtualenv in Linux:

    source env/bin/activate

Or in Windows:

    .\env\Scripts\activate.bat

If multiple versions of python are installed, can specify the version of Python with the `-p` flag:

    virtualenv -p /usr/bin/python3.7 env
    
## virtualenvwrapper

    pip install virtualenvwrapper(-win)

Create a virtualenv

    mkvirtualenv my_project

virtualenv virtual env will be created in the $WORKON_HOME directory

Activate the virtualenv

    workon my_project

virtualenvwrapper will find the virtual env for you as long as its in $WORKON_HOME
