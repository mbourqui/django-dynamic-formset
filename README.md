[![Python](https://img.shields.io/badge/Python-3.4,3.5,3.6-blue.svg?style=flat-square)](/)
[![Django](https://img.shields.io/badge/Django-1.8,1.9,1.10,1.11-blue.svg?style=flat-square)](/)
[![License](https://img.shields.io/badge/License-BSD-blue.svg?style=flat-square)](/LICENSE)
[![PyPIv](https://img.shields.io/pypi/v/django-formset-bootstrap.svg?style=flat-square)](https://pypi.org/project/django-formset-bootstrap)
[![PyPIs](https://img.shields.io/pypi/status/django-formset-bootstrap.svg)](https://pypi.org/project/django-formset-bootstrap)



# A jQuery plugin for managing Django formsets

This [jQuery][] plugin helps you create more usable [Django][] formsets
by allowing clients add and remove forms on the client-side.

The latest versions of these documents can be found on the
Github web site for this application, which is located at
`https://github.com/mbourqui/django-dynamic-formset`.


## Requirements

* [Python][] >= 3.4
* [Django][] >= 1.8
* [jQuery][] >= 1.2.6


## Installation

### Using PyPI
1. Run `pip install django-formset-bootstrap`

### Using the source code
1. Make sure [Pandoc][] is installed
1. Run `./pypi_packager.sh`
1. Run `pip install dist/django_formset_bootstrap-x.y.z-[...].wheel`,
   where `x.y.z` must be replaced by the actual version number and
   `[...]` depends on your packaging configuration


## Configuration

1. Add `formset-bootstrap` to the `INSTALLED_APPS` in your project's
   settings (usually `settings.py`). This is required in order to be
   able to load the script from the static files of your project.


## Usage

In your templates using formsets, be sure to load the static files:

```Django
{% load static %}
```

Then include the script:

```Django
<script src="{% static 'formset_bootstrap/js/jquery.formset.js' %}" type="text/javascript"></script>
```

Finally, set up your dynamic formset:

```Django
<script type="text/javascript">
    $(function () {
        $('#formset-id fieldset').formset();
    });
</script>
```



# Setting up the demo project

Once you've got the source code, run the following commands to set up
the SQLite3 database and start the development server::

    cd demo
    virtualenv venv
    source venv/bin/activate
    pip install -r requirements.txt
    chmod a+x manage.py
    ./manage.py syncdb
    ./manage.py runserver

You can now browse to ``http://localhost:8000/`` and view the examples.

Credits

This is a fork of [django-dynamic-formset](https://github.com/elo80ka/django-dynamic-formset) from [elo80ka](https://github.com/elo80ka).


  [python]:     https://www.python.org/             "Python"
  [django]:     https://www.djangoproject.com/      "Django"
  [jquery]:     http://jquery.com/                  "jQuery"
  [pandoc]:     http://pandoc.org/index.html        "Pandoc"
