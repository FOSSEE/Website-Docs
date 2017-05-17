Document Information
====================

Name of the Document: Developer Documentation for Case Study Feature

Date: 11/05/2017

Author: Priyanka Bhagwat

Designation: Software Engineer

Introduction
============

The Case Studies Project aims to promote open source software, such as
OpenFOAM by developing complex case studies using OpenFOAM available to
CFD researchers and users for reference and usage. The participants of
this project can share complex computation problems for this purpose.

Assumptions
===========

It is assumed that the readers of this document are familiar with the
Drupal 7, PHP, MySQL and software engineering. It is also assumed that
the required resources will be available to achieve the objectives of
the plan.

Module Requirements
===================

To achieve this feature the following modules are required

Views

Panels

Entity

Token

Entity\_reference

Rules,

Date,

Link,

Linkicon,

Ctools,

Fieldaccess

Auto\_entitylabel

Disable Field

Field collection

Field Conditional State

SMTP Authentication Support

**Structure-> Field collection-> Field collection
field\_personal\_details**

|image0|

**Create-> Content Types -> Case Study Proposal**

**Purpose-** To propose the case study project using the proposal form.

**Modules used (other than core)** -

-  Field Conditional State-When the user selects the checkbox, the
       respective fields are visible.

-  Field Collection- field\_personal\_details field collection is used

-  Date

|image1|

**Create-> Content Types -> Case Study Code Submission**

**Purpose-** To submit the case study codes once the proposal is
accepted.

**Modules used (other than core)** -

-  Date

|image2|

**Views**

1. **Manage Proposal.**

    **Purpose-** This is the admin interface for the reviewer to
    accept/reject the case study proposal.

    **URL-**
    `*http://cfd.fossee.in/case-study/manage-proposal* <http://cfd.fossee.in/case-study/manage-proposal>`__

    **Roles-** Administrator, Case Study Reviewer

    Description

-  The display is in the table format

-  The view is filtered by the criteria - Case study proposal and
       whether the content is published

|image3|

.. |image0| image:: media/image8.png
   :width: 6.26772in
   :height: 2.51389in
.. |image1| image:: media/image5.png
   :width: 6.71875in
   :height: 5.14063in
.. |image2| image:: media/image3.png
   :width: 6.27083in
   :height: 2.38021in
.. |image3| image:: media/image7.png
   :width: 6.84375in
   :height: 4.31771in

