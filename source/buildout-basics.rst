Buildout Basics
================

Overview of a buildout environment
-----------------------------------

A basic buildout consist of a single ``buildout.cfg`` configuration file, and a
``bootstrap.py`` which initialize the environment. 

For a Plone buildout, we will usually have these directories generated in the
buildout, alongside several others:

* ``bin/`` - generated executable scripts will be stored here
* ``eggs/`` - installed Python eggs will be stored here
* ``var/`` - this is where all Plone data (ie: the database, logs, etc) will 
  be stored

Initializing and building a buildout
------------------------------------

A buildout can be initialized by executing ``boostrap.py`` with your selected
version of Python. To avoid conflict with any libraries pre-installed with the
Python environment, we recommend creating a clean separated Python environment
using ``virtualenv`` before initializing a buildout.

Installing and initializing virtualenv::

    easy_install-2.6 virtualenv
    virtualenv -p /usr/bin/python2.6 /opt/python26/

Initializing buildout::

    /opt/python26/bin/python boostrap.py

This will initialize the necessary scripts and directories needed to run a
buildout. 

Once a buildout is initialized, you can start the building process by running::

   ./bin/buildout -vvv

If the buildout ran successfully, you will get plenty of eggs installed in the
``eggs/`` directory, and several scripts generated in ``bin/``

.. NOTE::
   Sometimes bootstrap.py might fail due to it is outdated. If it is, download
   the latest bootstrap.py by running this command::

      wget http://downloads.buildout.org/2/bootstrap.py -O bootstrap.py
