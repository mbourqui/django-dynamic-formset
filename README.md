

# A jQuery plugin for managing Django formsets

This [jQuery][] plugin helps you create more usable [Django][] formsets by
allowing clients add and remove forms on the client-side.

The latest versions of these documents can be found on the
Github web site for this application, which is located at
`https://github.com/mbourqui/django-dynamic-formset`.


# Installation instructions

There are two ways to install this application for use by your
projects; the first is to do a Subversion checkout::

    pip install https://github.com/mbourqui/django-formset-bootstrap


# Setting up the demo project

Once you've got the source code, run the following commands to set up the
SQLite3 database and start the development server::

    cd demo
    virtualenv venv
    source venv/bin/activate
    pip install -r requirements.txt
    chmod a+x manage.py
    ./manage.py syncdb
    ./manage.py runserver

You can now browse to ``http://localhost:8000/`` and view the examples.


  [python]:     https://www.python.org/             "Python"
  [django]:     https://www.djangoproject.com/      "Django"
  [jquery]:     http://jquery.com/                  "jQuery"
