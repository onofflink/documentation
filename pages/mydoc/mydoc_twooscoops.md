---
title: two scoops of django
tags: [school django ]
last_updated: July 14, 2021
keywords: API, content API, UI text, inline help, context-sensitive help, popovers, tooltips
summary: "summary."
sidebar: mydoc_sidebar
permalink: mydoc_twoscoops.html
folder: mydoc
---

## chapter 3 django project layout

### project templates

https://github.com/pydanny/cookiecutter-django
Featured in this chapter.

https://github.com/grantmcconnaughey/cookiecutter-django-vue-graphql-aws
Also featured in this chapter.

https://djangopackages.org/grids/g/cookiecu

### default directory map

```
mysite/
├── manage.py
├── my_app
│ ├── __init__.py
│ ├── admin.py
│ ├── apps.py
│ ├── migrations
│ │
│ ├── models.py
│ ├── tests.py
│ └── views.py
└── __init__.py
└── mysite
├── __init__.py
├── asgi.py
├── settings.py
├── urls.py
└── wsgi.py
```

### Big map

```
<repository_root>/
├── <configuration_root>/
├── <django_project_root>/
```

`EADME.md, docs/ directory, manage.py, .gitignore, requirements.txt files, and other high-level files that are required for deployment and running the project.`

### cookiecutter map

