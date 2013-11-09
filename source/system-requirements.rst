Plone System Requirements
==========================

Operating System Platform
--------------------------

Basic Plone deployment supports multiple platform to run it, which includes
both Windows, and \*Nix variations such as Linux and MacOS. However, many Plone
add-ons, such as the DocumentViewer, and PDF Exporter requires \*Nix specific 
tools and services. Therefore it is recommended that Plone is deployed on a
Linux based system.

Memory / RAM
---------------------

Zope and Plone have a rather high base memory footprint. This is due to it
loads a huge amount of Python code to run, and also objects are usually cached
inside the Zope instances. 

For a cluster with 1 Varnish, 2 Zope instances, and 1 ZEO instance, we
recommend at least 2GB of RAM for optimal performance. The more RAM is better.

A single cluster can serve multiple Plone sites, and RAM requirement usually 
does not grow too far from the base requirement unless there are memory-heavy
add-ons installed. This lowers the requirement when using a single deployment
to serve multiple sites.

System Tools and Libraries
--------------------------

These are the required tools and development libraries required:

* Python 2.6 (for Plone < 4.2) or Python 2.7 (for Plone > 4.3)
* Python development libraries
* libjpeg-devel
* zlib-devel
* bzip-devel
* libxslt-devel
* libxml2-devel 

References
----------

* Plone system requirements: http://plone.org/documentation/kb/plone-system-requirements

