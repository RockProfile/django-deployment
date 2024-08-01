Django Deployment
=========

Django Deployment is a role that deploys a Django application on a server. It installs the required packages,
creates a virtual environment, and sets up the Django application.

Requirements
------------

The role requires the following packages to be installed on the server:

- ansible >= 2.1

During the deployment, the role will install the following packages:

- apache2
- certbot
- git
- libapache2-mod-wsgi-py3
- mod_wsgi
- python3.11
- python3-certbot-apache

Role Variables
--------------

## Required Variables

The following variables must be defined in the playbook:

### django_allowed_hosts

Defines the allowed hosts for the Django application.

### django_git_url

Define the URL of the Git repository that contains the Django application.ß

### django_site_hostname

Define the hostname of the Django application for Apache configuration.

### django_secret_key

Define the secret key of the Django application.

### django_project_name

Define the URL of the Git repository that contains the Django application.

## Optional Variables

The following optional variables can be defined in the playbook:

### django_apache_webmaster_email

Defines the email address of the webmaster. The default value is `webmaster@localhost`.

### django_debug

Defines the debug mode of the Django application. The default value is `false`.

### django_python_version

Defines the version of Python to use. The default value is `3.11`.

### django_repo_version

Defines the branch of the Git repository to deploy. The default value is `master`.

### django_site_module

Defines the name of the Django application module. The default value is `site`.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

MIT