```
.
├── bin
│   └── post_compile
├── compose
│   ├── local
│   │   ├── django
│   │   │   ├── Dockerfile
│   │   │   └── start
│   │   └── docs
│   │       ├── Dockerfile
│   │       └── start
│   └── production
│       ├── django
│       │   ├── Dockerfile
│       │   ├── entrypoint
│       │   └── start
│       ├── postgres
│       │   ├── Dockerfile
│       │   └── maintenance
│       │       ├── backup
│       │       ├── backups
│       │       ├── restore
│       │       └── _sourced
│       │           ├── constants.sh
│       │           ├── countdown.sh
│       │           ├── messages.sh
│       │           └── yes_no.sh
│       └── traefik
│           ├── Dockerfile
│           └── traefik.yml
├── config
│   ├── __init__.py
│   ├── settings
│   │   ├── base.py
│   │   ├── __init__.py
│   │   ├── local.py
│   │   ├── production.py
│   │   └── test.py
│   ├── urls.py
│   └── wsgi.py
├── CONTRIBUTORS.txt
├── cookiecutter
│   ├── conftest.py
│   ├── contrib
│   │   ├── __init__.py
│   │   └── sites
│   │       ├── __init__.py
│   │       └── migrations
│   │           ├── 0001_initial.py
│   │           ├── 0002_alter_domain_unique.py
│   │           ├── 0003_set_site_domain_and_name.py
│   │           ├── 0004_alter_options_ordering_domain.py
│   │           └── __init__.py
│   ├── __init__.py
│   ├── static
│   │   ├── css
│   │   │   └── project.css
│   │   ├── fonts
│   │   ├── images
│   │   │   └── favicons
│   │   │       └── favicon.ico
│   │   ├── js
│   │   │   └── project.js
│   │   └── sass
│   │       ├── custom_bootstrap_vars.scss
│   │       └── project.scss
│   ├── templates
│   │   ├── 403.html
│   │   ├── 404.html
│   │   ├── 500.html
│   │   ├── account
│   │   │   ├── account_inactive.html
│   │   │   ├── base.html
│   │   │   ├── email_confirm.html
│   │   │   ├── email.html
│   │   │   ├── login.html
│   │   │   ├── logout.html
│   │   │   ├── password_change.html
│   │   │   ├── password_reset_done.html
│   │   │   ├── password_reset_from_key_done.html
│   │   │   ├── password_reset_from_key.html
│   │   │   ├── password_reset.html
│   │   │   ├── password_set.html
│   │   │   ├── signup_closed.html
│   │   │   ├── signup.html
│   │   │   ├── verification_sent.html
│   │   │   └── verified_email_required.html
│   │   ├── base.html
│   │   ├── pages
│   │   │   ├── about.html
│   │   │   └── home.html
│   │   └── users
│   │       ├── user_detail.html
│   │       └── user_form.html
│   ├── users
│   │   ├── adapters.py
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── forms.py
│   │   ├── __init__.py
│   │   ├── migrations
│   │   │   ├── 0001_initial.py
│   │   │   └── __init__.py
│   │   ├── models.py
│   │   ├── tests
│   │   │   ├── factories.py
│   │   │   ├── __init__.py
│   │   │   ├── test_admin.py
│   │   │   ├── test_forms.py
│   │   │   ├── test_models.py
│   │   │   ├── test_urls.py
│   │   │   └── test_views.py
│   │   ├── urls.py
│   │   └── views.py
│   └── utils
│       ├── context_processors.py
│       └── __init__.py
├── docs
│   ├── conf.py
│   ├── howto.rst
│   ├── index.rst
│   ├── __init__.py
│   ├── make.bat
│   ├── Makefile
│   ├── pycharm
│   │   ├── configuration.rst
│   │   └── images
│   │       ├── 1.png
│   │       ├── 2.png
│   │       ├── 3.png
│   │       ├── 4.png
│   │       ├── 7.png
│   │       ├── 8.png
│   │       ├── f1.png
│   │       ├── f2.png
│   │       ├── f3.png
│   │       ├── f4.png
│   │       ├── issue1.png
│   │       └── issue2.png
│   └── users.rst
├── LICENSE
├── locale
│   └── README.rst
├── local.yml
├── manage.py
├── merge_production_dotenvs_in_dotenv.py
├── Procfile
├── production.yml
├── pytest.ini
├── README.rst
├── requirements
│   ├── base.txt
│   ├── local.txt
│   └── production.txt
├── requirements.txt
├── runtime.txt
├── setup.cfg
└── tree.md

37 directories, 120 files
.
├── bin
│   └── post_compile
├── compose
│   ├── local
│   │   ├── django
│   │   │   ├── Dockerfile
│   │   │   └── start
│   │   └── docs
│   │       ├── Dockerfile
│   │       └── start
│   └── production
│       ├── django
│       │   ├── Dockerfile
│       │   ├── entrypoint
│       │   └── start
│       ├── postgres
│       │   ├── Dockerfile
│       │   └── maintenance
│       │       ├── backup
│       │       ├── backups
│       │       ├── restore
│       │       └── _sourced
│       │           ├── constants.sh
│       │           ├── countdown.sh
│       │           ├── messages.sh
│       │           └── yes_no.sh
│       └── traefik
│           ├── Dockerfile
│           └── traefik.yml
├── config
│   ├── __init__.py
│   ├── settings
│   │   ├── base.py
│   │   ├── __init__.py
│   │   ├── local.py
│   │   ├── production.py
│   │   └── test.py
│   ├── urls.py
│   └── wsgi.py
├── CONTRIBUTORS.txt
├── cookiecutter
│   ├── conftest.py
│   ├── contrib
│   │   ├── __init__.py
│   │   └── sites
│   │       ├── __init__.py
│   │       └── migrations
│   │           ├── 0001_initial.py
│   │           ├── 0002_alter_domain_unique.py
│   │           ├── 0003_set_site_domain_and_name.py
│   │           ├── 0004_alter_options_ordering_domain.py
│   │           └── __init__.py
│   ├── __init__.py
│   ├── static
│   │   ├── css
│   │   │   └── project.css
│   │   ├── fonts
│   │   ├── images
│   │   │   └── favicons
│   │   │       └── favicon.ico
│   │   ├── js
│   │   │   └── project.js
│   │   └── sass
│   │       ├── custom_bootstrap_vars.scss
│   │       └── project.scss
│   ├── templates
│   │   ├── 403.html
│   │   ├── 404.html
│   │   ├── 500.html
│   │   ├── account
│   │   │   ├── account_inactive.html
│   │   │   ├── base.html
│   │   │   ├── email_confirm.html
│   │   │   ├── email.html
│   │   │   ├── login.html
│   │   │   ├── logout.html
│   │   │   ├── password_change.html
│   │   │   ├── password_reset_done.html
│   │   │   ├── password_reset_from_key_done.html
│   │   │   ├── password_reset_from_key.html
│   │   │   ├── password_reset.html
│   │   │   ├── password_set.html
│   │   │   ├── signup_closed.html
│   │   │   ├── signup.html
│   │   │   ├── verification_sent.html
│   │   │   └── verified_email_required.html
│   │   ├── base.html
│   │   ├── pages
│   │   │   ├── about.html
│   │   │   └── home.html
│   │   └── users
│   │       ├── user_detail.html
│   │       └── user_form.html
│   ├── users
│   │   ├── adapters.py
│   │   ├── admin.py
│   │   ├── apps.py
│   │   ├── forms.py
│   │   ├── __init__.py
│   │   ├── migrations
│   │   │   ├── 0001_initial.py
│   │   │   └── __init__.py
│   │   ├── models.py
│   │   ├── tests
│   │   │   ├── factories.py
│   │   │   ├── __init__.py
│   │   │   ├── test_admin.py
│   │   │   ├── test_forms.py
│   │   │   ├── test_models.py
│   │   │   ├── test_urls.py
│   │   │   └── test_views.py
│   │   ├── urls.py
│   │   └── views.py
│   └── utils
│       ├── context_processors.py
│       └── __init__.py
├── docs
│   ├── conf.py
│   ├── howto.rst
│   ├── index.rst
│   ├── __init__.py
│   ├── make.bat
│   ├── Makefile
│   ├── pycharm
│   │   ├── configuration.rst
│   │   └── images
│   │       ├── 1.png
│   │       ├── 2.png
│   │       ├── 3.png
│   │       ├── 4.png
│   │       ├── 7.png
│   │       ├── 8.png
│   │       ├── f1.png
│   │       ├── f2.png
│   │       ├── f3.png
│   │       ├── f4.png
│   │       ├── issue1.png
│   │       └── issue2.png
│   └── users.rst
├── LICENSE
├── locale
│   └── README.rst
├── local.yml
├── manage.py
├── merge_production_dotenvs_in_dotenv.py
├── Procfile
├── production.yml
├── pytest.ini
├── README.rst
├── requirements
│   ├── base.txt
│   ├── local.txt
│   └── production.txt
├── requirements.txt
├── runtime.txt
├── setup.cfg
└── tree.md

37 directories, 120 files
```


