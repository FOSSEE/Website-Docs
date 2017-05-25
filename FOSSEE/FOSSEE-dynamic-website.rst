Document Information
====================

Name of the Document: FOSSEE Dynamic Website

Date:23/05/2017

Author: Priyanka Bhagwat

Designation: Software Engineer

Introduction
============

This document focuses on the development of the new FOSSEE Website.

Website
=======

http://fossee.in/

Assumptions
===========

It is assumed that the readers of this document are familiar with the
Drupal 7, PHP, MySQL and software engineering.

Module Requirements
===================

To achieve this feature the following modules are required

Views

Panels

Entity

Token

Radix Layout

Quicktabs

Radix Layout

Owl Carousel

Entity\_reference

Rules

Date

Link

Linkicon

Ctools

Fieldaccess

Auto\_entitylabel

Disable Field

Field collection

Field Conditional State

SMTP Authentication Support

**Website Theme**
-----------------

**Choose an Existing Starterkit**
---------------------------------

-  *CDN Starterkit* <https://drupal-bootstrap.org/api/bootstrap/starterkits%21cdn%21README.md/group/subtheme_cdn/7>

-   *Less Starterkit* <https://drupal-bootstrap.org/api/bootstrap/starterkits%21less%21README.md/group/subtheme_less/7>`__

-  *Sass Starterkit* <https://drupal-bootstrap.org/api/bootstrap/starterkits%21sass%21README.md/group/subtheme_sass/7>`_


Here we are using the CDN Starterkit.

**Create a New Sub-theme**
--------------------------

1. Copy over one of the starterkits you have chosen from the
       ./bootstrap/starterkits folder into sites/all/themes or a
       respective sites/\*/themes folder.

2. Rename the folder to a unique machine readable name. This will be
       your sub-theme's "name". For this example and future examples
       we'll use subtheme.

3. Rename ./subtheme/cdn.starterkit or, if using the LESS Starterkit,
       ./subtheme/less.starterkit to match the folder name and append
       .info (e.g. ./subtheme/subtheme.info).

4. Open ./subtheme/subtheme.info and change the name, description and
       any other properties to suite your needs.

    WARNING: Ensure that the .starterkit suffix is not present on your
    sub-theme's .info filename. This suffix is simply a stop gap measure
    to ensure that the bundled starter kit sub-theme cannot be enabled
    or used directly. This helps people unfamiliar with Drupal avoid
    modifying the starter kit sub-theme directly and instead forces them
    to create a new sub-theme to modify.

**Enable Your New Sub-theme**
-----------------------------

In your Drupal site, navigate to admin/appearance and click the Enable
and set default link next to your newly created sub-theme.

**Content Types**
-----------------

**Structure->Content types**

Designation

|image0|

Faculty members

|image1|

FOSSEE Projects

|image2|

FOSSEE Projects contacts

|image3|

Generic links

|image4|

Team Members

|image5|

Resources

|image6|

Article

|image7|

Activities

|image8|

**Views**
---------

**Structure ->Views**

**Faculty members**

**Query**

 SELECT node.nid AS nid, node.created AS node\_created, 'node' AS
  field\_data\_field\_faculty\_name\_node\_entity\_type, 'node' AS
  field\_data\_field\_faculty\_link\_node\_entity\_type
 FROM
 {node} node
 WHERE (( (node.status = '1') AND (node.type IN ('faculty\_members'))  ))
 ORDER BY node\_created ASC

|image9|

**Output**

|image10|

**FOSSEE Projects**

**Query**

  field\_data\_field\_project\_link\_node\_entity\_type, 'node' AS
  SELECT node.nid AS nid, node.created AS node\_created, 'node' AS
  field\_data\_field\_project\_name\_node\_entity\_type, 'node' AS
  field\_data\_field\_project\_logo\_image\_node\_entity\_type, 'node' AS 
  field\_data\_body\_node\_entity\_type
  FROM
  {node} node
  INNER JOIN {field\_data\_field\_project\_status}
  field\_data\_field\_project\_status ON node.nid =
  field\_data\_field\_project\_status.entity\_id AND
  (field\_data\_field\_project\_status.entity\_type = 'node' AND  field\_data\_field\_project\_status.deleted = '0')
  WHERE (( (node.status = '1') AND (node.type IN ('projects')) AND
  (field\_data\_field\_project\_status.field\_project\_status\_value =
  '0') ))
  ORDER BY node\_created DESC

|image11|

**Rewrite results**

|image12|

**Output**

|image13|

.. |image0| image:: media/designation.png
   :width: 6.92188in
   :height: 1.45833in
.. |image1| image:: media/faculty-members.png
   :width: 6.88021in
   :height: 2.00000in
.. |image2| image:: media/fossee-projects.png
   :width: 6.79167in
   :height: 3.36979in
.. |image3| image:: media/fossee-contact.png
   :width: 6.70313in
   :height: 2.03125in
.. |image4| image:: media/generic-links.png
   :width: 6.73958in
   :height: 2.23438in
.. |image5| image:: media/team-members.png
   :width: 6.27083in
   :height: 2.51563in
.. |image6| image:: media/resources.png
   :width: 6.27083in
   :height: 1.65104in
.. |image7| image:: media/article.png
   :width: 6.26772in
   :height: 1.65278in
.. |image8| image:: media/activities.png
   :width: 6.27083in
   :height: 1.76563in
.. |image9| image:: media/view-block-faculty-members.png
   :width: 6.73438in
   :height: 3.64583in
.. |image10| image:: media/output-faculty.png
   :width: 6.81250in
   :height: 3.34896in
.. |image11| image:: media/view-block-fossee-projects.png
   :width: 6.27083in
   :height: 3.58854in
.. |image12| image:: media/block-view-fossee-projects-rewrite.png
   :width: 6.26772in
   :height: 4.48611in
.. |image13| image:: media/projects.png
   :width: 6.26772in
   :height: 5.93056in
