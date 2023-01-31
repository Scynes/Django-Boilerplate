
# Django Project Boilerplate

A simple markdown for creating a Django project boilerplate using Pipenv. This setup does not go through prequisites such as installing Python.

## Pipenv (required for this boilerplate)

If you are familiar with running a virtual environment, than you've probably at some point ran into the issue of virtual environment becoming a pain to manage. 

Meet ```Pipenv```, a python package that streamlines and removes a lot of the legwork of numerous aspects of running a virtual environment. If you are familiar with running a ```Node.JS``` project, than welcome home.  ```Pipenv``` creates a ```Pipfile```which holds information about packages/dependencies running for the environment, and a ```Pipfile.lock``` JSON file that is similar to ```package-lock.json``` in Node.

You can find out more at https://github.com/pypa/pipenv


#### Install

```
pip3 install pipenv
```


## Boilerplate Setup

With ```Pipenv``` installed, we can now setup our Django boilerplate!

#### Step 1
First, navigate to a directory and create a project container folder. For the sake of this example, we will create a ```Django Boilerplate``` folder. I will be using MacOS for this setup.


```
mkdir "Django Boilerplate"

cd "Django Boilerplate"
```

#### Step 2
Next, inside of the "Django Boilerplate" directory we just created, we're going to install our ```pipenv``` dependencies for the project.

```
pipenv install Django

pipenv install Psycopg2-binary
```

After both dependencies are installed you should now see, in the same directory, ```Pipfile``` and ```Pipfile.lock```.

#### Step 3

Now we're going to start the virtual environment. This will allow us to use the packages we previously installed inside of a 'virtual instance'. Without that virtual instance, our project won't know what Django is! 

This is similar to when you fork a ```Node.JS``` project, but don't run ```npm install```. If the dependencies are not installed for the environment or in this case the environment isn't running, than our project doesn't know how to reference libraries used inside of the project!

```
pipenv shell
```

To end a virtual session -
```
exit
```

#### Step 4
With our virtual environment shell now active, we can proceed to creating the actual Django project structure.

```
django-admin startproject django-boilerplate .
```

Once this command is finished running, you should now see a folder structure inside of "Django Boilerplate" like below -

```bash
Django Boilerplate
├── Pipfile
├── Pipfile.lock
├── django_boilerplate
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── manage.py
```

#### Step 5
Congratulations! You're now ready to run your django project. Simply run the below 

MacOS
```
python3 manage.py runserver
```
Windows
```
python manage.py runserver
```




