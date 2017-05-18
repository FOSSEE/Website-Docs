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


**Structure-> Field collection-> Field collection field\_personal\_details**
**Create-> Content Types -> Case Study Proposal**

|image111|


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


**View**

**Structure -> Views ->Case Study**

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

2. **In Progress**

    **Purpose-** This page displays the case studies in progress. The
    Proposals that are approved but not competed.

    **URL-**
    `*http://cfd.fossee.in/case-study/cs-in-progress* <http://cfd.fossee.in/case-study/cs-in-progress>`__

    **Roles-** All

    Description

-  The display is in the table format

-  The view is filtered by the criteria -

   -  Case study proposal

   -  Content is published

   -  Proposal Status

|image4|

3. **Code Submission**

    **Purpose-** This is the interface where the user can submit the
    codes once the proposal is accepted

    **URL-**
    `*http://cfd.fossee.in/case-study/cs-code-submission* <http://cfd.fossee.in/case-study/cs-code-submission>`__

    **Roles-** All

    Description

-  The display is in the table format

-  The view is filtered by the criteria -

   -  Case study proposal

   -  Content is published

   -  Proposal Status

|image5|

4. **Manage code**

    **Purpose-** This is the admin interface for the reviewer to
    accept/reject the case study codes are submitted.

    **URL-**
    `*http://cfd.fossee.in/case-study/cs-manage-code* <http://cfd.fossee.in/case-study/cs-manage-code>`__

    **Roles-** Administrator, Case Study Reviewer

    Description

-  The display is in the table format

-  The view is filtered by the criteria -

   -  Case study proposal

   -  Content is published

   -  Proposal Status

|image6|

5. **Completed Case Studies**

    **Purpose-** This is the admin interface for the reviewer to
    accept/reject the case study codes are submitted.

    **URL-**
    `*http://cfd.fossee.in/case-study/cs-code-submission* <http://cfd.fossee.in/case-study/cs-code-submission>`__

    **Roles-** Administrator, Case Study Reviewer

    Description

-  The display is in the table format

-  The view is filtered by the criteria -

   -  Case study proposal

   -  Content is published

   -  Proposal Status

|image7|

6. **Attachment- After code submission**

    **Purpose-** This is the admin interface for the reviewer to
    accept/reject the case study codes are submitted.

    **URL-**
    `*http://cfd.fossee.in/case-study/cs-code-submission* <http://cfd.fossee.in/case-study/cs-code-submission>`__

    **Roles-** Administrator, Case Study Reviewer

    Description

-  The display is in the table format

-  The view is filtered by the criteria -

   -  Case study proposal

   -  Content is published

   -  Proposal Status

|image8|

**Configuration -> Workflow -> Rules**

The Rules module allows site administrators to define conditionally
executed actions based on occurring events

On approval CS

.. |image111| image:: media/personaldetailsFC.png
   :width: 6.65104in
   :height: 2.37500in
.. |image1| image:: media/CT-proposal.png
   :width: 6.71875in
   :height: 5.14063in
.. |image2| image:: media/CT-submission.png
   :width: 6.27083in
   :height: 2.38021in
.. |image3| image:: media/manage-proposal.png
   :width: 6.91146in
   :height: 3.77083in
.. |image4| image:: media/in-progress.png
   :width: 6.96354in
   :height: 3.97917in
.. |image5| image:: media/code-submission.png
   :width: 6.95313in
   :height: 4.10417in
.. |image6| image:: media/manage-code.png
   :width: 6.80729in
   :height: 3.98958in
.. |image7| image:: media/competed-cs.png
   :width: 6.86979in
   :height: 4.19792in
.. |image8| image:: media/after-code-sub.png
   :width: 6.26772in
   :height: 2.90278in
