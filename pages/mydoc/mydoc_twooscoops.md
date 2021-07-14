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
