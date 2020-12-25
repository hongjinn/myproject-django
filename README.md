## A very basic Django project

Not very different from doing ```django-admin startproject myproject```
For deployment on AWS with Nginx: https://github.com/hongjinn/myproject-django-gunicorn-nginx
For deployment on AWS with Apache: https://github.com/hongjinn/myproject-django-mod_wsgi-apache

```
# Directory structure

whateveryouwant/            # This is the only folder you can name whatever you want and is on your local machine but not on the EC2
    myproject/              # The is the root folder of this repository. This folder is on the EC2 and should keep the name myproject
        myapp/              # Folder for your Django app, this is the Django folder itself
            mysite/         # Houses the hello world template
        venv/               # Folder for the virtual environment that is needed for WSGI
        .git/               # Folder for Git
        .gitignore          # File that tells Git what to ignore
        requirements.txt    # Python dependencies, for example Django REST framework
        README.md           # The file that generates these instructions
```

## Getting started

```
git clone https://github.com/hongjinn/myproject-django        # Clone repository
mv myproject-django myproject                                 # Optional: rename the folder to myproject (for config files)
python3 -m venv venv                                          # Creates a venv called "venv"
source venv/bin/activate                                      # Now let's activate it
pip3 install -r requirements.txt                              # Install dependencies
python myproject/myapp/manage.py runserver                    # Start development server in myproject/myapp/manage.py
```
