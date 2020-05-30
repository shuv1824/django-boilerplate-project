# Django 3 Boilerplate Project
This is a boilerplate Django 3 project that includes 
some extensions/plugins for a better developer experience.

## Django Debug Toolbar
The first extension added to the project is the 
[Django Debug Toolbar](https://django-debug-toolbar.readthedocs.io/en/latest/) 
which provides some very handy debugging features 
in the development environment.

## Multiple Settings Module
For ease of debugging and deployment the `settings.py` 
file has been split into 3 different files. Inside the
main project directory a subdirectory named `settings` 
is included and inside that directory there are 3 files 
namely `base.py`, `development.py` and `production.py`. 
The `base.py` file contains all the mandatory settings. 
The `development.py` file contains only the settings 
required during development and the `production.py` file 
contains the settings those are only needed for production 
environment. In the `manage.py` file the `development.py` 
file is pointed by default. Before deploying to production 
it should be changed to `production.py`

## Python Decouple for Environment Variables
To isolate the sensitive data from the code `python-decouple` 
library is used and the secret variables are kept inside a 
`.env` file. Put all your sensitive information inside this 
file and reference in your `settings` files with `config()` 
from `decouple`. The `.env` file must be added to `.gitignore` 
for your projects. It is added to this repo for clarification. 

## How to use
To use this boilerplate as a starting Django project simply 
clone this repository and inside a python 3.6 or higher 
virtual environment run: 
```shell script
$ pip install -r requirements.txt
```
The project is named `demo`. So you can rename it with:
```shell script
$ python manage.py rename <your-project-name>
```
Your fresh Django 3 project is ready with some extra goodies. 
