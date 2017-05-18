Document Information
====================

Name of the Document: Instruction sheet for developing and deploying new
website

Date: 16/05/2017

Author: Priyanka Bhagwat

Designation: Software Engineer

Introduction
============

This document gives the steps involved while developing a new FOSSEE
website.

Assumptions
===========

It is assumed that the readers of this document are familiar with the
Drupal 7, PHP, MySQL and software engineering. It is assumed that the
DOCS mentioned in the file are already shared, if not found please
contact the senior webteam member/Sysads/managers for the same.

For any new website similar to Scilab Webiste

Step 1: **General Requirements**

1. **URL**: “domain” on main server

2. **URL**: “domain” on test server eg “r.fossee.aero.iitb.ac.in

3. **Contact Id**: contact-id(at)fossee(dot)in

4. **Mailing List**: group mailing list for members for example
       r(dot)fossee(dot)in

5. **AWstats** and **Google analytics** for the same.

Step 2: **On Local machine**

1.  Copy the latest working project directory and database from the main
        server on your **local** machine

2.  Login as **superuser**

3.  Find and replace the existing name/email ids/contact-ids according
        to the new project name.

4.  Follow step 3 for database tables as well

5.  Clean the database entries for custom modules and user table
        **except the superuser**

6.  Create required directories for code uploads as per requirement

7.  Add necessary information to the TBC/LM settings for eg- CC, BCC,
        contact ids etc

8.  Disable Captcha

9.  Add the **AWstats** and **Google analytics.** The details can be
        viewed at “\ **FOSSEE WEBSITES STATISTICS SHEET**\ ” GDOC

10. Test it locally.

Step 3: **On Test Server**

1. If testing is successful, ask Sysads to deploy it on **test server**

2. Ask the respective team to test the site on test server

3. Resolve errors, if any

4. Ask the Sysads to deploy it to the main server

Step 4: **On Main Server**

1. Check if the Uploads folder is present

2. Check for CAPTCHA and RECaptcha

3. Create and Update new Superuser username and password and add it to
       the “\ **Web Team Access**\ ” GDOC

4. Test with dummy data, once OK clear the dummy data added

5. Make the site available for use

Step 5: FOSSEE Statistics

1. FOSSEE Site statistics

   a. Copy the php file from main server.
          Location:/Sites/fossee\_drupal/data/project-statistics.php

   b. Add the new website details to the file.

   c. Update the file on the main server, assuming you have necessary
          permissions.

   d. The site stats can be view at
          `*http://fossee.in/data/project-statistics.php* <http://fossee.in/data/project-statistics.php>`__

2. FOSSEE Activity statistics

   a. You need a working fossee.in copy on your local.

   b. Either Fork or Clone the repo
          `*https://github.com/FOSSEE/FOSSEE\_Stats* <https://github.com/FOSSEE/FOSSEE_Stats>`__

   c. Add the new website database details to settings.php.

   d. Make the necessary changes

   e. Send pull request to the repo.

   f. Pull the changes on test server.

   g. If ok, ask sysads to merge the changes to the main server.
