Preface
========

About the Author
------------------

Mohd Izhar Firdaus Bin Ismail, or, more commonly known in the Malaysian tech /
Open Source community as KageSenshi, is a co-founder and system engineer in
`Inigo Consulting <http://www.inigo-tech.com>`_. With over 5 years experience
developing and maintaining Plone sites and addons for United Nations
International Labour Organization, 
World Council of Churches, and various NGOs, Izhar, alongside with his
colleagues in Inigo Consulting, are one of the few Plone specialists in
Malaysia and neighboring countries. 

This guide serve as a gathering of these experience into a documented format,
for others to quickly able to setup a Plone infrastructure for their
organization and also as a future reference for himself.

Who is this guide is for?
-------------------------

This guide is aimed towards system administrators who wish to quickly deploy a
Plone based site in their organization. We will be covering deployment setups
from a basic, single Zope instance deployment, to setting up a
horizontal-scalable cluster complete with HTTP caching and loadbalancing support.

This guide is not meant to be a replacement for the official `Plone
Developer Documentation 
<http://developer.plone.org/reference_manuals/active/deployment/index.html>`_, 
but rather to complement it as a simplified quick guide to set up Plone.

How this guide is organized?
-----------------------------

This guide is organized in sections that focuses on immediate sysadmin goals.
Each section consist of an introduction on the setup, its use-case, a
step-by-step guide to solve the goal, and is followed by some common
troubleshooting questions related to the task in hand.


Assumptions
-----------

This guide assumes you are on a RedHat/CentOS/Fedora based system with
Python2.6 installed. 
