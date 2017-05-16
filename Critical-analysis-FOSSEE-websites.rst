Document Information
====================

Name of the Document: Critical Analysis of FOSSEE Websites

Date: 4/05/2017

Author: Priyanka Bhagwat

Designation: Software Engineer

Introduction
============

This document aims to identify website features/modules that should be
removed/improve and identifying bugs

Assumptions
===========

It is assumed that the readers of this document are familiar with the
Drupal 7, PHP, MySQL and software engineering. It is also assumed that
the required resources will be available to achieve the objectives of
the plan.

Common Suggestions for all the websites
=======================================

Centralised login ( if possible)

Search Engine Optimisation

Standardise menu names and URL’s throughout all websites.

Database structure to be standardized across all websites.

Scilab Website
==============

+-------+---------------------+
| URL   | http://scilab.in/   |
+=======+=====================+
+-------+---------------------+

1. General Comments

   a. Reduce content on website. Too much content on the site makes it
          look bulky and hence many times other lightweight themes
          cannot be implemented. Even too many links on the site. We can
          come up with better way to display side navigations, Few
          examples at
          `*https://dcrazed.com/jquery-navigation-plugins-menus/* <https://dcrazed.com/jquery-navigation-plugins-menus/>`__

    `*http://cssmenumaker.com/menu/modern-accordion-menu#* <http://cssmenumaker.com/menu/modern-accordion-menu#>`__

   b. Git implementation to be done. Currently the completed books are save
	       on the server and its entry in database. On completed book
	       checkbox selection the files should be automatically be pushed to
	       GIT repo.

2. Apache Solr Search

   a. New searching techniques to be implemented.

    `*https://wunder.io/blog/build-advanced-content-listings-with-apache-solr-search-api-facet-api/2012-04-20* <https://wunder.io/blog/build-advanced-content-listings-with-apache-solr-search-api-facet-api/2012-04-20>`__

   b. Result display of search can be improved.

   c. Sometimes cannot handle search limit, throws Indexoutofbound()
	       exception.

3. Textbook Companion/Lab Migration

   a. User dashboard according to each role

   b. Improve mail functions.

   c. The overall way how the data is displayed can be improved. Can use
          flat UI.

    `*http://bootsnipp.com/snippets/W7gNz* <http://bootsnipp.com/snippets/W7gNz>`__

   d. Payment interface to be tested.

4. Scilab Toolbox Interface

   a. Currently, this content is added as static HTML. An interface to
          be developed which will take data as input and render it to
          the decided format. The parameters to be given by scilab team.

5. Scilab on cloud

   a. Currently the Categories loaded are written static. For future
          scope this should also be loaded dynamically from the
          database.

FOSSEE Website
==============

+-------+---------------------+
| URL   | http://fossee.in/   |
+=======+=====================+
+-------+---------------------+

1. Statistics Module

   a. The overall code written needs to be simplified and an standard
          way to add new projects needs to be implemented. Currently the
          process is quite complicated.

2. Inventory System

   a. We can add inventory system to the site where the office staff can
          add details of hardwares and other stationery and can assign
          to the FOSSEE Employees.