## Chapter 2

### virtualenv and pythonpath

```
You can also set your virtualenv’s PYTHONPATH to include the current directory with
the latest version of pip. Running “ pip install -e . ” from your project’s root
directory will do the trick, installing the current directory as a package that can be edited in place.

```
  
> django-admin and manage.py¶  
> [link](https://docs.djangoproject.com/en/3.2/ref/django-admin/)
django-admin is Django’s command-line utility for administrative tasks. This document outlines all it can do.

In addition, manage.py is automatically created in each Django project. It does the same thing as django-admin but also sets the DJANGO_SETTINGS_MODULE environment variable so that it points to your project’s settings.py file.

The django-admin script should be on your system path if you installed Django via pip. If it’s not in your path, ensure you have your virtual environment activated.

Generally, when working on a single Django project, it’s easier to use manage.py than django-admin. If you need to switch between multiple Django settings files, use django-admin with DJANGO_SETTINGS_MODULE or the --settings command line option.

The command-line examples throughout this document use django-admin to be consistent, but any example can use manage.py or python -m django just as well.

```
$ django-admin <command> [options]
$ manage.py <command> [options]
$ python -m django <command> [options]
```


### django and docker 

>References for developing with Docker:

- https://cookiecutter-django.readthedocs.io/en/latest/developing-locally-docker.html
- http://bit.ly/1dWnzVW Real Python article on Django and Docker Compose
- https://dockerbook.com
