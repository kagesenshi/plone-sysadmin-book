Introduction to the tools
==========================

Plone
------

Plone is a powerful, Free and Open Source Content Management System developed 
on the Zope application server. Plone can be used for various kind of purposes,
such s public corporate or organization websites, to private intranet/extranet,
and as document sharing and knowledge management platform.

Plone strengths lies on its ease of use, extensibility, fine grained 
permission control, and great security track record. 

Features provided by Plone includes:

* Inline editing through the web.
* Workflow.
* Collaboration and sharing
* Discussions and commenting.
* Full-text indexing of Office and PDF documents.
* Inline document preview using DocumentViewer.
* Faceted search using Faceted Navigation addon.
* Displaying of events in calendar format.

A non-exhaustive list of features provided by Plone can be viewed at its
`wikipedia page <http://en.wikipedia.org/wiki/Plone_%28software%29>`_. 

* http://www.plone.org

Zope / ZEO
-----------

Zope is the application server which Plone runs on. It is written in Python and
utilize an Object Database called Zope Object Database (ZODB) for its data 
storage. Zope provides a powerful component-based programming framework and
platform for developing highly extensible systems. 

ZEO is the database server for ZODB. Zope itself can comes with ZODB support
built-in, which makes ZEO optional for a basic deployment. However, for scaling
purposes, a separate ZEO server serving only the database is required for
deploying a horizontally scalable cluster of multiple Zope with a single ZEO
instance.

* http://www.zope.org

Buildout
---------

Buildout is the de-facto Zope/Plone environment setup build tool. It assembles
the necessary components and packages required to run a Zope/Plone 
infrastructure for both development and deployment. 

* http://www.buildout.org

inigo.templer
-------------

inigo.templer is a set of convenient templates which allows you to quickly
bootstrap the necessary code structure needed for setting up a Zope/Plone
deployment, and also for initializing a custom add-on product.

* http://github.com/inigoconsulting/inigo.templer

HAProxy
-------

HAProxy is a load balancer daemon. In a multi-instance Zope/Plone deployment,
HAProxy is used to balance the load between the instance clusters.

* http://haproxy.1wt.eu/

Varnish
-------

Zope ZServers have limited threads to handle requests, which could cause
blocking issue on a site with many users. Varnish is used to cache static
resources so that Zope does not have to recalculate the pages to serve them, 
radically improving performance of a site.

* https://www.varnish-cache.org/
