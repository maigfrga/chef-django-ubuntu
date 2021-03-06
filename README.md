chef-django-ubuntu
==================

A set of recipes to provision an ubuntu server using [Chef](http://www.opscode.com/chef/).

The main goal is provisioning and deploying a django app.

Original idea from bsnux [chef-mint](http://github.com/bsnux/chef-mint).

*chef-solo* is used for simplicity because we only want to provide one machine. However, you can adapt the recipes to provision *n* machines using regular *Chef*.

[OPSCODE](http://www.opscode.com/chef/) offers a complete set of independient operating system recipes.

Requirements
------------

* [Chef](http://www.opscode.com/chef/). See [installation](http://wiki.opscode.com/display/chef/Installation) instructions.

Installation
-------------

1. Clone current repo.

2. If *Chef* is not installed on your machine, you can execute:

    $ sudo ./init.sh

Components
----------
1. web.json: web stack attributes

2. web.rb: web stack configuration file

3. cookbooks/main/ : system setup cookbooks

4. cookbooks/nginx/ : nginx setup cookbooks

5. cookbooks/python/ : python basic stuff

6. cookbooks/gunicorn/ : gunicorn install and configuration

Usage
-----
Web stack:

    $ cd chef-django-ubuntu

    $ sudo chef-solo -c web.rb -j web.json

Postgresq:
    $ cd chef-django-ubuntu

    $ sudo chef-solo -c web.rb -j pgdb.json
See also
---------
[Chef Solo tutorial: Managing a single server with Chef](http://www.opinionatedprogrammer.com/2011/06/chef-solo-tutorial-managing-a-single-server-with-chef/)

[Complete and official cookbook repository for chef](https://github.com/opscode-cookbooks)

[Python cookbook](https://github.com/opscode-cookbooks/python)

[ngnix cookbook](https://github.com/opscode-cookbooks/nginx)

[gunicorn cookbook](https://github.com/opscode-cookbooks/gunicorn)

[Postgresql cookbook](https://github.com/opscode-cookbooks/postgresql)

[Setting up Django with Green Unicorn, nginx, supervisord and fabric on CentOS 5.5](http://www.kencochrane.net/blog/2011/06/django-gunicorn-nginx-supervisord-fabric-centos55/)

[Deploying Django with nginx and gunicorn](http://honza.ca/2011/05/deploying-django-with-nginx-and-gunicorn)

[JasonGiedymin / nginx-init-ubuntu](https://github.com/JasonGiedymin/nginx-init-ubuntu)
