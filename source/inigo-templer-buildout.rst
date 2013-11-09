Using inigo.templer for deploying Plone
=========================================

``inigo.templer`` aids you in quickly setting up your Zope/Plone infrastructure
by providing you a pre-configured skeleton to work with. Functionalities
provided by ``inigo.templer`` includes:

* A skeleton template for a deployment buildout
* A skeleton template for writing Plone addon products
* A skeleton template for writing Plone themes

Setting up a buildout for inigo.templer
----------------------------------------

So, lets setup a buildout for inigo.templer. First, you will need to create our
working directory. In this example, we will be using ``~/inigo.templer`` as our
working directory.

Now, let initialize the working directory and populate it with the most important
component of a buildout, which is, the bootstrapper by running these commands::

    mkdir ~/inigo.templer
    cd ~/inigo.templer
    wget http://downloads.buildout.org/2/bootstrap.py -O bootstrap.py

Afterwards, create the initial buildout.cfg for installing inigo.templer::

    [buildout]
    develop = . 
    parts = scripts 
    versions = versions
    newest = true
    
    [scripts]
    recipe = zc.recipe.egg
    eggs = 
        templer.core
        templer.buildout
        templer.plone
        inigo.templer
        zest.releaser

Lets buildout!::

    /opt/python26/bin/python bootstrap.py
    ./bin/buildout -vvv

Once the build process is done, you should get a script called ``templer``
in the ``bin/`` directory. We will be using this script later to create our 
deployment buildout.

Introducing the inigo_buildout templer template
----------------------------------------------- 

inigo.templer provides a template called inigo_buildout which will generate a
base buildout for deploying Plone. The buildout have been preconfigured with
functionalities such as:

* Separate buildout configuration for development and production use
* Automatically generated sample configuration for HAProxy and Varnish
* Single Zope instance deployment for development use
* Dual Zope instance + single ZEO instance deployment for production use



